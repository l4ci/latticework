# jobs-to-be-done

## What this is

Jobs-to-Be-Done is a lens on customer motivation: customers do not buy products, they hire a solution to make progress in a struggling moment. The unit of analysis is the *job in a circumstance*, solution-agnostic and stable over time, not the customer's demographics and not a feature list. People don't want a quarter-inch drill, they want a quarter-inch hole, and beyond that the progress the hole enables. The lens is associated with Clayton Christensen, who popularized it (notably in *Competing Against Luck*, 2016), and with the outcome-driven innovation tradition of Tony Ulwick, who developed the measurable-outcome and opportunity-scoring side of it. The "milkshake" and "quarter-inch hole" framings made it widely known, though the underlying idea traces back further (the drill quote is often attributed to Theodore Levitt).

The three dimensions, desired outcomes, the four forces, the job-story format, and the opportunity-scoring formula are in [references/jtbd.md](references/jtbd.md).

## What it does

The skill frames the job first, then runs the analysis in parallel. After defining the customer and the struggling moment precisely, five analyst subagents each take one facet: the functional job; the emotional and social job; the desired outcomes (as measurable outcome statements); the competing solutions including workarounds and nonconsumption; and the four forces of progress that drive or block a switch. A synthesis pass then writes the job story, ranks the desired outcomes by opportunity score to find the underserved ones, reads whether the four forces favor a switch, and draws implications for the offering. The output is a saved markdown report. Three guardrails counter the recurring traps: every job is anchored to a trigger rather than demographics, all three dimensions are carried through to synthesis, and nonconsumption is counted as a competitor so the largest rival is not missed.

## When to use it

Reach for this skill to shape or reposition an offering around what customers are trying to accomplish, decide what to build, or understand why customers switch.

- This skill *finds* the job and where current solutions fall short; once the job is understood, use [value-proposition-canvas](../value-proposition-canvas/) to *map* a specific offering onto it.
- If you are classifying which features drive satisfaction for the job, use [kano-model](../kano-model/).
- If you want to design and test solutions to the job through user research, use [design-thinking](../design-thinking/).

## How to get started

**You provide:** the product, service, or category and the customer it serves; optionally the struggling moment, the segment or market, and the decision the analysis should inform. Something like "what job are customers hiring this for?"

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
