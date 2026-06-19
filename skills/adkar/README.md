# adkar

## What this is

ADKAR is Prosci's model for the people side of change, from Jeff Hiatt's *ADKAR: A Model for Change* (2006). Its premise is that organizations do not change; the people in them do, and a project succeeds only when enough of the affected people make their own transition. Each person moves through five blocks in order: Awareness of why the change is needed, Desire to support it, Knowledge of how to change, Ability to actually perform the new way, and Reinforcement that holds it in place. Because the blocks are sequential, a change stalls at the first one a person has not reached. That stall point is the barrier, and it is where the work has to go. The unit of analysis is the affected group, not the whole organization, since different groups sit at different barriers.

The five elements, their diagnostic questions, the strength-rating scale, the barrier-point logic, and the pitfalls live in [references/adkar.md](references/adkar.md).

## What it does

The skill scopes the affected groups, then runs the assessment in parallel. Five subagents each assess one element, rating how well it is achieved for every group against the evidence: what was communicated, what training exists, how people actually behave, what gets rewarded. A synthesis pass finds the barrier point for each group (the first weak element, read in order), works out the specific gap behind it, and designs interventions starting at the barrier and sequenced through the blocks beyond it, with owners. The output is a saved markdown report with a per-group scorecard, the barrier for each group, and the ordered plan.

It guards against the failure modes that sink most change work. Projects reach for training because it is easy to schedule, but training people who have no Desire produces capable people who will not use what they learned, so the skill diagnoses Desire before Knowledge. It refuses a single org-wide score, because an average hides where adoption is breaking down. And it checks Reinforcement, the block teams skip when they declare victory at go-live and then watch people drift back.

## When to use it

Reach for this when a change is in flight or planned and you want to understand why it is not being adopted, or to plan the people side before launch. The unit is the individual moving through the change, assessed per affected group.

- ADKAR diagnoses the individual side of the same change that [kotter-change](../kotter-change/) leads at the org level; the two pair directly, so run both when a change needs work at both levels.
- If you first need to map who the affected groups are and how to engage them, use [stakeholder-analysis](../stakeholder-analysis/).
- If the missing block is Desire and you want to dig into the motivation behind resistance, use [com-b](../com-b/).
- If you want to weigh the forces for and against the change as a whole, use [force-field-analysis](../force-field-analysis/).

## How to get started

**You provide:** the specific change being made and who is making it; affected groups and history are optional but sharpen the read. Something like "Run an ADKAR analysis on why field sales aren't adopting our new CRM."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
