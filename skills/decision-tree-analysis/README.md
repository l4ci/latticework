# decision-tree-analysis

## What this is

A decision tree maps a decision and the uncertain events that follow it into one diagram, read left to right in the order things happen. Square nodes are your choices, circle nodes are the world's uncertain events (each branch carrying a probability), and the leaves are payoffs measured in one common unit. It comes from statistical decision theory worked out in the 1960s by Ronald Howard at Stanford and Howard Raiffa at Harvard. You solve a tree by folding back: at each chance node the value is the expected value (probability times payoff, summed); at each decision node you take the best branch and prune the rest. The surviving choices are the plan that maximizes expected value. On top of that sit three extensions: a break-even probability that says how far an estimate can move before the answer flips, the expected value of perfect information that prices what resolving an uncertainty is worth, and a risk note for when the stakes are large enough that plain expected value is the wrong objective.

The node types, the fold-back arithmetic, the sensitivity and value-of-information formulas, and the risk-attitude rule live in [references/decision-tree-analysis.md](references/decision-tree-analysis.md).

## What it does

The skill frames the tree inline first: the root decision and its alternatives, the later choices, the chance events between them, the single payoff measure with its sign, and the horizon. It refuses to proceed without a common payoff measure, and if there is no real uncertainty it routes you to a deterministic ranking instead. Then it fans out, one subagent per top-level alternative (or per major chance node), each estimating that branch's chance-node probabilities (summing to 1, grounded in evidence or a reference class, confidence-flagged) and its terminal payoffs. A synthesis pass assembles the tree, folds it back with the arithmetic shown, marks the optimal path, finds the break-even probability and the payoff swings that would change the call, computes the expected value of perfect information, and adds a risk note where the stakes warrant. The output is a saved markdown report with the tree structure, branch detail, the fold-back, the sensitivity and value-of-information analysis, and a recommendation.

## When to use it

Reach for a decision tree when a choice now depends on uncertain events you can put probabilities on, especially when an early decision is followed by later ones once events resolve (launch now, test first, or shelve). It is the tool for decisions under quantifiable uncertainty, so prefer a different one when that shape does not fit:

- If there is no real uncertainty and you are scoring fixed options against criteria, use [weighted-decision-matrix](../weighted-decision-matrix/).
- If the hard part is estimating one event's probability from how similar cases turned out, use [reference-class-forecasting](../reference-class-forecasting/) and feed its number into a chance node here.
- If the future has too many unknowns to pin to probabilities, use [scenario-planning](../scenario-planning/).
- If you have settled on a plan and want to surface how it could fail before committing, use [pre-mortem](../pre-mortem/).

## How to get started

**You provide:** the decision and its alternatives, the single payoff measure every outcome is scored in (with its sign convention), the horizon, and any known probabilities, cost figures, or reference classes. Something like "Decide whether to launch our product now, run a paid market test first, or shelve it, scored on three-year NPV in dollars."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
