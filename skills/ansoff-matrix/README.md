# ansoff-matrix

## What this is

The Ansoff Matrix maps how a company or product can grow along two axes: products (existing or new) and markets (existing or new). The four cells are four routes to growth of rising risk. Market Penetration sells more of what you have to who you already serve (lowest risk), Market Development takes existing products to new markets, Product Development builds new products for existing customers, and Diversification puts new products into new markets (highest risk, since nothing is known territory). Igor Ansoff set it out in the Harvard Business Review in 1957.

The four strategies, their risk profiles, how to use the matrix, and the pitfalls live in [references/ansoff.md](references/ansoff.md).

## What it does

The skill runs the analysis in parallel. Four strategist subagents each work one quadrant, generating concrete, specific growth options (a named market, channel, segment, or product) with the risk, the capabilities required, and rough investment and reward. A synthesis pass then ranks every option against the growth objective and sequences a realistic growth path, on the principle that cheaper, lower-risk growth is usually exhausted before higher-risk moves are justified. The output is a saved markdown report with the matrix, per-quadrant options, prioritized options, and a recommended growth path. Two rules keep it honest: options must be concrete rather than restatements of a quadrant, and capability fit is treated as a source of risk equal to market novelty.

## When to use it

Reach for the Ansoff matrix when you want growth options and a path: how a company or product should grow, and which moves to make first. It assumes a growth objective, so prefer a different tool when the question sits elsewhere:

- If the question is which products to fund across an existing portfolio, use [bcg-matrix](../bcg-matrix/).
- If you want to balance near-term, emerging, and future growth over time, use [three-horizons](../three-horizons/).
- If the growth problem itself is still fuzzy, frame it first with [tosca-problem-definition](../tosca-problem-definition/).
- If you want to escape head-to-head competition entirely, use [blue-ocean-strategy](../blue-ocean-strategy/).

## How to get started

**You provide:** the company or product seeking growth. A growth objective and current markets or capabilities are optional but valuable. Something like "Work up an Ansoff matrix for our meal-kit subscription."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
