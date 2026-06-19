# scenario-planning

## What this is

Scenario planning builds several distinct, plausible futures for a decision instead of a single forecast. The method here is the 2x2 critical-uncertainties technique from the Global Business Network and Royal Dutch Shell tradition, set out by Peter Schwartz in *The Art of the Long View* (1991). You start from a focal question tied to a real decision, gather the forces that could shape the answer, and find the two forces that both matter most and are hardest to call. Crossing those two gives four corners, and each corner is a different world. The aim is to prepare for an uncertain future, not to predict the one that shows up.

The method, the axis-selection logic, what makes a good scenario, how to write signposts, and the pitfalls are in [references/scenarios.md](references/scenarios.md).

## What it does

The skill runs the analysis across three stages. First it gathers the driving forces (a PESTEL scan is a good source), ranks them by impact and uncertainty, and picks the two critical uncertainties as the axes. Then four scenario-builder subagents work at once, one per quadrant, each developing a named world: how it got there from today, what it looks like, and what it means for the focal question. A synthesis pass then turns the four scenarios into strategy, separating the moves that make sense in every future from the hedges tied to one, and pulling out the early signposts that tell you which future is arriving. The output is a saved markdown report with the 2x2, the four scenarios, the robust-versus-contingent strategy, and the signpost dashboard.

Three rules guard against the failures that wreck a scenario set: only genuinely uncertain forces may be axes (predetermined trends become the shared backdrop), the two axes are tested for independence so the 2x2 does not collapse into one future at four intensities, and no scenario carries a probability so the work ends in strategy rather than a disguised forecast.

## When to use it

Reach for scenario planning when a decision's right answer depends on an uncertain future and you want to stress-test strategy against several of them rather than one forecast. The unit of analysis is a focal question tied to a decision-maker and a horizon, not "the future" in the abstract. Pick a different tool when uncertainty is not the crux:

- If you first need to surface the macro forces that could become axes, run [pestel-analysis](../pestel-analysis/); its high-impact, high-uncertainty watch list feeds straight in.
- If the future is clear enough for a single read of position, use [swot-analysis](../swot-analysis/).
- If the scenarios are set and you need to sequence moves over time, use [three-horizons](../three-horizons/).

## How to get started

**You provide:** a focal question tied to a real decision and entity, plus a horizon and any driving forces already known (a PESTEL scan is a good source). Something like "Run scenario planning on our on-prem product line over the next decade."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
