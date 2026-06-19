# storm-research

## What this is

STORM (Synthesis of Topic Outlines through Retrieval and Multi-perspective Question Asking) is a research method Stanford published in 2024, peer-reviewed at NAACL 2024 ([Shao et al.](https://aclanthology.org/2024.naacl-long.347/)). Its idea is that good coverage comes from asking questions from many viewpoints at once: rather than one searcher chasing one line of inquiry, it spins up several expert perspectives that each retrieve and interrogate sources, then reconciles them. In Stanford's evaluation, human raters judged more of STORM's articles to be well-organized, a 25% absolute gain over a retrieval-augmented baseline, with 10% broader coverage. Stanford runs a free demo at [storm.genie.stanford.edu](https://storm.genie.stanford.edu), which needs a free account.

## What it does

The skill replicates the method inside an agent and runs it in parallel. Five expert subagents (a practitioner, an academic, a skeptic, an economist, a historian) each do their own retrieval and return a core position with sources. A contradiction map then catalogs where they clash, names the crux question, and flags the blind spot none of them covered. A synthesis pass folds everything into a briefing: a one-paragraph summary, five ranked findings, a hidden connection, an actionable insight, and a frontier question. Finally a panel of three independent critics peer-reviews the result, assigning per-finding confidence scores and naming the gaps. The output is a saved markdown briefing followed by the reconciled review. Stanford flagged that STORM does not self-critique, so the critic panel is the guardrail: each perspective must ground its claims in real sources, and an agent with no retrieval lowers its own confidence rather than inventing citations.

## When to use it

Reach for STORM when you want a rigorous, multi-source, self-critiqued briefing on a topic rather than a quick answer, and the cost of a one-sided read is high. Triggers: "research X deeply", "PhD-level research", "give me a briefing with confidence scores", "what does the evidence actually say".

- If you already have rival explanations and need to decide which the evidence supports, use [analysis-of-competing-hypotheses](../analysis-of-competing-hypotheses/). STORM gathers the perspectives; ACH adjudicates between them.
- If the question is a quantity with no data at hand, use [fermi-estimation](../fermi-estimation/).
- If you want the outside-view base rate for how cases like yours turn out, use [reference-class-forecasting](../reference-class-forecasting/).

## How to get started

**You provide:** the topic to research, and optionally who the insight is for. Something like "Do a STORM-style deep research briefing on whether GLP-1 drugs cut cardiovascular risk independent of weight loss."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
