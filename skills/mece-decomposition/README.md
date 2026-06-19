# mece-decomposition

## What this is

MECE is the test of a good breakdown: a set of categories is Mutually Exclusive when no item fits more than one (no overlaps) and Collectively Exhaustive when every item fits somewhere (no gaps). Pass both and a vague problem becomes a logic tree, also called an issue tree, that can be divided, delegated, and solved without double-counting or blind spots. The principle comes from structured problem solving at McKinsey and was popularized by Barbara Minto in *The Pyramid Principle* (1973). The first cut decides most of it, meaning the logic used to split the top level: get that right and the rest of the tree follows, get it muddled and you end up with overlaps and gaps that no amount of tidying will fix.

The principle, the decomposition archetypes, and the ME and CE tests are in [references/mece.md](references/mece.md).

## What it does

Because the first cut decides everything, the skill does not commit to the first idea. Three decomposer subagents propose competing top-level cuts in parallel, each using a different logic (algebraic, process, segment, and so on). A selection pass picks or merges the sharpest, the tree is built only as deep as the purpose needs, and then two checkers audit it in parallel: one hunts overlaps, the other hunts gaps and inconsistent levels. Violations are fixed at the level where they originate rather than patched at the leaves. The output is a saved markdown logic tree with its MECE check and the alternatives considered.

One rule keeps it honest: a catch-all "Other" branch is allowed only when the remainder is genuinely small and varied, and it must be labeled, never used to hide a real category. The skill structures the problem, it does not solve it.

## When to use it

Reach for MECE when you need rigorous structure: a problem to break down, a metric to decompose into drivers, a topic to map completely, or an issue tree to build. If you only need a quick informal list, this is heavier than necessary.

- To sharpen the problem before decomposing it, use [tosca-problem-definition](../tosca-problem-definition/) first.
- If the goal is to test which of several explanations holds, use [analysis-of-competing-hypotheses](../analysis-of-competing-hypotheses/).
- To structure the answer for a reader once the analysis is done, use [scqa-pyramid](../scqa-pyramid/), whose key line must itself be MECE.

## How to get started

**You provide:** what to decompose (a problem, question, metric, or topic), and optionally what the breakdown is for. Something like "Build an issue tree for why our revenue dropped."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
