---
name: decision-tree-analysis
description: Use when the user faces a decision with uncertain outcomes and wants the choice that maximizes expected value, or asks to map options and chance events into a decision tree and solve it. Frames the root decision, its later choices, and the chance events into one tree, fans out parallel subagents to estimate each branch's probabilities and payoffs, then folds back (expected value at chance nodes, best choice at decision nodes) to mark the optimal path, with break-even and value-of-information analysis, in a detailed markdown report. Triggers include "decision tree", "expected value", "decision analysis", "EV", "fold back", "decision under uncertainty".
---

# decision-tree-analysis

Maps a decision and the uncertain events that follow it into a tree, then solves it for the sequence of choices that maximizes expected value. Catches the failure where options are weighed by gut feel: the tree forces which moves are yours, which are the world's, and what every outcome is worth into one diagram, and folding back turns that into a defensible recommendation plus a price on resolving the uncertainty.

The node types, the fold-back arithmetic, break-even and sensitivity analysis, expected value of perfect information, and the risk-attitude rule live in [references/decision-tree-analysis.md](references/decision-tree-analysis.md). Load that file before working and follow the fold-back and probabilities-sum-to-one rules exactly.

## When to use

The user faces a choice whose outcome depends on uncertain events, and wants the option that maximizes expected value over a horizon. Decision tree analysis fits when there is genuine uncertainty with probabilities you can estimate, and especially when a decision now is followed by later decisions once events resolve (launch now, test first, or shelve).

- If there is no real uncertainty and the choice is between options scored on fixed criteria, it is a deterministic ranking, so use [weighted-decision-matrix](../weighted-decision-matrix/) instead.
- If the hard part is estimating the probability of one event from how similar cases turned out, use [reference-class-forecasting](../reference-class-forecasting/), then feed its number into a chance node here.
- If the future has too many unknowns to pin to probabilities and you need to plan against distinct futures instead, use [scenario-planning](../scenario-planning/).
- If you have settled on a plan and want to surface how it could fail before committing, use [pre-mortem](../pre-mortem/).

## Language

Conduct the session and write the report in the language the user is writing in. The reference file is English; keep the framework keyed to it regardless of output language.

## Inputs

- **DECISION** (required): the root choice and its alternatives (for example "launch the product now, run a paid market test first, or shelve it").
- **PAYOFF MEASURE** (required): the single common unit every outcome is scored in, with its sign convention (for example net present value in dollars, gains positive and costs negative). Without one common measure the tree cannot be folded back, so if the user does not give one, ask for it before starting.
- **HORIZON** (required): the time window the payoffs cover, so chance events and discounting are consistent across branches.
- **CONTEXT** (optional): known probabilities, cost figures, reference classes, constraints, and the decider's resources (which governs the risk note). Sharpens every branch estimate.

If there is no genuine uncertainty, this is a deterministic choice: stop and route to [weighted-decision-matrix](../weighted-decision-matrix/).

## Orchestration map

```
Stage 1  Frame              ── inline, 1 pass ──────────────────────┐  (root decision, later choices, chance events, payoff measure, horizon)
Stage 2  Branch Estimation  ── N subagents IN PARALLEL ────────────┤  (one per top-level alternative or major chance node: probabilities + payoffs)
Stage 3  Fold-Back          ── 1 agent, needs all branches ────────┘  (assemble tree, fold back, sensitivity, EVPI, recommendation)
```

## Stage 1: Frame (inline)

Pin the structure of the tree before estimating anything, so every subagent works the same tree:

1. **Root decision and alternatives.** The choice being made now and the options at it (the first branches out of the root square).
2. **The sequence.** After each alternative, which uncertain event resolves (a chance node) and whether a later decision follows it. Lay nodes out in the order they happen in time.
3. **Payoff measure and sign.** The single unit every leaf is scored in, with gains and costs signed consistently.
4. **Horizon.** The window the payoffs cover.

Refuse to proceed without a payoff measure. If there turns out to be no genuine uncertainty (no chance node with real branching), it is a deterministic choice: stop and route to [weighted-decision-matrix](../weighted-decision-matrix/).

## Stage 2: Branch Estimation (PARALLEL)

