# vrio-analysis

## What this is

VRIO tests whether a firm's resources and capabilities are a source of sustained competitive advantage. It comes from the resource-based view, set out by Jay Barney in "Firm Resources and Sustained Competitive Advantage" (Journal of Management, 1991), with the VRIO form appearing in his Gaining and Sustaining Competitive Advantage (1995). Each resource runs through four questions in order: is it Valuable, is it Rare, is it Costly to Imitate, and is the firm Organized to capture its value? The first "no" decides the verdict, which lands at competitive disadvantage, parity, temporary advantage, or sustained advantage. VRIN is the earlier four-attribute form (Valuable, Rare, Imitable with difficulty, Non-substitutable); VRIO folds substitutability into the imitation question and adds Organization.

The four questions, the sources of inimitability, and the decision table live in [references/vrio.md](references/vrio.md).

## What it does

The skill runs the analysis in parallel. One analyst subagent takes each resource and walks it through the four gates with evidence, naming the mechanism that protects it and assigning the competitive implication. A synthesis pass then ranks the resources, names the few that reach sustained advantage, and flags the ones that are valuable, rare, and costly to imitate but sit unused because nothing in the organization is set up to exploit them. If the user has not listed resources, an opening pass surfaces candidates first. The output is a saved markdown report with a verdict table, per-resource detail, the strategic core, and fixable gaps.

Three rules keep it honest. The procedure screens out industry table stakes before fanning out, since resources every rival holds fail the Rare gate by definition. Each subagent must name the mechanism behind any rare or inimitable claim rather than asserting it. And the analysis tracks whether each protection is eroding, so a snapshot is not read as a forecast.

## When to use it

Reach for this when you want to know whether a firm's strengths actually hold up as durable advantages, or whether they are table stakes that rivals match. The unit of analysis is a single resource or capability, not the industry and not the firm as a whole.

- It pairs downstream of [value-chain-analysis](../value-chain-analysis/): the value chain finds where advantage seems to live across activities, and VRIO then tests whether each candidate resource that emerges actually lasts.
- For the external view of industry structure and competitive pressure, use [porters-five-forces](../porters-five-forces/).
- For a broad internal-and-external read on position, use [swot-analysis](../swot-analysis/).

## How to get started

**You provide:** the firm or business unit (required), optionally the resources to test (it surfaces candidates if you don't), plus optional industry, competitors, and the strategic question. Something like "run a VRIO analysis on us."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
