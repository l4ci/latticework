# cognitive-bias-audit

## What this is

A cognitive bias is a systematic, not random, departure from sound reasoning: the same pressures bend a decision the same way every time, which is why you cannot simply notice them and think them away. The idea comes from the heuristics-and-biases tradition founded by Amos Tversky and Daniel Kahneman in the 1970s (their 1974 Science paper "Judgment under Uncertainty: Heuristics and Biases") and the large body of work that followed, including Kahneman's 2011 Thinking, Fast and Slow. This audit groups the named biases into five families: belief and evidence, confidence and prediction, attachment and loss, social, and framing and salience. What works against them is not generic awareness but auditing a specific decision against the known families and installing structural countermeasures into the process that produced it.

The bias families, each with its tell and its countermeasure, plus the debiasing toolkit, are in [references/biases.md](references/biases.md).

## What it does

The skill runs the audit in parallel. Five hunter subagents each take one bias family and look for where this reasoning is actually exposed, citing the step or claim where each bias operates, rating how much it could distort the call, and how sure they are it is operating. A synthesis pass then ranks the live biases by how much they threaten this particular decision, names the one or two most dangerous, prescribes specific debiasing moves (a pre-mortem, the outside view, forcing explicit criteria, separating the reads), and gives a corrected read of the decision. The output is a saved markdown report.

The framework fails in three predictable ways, and the skill is built around them. People label biases generically with no evidence any of them operate here, which is just theater. People audit everyone else's reasoning and never their own. And people reach for "that's just confirmation bias" to wave away a conclusion they dislike. The guard is the same throughout: every flagged bias must quote the actual reasoning where it shows up, the findings are severity-ranked to this decision, and the prescriptions are process changes rather than "just be aware." A bias label marks where the process is exposed, not a refutation, so the audit ends with what survives it.

## When to use it

Reach for a bias audit before committing to a high-stakes decision or forecast, or to pressure-test an analysis you or someone else produced. The unit is one decision and the reasoning behind it. It often prescribes the sibling tools as countermeasures, so reach for those directly when they fit:

- If you want to imagine the decision has already failed and work backward, use [pre-mortem](../pre-mortem/).
- If you are choosing among options and want explicit, weighted criteria, use [weighted-decision-matrix](../weighted-decision-matrix/).
- If forecasting accuracy is the worry, anchor on base rates with [reference-class-forecasting](../reference-class-forecasting/).
- If competing explanations need disconfirmation, use [analysis-of-competing-hypotheses](../analysis-of-competing-hypotheses/).

## How to get started

**You provide:** the decision being made and the reasoning behind it (both required; the stakes are optional and sharpen the ranking). Something like "Audit our decision to acquire this competitor for cognitive biases."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
