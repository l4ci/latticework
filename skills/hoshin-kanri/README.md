# hoshin-kanri

## What this is

Hoshin Kanri is a strategy-deployment method from Japanese Total Quality Management, formalized by Yoji Akao and others in the 1960s and 1970s and adopted at Toyota, Bridgestone, and Hewlett-Packard. The name translates roughly as "direction management"; in English it is usually called policy deployment or strategy deployment. It rests on two ideas. The first is the vital few, where a year's strategy is concentrated into three or four breakthrough objectives rather than spread across everything. The second is catchball, where objectives and targets are negotiated up and down the organization so the people who must deliver them help shape them. Its central artifact is the X-matrix, a single page linking breakthrough objectives, annual objectives, improvement priorities, measurable targets, and owners, with correlation marks showing how each leg connects to the next.

The X-matrix, the catchball process, the review cadence, and the pitfalls live in [references/hoshin.md](references/hoshin.md).

## What it does

The skill runs the cascade in parallel. It first sets the breakthrough objectives and this year's annual objectives with the user, holding the line on the vital few, then dispatches one strategist subagent per annual objective to develop its improvement priorities, measurable targets, owners, and the pushback the working level would raise. A synthesis pass then builds the X-matrix, marks the correlations, traces the golden thread so every priority and target ties back to a breakthrough objective, flags the orphans on either side, and sets the catchball rounds and the PDCA review cadence. The output is a saved markdown report with the vital few, the X-matrix, deployment detail, the alignment check, and the review rhythm.

Four guardrails work against the method's usual failures. Stage 1 pushes back toward three or four objectives when teams cascade too many. The strategists surface realistic pushback before anything is committed, so plans are not handed down without catchball. Every priority must earn a number with a level and a date, so activities cannot pose as targets. And the report ends in a tracking and review rhythm, so the matrix is not built once and filed.

## When to use it

Reach for Hoshin Kanri when you have a strategy and need to turn it into a focused, owned, measurable plan that reaches the working level, where alignment across levels matters more than speed. It catches the failure where strategy stays at the top and daily work drifts from it.

- For a lighter, more recent goal-setting method without the X-matrix or formal catchball, use [okr](../okr/).
- For translating strategy into balanced measures and a strategy map rather than deploying the vital few, use [balanced-scorecard](../balanced-scorecard/).
- For the plan-do-check-act loop Hoshin reviews on, use [pdca-cycle](../pdca-cycle/).

## How to get started

**You provide:** the organization deploying the strategy and the strategy or breakthrough objectives themselves; optionally the planning horizon, the levels to cascade through, and any fixed constraints. Something like "Run a Hoshin Kanri on our new strategy."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
