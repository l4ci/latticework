# impact-feasibility-matrix

## What this is

The impact-feasibility matrix prioritizes a set of options (initiatives, ideas, features, projects) by plotting each on two axes, impact and feasibility, and sorting them into four quadrants: quick wins (high impact, high feasibility, do first), major projects (high impact, low feasibility, plan and stage), fill-ins (low impact, high feasibility, spare capacity only), and thankless tasks (low impact, low feasibility, drop). It is also called the impact-effort matrix, where feasibility is the inverse of effort and risk. It belongs to the family of 2-by-2 prioritization grids that spread through management consulting in the late twentieth century; no single inventor is credited, and the tool is better understood as a convention than a named theory.

The axes, the four quadrants, and the scoring guidance are in [references/impact-feasibility.md](references/impact-feasibility.md).

## What it does

The skill calibrates the axes first, stating exactly what impact means for the stated objective and what drives feasibility (effort, cost, risk, dependencies), because unanchored scores just encode bias. It then scores every option in parallel, one subagent per option, deliberately pessimistic about feasibility. A synthesis pass recalibrates the scores for consistency (the parallel scorers did not see each other), places the quadrants, maps dependencies between options, and produces a sequenced plan rather than four unordered piles. The output is a saved markdown report with the matrix, the scored options, and a recommended order of action. Two guardrails keep it honest: the calibration step handles undefined axes, and prompting scorers to probe what could make each option harder handles optimism on effort. Often the most useful output is a clear case for stopping the thankless work.

## When to use it

Reach for this when you have more options than you can do and need to decide what to do first, what to plan, and what to drop. If the options do not yet exist, generate them first; this skill prioritizes an existing set.

- If the criteria are many or specific to the decision rather than just impact and effort, use [weighted-decision-matrix](../weighted-decision-matrix/).
- If you are sequencing a product backlog and reach and confidence matter enough to model, use [rice-prioritization](../rice-prioritization/).
- If you want to stress-test the chosen plan for how it could fail before committing, use [pre-mortem](../pre-mortem/).

## How to get started

**You provide:** the list of options to prioritize and the objective impact is measured against, optionally the resources, constraints, timeframe, and known dependencies. Something like "prioritize these by impact and feasibility."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
