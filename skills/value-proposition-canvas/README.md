# value-proposition-canvas

## What this is

The Value Proposition Canvas zooms into the customer-fit detail of the Business Model Canvas: it takes just two of that canvas's nine blocks, Value Propositions and Customer Segments, and examines whether they fit. It comes from Alexander Osterwalder, Yves Pigneur, Greg Bernarda, and Alan Smith (*Value Proposition Design*, 2014). It has two halves: the Customer Profile, where you describe the customer's jobs, pains, and gains; and the Value Map, where you describe the offering's products and services, pain relievers, and gain creators. Fit is the match between them, where relievers and creators land on the customer's most important jobs, severest pains, and most-wanted gains.

The two sides, the ranking rule, the fit-check table, and the three levels of fit are in [references/value-proposition.md](references/value-proposition.md).

## What it does

The skill runs the analysis in parallel. Six analyst subagents work the two sides at once: three describe and rank the Customer Profile, three describe the Value Map, and all mark every claim a fact or an assumption still to be tested. A fit-assessment pass then ranks the customer side and checks the match: which of the customer's most important jobs, severest pains, and most-wanted gains the value map actually addresses, which it misses, and which relievers and creators chase pains and gains nobody ranks highly. The output is a saved markdown report with both sides laid out, a fit verdict, and the riskiest assumptions called out. Ranking the customer side by importance before the value side is touched is the guardrail: it exposes effort aimed at minor items. The skill is also explicit that a canvas shows problem-solution fit at most, not product-market fit (needs market evidence) or business-model fit (needs the Business Model Canvas).

## When to use it

Reach for this skill to test problem-solution fit for one offering aimed at one customer segment, when the question is narrower than the whole business model.

- If you want the whole model and its viability across nine blocks, use [business-model-canvas](../business-model-canvas/); this is its zoom-in companion.
- If the underlying job is not yet clear, run [jobs-to-be-done](../jobs-to-be-done/) first, which goes deeper on the Customer Jobs half.
- If you are classifying which features drive satisfaction once the fit is understood, use [kano-model](../kano-model/).

## How to get started

**You provide:** the one offering to test and the one customer segment it is aimed at (both required), plus optional context like stage, evidence available, and the decision it should inform. Something like "build a Value Proposition Canvas for our app."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
