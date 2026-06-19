# balanced-scorecard

## What this is

The Balanced Scorecard, from Robert Kaplan and David Norton (Harvard Business Review, 1992; expanded in their 1996 book *The Balanced Scorecard: Translating Strategy into Action*), translates a strategy into objectives and measures across four perspectives: Financial, Customer, Internal Process, and Learning & Growth. The point is to steer a business by more than its financial numbers, which only report results after the fact, and to wire every measure back to the strategy through a chain of cause and effect rather than collecting metrics for their own sake. That chain, drawn across the four perspectives, is the strategy map, which is what separates a scorecard from a plain KPI dashboard.

The four perspectives, the objective/measure/target/initiative structure, the strategy-map logic, and the pitfalls live in [references/scorecard.md](references/scorecard.md).

## What it does

The skill runs the analysis in parallel. Four analyst subagents each take one perspective and derive, from the stated strategy, a few objectives, the measures that track them, the targets to hit, and the initiatives to get there. A synthesis pass then builds the strategy map bottom-up, so the capabilities in Learning & Growth drive the Internal Processes that deliver the Customer value proposition that produces Financial results. The output is a saved markdown report with the four-perspective scorecard table, the strategy map, per-perspective detail, and caveats.

Three guardrails keep it honest, each aimed at a known scorecard failure. The cause-effect links are built explicitly, since a wall of KPIs with no map behind it is a dashboard, not a scorecard. The mix of leading and lagging indicators is checked, since an all-lagging set steers by the rear-view mirror. And the measures are cut to a vital few per perspective, since every function wants its metric on the board.

## When to use it

Reach for the Balanced Scorecard when you have a strategy or vision and want it made measurable: objectives, KPIs, targets, and initiatives that track whether the strategy is being executed, not just whether last quarter's revenue held up. This is where the diagnostic skills hand off, turning a direction into measures someone can be held to.

- For the near-term goal-setting layer that cycles targets each quarter, use [okr](../okr/); the scorecard sets the durable perspectives, OKRs cycle the goals within them.
- For deploying the vital few into owned annual action with formal catchball, use [hoshin-kanri](../hoshin-kanri/).
- To produce the strategic direction the scorecard then measures, use [porters-five-forces](../porters-five-forces/) or [mckinsey-7s](../mckinsey-7s/).

## How to get started

**You provide:** the organization and the strategy being translated (a vague strategy gets drawn out first; unit level and horizon are optional). Something like "Turn our retention-led strategy into a balanced scorecard."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
