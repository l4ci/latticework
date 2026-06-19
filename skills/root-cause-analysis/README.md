# root-cause-analysis

## What this is

Root-cause analysis finds and verifies the cause of a problem instead of patching its symptom. It combines two classic tools. The Ishikawa fishbone (cause-and-effect diagram), developed by Kaoru Ishikawa in 1960s Japan and widely published by 1968, sorts possible causes into categories so the search covers everything. The 5 Whys, attributed to Sakichi Toyoda and built into the Toyota Production System, drills a candidate cause down through repeated "why" questions until it reaches a cause you can act on. The default category set is the 6 Ms used in manufacturing and operations (People, Machine, Method, Material, Measurement, Environment), with service variants (the 4 Ps and 8 Ps) for process and service problems.

The fish head, the category sets, the 5 Whys discipline, the verification tests, and the failure modes are in [references/root-cause.md](references/root-cause.md).

## What it does

The skill runs the cause search in parallel. It first states the problem precisely as the head of the fish, quantified where the data allows, and picks the category set. Then a finder subagent takes each category and brainstorms the candidate causes that live there, with the mechanism for each and any supporting evidence, ranked strongest first. A final pass pools the candidates across every category, drills the strongest with why-chains to reach root causes, verifies each against the timeline and the data, separates root causes from contributing ones, and recommends countermeasures that remove the roots. The output is a saved markdown report with the full fishbone, the why-chains, the verification, and ranked countermeasures.

The skill guards against the recurring ways an RCA fails: stopping at the symptom, fixating on the first cause and never scanning the other categories, settling on "human error" instead of the system cause, and letting a lone 5 Whys collapse into one unverified linear guess. It holds the line that a fishbone only lists possible causes and a why-chain is a hypothesis until evidence backs it.

## When to use it

Reach for RCA when a defect, failure, incident, or recurring problem has already happened and its cause is unclear. The unit of analysis is one precisely stated effect, not a vague dissatisfaction. It is the diagnostic engine of the Analyze phase of DMAIC and the Check/Act of a PDCA cycle, and you can also run it directly.

- For the full measure-and-control improvement project this sits inside, use [six-sigma-dmaic](../six-sigma-dmaic/).
- For a fast improvement loop where the cause is already clear enough to act on, use [pdca-cycle](../pdca-cycle/).
- To anticipate how a plan that has not yet run might fail, rather than diagnose one that already did, use [pre-mortem](../pre-mortem/).

## How to get started

**You provide:** one precisely stated effect to diagnose (quantified where possible), plus any data, logs, or context on when it occurs and what changed. Something like "Run an RCA, our checkout API has been timing out since Tuesday."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
