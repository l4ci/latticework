# first-principles

## What this is

First-principles thinking reasons up from fundamental, established truths rather than by analogy to how a thing is already done. The idea is old: in Aristotle a first principle is a foundational proposition that cannot be deduced from any other, the bedrock a chain of reasoning bottoms out in. The modern practice belongs to the mental-models tradition (Charlie Munger, the Farnam Street writing on latticework), and it is the discipline behind costing a product up from its raw materials instead of from what the market charges. The move is always the same: strip a problem down to the few things that genuinely hold, then rebuild from there as if the conventional answer did not exist.

The method, the bedrock test that separates fact from assumption, and the reconstruction step live in [references/first-principles.md](references/first-principles.md).

## What it does

The skill runs in three stages. First it frames the problem, the real goal it serves, and the conventional approach with the assumptions baked into it. Then it fans out four subagents in parallel, each attacking the problem through a different lens (physical and material limits, the cost floor, the real requirement, and hard constraints like regulation), to decide for each assumption whether it is necessarily true or merely inherited by analogy, and to establish what is actually bedrock. A final pass assembles the surviving fundamentals, flags each as fact or assumption, discards the assumptions that fell, reconstructs a solution from the bedrock alone, and sets it beside the convention to show what convention was costing. The output is a saved markdown report with the teardown table, the bedrock, the reconstruction, and a side-by-side contrast.

Two rules keep it honest: every bedrock truth is flagged fact or assumption so a buried guess is never mistaken for a foundation, and every piece of the convention is treated as inherited until a test proves it necessary.

## When to use it

Reach for first principles when you are stuck inside a conventional approach and want to know whether the convention is load-bearing or merely "how it has always been done." It is the tool for the question "why do we do it this way, and does it have to be?" It is expensive, so prefer a sharper or lighter tool when the question is narrower:

- If you only need to break one problem into clean, non-overlapping branches, use [mece-decomposition](../mece-decomposition/).
- If you need to list the assumptions a plan rests on and rank them by fragility, use [key-assumptions-check](../key-assumptions-check/).
- If you want to find the worst outcome and reason backward to avoid it, use [inversion](../inversion/).
- If you are tracing a failure that already happened back to its origin, use [root-cause-analysis](../root-cause-analysis/).

## How to get started

**You provide:** the problem, the conventional or current way it is done, and the real goal that approach is meant to serve. Something like "We run a 24/7 staffed support desk because that is what support means. Reason it from first principles."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
