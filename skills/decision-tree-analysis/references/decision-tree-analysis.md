# Decision tree analysis: framework, fold-back, and value of information

A decision tree maps a decision and the uncertain events that follow it into one diagram, then solves it for the sequence of choices that maximizes expected value. It comes from statistical decision theory, developed in the 1960s by Ronald Howard (decision analysis, Stanford) and Howard Raiffa (Harvard), building on Bayesian statistics and von Neumann-Morgenstern utility.

The method forces three things into the open: which moves are yours, which are the world's, and what every outcome is worth in one common unit. A list of options without that structure hides where the uncertainty actually bites.

## The three node types

A tree is read left to right in the order events happen, and solved right to left.

| Node | Drawn as | Belongs to | Branches |
|---|---|---|---|
| **Decision node** | square | you (a choice you control) | the alternatives you can pick |
| **Chance node** | circle | the world (an uncertain event) | the outcomes that can occur, each with a probability |
| **Terminal node** | triangle / leaf | end of a path | a single payoff in the common unit |

Every path from the root to a leaf is one complete story: a sequence of your choices and the world's outcomes, ending in a payoff. The tree alternates between the two kinds of node as the situation unfolds (decide, then an event resolves, then maybe decide again).

## Two rules that keep the tree honest

1. **One payoff measure, one sign convention.** Every leaf is measured in the same unit: dollars, net present value (NPV), lives, utils, days saved. Costs and gains carry a consistent sign (gains positive, costs negative). A tree mixing units cannot be folded back.
2. **Probabilities at a chance node sum to 1.** The branches out of a circle are the mutually exclusive, exhaustive outcomes of that event, so their probabilities total exactly 1. Ground each probability in data or a reference class where you can, and flag how confident you are. A made-up probability produces a made-up recommendation.

---

## Folding back (rollback, backward induction)

Solving the tree means working from the leaves back to the root, assigning a value to every node:

- **At a chance node (circle):** the value is the **expected value**, the probability-weighted average of its branches.

  `EV(node) = sum over branches of ( probability x value of that branch )`

- **At a decision node (square):** you control the choice, so the value is the **best branch**: the maximum value among the alternatives. Take that branch and **prune** the rest. Mark which alternative won.

- **At a terminal node (leaf):** the value is just its payoff.

Repeat until the root has a value. That root value is the expected value of the whole decision played optimally. The **recommended plan** is the sequence of surviving (un-pruned) choices from the root outward: what to do now, and what to do at each later decision once the intervening uncertainty has resolved.

Folding back assumes you will keep making the best choice at every future decision node. That is why a later decision can be left open in the plan: you do not have to decide it now, only commit to deciding it well when you get there.

---

## Sensitivity and break-even analysis

A single EV recommendation hides how fragile it is. The inputs (probabilities, payoffs) are estimates, so test how much they can move before the answer changes.

- **Break-even probability.** Take the key uncertain probability and ask: at what value does the recommended branch stop being best and another branch take over? Solve for the probability that makes two branches' expected values equal. Report that threshold and where the current estimate sits relative to it. If the estimate is 0.6 and the break-even is 0.58, the recommendation is fragile. If break-even is 0.30, it is safe.
- **Payoff swings.** Do the same for the payoffs that drive the result: how far can a key payoff move before the decision flips. Name the inputs the answer is sensitive to; those are the ones worth nailing down.

Sensitivity analysis converts "the answer is X" into "the answer is X unless this probability is below 0.58 or that payoff is overstated by more than 20%," which is what a decider actually needs.

---

## Expected value of perfect information (EVPI)

Some uncertainties are worth resolving before you decide, and some are not. EVPI puts a price on resolving one.

`EVPI = (EV if you knew the outcome before choosing) minus (EV of the best choice without that knowledge)`

The first term imagines a clairvoyant who tells you how the chance node resolves before you choose, so you make the best choice for each outcome and then average those over the outcome probabilities. The second term is the plain folded-back EV of deciding now. The difference is the most you should rationally pay to learn the outcome in advance (a market test, a study, a pilot). If a test costs more than the EVPI for the uncertainty it resolves, it is not worth running even if it is perfectly accurate.

EVPI is an upper bound, since real information is rarely perfect. The value of an imperfect test (expected value of sample information) is lower, but EVPI is the quick screen: if even perfect information is not worth the test's price, stop there.

---

## Risk attitude: when plain EV is the wrong objective

Folding back on raw payoffs assumes **risk-neutrality**: that a decider values a sure $1M and a coin-flip between $0 and $2M equally, because both have EV $1M. That holds when the stakes are small relative to the decider's resources. It breaks when a payoff is large enough to matter for survival.

A founder choosing between a guaranteed $2M acquisition and an 11% shot at $20M (EV $2.2M) may rationally take the sure $2M, because losing the $2M outright would end the company. That is not irrational; it is **risk aversion**, and the fix is to fold back on **utilities** rather than dollars. Convert each payoff to a utility with a concave function (so each extra dollar is worth less than the last), then take expected utility at chance nodes. The branch with the highest expected utility can differ from the one with the highest expected dollar value, and that is the point.

Flag this whenever a payoff is large relative to the decider's resources. When stakes are modest, plain EV is the right objective and the utility step is unnecessary.

---

## How to build a tree

1. **Fix the root decision** and its alternatives (the squares' first branches).
2. **Lay out the sequence:** after each choice, what uncertain event resolves (a circle), and whether a later decision follows. Order the nodes in real time order.
3. **Attach probabilities** to every chance branch, summing to 1 at each circle, grounded and confidence-flagged.
4. **Put a payoff on every leaf** in the one common unit, net of the costs along that path.
5. **Fold back:** EV at circles, max at squares, prune the losers.
6. **Read the optimal path** off the surviving branches.
7. **Stress it:** break-even probabilities, payoff swings, EVPI, and a risk note where stakes are large.

A tree only answers among the options and outcomes you drew. An alternative you did not model cannot win, and an outcome you left off a chance node silently distorts every EV above it.
