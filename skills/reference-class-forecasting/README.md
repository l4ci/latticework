# reference-class-forecasting

## What this is

Reference-class forecasting predicts a duration, cost, success rate, or outcome by anchoring on how similar past cases actually turned out. It grows from Daniel Kahneman and Amos Tversky's distinction between the inside view and the outside view, and was operationalized for real planning by Bent Flyvbjerg, who used it to expose the chronic cost and schedule overruns of large projects. It treats your case not as a unique story to reason about from its details, but as one instance of a class of comparable efforts whose realized outcomes are the most reliable anchor available. The method exists to defeat the planning fallacy: forecasting from the inside view (the specific plan, the specific team, the reasons this time will go smoothly) systematically underestimates time and cost and overstates success, because it sees the plan but not the unknown unknowns that derailed every comparable effort.

## What it does

The skill runs reference-class forecasting inside an agent and parallelizes it. It frames the prediction precisely (target variable, units, the case), then proposer subagents build the reference class several ways (narrow-and-similar, broad-and-numerous, the mechanism class, the outcome class), balancing similarity against sample size, and reconcile to one class with explicit, auditable inclusion criteria. A distribution pass gathers the realized outcomes of the class members, not their original plans, and constructs the empirical base rate (median, range, key percentiles) with its data-quality caveats. Three critics then place the case in that distribution: a placement analyst who must name evidence for any departure from the median, a regression critic who pushes the case back toward the mean, and an optimism critic who checks that the adjustments don't all point toward "faster, cheaper, more likely". The output is a saved markdown report with the forecast as a distribution, the base rate, the planning-fallacy gap between the inside-view estimate and the outside view, every adjustment made and rejected with its evidence, and the contingency the class implies. The discipline throughout is to anchor on the base rate first, keep adjustments small and backed by evidence, and forecast a range rather than a point.

## When to use it

Reach for it when you must predict a quantity or outcome for a case that belongs to a recognizable class of similar efforts, and especially when the inside-view estimate feels confident and you suspect that confidence is the problem: how long a project will take, what it will cost, whether a launch will hit its target, the odds a venture succeeds. Triggers: "outside view", "base rate", "planning fallacy", "how long will this really take", "are we being too optimistic".

- If you want the inside view (an estimate built up from this case's own specifics), use [fermi-estimation](../fermi-estimation/). Reference-class is its outside-view counterpart; run both and reconcile the gap.
- If the base rate of failure is the reason to take a failure exercise seriously, follow with a [pre-mortem](../pre-mortem/).
- If you need plausible futures rather than a single calibrated forecast, use [scenario-planning](../scenario-planning/).
- If the question is which explanation is true rather than what to expect, use [analysis-of-competing-hypotheses](../analysis-of-competing-hypotheses/).

## How to get started

**You provide:** what you're forecasting (a duration, cost, or success rate) and enough about the case to find its peers. Your own inside-view estimate is optional and is used to measure the gap, not to anchor the forecast. Something like "Give me the outside view on how long this migration will take."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
