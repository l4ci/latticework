# bcg-matrix

## What this is

The BCG Growth-Share Matrix plots a portfolio of business units or product lines on two axes: market growth rate (how much cash a unit consumes) and relative market share (the unit's share divided by the largest competitor's, a proxy for competitive strength). Each unit lands in one of four quadrants. Stars are high growth and high share, Cash Cows are low growth and high share, Question Marks are high growth and low share, and Dogs are low growth and low share. Every quadrant implies a move: invest, milk, build-or-divest, or release. Bruce Henderson and the Boston Consulting Group introduced it in 1970.

The two axes, the four quadrants and their strategies, the cash-flow logic, and the critiques live in [references/bcg.md](references/bcg.md).

## What it does

The skill runs the analysis in parallel. One analyst subagent places each unit, stating the market definition it used, finding the growth rate and the relative share against the largest competitor, and sizing the unit by revenue. A synthesis pass then assesses whether the portfolio is self-funding, traces which units should fund which (Cash Cows funding Stars and the Question Marks worth backing), and recommends per-unit and portfolio-level moves. The output is a saved markdown report with the matrix, per-unit placements, a cash-flow balance assessment, and recommendations. The framework's critiques travel into the analysis: market definition drives every placement, relative share is a crude proxy for advantage, and a Dog can be profitable while a Star loses money.

## When to use it

Reach for the BCG matrix when you have two or more business units or products and need to decide where to invest, hold, harvest, or divest, or to see whether the portfolio is balanced. It needs a portfolio, so prefer a sharper tool when the question is narrower:

- If the question is how the firm should grow rather than which units to fund, use [ansoff-matrix](../ansoff-matrix/).
- If you want to balance core, emerging, and future bets over time, use [three-horizons](../three-horizons/).
- If the question is one market's competitive structure, use [porters-five-forces](../porters-five-forces/).
- If you want a resource-based read on what sustains a unit's advantage, use [vrio-analysis](../vrio-analysis/).

## How to get started

**You provide:** the portfolio of two or more business units or product lines. Growth, share, and revenue data are optional but valuable, and estimated where missing. Something like "Run a BCG matrix across our product portfolio."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
