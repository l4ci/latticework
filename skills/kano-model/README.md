# kano-model

## What this is

The Kano model classifies product features by how their presence or absence drives customer satisfaction, so investment lands where it pays. It was developed by Noriaki Kano and colleagues at the Tokyo University of Science, published in 1984. Features sort into five categories: must-be features that are expected and only punish you when missing; one-dimensional features whose satisfaction rises with how well you do them; attractive features that delight precisely because no one expected them; indifferent features nobody cares about; and reverse features that customers would rather not have. Each category follows a different satisfaction curve, which is why treating them all the same wastes effort.

The five categories, the evaluation table, the satisfaction curves, decay, and the pitfalls are in [references/kano.md](references/kano.md).

## What it does

The skill runs the classification in parallel. One analyst subagent takes each feature, reasons through the paired functional question ("how would this segment feel if it's present?") and dysfunctional question ("how would they feel if it's absent?"), maps the answer pair through the Kano evaluation table to a category, and notes confidence, decay risk, and how the category shifts across segments. A synthesis pass then turns categories into decisions: confirm every must-be is covered, pick the performance features to compete on, back a few delighters, cut the indifferent, avoid the reverse, and sequence the work with a decay timeline. The output is a saved markdown report with a classification table, per-feature reasoning, and a recommended feature set. Guardrails address the recurring traps: must-be coverage is forced before any delighter spend, every classification is keyed to a named segment with decay marked, and a classification made without real customer data is flagged as a reasoned proxy for a survey, not the survey itself.

## When to use it

Reach for this skill when deciding which features to build, prioritize, cut, or how to position them, and you want to know which features matter to satisfaction and why.

- Kano says which features matter and why, but does not score effort or revenue; pair it with [rice-prioritization](../rice-prioritization/) to sequence the backlog.
- If you first need to understand the underlying jobs the features serve, use [jobs-to-be-done](../jobs-to-be-done/).
- If you want to map features to customer pains and gains, use [value-proposition-canvas](../value-proposition-canvas/).

## How to get started

**You provide:** the target customer segment and the candidate feature list to classify; optionally the product, its market and competitors, the decision it informs, and any real customer data. Something like "run a Kano analysis on these features."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
