# weighted-decision-matrix

## What this is

A weighted decision matrix chooses among several named options by scoring each against the criteria that matter, with every criterion weighted by how much it counts. List the options, define and weight the criteria, score every option on every criterion, sum weight times score, and rank. Stuart Pugh formalized the comparative variant in his concept-selection work (his teaching dates to the early 1980s, set down in *Total Design*, 1991): instead of absolute scores, you pick a baseline and mark every other option better, same, or worse on each criterion. Either way the aim is the same, to rank options against weighted criteria in a way you can show and defend rather than a hunch taken on trust.

The method, how to pick independent and covering criteria, why weights come before scores, the scoring scales, the weighted-sum computation, the Pugh variant, and the sensitivity check are in [references/decision-matrix.md](references/decision-matrix.md).

## What it does

The skill calibrates the criteria, their weights, and the scoring scale first, then scores the options in parallel, one subagent per option, each scoring its option on every criterion with a rationale. Fixing the weights before anyone scores is deliberate: weights set afterwards tend to drift toward whichever option you already liked. A synthesis pass reconciles the independently produced scores, computes the weighted totals, ranks them, and runs a sensitivity check, varying the weights to see whether the winner holds or flips. The output is a saved markdown report with the scored matrix, per-option detail, a sensitivity note, and a recommendation. It guards against the usual failures: criteria that overlap and quietly count the same thing twice, weights nudged after the scores are in, false precision where a 3.8 beats a 3.9 and someone calls it decisive, and a winner reported with no sensitivity check. A near-tie is not a defect; it means the options really are close, and the choice comes down to which criterion you trust.

## When to use it

Reach for this when you are choosing between named alternatives and want the choice scored against several things that matter, not decided by gut alone. If there is only one option there is nothing to compare; if the options do not yet exist, generate them first.

- It generalizes [impact-feasibility-matrix](../impact-feasibility-matrix/) from two fixed axes to any number of weighted criteria; use that one when the two axes are exactly impact and effort, and this one when the criteria are many.
- If you are sequencing a product backlog by value per unit of effort rather than choosing one option, use [rice-prioritization](../rice-prioritization/).
- If you want to stress-test the chosen option for how it could fail before committing, use [pre-mortem](../pre-mortem/).

## How to get started

**You provide:** what you are choosing and the options to choose between (required), optionally the criteria and weights (it derives them with you if absent), plus any constraints and priorities. Something like "help me choose our new CRM with a weighted decision matrix."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
