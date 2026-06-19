# swot-analysis

## What this is

SWOT sorts the factors bearing on a goal into four quadrants: Strengths and Weaknesses (internal to the subject) and Opportunities and Threats (out in the world). Its origins are debated, usually traced to business-policy teaching at Harvard in the 1960s and to Albert Humphrey's research at the Stanford Research Institute. On its own the framework is just four lists. The value comes from the TOWS matrix, a later addition (Heinz Weihrich, 1982) that crosses the quadrants into concrete strategic options: use strengths on opportunities, defend weaknesses against threats, and so on.

The framework, the quadrant checklists, the scoring, and the TOWS logic live in [references/framework.md](references/framework.md).

## What it does

The skill runs the analysis in parallel. Four analyst subagents each take one quadrant, ground their factors in evidence, and prioritize them by magnitude (and likelihood, for the external quadrants). A synthesis pass then validates that each factor sits on the right axis, builds the TOWS matrix (SO, ST, WO, WT), and ranks the resulting options by impact and feasibility. The output is a saved markdown report with the SWOT grid, the prioritized quadrants, the TOWS strategy matrix, and ranked recommendations.

Two rules keep it honest, both guarding against common SWOT failures: every factor is judged against a stated objective, and internal attributes never get filed as external conditions.

## When to use it

Reach for SWOT to assess the position of a company, product, project, team, or decision when you need a broad, qualitative read before settling on a strategy. It is the generalist of the positioning tools, so prefer a sharper one when the question is narrow:

- If the question is specifically about industry profit structure and competitive pressure, use [porters-five-forces](../porters-five-forces/).
- If you only need to scan the external macro-environment, use [pestel-analysis](../pestel-analysis/).
- If the future is too uncertain for a single read, use [scenario-planning](../scenario-planning/).
- If the goal is to break out of head-to-head competition, use [blue-ocean-strategy](../blue-ocean-strategy/).

## How to get started

**You provide:** what is being analyzed and the objective the SWOT serves, plus any context on competitors and time horizon. Something like "Run a SWOT on our meal-kit startup, to decide whether to expand into California."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
