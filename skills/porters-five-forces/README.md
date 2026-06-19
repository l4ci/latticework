# porters-five-forces

## What this is

Porter's Five Forces reads the profit potential of an industry through five competitive forces: threat of new entrants, bargaining power of suppliers, bargaining power of buyers, threat of substitutes, and competitive rivalry. The stronger the forces, the thinner the profit an average competitor can hold; where all five are weak, the industry can sustain high returns. The framework comes from Michael Porter, first in his Harvard Business Review article "How Competitive Forces Shape Strategy" (1979) and then in *Competitive Strategy* (1980). The unit of analysis is an industry, a market for a defined product or service in a defined geography, not any single company.

The five forces, their determinants, and the 1-to-5 scoring rubric are in [references/forces.md](references/forces.md).

## What it does

The skill runs the analysis in parallel. Five analyst subagents each take one force, work through its standard determinants with real evidence, and score its intensity from 1 to 5. A synthesis pass then weighs the forces rather than averaging them, names the one or two that dominate, locates where in the value chain the profit pool sits, and draws strategic implications tied to the firm's position. The output is a saved markdown report with a per-force breakdown, a verdict on attractiveness, and clear caveats.

Two rules keep it honest. Every force score must trace to its determinants with evidence, and where data is thin the skill lowers its confidence instead of inventing numbers. The synthesis treats the binding constraint on profit as one or two forces, not the arithmetic of all five.

## When to use it

Reach for Five Forces to judge the competitive structure and attractiveness of an industry, to weigh entering or exiting one, or to ground a strategy in industry structure rather than growth or hype. It is the industry-structure specialist, so prefer a different lens when the question sits elsewhere:

- If you only need the external macro-environment around the industry, use [pestel-analysis](../pestel-analysis/).
- If you want a broad position read that also weighs internal strengths, use [swot-analysis](../swot-analysis/).
- If the answer is to change which factors competition runs on rather than win the current game, use [blue-ocean-strategy](../blue-ocean-strategy/).

## How to get started

**You provide:** the industry to analyze (a defined product or service in a defined geography), and optionally the firm's position and the decision it informs. Something like "Run a Five Forces on the UK meal-kit industry."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
