# hexaco-personality-test

## What this is

HEXACO describes personality along six dimensions: Honesty-Humility, Emotionality, eXtraversion, Agreeableness, Conscientiousness, and Openness to Experience, each broken into four facets. It was developed by Kibeom Lee and Michael Ashton from lexical studies across many languages, which kept turning up a sixth factor the Big Five misses. That factor, Honesty-Humility (sincerity, fairness, greed-avoidance, modesty), predicts integrity-relevant behavior such as exploitation and entitlement. HEXACO also rotates Emotionality and Agreeableness relative to Big Five Neuroticism and Agreeableness, so the anger pole sits under low Agreeableness rather than Neuroticism. The version used here is the public-domain 240-item IPIP-HEXACO scales (Ashton, Lee, and Goldberg, 2007), ten items per facet rated on a 1-to-5 accuracy scale.

The 240 questionnaire items live in [references/items.md](references/items.md).

## What it does

The skill administers the questionnaire as a conversation in the user's own language, presenting the 240 items in batches with the accuracy scale shown each time, and can run across several sittings since it is long (roughly 30 to 40 minutes). It hides which factor or facet each item belongs to and how it is keyed while testing, so answers track the statement rather than the trait. On completion it reverse-scores the keyed items, takes the mean of each facet and factor, assigns bands, and writes a saved markdown report: a summary table with text bars, a per-factor deep dive with facet breakdowns grounded in the actual answer pattern, notable trait interactions, reflection prompts, and caveats. Honesty-Humility gets full weight, since it is what this instrument adds over Big Five. The report carries the limits plainly: self-report captures self-image on one day, this preliminary IPIP-HEXACO set has no population norms and facet scales are short, so readings are indicative, and this is not a clinical or diagnostic tool.

## When to use it

Reach for this when the user wants a six-factor personality read, or specifically wants the Honesty-Humility dimension that Big Five omits, and is willing to sit through the long form for facet-level detail.

- For a quicker five-factor result (50 items, about ten minutes), use [ocean-personality-test](../ocean-personality-test/), which cannot measure Honesty-Humility.
- To surface the assumptions a person or team is making about a decision, use [key-assumptions-check](../key-assumptions-check/).
- To check reasoning for systematic distortion rather than measure traits, use [cognitive-bias-audit](../cognitive-bias-audit/).

## How to get started

**You provide:** nothing; the skill interviews you, presenting the 240 items in batches and scoring your answers. Something like "Give me a HEXACO test."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
