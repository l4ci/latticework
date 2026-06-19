# pestel-analysis

## What this is

PESTEL scans the macro-environment around a subject: the Political, Economic, Social, Technological, Environmental, and Legal forces that shape a market but lie outside any one firm's control. It is the macro layer of strategy analysis, sitting above industry forces and a firm's own position. The model grew out of the PEST framework of the 1960s, often credited to Harvard professor Francis Aguilar, who included a scanning checklist (ETPS) in his 1967 book *Scanning the Business Environment*. The Environmental and Legal factors were split out later to give them their own weight, and the same scan also goes by PESTLE and other reorderings.

The six factors, their probes, the prioritization logic, and the pitfalls are in [references/pestel.md](references/pestel.md).

## What it does

The skill runs the scan in parallel. Six analyst subagents each take one factor and identify the forces that bear on the subject, with each force's direction, timeframe, whether it is an opportunity or a threat, and how certain it is. A synthesis pass then prioritizes the forces by impact crossed with certainty, which separates what to act on from what to merely monitor. It maps the chains where forces across factors add up to a larger movement, and it draws the implications. The output is a saved markdown report led by the priority forces, with per-factor detail and an opportunities-and-threats list ready to feed a SWOT.

The skill guards against the framework's most common failure, the unranked laundry list, by forcing prioritization and a "so what" on every force, and by holding the analysis at the macro altitude rather than drifting into competitors or the company itself.

## When to use it

Reach for PESTEL when you need the external macro context for a company, industry, market entry, or strategic decision, before competitors or internal capabilities come into it. It is the widest lens of the positioning tools, so hand off when the question narrows:

- If the question is about industry profit structure and competitive pressure, use [porters-five-forces](../porters-five-forces/).
- If you want an objective-anchored read that weighs internal strengths against external forces, use [swot-analysis](../swot-analysis/).
- If a high-impact force is genuinely too uncertain to call, feed it into [scenario-planning](../scenario-planning/).

## How to get started

**You provide:** the subject (a company, industry, market, or decision) and the geography in scope, plus an optional horizon and the decision it informs. Something like "Run a PESTEL for an EV-charging installer entering Germany."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
