# thomas-kilmann

## What this is

The Thomas-Kilmann Conflict Mode Instrument, from Kenneth Thomas and Ralph Kilmann, places conflict behavior on two axes: assertiveness, or how much you push for your own goals, and cooperativeness, or how much you work to satisfy the other party's. The two axes produce five modes: Competing (assertive, uncooperative), Collaborating (assertive, cooperative), Avoiding (unassertive, uncooperative), Accommodating (unassertive, cooperative), and Compromising in the middle. The instrument's founding claim is that none of them is best: each fits some situations and fails in others, and the skill of conflict handling is matching the mode to the situation in front of you rather than the one you reach for by habit.

The two axes, the five modes with their fits and risks, and the pitfalls live in [references/thomas-kilmann.md](references/thomas-kilmann.md).

## What it does

The skill runs the analysis in parallel. First it pins down the situation: the stakes for each side, the power balance, how much the relationship matters, the time pressure, and the trust between the parties. Then five analyst subagents each take one mode and judge how well it fits those exact facts, with pros, cons, a likely outcome, and a fit score. A synthesis pass ranks the modes, recommends a primary mode and a fallback for when it stalls, and turns the choice into concrete things to say and do. The output is a saved markdown report with a verdict, the situation, the five mode assessments, and the recommendation. Three guardrails keep it honest: it anchors every judgment to the situational factors rather than preference, it refuses a universal favorite (especially chronic collaborating, which wastes time on trivia, or chronic avoiding, which lets conflicts fester), and it flags when the user's habitual style is the wrong fit for this particular conflict.

## When to use it

Reach for this skill when you face a concrete conflict, disagreement, or dispute between defined parties and are deciding how to approach it. The unit of analysis is one situation, not a personality and not a general communication style.

- If the chosen mode is collaborating or compromising and a deal must be worked, use [negotiation-prep](../negotiation-prep/).
- If the conflict spans several parties with different stakes and power, use [stakeholder-analysis](../stakeholder-analysis/).
- If the question is the underlying behaviour you want from someone rather than how to handle a dispute, use [com-b](../com-b/).

## How to get started

**You provide:** the conflict to navigate (the parties, what each wants, what's at stake), plus any context on power, the relationship, time, and your own habitual style. Something like "Help me handle this conflict with a co-founder using Thomas-Kilmann."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
