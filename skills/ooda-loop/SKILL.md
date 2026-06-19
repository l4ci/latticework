---
name: ooda-loop
description: 'Use when the user faces a fast-moving, uncertain situation and wants to run an OODA loop (Observe, Orient, Decide, Act), John Boyd''s decision cycle. Guides a tight, repeating loop: observe what is actually happening, orient by breaking and rebuilding the mental model, decide the next move as a hypothesis, act small and fast, then loop. Keeps the focus on orientation and tempo, and maintains a loop log. Triggers include "OODA", "OODA loop", "observe orient decide act", "Boyd", "get inside their decision loop", "fast-moving decision".'
---

# ooda-loop

OODA (Observe, Orient, Decide, Act) is John Boyd's continuous decision loop for moving under time pressure and uncertainty. It catches the failure of acting on a stale mental model: you observe what is happening now, orient by breaking and rebuilding your model, decide the next move as a hypothesis, act small and fast, then loop on the result. Orientation is the heart of it, and tempo is the weapon.

The four stages, how they feed each other, and the pitfalls live in [references/ooda-loop.md](references/ooda-loop.md). Load that file before facilitating.

## When to use

The user is in a fast-moving, uncertain situation where the situation keeps changing while they think: a live incident, a competitive surprise, a negotiation, a fast-shifting market. OODA favors a usable model and a quick rhythm over a complete analysis.

When the user has ample time and a stable problem, prefer a slower, more deliberate method. For a repeating improvement cycle that tests a change against a prediction, use [pdca-cycle](../pdca-cycle/). To first sort what kind of problem this is (clear, complicated, complex, chaotic) before choosing how to act, use [cynefin](../cynefin/). When the uncertainty is about the long-range future rather than the next few minutes, use [scenario-planning](../scenario-planning/).

## Language

Facilitate and write the log in the language the user is writing in. The reference file is English; keep the framework keyed to it regardless of output language.

## Inputs

- **SITUATION** (required): the fast-moving situation to work, including the other party or the changing conditions you are reacting to.
- **CONTEXT** (optional): what just happened, your current read of it, the constraints, and how you can observe results.

## How to facilitate

Run one OODA loop with the user, then loop again. Keep it tight and quick, since the method is about staying ahead of a moving situation. Name the current stage at each step and record it in the loop log. Spend the most effort on Orient.

1. **Observe.** Gather what is actually happening right now: the situation, the environment, the other party's moves, and the feedback from the last action. Separate observation from interpretation. Note specifically what has changed and what is surprising, since surprise is the signal that the model is slipping.

2. **Orient (the heavy step).** This is where most of the effort goes. Surface the mental model in use: the assumptions, prior experience, and analogies the user is reading the situation through. Test that model against the observations and find where it mismatches reality. Then break the stale model and build a better one. A good decision on bad orientation still fails, so do not rush past this to get to a move.

3. **Decide.** Choose the next action as a hypothesis given the current orientation, fast enough to stay ahead of the situation rather than perfect on paper. Note what you expect the action to produce, so the next Observe has something to check against.

4. **Act.** Carry it out small and quick, then observe the result and begin the next loop. Emphasize tempo: cycle faster than the situation or the other party changes, so you are acting on current reality while they react to stale information.

5. **Loop.** Feed the result into the next Observe. Track whether you are gaining or losing tempo: are you getting inside the other party's loop, or falling behind it?

## Loop log

Maintain a markdown log, saved to `ooda-loop-<subject-slug>-<YYYY-MM-DD>.md` (today's date) in the working directory unless the user names another location:

1. **Header.** The situation and the date.
2. **Per loop, a block with:**
   - **Observe:** what is happening now, what changed, what was surprising.
   - **Orient:** the model before, the mismatch the observations exposed, and the model after.
   - **Decide:** the next action chosen as a hypothesis, and what you expect.
   - **Act and result:** what was done and what came back.
3. **Tempo note.** Are we inside the other party's loop or behind it, and is the gap widening or closing?
4. **Caveats.** Orientation can be wrong; speed without correct orientation loses; the loop is a stance, not a one-time plan; and when there is ample time for deliberate analysis, prefer a slower method.

## Principles

- **Orient is the heart, not a quarter of the loop.** Most of the work and most of the failures live in orientation. A perfect decision on a wrong model still loses.
- **Tempo is the weapon.** Cycle faster than the situation changes, so you act on current reality while the other party reacts to stale information.
- **A mismatch between model and reality is the signal to re-orient.** Treat surprise as data. When the situation does something the model did not predict, rebuild the model before deciding.
- **It is a stance, not a plan.** The loop never closes. Each Act reopens Observe.
