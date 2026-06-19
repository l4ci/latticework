# scarf

## What this is

SCARF reads a situation for social threat and reward across five domains, on the premise that the brain treats social experience much like physical survival. It comes from David Rock (*SCARF: A Brain-Based Model for Collaborating with and Influencing Others*, 2008). Status is your relative standing; Certainty is your ability to predict what comes next; Autonomy is your sense of control and choice; Relatedness is your sense of belonging and safety with others; Fairness is your read on whether exchanges are even-handed. A threat in any domain pushes people to pull away; a reward pulls them in. The asymmetry matters: a threat fires faster and harder than an equivalent reward, and a single high threat can swamp rewards spread across the rest.

The five domains, their threat and reward triggers, the levers, and the pitfalls live in [references/scarf.md](references/scarf.md).

## What it does

The skill runs the read in parallel. Five analyst subagents each take one domain, assess what the situation does there for the people affected, mark the threat and the reward with evidence and a severity, and propose specific levers. A synthesis pass then ranks the threats, names the domains most at risk, and designs concrete moves that lower threat and add reward, prioritizing the few highest-leverage ones. The output is a saved markdown report with a per-domain read, a verdict on where it lands hardest, and an ordered list of what to do first. Three guardrails keep it honest: it caveats the science throughout (SCARF is a heuristic for noticing social threat, not a measurement instrument), it ranks by which domain carries the biggest threat so an easy fix elsewhere cannot mask the worst one, and it forces every fix to name a domain and a concrete action rather than fall back on "communicate more."

## When to use it

Reach for SCARF when you are about to do something to or with people who may feel threatened: announce a change, give feedback, send a difficult message, reorganize a team, or make a contentious decision. The unit of analysis is one situation and the people it affects, read for where it will land as a threat and how to defuse it.

- If you need to plan the change itself rather than defuse a single moment, use [kotter-change](../kotter-change/), [adkar](../adkar/), or [force-field-analysis](../force-field-analysis/).
- If the question is the standing climate of a team rather than one event, use [psychological-safety](../psychological-safety/).
- If you need to map power and interest across many parties, use [stakeholder-analysis](../stakeholder-analysis/).

## How to get started

**You provide:** one concrete situation (a change, message, or decision) and, where you can, who is affected and from whose point of view to read the threat. A phrase like "Use SCARF on the reorg announcement I'm about to send."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
