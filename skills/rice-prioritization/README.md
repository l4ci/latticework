# rice-prioritization

## What this is

RICE ranks a backlog of product initiatives by RICE = (Reach x Impact x Confidence) / Effort. Each item gets one comparable number: how many people or events it reaches in a fixed window, how much it moves a single goal, how confident the estimate is, and how much whole-team effort it costs. Higher score, do first. The score is a rate, so a cheap win can outrank a large feature that costs a year of work. The model comes from Intercom, where Sean McBride built it around 2016 to sequence the product roadmap without the loudest voice winning.

The formula, the four factors, their scales, the Confidence bias check, the sensitivity logic, and the pitfalls are in [references/rice.md](references/rice.md).

## What it does

The skill calibrates with the user first: the goal, the Reach time window and its data source, the Impact multiplier scale, the Confidence levels, and the Effort unit. It writes those down before touching any item, the same way a weighted matrix locks its weights before scoring. Then one scorer subagent per initiative estimates the four factors against those fixed definitions, each with a rationale and its stated evidence or assumption, lowering Confidence rather than inventing data. A synthesis pass computes the scores, ranks them, and runs a sensitivity check on Confidence and Effort. The output is a saved markdown report with the RICE table, per-item detail, a sensitivity note, and a recommended roadmap order. It guards against four recurring mistakes: treating Reach as a measured fact when it is a guess about the future, skipping Confidence (the very factor that penalizes wishful thinking), underestimating Effort (which sits in the denominator and silently inflates the score), and comparing items whose Reach uses different time windows. Confidence stays mandatory, items below 50% are sent to validation rather than scored, and high-rank items resting on an optimistic estimate are flagged "validate before committing."

## When to use it

Reach for this when you have many roadmap initiatives that differ in reach, impact, and effort, and want them sequenced by expected value. RICE sequences a backlog; it does not pick among a handful of designs. If there are only two or three items, rank them by hand.

- It is a product-roadmap specialization of [weighted-decision-matrix](../weighted-decision-matrix/); use the matrix to choose among a few options on bespoke weighted criteria, and RICE to sequence many items on four fixed factors.
- For a quick two-axis sort when reach and confidence do not matter enough to model, use [impact-feasibility-matrix](../impact-feasibility-matrix/).
- To understand which features matter and why before sequencing them, use [kano-model](../kano-model/); Kano explains demand, RICE sequences supply.

## How to get started

**You provide:** the backlog of initiatives to rank, plus the one goal Impact is measured against. A phrase like "Run RICE on our Q3 backlog."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