Dispatch one subagent per top-level alternative (or per major chance node when one alternative dominates the tree's uncertainty). Give each the shared framing from Stage 1 as a quoted prompt block plus the part of the tree it owns.

Tell each subagent its final message is the return value: structured data, not prose for a human. Subagents should use available retrieval tools to ground probabilities and payoffs in real evidence or reference classes.

**Shared framing (send to each estimator):**

> Estimate one branch of a decision tree for this decision: **[DECISION]**. Payoff measure: **[PAYOFF MEASURE]** (sign convention: **[SIGN]**). Horizon: **[HORIZON]**. Your branch begins with the alternative or chance node: **[BRANCH]**.
> Map out the chance nodes that follow on your branch and, for each, its outcomes. Return structured data:
> - **Chance nodes:** for each, the list of outcomes with a **probability** per outcome that **sums to exactly 1** across the node, the **evidence or reference class** behind each probability, and a **confidence** (high, medium, low) lowered when grounding is thin.
> - **Terminal payoffs:** for every leaf on your branch, the payoff in the common unit, net of all costs along that path, with how it was derived.
> - **Notes:** any later decision node on your branch and the choices at it, and any assumption a reviewer must check.
>
> Context: [CONTEXT]

Collect every branch's structured result before continuing. Re-dispatch any estimator that fails, or whose probabilities do not sum to 1, rather than folding back with a gap.

## Stage 3: Fold-Back Synthesis (SEQUENTIAL, needs all branches)

One agent assembles the tree and solves it:

1. **Assemble the tree.** Stitch the branches into one tree in time order. Check every chance node's probabilities sum to 1 and every leaf is in the common unit; fix or re-dispatch any that are not.
2. **Fold back.** Working from the leaves to the root: expected value at each chance node (sum of probability times branch value), the best branch at each decision node (prune the rest). Show the arithmetic at each node.
3. **Mark the optimal path.** Read the surviving choices off the root outward into the recommended plan: what to do now, and what to do at each later decision once the intervening event resolves.
4. **Sensitivity.** Find the **break-even probability** for the key uncertain event (the value at which the recommended branch ties the next-best, and which side of it the current estimate sits on), and the payoff swings that would flip the decision. Name the inputs the answer is sensitive to.
5. **Value of information.** Compute **EVPI** for the uncertainty that drives the result: the EV with perfect foresight minus the folded-back EV of deciding now. State the most it is worth paying to resolve that uncertainty before committing, and whether any proposed test or pilot clears that bar.
6. **Risk note.** Where a payoff is large relative to the decider's resources, flag that plain EV assumes risk-neutrality, and say how a risk-averse decider's choice could differ once payoffs are read as utilities.
7. **Recommendation.** The optimal path and the EV it earns, the threshold that would change it, and what to investigate before committing.

## Report structure

Write a thorough markdown report and save it to `decision-tree-analysis-<subject-slug>-<YYYY-MM-DD>.md` (today's date) in the working directory unless the user names another location.

1. **Header.** The decision, the payoff measure and sign convention, the horizon, and the date.
2. **Tree structure.** An indented outline or table of the whole tree: decision nodes, chance nodes with their branch probabilities, and terminal payoffs, in time order.
3. **Branch detail.** Per branch: the probabilities and payoffs, the evidence or reference class behind each, and a confidence flag.
4. **Fold-back.** The expected value computed at each node with the arithmetic shown, and the optimal path highlighted.
5. **Sensitivity and value of information.** The break-even probability for the key event, the payoff swings that matter, the EVPI figure, and what to investigate before committing.
6. **Risk note.** Whether the stakes are large enough that risk attitude changes the call, and how.
7. **Recommendation.** The recommended plan, the EV it earns, and the threshold that would change it.
8. **Caveats.** EV is an average over a bet you may take only once; the recommendation is only as good as the probabilities and payoffs fed in; plain EV assumes risk-neutrality; and the tree only covers the options and outcomes you modeled, so an unmodeled alternative cannot win and an omitted outcome distorts every EV above it.

## Principles

- **Fold back, do not eyeball.** The recommendation is the folded-back EV, computed node by node, not a feel for which option looks best.
- **Every probability sums to 1 and is grounded.** A chance node's branches are mutually exclusive and exhaustive; ground each probability in data or a reference class and flag confidence rather than inventing certainty.
- **One unit, one sign.** Every leaf is in the same common measure, net of costs along its path, or the tree cannot be solved.
- **Report the threshold, not just the answer.** A break-even probability and an EVPI say how fragile the call is and what is worth paying to firm it up, which is what a decider needs.
- **Name the risk assumption.** Plain EV is risk-neutral. When a payoff could sink the decider, say so and read the payoffs as utilities.
