# fermi-estimation

## What this is

Fermi estimation is a way to produce a defensible order-of-magnitude estimate of a quantity with no data at hand. It is named for the physicist Enrico Fermi, who was known for answering seemingly unanswerable questions ("how many piano tuners are there in Chicago?") by decomposing them into factors he could each guess roughly. It works because of how the errors behave: when you break a quantity into a chain of independent estimated factors, the over- and under-estimates tend to cancel, so a product of rough guesses is far more accurate than one rough guess at the whole. The method handles two opposite failures: the blind guess (a number from nowhere, impossible to interrogate) and the refusal ("we have no data, so we can't say"). You can always get an auditable answer good to roughly an order of magnitude.

## What it does

The skill runs Fermi estimation inside an agent and parallelizes it. It first frames the quantity precisely, pinning the scope, the units, and whether to build bottom-up or top-down. Decomposer subagents then break the quantity apart several independent ways (bottom-up, top-down, proxy, dimensional), and the cleanest chain is picked as primary with a structurally different one reserved as a cross-check. One subagent per leaf factor estimates it as a low/best/high range with its basis, anchoring on a real figure where one exists. A combine pass multiplies the chain, propagates the uncertainty into an honest band, and reports the answer to one or two significant figures. Three critics then run the reserved second path, sanity-check against hard bounds, and name the dominant factor whose uncertainty swamps the rest. The output is a saved markdown report with the estimate and its band, the auditable decomposition table, the load-bearing factors, the dominant uncertainty, and the independent cross-check. Throughout, the method works in ranges rather than single points, checks the estimate against a second path, and reports no more significant figures than the inputs justify.

## When to use it

Reach for Fermi estimation when you need a number, have little or no direct data, and a rough answer now is worth more than a precise answer you will never get: market sizing, capacity and load estimates, cost or effort ballparks, feasibility sanity checks. The point is an auditable estimate where any single factor can be challenged. Triggers: "Fermi estimate", "back-of-the-envelope", "order of magnitude", "ballpark this", "how many, roughly".

- If you want the outside view (how similar cases actually turned out), use [reference-class-forecasting](../reference-class-forecasting/). Fermi is the inside-view counterpart that builds the estimate up from this case's own components; running both and reconciling the gap is a strong cross-check.
- If the question is not really quantitative but is about which explanation is true, use [analysis-of-competing-hypotheses](../analysis-of-competing-hypotheses/).
- If a quantified option needs to feed a choice, pass the estimate into a [weighted-decision-matrix](../weighted-decision-matrix/).

## How to get started

**You provide:** the quantity to estimate, stated with its units. The precision you need and any real numbers you already have are optional. Something like "Fermi-estimate the UK market for electric cargo bikes."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
