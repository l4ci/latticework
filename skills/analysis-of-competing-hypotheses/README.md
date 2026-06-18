# analysis-of-competing-hypotheses

Adjudicates which of several rival explanations the evidence actually supports, using Analysis of Competing Hypotheses (ACH) — the structured analytic technique developed by Richards Heuer at the CIA and published in *Psychology of Intelligence Analysis* (1999).

ACH is built to defeat confirmation bias. Instead of picking a favored explanation and reading new facts as support, it lays out every plausible hypothesis at once and scores all of the evidence against all of them. Its signature move is ranking by **disconfirmation**: the most likely hypothesis is the one with the *least evidence against it*, not the one with the most evidence for it — because evidence "for" a hypothesis is usually consistent with several rivals and proves little.

This skill runs ACH inside an agent and parallelizes it. It fans out subagents to propose a near-exhaustive hypothesis set (including the unwelcome and the deceptive), gathers the evidence (including the telling *absence* of evidence), then scores each hypothesis in its own column with an independent mind committed to disproving it. It drops the evidence that can't discriminate, ranks the hypotheses by weighted inconsistency, stress-tests the few linchpin facts the answer depends on, and reports the full field of relative likelihoods with the indicators that would change the verdict.

It is the natural partner to [storm-research](../storm-research/): STORM gathers the evidence and the perspectives; ACH decides which story that evidence supports.

The skill itself lives in [SKILL.md](SKILL.md).
