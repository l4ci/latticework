# ocean-personality-test

## What this is

The Big Five model (OCEAN) describes personality along five broad dimensions: Openness, Conscientiousness, Extraversion, Agreeableness, and Neuroticism. It grew out of the lexical hypothesis, the idea that the traits people care about end up encoded as words in their language, and took shape through factor-analytic work by researchers including Lewis Goldberg, who coined the "Big Five" label in 1981. The version used here is Goldberg's public-domain 50-item IPIP Big-Five Factor Markers (1992), with ten items per dimension rated on a 1-to-5 scale.

The 50 questionnaire items live in [references/items.md](references/items.md).

## What it does

The skill administers the questionnaire as a conversation in the user's own language, presenting the 50 items in batches of ten with the Likert scale shown each time. It hides which factor each item belongs to and how it is keyed while testing, so the user answers the statement rather than the trait. On completion it reverse-scores the keyed items, sums each dimension into a total and a per-item average, assigns a band, and writes a saved markdown report: a summary table with text bars, a deep dive per dimension grounded in the actual answer pattern, notable trait interactions, reflection prompts, and caveats. The interpretation cites the answers that drove each band rather than reciting generic trait blurbs, and the report carries the limits plainly: self-report captures self-image on one day, the IPIP-50 has no population norms, and this is not a clinical or diagnostic tool.

## When to use it

Reach for this when the user wants to take a Big Five or OCEAN personality test, or wants their personality read across the five dimensions, and a quick five-factor result is enough.

- For a longer, facet-level result that also measures Honesty-Humility (the integrity-relevant dimension Big Five omits), use [hexaco-personality-test](../hexaco-personality-test/).
- To surface the assumptions a person or team is making about a decision, use [key-assumptions-check](../key-assumptions-check/).
- To check reasoning for systematic distortion rather than measure traits, use [cognitive-bias-audit](../cognitive-bias-audit/).

## How to get started

**You provide:** nothing; the skill administers the 50-item questionnaire and you answer as you go. Something like "Give me the Big Five personality test."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
