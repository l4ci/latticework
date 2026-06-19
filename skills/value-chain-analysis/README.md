# value-chain-analysis

## What this is

The value chain breaks a firm into the activities through which it creates value, so the sources of competitive advantage can be located. Michael Porter set it out in Competitive Advantage (1985). The chain has nine activity categories: five primary (inbound logistics, operations, outbound logistics, marketing and sales, service) and four support (firm infrastructure, human resource management, technology development, procurement). The premise is that advantage comes from specific activities and from how they link, not from the firm as a whole, and the gap between the value the output commands and the cost of the activities is the firm's margin.

The nine activities, what to assess for each, and the role of linkages live in [references/value-chain.md](references/value-chain.md).

## What it does

The skill runs the analysis in parallel. One analyst subagent takes each activity, describes how the firm actually performs it, and assesses its cost contribution, its value contribution, and whether it is an advantage, parity, or disadvantage versus competitors. A synthesis pass, read through the firm's chosen strategy (cost leadership or differentiation), locates where the advantage lives, finds the value leaks and weak links, and surfaces the linkages between activities that are hardest for rivals to copy. The output is a saved markdown report with a value-chain map, per-activity detail, and recommendations.

Two guardrails keep it honest: every activity is assessed for cost and value rather than merely described, and advantage is always judged against competitors, since doing something well is no edge when every rival does it as well.

## When to use it

Reach for this when you want an internal view of how a company creates value, where it carries excess cost, and where its competitive advantage lives across its activities. It is the internal counterpart to the external positioning tools.

- For the external view of industry profit structure and competitive pressure, use [porters-five-forces](../porters-five-forces/).
- Once the chain shows where advantage seems to live, test whether each candidate resource actually lasts with [vrio-analysis](../vrio-analysis/); the two pair naturally.
- For organizational alignment rather than value creation, use [mckinsey-7s](../mckinsey-7s/).
- For a broad qualitative read on position before settling on strategy, use [swot-analysis](../swot-analysis/).

## How to get started

**You provide:** the company or business unit and the strategy it pursues (cost leadership or differentiation), both required, plus optional competitors and known concerns. Something like "run a value chain analysis on our coffee roastery."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
