# tuckman

## What this is

Bruce Tuckman's stages of group development hold that teams mature through predictable stages. The model comes from Tuckman's 1965 paper, with Adjourning added in 1977, and runs through five stages: Forming, where a polite, anxious team leans on the leader and roles are unclear; Storming, where conflict and jockeying break out and most teams stall; Norming, where norms, trust, and cohesion settle in; Performing, where the team is autonomous and runs itself; and Adjourning, where it disbands. Performance does not climb in a straight line: it dips through Storming before it rises. The stages are not a one-way ratchet either, since a team can regress when membership, leadership, or goals change.

The five stages, the leadership focus each needs, the bar for advancing, regression, and the pitfalls live in [references/tuckman.md](references/tuckman.md).

## What it does

The skill runs the diagnosis in parallel. After a quick pass to identify the team and gather observable behaviors and history, five assessor subagents each score how well the team matches one stage, with evidence and any sign of regression. A synthesis pass then locates the current stage, checks whether a recent change dropped the team back a stage, prescribes the leadership style the stage actually needs (direct, coach, facilitate, delegate, or close well), lays out concrete moves to advance, and names what is blocking the transition. The output is a saved markdown report with a per-stage assessment, a verdict, and the single most important move called out.

Three guardrails keep it honest. It scores each stage from observed behavior rather than how the team describes itself, so surface calm never gets mistaken for cohesion. It accounts for regression instead of assuming a team holds the highest stage it ever reached. And it treats Storming as the work, not a detour to be skipped, then matches the leadership style to the actual stage.

## When to use it

Reach for this when a real team is new, has just changed shape, is stuck in conflict, is onboarding, or is trying to mature, and you want to know where it is and what would help it advance. The unit is one team's developmental stage. Pick a sibling when the question is different:

- If the question is the five behaviors that break a team's results, use [five-dysfunctions-of-a-team](../five-dysfunctions-of-a-team/).
- If the question is whether members feel safe to speak up, use [psychological-safety](../psychological-safety/).
- If the situation is an organizational change rolling out across a team, use [kotter-change](../kotter-change/).

## How to get started

**You provide:** the one team to diagnose (required), and optionally context like tenure, recent changes, and how meetings and conflict go. Something like "what Tuckman stage is my team at?"

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
