# force-field-analysis

## What this is

Force field analysis is Kurt Lewin's way of looking at a proposed change, from his 1943 field theory of change. Any situation that holds steady is in equilibrium: driving forces push toward the change, restraining forces resist it and hold the status quo, and the two are in balance. The status quo is that balance point. You move toward what you want by shifting the balance, either pushing harder on the drivers or easing off the restrainers. Lewin argued the two routes are not equivalent: adding driving force raises the tension and provokes equal counter-pressure, so what moves is fragile and snaps back, while weakening a restrainer lowers tension and lets the situation drift toward the change and stay there. You analyze one specific, well-defined change at a time, since a force can only be judged against a target precise enough to be for or against.

The equilibrium model, the driving and restraining forces with the lenses to hunt across, the 1-to-5 strength scale, the net-field read, and the pitfalls live in [references/force-field.md](references/force-field.md).

## What it does

The skill runs the analysis in parallel. Finder subagents hunt the driving and restraining forces across different lenses (people, organizational, technical, external) and score each one by strength with a rationale. A synthesis pass builds the scored field, reads whether the change is feasible as things stand, and finds the highest-leverage moves to shift the balance, favouring the weakening of restrainers over adding drivers. The output is a saved markdown report with the two-column scored field, the net read, the binding and load-bearing forces, and the leverage moves.

Two rules keep the analysis honest. Both sides get equal effort, because a list that is mostly drivers usually means the restrainer hunt was lazy, not that the change is easy. And every force is scored, because a bare list cannot be read as a field. The net read weighs the columns rather than averaging them, since one binding restrainer can block a change the totals call feasible.

## When to use it

Reach for this when you have a defined change, decision, or goal and want a lighter analytical read on what is pushing for it, what is holding it back, whether it is feasible as things stand, and where the leverage is.

- If you want to lead a full organizational change through to completion rather than just assess it, use [kotter-change](../kotter-change/).
- If you want the individual people-and-adoption side of a change, use [adkar](../adkar/).
- If the forces in play are mostly specific people and you want to map their power and stance, use [stakeholder-analysis](../stakeholder-analysis/).
- If you want to imagine the change failing in order to surface the restrainers, use [pre-mortem](../pre-mortem/).

## How to get started

**You provide:** the change, decision, or goal being assessed, stated as a precise desired state; context on who is involved and the constraints is optional. Something like "do a force field analysis on moving support to a four-day week."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
