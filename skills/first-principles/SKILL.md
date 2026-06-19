---
name: first-principles
description: Use when the user wants to reason a problem up from fundamentals instead of by analogy to how it is already done, challenge the assumptions baked into a conventional approach, or rebuild a solution from the ground up. Frames the received approach and the goal it serves, fans out parallel subagents that tear down inherited assumptions and establish what is actually bedrock, then reconstructs a solution from the surviving fundamentals and contrasts it with convention in a detailed markdown report. Triggers include "first principles", "first-principles thinking", "reason from scratch", "challenge assumptions", "why do we do it this way", "from the ground up".
---

# first-principles

Reasons a problem up from fundamental, established truths rather than by analogy to how it is already done. A first principle, in Aristotle, is a foundational proposition that cannot be deduced from any other. The discipline is to strip a problem down to the few things that genuinely hold (physical limits, definitions, hard constraints, the real goal) and rebuild from there, ignoring inherited form. Catches the failure where "that is how it is done" is mistaken for "that is how it must be done."

The method, the bedrock test (fact versus assumption), and the reconstruction step live in [references/first-principles.md](references/first-principles.md). Load that file before reasoning and follow the separate-fact-from-assumption rule exactly.

## When to use

The user is stuck inside a conventional approach and wants to know whether the convention is load-bearing or merely inherited. The unit of analysis is one problem and the received way of solving it. It pairs with neighbors but is distinct from them:

- If the job is to break one problem into clean, non-overlapping branches, use [mece-decomposition](../mece-decomposition/).
- If the job is to list the assumptions a plan rests on and rank them by fragility, use [key-assumptions-check](../key-assumptions-check/).
- If the job is to find the worst outcome and reason backward to avoid it, use [inversion](../inversion/).
- If the job is to trace a failure that already happened to its origin, use [root-cause-analysis](../root-cause-analysis/).

First-principles reasoning is expensive. Reach for it when convention is costly, suspect, or untested, not for routine problems where reasoning by analogy works fine.

## Language

Conduct the session and write the report in the language the user is writing in. The reference file is English; keep the framework keyed to it regardless of output language.

## Inputs

- **PROBLEM** (required): what is being solved or reconsidered. If only a topic is given, pull out the actual problem before starting.
- **CONVENTIONAL APPROACH** (required): the received or current way it is done, the "we do it this way because that is how it is done" answer. Without a convention to challenge there is nothing to reason against; if it is missing, ask for it or state it explicitly.
- **GOAL** (optional): the real outcome the approach is meant to serve, separate from the form it currently takes. Naming the true goal is often where the convention first cracks, so surface it if the user has not.

## Orchestration map

```
Stage 1  Frame              ── inline, 1 pass ────────────────────────┐  (problem, the goal it serves, the conventional approach and its embedded assumptions)
Stage 2  Assumption Teardown ── 4 subagents IN PARALLEL ─────────────┤  (one per lens: inherited vs necessary, and what is bedrock)
Stage 3  Reconstruct        ── 1 agent, needs all 4 ─────────────────┘  (verified bedrock, discard the rest, rebuild, contrast with convention)
```

## Stage 1: Frame (inline)

Pin down what is being reasoned about so every teardown attacks the same target:

1. **The problem.** State it in one line, separate from any solution.
2. **The goal it serves.** The real outcome wanted, named independently of the current form. "Move people across the city," not "run more buses."
3. **The conventional approach.** The received or current answer, and the assumptions embedded in it: the things taken as fixed because that is how it is done. List them as plainly as you can, since the next stage tests them.

If the conventional approach is vague, sharpen it before continuing. The subagents need a concrete convention with stated assumptions to attack, not a vibe.

## Stage 2: Assumption Teardown (PARALLEL)

Dispatch four subagents at once, each attacking the problem from a distinct lens to surface and test the inherited assumptions and to establish what is actually fundamental. Suggested lenses: physical and material constraints, the economic or cost floor, the real goal and requirement, and regulatory or other hard constraints. Give each the framed problem, the conventional approach with its assumptions, the shared framing, and its lens.

Tell each subagent its final message is the return value: structured data, not prose for a human. Subagents should use available retrieval tools to ground bedrock claims (material costs, physical limits, statutes, established figures) in real evidence.

