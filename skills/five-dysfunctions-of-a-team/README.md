# five-dysfunctions-of-a-team

## What this is

In Patrick Lencioni's Five Dysfunctions of a Team (*The Five Dysfunctions of a Team*, 2002), the five dysfunctions stack into a pyramid rather than sitting side by side in a list: Absence of Trust at the base, then Fear of Conflict, Lack of Commitment, Avoidance of Accountability, and Inattention to Results at the top. The order matters because each layer rests on the one below. Conflict needs trust, commitment needs conflict, accountability needs commitment, and results need accountability. A team cannot fix a higher layer while the layer beneath it is broken, so a high symptom is usually a lower break showing through.

The pyramid, the hierarchy rule, each layer's tells and interventions, and the classic failure modes live in [references/five-dysfunctions.md](references/five-dysfunctions.md).

## What it does

The skill runs the assessment in parallel. Five analyst subagents each take one layer, compare the team against that layer's specific tells with concrete behavioral evidence, and score how present and severe the dysfunction is. A synthesis pass then reads the pyramid bottom to top, finds the lowest broken layer, traces how that crack surfaces as symptoms higher up, reconciles the surface complaint, and sequences interventions from the base upward. The output is a saved markdown report with the pyramid scored layer by layer, the binding constraint named, the cascade explained, and the rebuild ordered.

Three guardrails keep it honest. It scores every layer against observed behavior rather than a feeling, it respects the hierarchy instead of summing five independent scores, and it traces a high-layer complaint down to the real break rather than treating the symptom where it shows.

## When to use it

Reach for this when a real, named working team is conflict-avoidant, political, slow to decide, or not delivering, and you want to know why. The unit is one team with a shared goal, not an individual, a whole organization, or a one-off group. Pick a sharper sibling when the question is narrower:

- If the question is specifically whether the team is safe to speak up and admit mistakes, use [psychological-safety](../psychological-safety/).
- If you want to place the team on its forming-storming-norming-performing arc, use [tuckman](../tuckman/).
- If the issue is who holds power and interest in a change, not internal team behavior, use [stakeholder-analysis](../stakeholder-analysis/).

## How to get started

**You provide:** one defined working team to diagnose; observable behaviors and symptoms you have noticed are optional but sharpen the read. Something like "diagnose my product leadership team with the Five Dysfunctions model."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
