# analysis-of-competing-hypotheses

## What this is

Analysis of Competing Hypotheses (ACH) is a structured analytic technique developed by Richards Heuer at the CIA and laid out in *Psychology of Intelligence Analysis* (1999). It counters confirmation bias. Instead of picking a favored explanation and reading new facts as support for it, ACH lays out every plausible hypothesis at once and scores all the evidence against all of them. The signature move is ranking by disconfirmation: the most likely hypothesis is the one with the least evidence against it, not the one with the most evidence for it, because evidence "for" a hypothesis is usually consistent with several rivals and proves little.

## What it does

The skill runs ACH inside an agent and parallelizes it. Proposer subagents fan out to build a near-exhaustive hypothesis set from different stances (the conventional read, the unwelcome read, the deception read, the base-rate read, the structural read), then the set is reconciled to a clean, mutually exclusive list. An evidence inventory captures every datum, including the telling absence of evidence. One subagent per hypothesis then scores each item in its own column, committed to disproving that hypothesis rather than defending it. A diagnosticity pass drops the evidence consistent with everything, weights the rest by credibility, and ranks the hypotheses by fewest weighted inconsistencies. Three critics stress-test the result for linchpin fragility, planted evidence, and missing hypotheses. The output is a saved markdown report with the auditable scoring matrix, relative likelihoods across the whole field, the linchpins the verdict depends on, and indicators to watch. Two rules hold the method together: rank by disconfirmation, and never prune a hypothesis to a favorite early, since one never on the matrix can never be tested.

## When to use it

Reach for ACH when you face a truth question with several rival explanations and the cost of anchoring on the wrong one is high: incident root-cause, diagnosis, attributing a trend to a cause, any "we think it's X" claim that deserves testing against the alternatives. Triggers: "which explanation is most likely", "what's really going on", "rule out the alternatives".

- If you first need to gather the evidence and perspectives, use [storm-research](../storm-research/), then bring its findings here. STORM gathers; ACH decides.
- If you are testing the assumptions an analysis rests on rather than rival explanations themselves, use [key-assumptions-check](../key-assumptions-check/).
- If the choice is about what is preferable rather than what is true, use [weighted-decision-matrix](../weighted-decision-matrix/).
- If you need plausible futures rather than the most likely past cause, use [scenario-planning](../scenario-planning/).

## How to get started

**You provide:** the truth question with its rival explanations. Any evidence you already hold, and who acts on the answer, are optional. Invoke with something like "Run an ACH on what's really behind our Q2 churn spike."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
