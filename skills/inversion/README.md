# inversion

## What this is

Inversion attacks a problem from the back. Forward thinking asks "how do I achieve X?"; inversion asks "what would guarantee I fail at X, or produce the opposite?", lists those failure paths, then avoids them. It comes from the mathematician Carl Jacobi, whose maxim "man muss immer umkehren" ("invert, always invert") urged solving hard problems by turning them around, and it was carried into decision-making by Charlie Munger: "All I want to know is where I am going to die, so I will never go there," and his standing preference for avoiding stupidity over seeking brilliance. The tool has two complementary uses. For a goal to reach, list everything that would cause the worst outcome and design to avoid them. For a quality to protect (trust, retention, safety), ask what would destroy it. Avoiding the obvious ways to fail often beats clever optimization.

The framework, the two uses, and the avoid-rule logic live in [references/inversion.md](references/inversion.md).

## What it does

The skill frames the goal forward, then flips it into a single inverted question. From there it runs in parallel: five generator subagents each manufacture concrete ways to cause the worst outcome from one lens (self-inflicted, external, people and incentives, process and execution, second-order and slow-burn), rating each path by how easily it gets taken and how badly it wrecks the goal. A synthesis pass then deduplicates and ranks the paths by plausibility times damage, distills the few absolute "never" bright lines, and converts each top path into an avoid-rule or action ("do not...", "ensure..."). The output is a saved markdown report with the ranked failure paths, the bright lines, the avoid-list turned into action, and a verdict.

Two rules keep it honest: the generators manufacture failure without hedging, and the run does not finish at a list of failures but at the constraints they convert into.

## When to use it

Reach for inversion when you have a goal, problem, or quality and want to find what would wreck it so you can steer clear, including when there is no plan yet. It is generative and general, so prefer a sharper tool when the fit is wrong:

- If there is already a specific, formed plan and you want that exact plan stress-tested and hardened, use [pre-mortem](../pre-mortem/). It assumes the plan failed and works backward; inversion needs no plan.
- If the worry is that flawed reasoning or blind spots are distorting the judgment itself, use [cognitive-bias-audit](../cognitive-bias-audit/).
- If you want to rebuild the goal from the ground up rather than find what would ruin it, use [first-principles](../first-principles/).

## How to get started

**You provide:** the goal, problem, or quality to invert, stated forward, plus any context on constraints and what the opposite outcome looks like. Something like "Invert our goal of keeping our best engineers for the next three years, so we can see how we'd drive them all out."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
