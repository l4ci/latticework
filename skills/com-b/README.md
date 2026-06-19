# com-b

## What this is

COM-B explains why a specific behaviour does or does not happen, and it sits at the hub of the Behaviour Change Wheel. It comes from Susan Michie, Maartje van Stralen, and Robert West (*Implementation Science*, 2011). Its claim is simple and unforgiving: a behaviour occurs only when three conditions hold at once. The actor needs the Capability to do it, the Opportunity for it to happen, and the Motivation to do it over the alternatives. Take away any one and the behaviour stops. Each component splits in two (Physical and Psychological Capability, Physical and Social Opportunity, Reflective and Automatic Motivation), and the wheel routes each gap to the intervention functions that can close it.

The framework, the six sub-components, the nine intervention functions, and the deficit-to-function mapping live in [references/com-b.md](references/com-b.md).

## What it does

The skill runs the diagnosis in parallel. Six analyst subagents each take one sub-component and judge whether it is sufficient for the behaviour or a barrier, with evidence, a severity, and a confidence. A synthesis pass then finds the binding constraint: the missing component without which nothing else matters. It maps that constraint to the right intervention functions of the wheel (Education, Persuasion, Incentivisation, Coercion, Training, Restriction, Environmental restructuring, Modelling, Enablement) and designs targeted interventions. The output is a saved markdown report with the component scan, the diagnosis, and the interventions. Two rules keep it honest: it checks all three components before blaming motivation (the classic, expensive error, since people who fail to act are usually willing but lack the capability or opportunity), and it insists the behaviour be defined as a concrete action by a concrete actor, because a vague goal cannot be diagnosed at all.

## When to use it

Reach for COM-B when you have an adoption, compliance, habit, or behaviour-change problem and want to know why a specific behaviour is not happening and what would change it. The unit of analysis is one behaviour by one actor, not a strategy or a culture in the abstract.

- If the question is how to run an organizational change programme, use [kotter-change](../kotter-change/) or [adkar](../adkar/).
- If the question is what outcome a customer is hiring a product for, use [jobs-to-be-done](../jobs-to-be-done/).
- If you need to map who holds power around the change, use [stakeholder-analysis](../stakeholder-analysis/).

## How to get started

**You provide:** the target behaviour (one concrete action: who does what, when, where) and the actor expected to perform it; context on what has been tried is optional. Something like "use COM-B to work out why engineers aren't logging near-misses."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
