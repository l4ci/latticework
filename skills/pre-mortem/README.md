# pre-mortem

## What this is

A pre-mortem stress-tests a plan, PRD, strategy, or decision before you commit to it. The technique uses prospective hindsight: imagine it is some months from now and the plan has already failed, then work backward to explain why. Naming a failure as a fact, rather than asking "what could go wrong?", removes the optimism of an open future and surfaces risks the open question tends to miss. The method comes from research psychologist Gary Klein, who popularized it in the 2000s, drawing on earlier work by Deborah Mitchell, Jay Russo, and Nancy Pennington showing that prospective hindsight raises the number of reasons people can generate for a future outcome.

## What it does

The skill runs the exercise in parallel. Six independent failure-finder subagents each attack the plan from a different lens (execution and technical, people and adoption, timeline and resources, assumptions and dependencies, second-order effects, external and competitive). A blind-spot pass then catches what every lens missed. The risks are deduplicated and clustered, scored by likelihood and impact, ranked by severity, and the worst ones get concrete mitigations, leading indicators, and contingencies. The output is a saved markdown report with an executive summary, a ranked risk register, detailed entries for the critical and high risks, the flagged blind spot, and an honest list of what the exercise judged low risk. The framing is enforced: it must be "it failed, explain why," not "what might go wrong," because treating the failure as certain is what gets people to answer honestly.

## When to use it

Reach for this when you have a plan, PRD, strategy, launch, migration, or decision and want it stress-tested before committing. Not for work already shipped (that is a post-mortem) and not for debugging a specific failure.

- If the subject is a system with many independent failure points rather than one plan with a dominant way to fail, use [fmea](../fmea/), the scored, enumerative counterpart.
- If you have already picked a direction and want it scored against weighted criteria, use [weighted-decision-matrix](../weighted-decision-matrix/).
- If the load-bearing beliefs behind the plan are what you most distrust, use [key-assumptions-check](../key-assumptions-check/).

## How to get started

**You provide:** the plan, PRD, strategy, or decision to stress-test, plus what "failure" means here. A phrase like "Run a pre-mortem on our Stripe billing migration."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
