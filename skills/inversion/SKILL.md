---
name: inversion
description: Use when the user wants to attack a goal or problem backward instead of forward, asking what would guarantee failure or the opposite outcome so those paths can be avoided. Fans out parallel subagents that each generate ways to cause the worst result across a distinct lens, then ranks the failure paths, distills the absolute bright lines, and turns each into an avoid-rule or action in a markdown report. Triggers include "inversion", "invert the problem", "work backward", "how could this fail", "avoid stupidity", "Munger inversion".
---

# inversion

Inversion attacks a goal from the back. Instead of asking "how do I achieve X?", it asks "what would guarantee I fail at X, or produce the opposite?", enumerates those failure paths, then systematically avoids or neutralizes them. The move follows Carl Jacobi's maxim "invert, always invert" and Charlie Munger's preference for avoiding stupidity over chasing brilliance. Catches the failure where forward planning chases clever optimization while an obvious, avoidable path to ruin sits in plain sight.

The framework, the two uses (a goal to reach, a quality to protect), and the avoid-rule logic live in [references/inversion.md](references/inversion.md). Load that file before working and follow the inverted-question and avoid-list rules exactly.

## When to use

The user has a goal, problem, or quality to protect and wants to find what would wreck it, so they can steer clear. Inversion is general and generative: it applies to any goal, including ones with no plan yet, and it returns a list of things to avoid and the constraints they imply. If there is already a specific, formed plan and the user wants that exact plan stress-tested, prefer [pre-mortem](../pre-mortem/), which assumes the plan failed and works backward to harden it. Inversion needs no plan; a pre-mortem needs one.

## Language

Conduct the session and write the report in the language the user is writing in. The reference file is English; keep the framework keyed to it regardless of output language.

## Inputs

- **GOAL** (required): the goal, problem, or quality to invert. Stated forward ("keep our best engineers", "launch a product users trust"). An inversion without a goal has nothing to invert, so if the user does not give one, ask for it before starting.
- **CONTEXT** (optional): constraints, the setting, who is involved, the time horizon, and what "the opposite outcome" concretely looks like. Sharpens both the failure generation and the avoid-list.

## Orchestration map

```
Stage 1  Frame             ── inline, no subagent ──────────────┐  (state forward, then invert)
Stage 2  Failure Generation ── 5 generator subagents IN PARALLEL ┤  (each manufactures failure from one lens)
Stage 3  Synthesis         ── 1 agent, needs all 5 ─────────────┘  (rank, distill bright lines, invert to action)
```

Tell each subagent its final message is the return value: structured data, not prose for a human.

## Stage 1: Frame (inline)

State the goal forward as the user gave it. Then restate it inverted: "How would we guarantee the opposite or the worst possible outcome?" Write the inverted question out in plain words, because every generator works from it. For a goal to reach, the inversion is "what would make us fail at it". For a quality to protect (trust, retention, safety), the inversion is "what would destroy it". Carry the inverted question into the shared framing below.

## Stage 2: Failure Generation (PARALLEL)

Dispatch five generator subagents at once, one per lens. Give every generator the shared framing plus one lens. The job is to manufacture failure on purpose, not to weigh whether it will happen; the weighing comes in Stage 3.

**Shared framing (send to every generator):**

> Your task is to guarantee the worst outcome. The goal, stated forward, is: **[GOAL]**. Inverted, the question you answer is: **[INVERTED QUESTION]**. Working only from your assigned lens, invent concrete, specific ways to cause that failure or the opposite result. Do not hedge, do not balance, do not suggest fixes: your single job is to find paths to ruin. Return a list of failure paths; for each one give:
> - **Failure path** (one line: the way to cause the bad outcome)
> - **Mechanism** (how it actually produces the opposite result, step by step)
> - **Plausibility** (1 to 5: how easily this path gets taken in real life, with a one-line reason)
> - **Damage** (1 to 5: how badly it wrecks the goal, with a one-line reason)
>
> Goal and context: [GOAL] / [CONTEXT]

**Lenses (one per generator):**

1. **Self-inflicted (own actions):** the ways we wreck it ourselves through our own choices, neglect, or arrogance. The own goals.
2. **External (environment):** the conditions outside our control that, if we walk into them or ignore them, cause the opposite outcome.
3. **People and incentives:** how the people involved, and what they are rewarded for, drive the result the wrong way. Misaligned incentives, who quits, who games it.
4. **Process and execution:** how the day-to-day mechanics, handoffs, and quality of doing the work produce failure even when the intent is right.
5. **Second-order and slow-burn:** the failures that build quietly over time, the moves that look fine now and rot later, the things that "succeed" while undermining the goal.

Collect all five structured results before continuing. Re-dispatch any generator that fails rather than synthesizing with a gap.

## Stage 3: Synthesis (SEQUENTIAL, needs all 5)

One agent merges everything and turns it from a pile of failure paths into a set of things to avoid:

1. **Deduplicate and cluster.** The same path often appears under several lenses, worded differently. Merge them, and note which lenses raised each, since cross-lens agreement is a signal of severity.
2. **Rank.** For each merged path settle on plausibility (1 to 5) and damage (1 to 5), compute **severity = plausibility x damage** (1 to 25), and rank. Band them: 20 to 25 critical, 12 to 19 high, 6 to 11 medium, 1 to 5 low.
3. **Distill bright lines.** From the top paths, name the few absolute "never" rules: the small set of things that, done even once, are catastrophic or irreversible. These are the bright lines, kept separate because they are not tradeoffs.
4. **Invert each path to an action.** For each top failure path, write the avoid-rule, constraint, or move that neutralizes it: a "do not..." or "ensure..." stated concretely enough to act on. This is the deliverable; an unconverted failure list is half-finished.
5. **Verdict.** What avoiding these failures changes about the approach, and the few avoid-rules that matter most.

## Report structure

Write a thorough markdown report and save it to `inversion-<subject-slug>-<YYYY-MM-DD>.md` (today's date) in the working directory unless the user names another location.

1. **Header.** The goal stated forward, the inverted question, the date, and any context.
2. **Failure paths.** A ranked table: the path, plausibility, damage, severity, band, the lens (or lenses) it came from.
3. **Bright lines.** The few absolute "never" rules distilled from the top paths, set apart because they are not tradeoffs.
4. **Avoid-list to action.** Each top failure path mapped to the constraint or move that neutralizes it, as a concrete "do not..." or "ensure...".
5. **Verdict.** What avoiding failure changes about the approach, and the avoid-rules that matter most.
6. **Caveats.** Inversion finds what to avoid, not the positive path to win, so pair it with forward planning. Avoiding every risk can mean achieving nothing; some failure paths are the cost of a worthwhile goal. The ranking is judgment, not measurement.

## Principles

- **Invert before you generate.** The whole method rests on a clean inverted question. State the goal forward, flip it, then work the flip.
- **Manufacture failure honestly.** In Stage 2 the job is to cause ruin, not to balance or reassure. Hedging dilutes the find. Weighing happens in Stage 3.
- **Finish with the avoid-list.** A list of failure paths is not the deliverable. The constraints and actions they convert into are.
- **Avoiding stupidity, not chasing brilliance.** The payoff is steering clear of the obvious ways to lose. Pair it with forward planning to actually win.
