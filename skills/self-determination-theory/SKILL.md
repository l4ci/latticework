---
name: self-determination-theory
description: Use when the user wants to understand why a person, role, or team has gone disengaged, demotivated, resistant, or burnt out, and what would actually re-engage them, including assessing their own motivation. Runs Deci and Ryan's Self-Determination Theory by fanning out three parallel analyst subagents, one per basic psychological need (Autonomy, Competence, Relatedness), each scoring both satisfaction and frustration for its need with evidence and how much it bears on the problem, then names the binding need, places motivation on the controlled-to-autonomous continuum, and prescribes targeted need-supportive moves in a detailed markdown report. Guards against the reflex of blaming generic "low motivation" when one specific need is being thwarted. Triggers include "self-determination theory", "SDT", "autonomy competence relatedness", "intrinsic motivation", "why is the team disengaged", "basic psychological needs".
---

# self-determination-theory

Runs Deci and Ryan's Self-Determination Theory to diagnose why motivation has dropped and what would restore it. The theory's core claim: three innate psychological needs (Autonomy, Competence, Relatedness) drive engagement and wellbeing when met and drive disengagement and ill-being when thwarted. So the question is never "is motivation high or low" but "which need is being thwarted, and how do we support it." Catches the costly default error of treating disengagement as a generic motivation deficit and reaching for a reward or a pep talk, when one specific need is being undermined and only supporting that need will help.

The three needs, the satisfaction-versus-frustration distinction, the controlled-to-autonomous motivation continuum, and the diagnostic prompts live in [references/self-determination-theory.md](references/self-determination-theory.md). Load that file before diagnosing and judge each need against it exactly. Do not reproduce any validated instrument's items; use the generic prompts in the reference.

## When to use

The user is looking at flagging motivation, disengagement, drift, resistance, or burnout in a person, a role, or a team, and wants to know what is actually driving it and how to turn it around. The unit of analysis is one person or one bounded group in one domain (work, study, a relationship to a task), read for the satisfaction and frustration of the three needs. The user may be assessing their own motivation, in which case the skill can interview them rather than work from secondhand report. Use [com-b](../com-b/) when the question is the mechanics of one specific behaviour (capability, opportunity, motivation) rather than the deeper quality and sources of someone's motivation. Use [scarf](../scarf/) when the question is where a specific change or message will land as a social threat. Use [psychological-safety](../psychological-safety/) for the standing climate of a team rather than the motivation of a person or role. Use [okr](../okr/) to set goals once motivation is understood, not to diagnose it.

## Language

Conduct the session and write the report in the language the user is writing in. The reference file is English; keep the framework keyed to it regardless of the output language.

## Inputs

- **SUBJECT** (required): whose motivation is in question, a person, a role, or a team (possibly the user themselves). If it is a broad group with different experiences, segment it or pick the segment that matters.
- **DOMAIN** (required): the area of life or work the motivation concerns (a job, a course, a particular kind of task). The same person can be autonomously motivated in one domain and amotivated in another, so the read is always domain-bound.
- **SIGNS** (required): the observed signs that prompted the question, disengagement, drift, resistance, burnout, quiet quitting, a drop in output or quality. These are the symptoms the diagnosis must explain. If the user only says "they seem off," sharpen it with a question or two first.
- **CONTEXT** (optional): recent changes, history, what has been tried, and the decision the diagnosis should inform. This shapes the weighting and the intervention design, not the per-need readings.

If the subject is the user's own motivation and the signs are vague, interview them: ask about each need in turn using the diagnostic prompts before dispatching the analysts, or have the analysts work from the interview answers.

## Orchestration map

```
Stage 1  Frame            ── inline ──────────────────────────────┐  (whose motivation, in what domain, observed signs)
Stage 2  Need Assessment  ── 3 analyst subagents IN PARALLEL ─────┤  (each scores satisfaction + frustration for one need)
Stage 3  Synthesis        ── 1 agent, needs all 3 ────────────────┘  (binding need → place on continuum → need-supportive moves)
```

Tell each subagent its final message is the return value: structured data, not prose for a human. Subagents should use available retrieval tools to ground their read in real evidence where the situation references documents, history, or stated reactions.

## Stage 1: Frame (inline)

State whose motivation is in question (SUBJECT), in what DOMAIN, and the observed SIGNS in one or two sentences. If the user is assessing their own motivation and the signs are loose, interview them first using the diagnostic prompts in the reference. Carry the framing into every analyst prompt so all three read the same situation.

## Stage 2: Need Assessment (PARALLEL)

Dispatch three analyst subagents at once, one per need: Autonomy, Competence, Relatedness. Give each the shared framing plus its need's section from the reference file.

**Shared framing (send to each analyst):**

