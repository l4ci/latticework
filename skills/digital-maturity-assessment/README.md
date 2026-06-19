# digital-maturity-assessment

## What this is

Digital maturity is how effectively an organization uses digital technology, data, and ways of working to create value. This assessment scores seven dimensions (strategy and leadership, customer experience, technology and architecture, data and analytics, operations and process, people and culture, and innovation and ecosystem) on a five-level scale from Nascent to Leading, locates the gaps against the organization's ambition, and produces a roadmap. There is no single founder. The dimensions and levels follow the structure shared by the established maturity models (MIT/Capgemini's Digital Transformation work and Deloitte's digital maturity model are the usual references), which agree that maturity is as much about strategy, people, and culture as about technology.

The five maturity levels, the seven dimensions, and the target-setting step live in [references/maturity.md](references/maturity.md).

## What it does

The skill runs the assessment in parallel. Seven assessor subagents each score one dimension against the level descriptors, using evidence of what is actually in production and in behavior rather than what is planned. A synthesis pass draws the maturity profile (the uneven shape, not a single average), finds the gaps that bind and the imbalances where a lagging dimension strands an advanced one, and sequences a roadmap toward the target. The output is a saved markdown report with the maturity profile, per-dimension detail, and a prioritized roadmap.

Two rules guard the result. Assessors score production and behavior, not decks and pilots, and flag missing evidence rather than guessing. And the analysis treats the lagging dimension, not the average, as the constraint on realized value, so a strong technology score stranded behind weak people and culture is read as the real limit.

## When to use it

Reach for this when you want to know where an organization stands on digital and what to do next: a transformation baseline, a readiness check, or a roadmap input. The unit is an organization or business unit, and the soft dimensions count as much as the hard ones.

- For general organizational alignment across the full firm rather than digital capability, use [mckinsey-7s](../mckinsey-7s/).
- For value creation and cost across the firm's activities, use [value-chain-analysis](../value-chain-analysis/).
- To run a structured improvement loop once the roadmap names the moves, use [pdca-cycle](../pdca-cycle/).
- To turn the roadmap into measurable goals, use [okr](../okr/).

## How to get started

**You provide:** the organization or unit to assess; a target maturity level and any evidence (systems, metrics, examples) are optional but valuable. Something like "assess the digital maturity of our regional insurance business."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
