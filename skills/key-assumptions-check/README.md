# key-assumptions-check

## What this is

The Key Assumptions Check (KAC) is a core structured analytic technique codified by Richards Heuer and Randolph Pherson in *Structured Analytic Techniques for Intelligence Analysis* (2010, with later editions). It catches a quiet failure: a confident conclusion rests on assumptions the analyst never noticed making, and when one breaks the whole structure falls, because the assumption was never on the table to be questioned. An assumption is anything taken as true, without current proof, to let the analysis proceed. The stated ones are rarely the problem; the unstated ones are. KAC puts every premise in the open, tests it, and tells you which ones the answer actually depends on.

## What it does

The skill runs KAC inside an agent and parallelizes it. Proposer subagents fan out to surface the full set of assumptions from several stances (stated premises, unstated premises, cultural defaults, continuity assumptions, actor assumptions), then the set is reconciled into one register. Each assumption is restated as a falsifiable proposition with scope, quantity, and timeframe made explicit. One subagent per assumption then tests it, committed to breaking it: confidence, the basis for that confidence, the conditions under which it fails, whether it has quietly decayed, and the impact if it is wrong. A classification pass sorts them into solid, caveated, or unsupported on a confidence-against-impact matrix. Three critics then hunt the linchpins, attack the register for what everyone missed, and reverse the most consequential assumptions to see if the answer changes. The output is a saved markdown report with the assumption register, the linchpins, the unsupported assumptions each paired with a next action, the caveats to carry, and indicators to monitor. A flagged assumption is something to act on rather than a final judgment, so each one comes with a way to verify it, hedge it, or rebuild without it.

## When to use it

Reach for KAC when an analysis, plan, recommendation, or forecast silently rests on something and the cost of that something breaking is high: a strategy that assumes a competitor won't react, a forecast that assumes the past pattern holds, a plan that assumes a dependency lands on time. Triggers: "what are we assuming", "what is this resting on", "what if we're wrong about X", "pressure-test the premises".

- If you are testing which of several rival explanations is true rather than what an analysis assumes, use [analysis-of-competing-hypotheses](../analysis-of-competing-hypotheses/). KAC tests what an analysis rests on; ACH tests the explanations themselves.
- If you want to imagine the fragile premises actually failing, run a [pre-mortem](../pre-mortem/) after the KAC.
- If the task is to choose between options on value grounds, use [weighted-decision-matrix](../weighted-decision-matrix/).

## How to get started

**You provide:** the analysis, plan, claim, or forecast to check, given as the reasoning or the conclusion with its main supporting argument. The domain, stakes, and who relies on it are optional. Something like "What are we assuming in our plan to enter the German market?"

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