**Shared framing (send to each subagent):**

> Attack this problem through your assigned lens to separate inherited convention from fundamental truth. Problem: **[PROBLEM]**. Goal it serves: **[GOAL]**. Conventional approach and its embedded assumptions: **[CONVENTIONAL APPROACH + ASSUMPTIONS]**.
> Through your lens, work each relevant assumption and ask: is this necessarily true, or merely customary and inherited by analogy from how it has always been done? Strip away what does not survive until you reach what genuinely holds. For each finding, return:
> - **Assumption**: the assumption from the conventional approach you are testing (or a new one you surfaced)
> - **Inherited or necessary**: whether it is customary-by-analogy or a genuine constraint
> - **Test applied**: the reasoning or evidence you used to decide, with figures or sources where you have them
> - **Verdict**: survives as bedrock, or falls
> - **Bedrock established**: any fundamental truth your lens can establish (a physical limit, a definition, an established fact, a hard constraint, the real requirement), each flagged **fact** (verifiable or established) or **assumption** (still a judgment you could not fully verify)
> Be honest about the boundary of your lens: an established fact and an unverified premise are not the same thing. Do not pad; a convention that survives the test intact is a real finding.

Collect all four structured results before continuing. Re-dispatch any subagent that fails rather than reconstructing with a gap.

## Stage 3: Reconstruct (SEQUENTIAL, needs all 4)

One agent assembles the teardowns into a rebuilt answer:

1. **Assemble the bedrock.** Gather the fundamental truths that survived across the four lenses. Flag each **fact** or **assumption**, and resolve conflicts where two lenses disagree on what is fundamental. This is the foundation everything else stands on, so be strict: a "fundamental" that is really a buried assumption will poison the reconstruction.
2. **Discard what fell.** List the inherited assumptions that did not survive, so it is visible what convention was carrying for free.
3. **Reconstruct from the bedrock.** Build a solution using only the surviving fundamentals and the real goal, ignoring inherited form. Ask: given only these, what is actually possible? Name the option or options that the bedrock allows but convention hid.
4. **Contrast with convention.** Set the reconstructed answer beside the conventional one, side by side: what convention was costing, what assumption that cost rested on, and what new options open up once it is dropped.
5. **Verdict.** Whether the convention is load-bearing or inherited, and what the first-principles read implies for the problem at hand. If the convention survives, say so plainly: that is a valid and useful result.

## Report structure

Write a thorough markdown report and save it to `first-principles-<subject-slug>-<YYYY-MM-DD>.md` (today's date) in the working directory unless the user names another location.

1. **Header.** The problem, the goal it serves, and the date.
2. **Conventional approach.** The received or current answer and the assumptions it rests on, listed plainly.
3. **Assumption teardown.** Each assumption with whether it is inherited or necessary, the test applied, and the verdict (survives or falls). A table works well.
4. **Bedrock.** The fundamental truths that survive, each flagged fact or assumption. This is the foundation the rebuild stands on.
5. **Reconstruction.** The solution built up from the bedrock, and the option or options it opens that convention hid.
6. **Conventional vs first-principles.** The two answers side by side: what convention cost, and the assumption that cost rested on.
7. **Verdict.** Load-bearing or inherited, and what it means for the problem.
8. **Caveats.** First-principles reasoning is expensive and is overkill for routine problems where reasoning by analogy works fine; you can reason rigorously from a "fundamental" that is actually wrong, so the bedrock must be verified, not assumed; and the method surfaces options, it does not prove them feasible, costed, or legal. A flagged assumption is not yet a fact.

## Principles

- **Separate fact from assumption.** Every bedrock truth is flagged as a verifiable fact or a still-unproven assumption. The whole method collapses if a buried assumption is treated as fundamental.
- **Inherited until proven necessary.** Treat every piece of the convention as customary-by-analogy until a test shows it is a genuine constraint. The default is to challenge, not to accept.
- **Rebuild, do not tinker.** Reconstruct from the bedrock and the real goal, ignoring the current form, rather than adjusting the convention at the edges. The hidden option lives outside the inherited shape.
- **A surviving convention is a real result.** If the received approach holds up against the bedrock, that is a finding worth stating, not a failed analysis.
