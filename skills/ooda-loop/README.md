# ooda-loop

## What this is

OODA (Observe, Orient, Decide, Act) is a continuous decision loop for acting under time pressure and uncertainty. You observe the unfolding situation, orient by making sense of what you see, decide the next move, and act, then the result feeds straight back into the next observation. John Boyd, a United States Air Force colonel, fighter pilot, and strategist, developed it from the 1970s to the 1990s out of air-combat analysis and his energy-maneuverability theory, then generalized it well beyond the cockpit. Orient is the most important station: it is where you break a stale mental model and build a better one, and it shapes everything else in the loop. The other lever is tempo, cycling faster than the situation or the other party changes, so your moves keep invalidating their read of reality.

The four stages, how they feed each other, and the common pitfalls are in [references/ooda-loop.md](references/ooda-loop.md).

## What it does

The skill facilitates one OODA loop end to end and then runs the next, keeping a loop log. Observe gathers what is actually happening now and separates fact from interpretation, flagging what changed and what was surprising. Orient is the heavy step: it surfaces the mental model in use, tests it against the observations, finds where it mismatches reality, and rebuilds it. Decide chooses the next action as a hypothesis given that orientation. Act carries it out small and quick and feeds the result back into the next loop. The output is a saved markdown loop log with one block per loop, a tempo note, and caveats.

Two things keep it honest, and the skill insists on both: the most effort goes into orientation rather than rushing to a move, and each loop tracks tempo, whether you are getting inside the other party's loop or falling behind it.

## When to use it

Reach for OODA in a fast-moving, uncertain situation where the situation keeps changing while you think: a live incident, a competitive surprise, a negotiation, a fast-shifting market. It trades a complete analysis for a usable model and a quick rhythm.

- For a repeating improvement cycle that tests a planned change against an explicit prediction, use [pdca-cycle](../pdca-cycle/).
- To first sort what kind of problem you face (clear, complicated, complex, chaotic) before deciding how to act, use [cynefin](../cynefin/).
- When the uncertainty is about the long-range future rather than the next few minutes, use [scenario-planning](../scenario-planning/).

## How to get started

**You provide:** the fast-moving situation to work, including the other party or the changing conditions you are reacting to, and optionally what just happened and how you can observe results. Something like "Run an OODA loop on a competitor that just undercut our price."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
