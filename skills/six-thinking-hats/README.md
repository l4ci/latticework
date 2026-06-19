# six-thinking-hats

## What this is

Six Thinking Hats is a method from Edward de Bono, set out in his 1985 book of that name. It turns a single topic over in six distinct modes of thought, one at a time, each assigned a colored hat: White for facts and figures, Red for feelings and hunches, Black for caution and risk, Yellow for benefits and value, Green for creativity and alternatives, and Blue for managing the process itself. Each hat is a direction of thinking, not a kind of person, and the whole group wears one hat at a time. The point is parallel thinking: instead of one person defending while another attacks, everyone looks the same way at once, so the topic gets examined from every angle rather than turning into a fight. That also separates ego from the view, since the hat owns the position, not the thinker.

The six hats, their discipline, the failure modes, and the suggested sequence are in [references/six-hats.md](references/six-hats.md).

## What it does

The skill runs the hats in parallel. The Blue hat opens by fixing one focus question, the sequence, and what a good outcome looks like. Five subagents then take White, Red, Black, Yellow, and Green at once, each confined to its mode and grounding its findings in evidence where the mode allows. A closing Blue-hat pass integrates them: it weighs the hats against each other, surfaces the gut read the Red hat flagged, sorts the Black-hat risks into those that must be mitigated and those a Green-hat idea already neutralizes, and reaches a conclusion with concrete actions. The output is a saved markdown report with the verdict, each hat laid out by direction, and the synthesis.

The method has three predictable failure modes, and the skill guards each. The Black hat is the easiest mode and quietly dominates, so every risk is met with a fair search for value and a way past it. Hats get mixed, so each is held strictly in its lane. Sessions get used to rubber-stamp a decision already made, so the Blue hat states up front that the conclusion is open. The Red hat earns its odd permission to skip justification because feelings leak into the rational hats unless they get a slot of their own.

## When to use it

Reach for Six Hats to evaluate an idea, plan, or decision from all sides, run a structured deliberation, or break a deadlock where people are talking past each other. The unit is one focus question examined in full, so prefer a sharper tool when the shape is different:

- If you only want to examine how something fails (the Black hat alone), use [pre-mortem](../pre-mortem/).
- If you are choosing among several options on known criteria, use [weighted-decision-matrix](../weighted-decision-matrix/).
- If the worry is that the reasoning itself is systematically distorted, use [cognitive-bias-audit](../cognitive-bias-audit/).

## How to get started

**You provide:** the idea, plan, or decision to examine, plus any context on the stakes and who's affected. Something like "Use six thinking hats on whether we should drop our free tier."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
