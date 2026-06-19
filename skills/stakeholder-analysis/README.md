# stakeholder-analysis

## What this is

Stakeholder analysis maps the people and groups who affect or are affected by an initiative and decides how much engagement each one is worth. The core tool is the power-interest grid (Aubrey Mendelow, 1991), which plots every stakeholder on two axes: their power to influence the outcome, and their interest in it. The axes cross into four quadrants, each with its own strategy. Key players who can decide the outcome and care about it get managed closely. People with power but little interest get kept satisfied so they do not intervene late. People who care but cannot drive it get kept informed. The rest get monitored. A usable analysis goes past the grid to read each stakeholder's current stance, what they want, what they fear, and who they sway. The point is to put effort where it changes the result instead of spreading it evenly.

The two axes, the four quadrants, the stance and influence-network dimensions, and the pitfalls live in [references/stakeholders.md](references/stakeholders.md).

## What it does

The skill builds the stakeholder list with you, then runs the analysis in parallel. One analyst subagent takes each stakeholder and reads their power, their interest, where they currently stand, what they actually want, what they fear, and who they sway, each judgment tied to evidence rather than a job title. A synthesis pass places everyone on the grid, writes the engagement plan per quadrant, maps the supporter coalition against the set of blockers, and names the few relationships that, if shifted, change the most. The output is a saved markdown report with the grid, per-stakeholder detail, the engagement plan, the coalition and blockers, and the highest-leverage moves.

Three failures show up again and again, and the skill guards against each. Power and interest get scored separately, so a loud stakeholder with no real lever is not managed like a decision-maker. Stance is checked rather than assumed, so unknowns are marked unknown instead of read as neutral. And the report is dated and meant to be re-run at milestones, because power, interest, and stance all move with each decision.

## When to use it

Reach for this when you are launching or steering a project, change, decision, or rollout and the risk is people rather than technical execution: who to involve, who to keep satisfied, who could block it, and who to win over.

- If the people side is part of a wider organizational change you are leading, use [kotter-change](../kotter-change/).
- If you want to diagnose whether individuals will actually adopt the change, use [adkar](../adkar/).
- If you want to weigh the forces for and against a specific change, use [force-field-analysis](../force-field-analysis/).
- If you want to stress-test how a key player turning blocker could sink the initiative, use [pre-mortem](../pre-mortem/).

## How to get started

**You provide:** the initiative whose stakeholders you are mapping, plus any context on its phase and known tensions. Something like "Do a stakeholder analysis for our move to a four-day work week."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