> Assess one basic psychological need for this subject: **[SUBJECT]**, in the domain of **[DOMAIN]**, who is showing these signs: **[SIGNS]**. Work only your assigned need, using its section and diagnostic prompts from the framework. Read the need twice, as two distinct measures, not one high-low scale. Ground each claim in evidence (stated facts, history, observed behaviour) where you can, and mark fact versus inference. Return:
> - **Satisfaction:** to what degree the need is actively met here, rated high / medium / low, with the specific tells and evidence.
> - **Frustration:** to what degree the need is actively thwarted or undermined here, rated high / medium / low, with the specific tells and evidence. Active thwarting is more damaging than mere low satisfaction, so report it separately and do not average it away.
> - **Bearing on the problem:** how much this need explains the observed signs, rated high / medium / low.
> - **Supports and thwarts:** what is supporting and what is thwarting this need in this specific situation.
> - **Confidence:** high, medium, or low, lowered when you are inferring rather than working from stated facts.
>
> Do not reproduce items from any validated scale; use the generic prompts. Context: [CONTEXT]

Collect all three structured results before continuing. Re-dispatch any analyst that fails rather than synthesizing with a gap.

## Stage 3: Synthesis (SEQUENTIAL, needs all 3)

One agent merges the three reads into a diagnosis and an intervention plan, finding the binding need rather than restating the three:

1. **Name the binding need.** Rank the three needs by how much they drive the observed signs, weighting active frustration over mere low satisfaction. Name the one (or at most two) needs most responsible: the most thwarted, least satisfied need that explains the disengagement. A need can be well satisfied and still leave the person disengaged if another is being thwarted; the thwarted one is the binding need.
2. **Guard against the mislabeling trap.** State plainly that the problem is a specific need being thwarted, not generic "low motivation." If the user, prior attempts, or the obvious framing assumed the person is just unmotivated or needs a reward, test that against the evidence and say which need is actually the wound. Adding a reward to a person whose autonomy is being crushed makes the controlled motivation worse, not better; name the error.
3. **Place motivation on the continuum.** Locate where the subject's current motivation sits on the controlled-to-autonomous continuum (amotivation, external, introjected, identified, integrated, intrinsic) and say what is driving the current behaviour. Thwarted needs push motivation toward the controlled end; the binding need usually explains the position.
4. **Prescribe need-supportive moves.** For each deficient need, turn its supports into specific actions for this subject and domain: what to do, change, or say, and who does it. Lift the thwarting first, then add support. No generic "boost morale"; name the concrete move. Note any secondary need that will need attention once the binding one is addressed.
5. **Set a re-check.** Say what to watch for and when to reassess, since needs interact and supporting one can change the reading on another.

## Report structure

Write a thorough markdown report and save it to `self-determination-theory-<subject-slug>-<YYYY-MM-DD>.md` (today's date) in the working directory unless the user names another location.

1. **Header.** The subject, the domain, the observed signs, the context if given, the date, and a one-line note that SDT diagnoses the sources of motivation, not a clinical state.
2. **Need profile.** A small summary table: each need (Autonomy, Competence, Relatedness) with its satisfaction rating, its frustration rating, and its bearing on the problem. Flag the binding need up front.
3. **Need detail (three sections).** Each need in turn: the tells, what supports and what thwarts it here, the evidence (fact versus inference), the satisfaction and frustration readings, and confidence.
4. **Binding need.** The one or two needs most responsible, why, and an explicit statement of the mislabeling trap (the specific need being thwarted, not generic low motivation).
5. **Motivation quality.** Where the subject sits on the controlled-to-autonomous continuum and what is driving the current behaviour.
6. **Interventions.** The targeted need-supportive moves per deficient need, each a concrete action with who does it, plus any secondary need waiting behind the binding one.
7. **Re-check.** What to watch for and when to reassess.
8. **Caveats.** SDT is a diagnostic of the sources of motivation, not a clinical or psychiatric assessment; it rests on self-report and inference, not measurement, and no validated instrument was administered; you can build conditions that support motivation but cannot manufacture someone else's autonomous motivation directly; and the three needs interact, so supporting one can shift the reading on another.

## Principles

- **Find the thwarted need, do not blame "low motivation."** Disengagement is a symptom; the cause is a specific need being undermined. Naming "low motivation" is the classic, costly mislabel.
- **Frustration outweighs low satisfaction.** Read each need twice. Active thwarting does more damage than mere neglect; rank by it and lift the thwarting first.
- **Motivation is quality, not amount.** Place it on the continuum. Controlled motivation can produce output and still be the problem; the aim is more autonomous motivation, not just more of it.
- **You support motivation, you do not install it.** Build need-supportive conditions; you cannot inject someone else's intrinsic motivation, and pressure aimed at it backfires.
