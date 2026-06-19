---
name: strategy-kernel
description: Use when the user wants to build or test a real strategy for an organization, unit, or initiative, or to check whether an existing "strategy" is actually one. Captures the challenge, fans out competing diagnostician subagents to name the crux from different angles in parallel, then synthesizes the sharpest diagnosis into a kernel (diagnosis, guiding policy, coherent action) and audits the result against Rumelt's four hallmarks of bad strategy in a detailed markdown report. Triggers include "strategy kernel", "good strategy bad strategy", "Rumelt", "what's our strategy", "diagnosis guiding policy", "is this a real strategy".
---

# strategy-kernel

Builds and tests a strategy using Richard Rumelt's kernel from *Good Strategy / Bad Strategy*: a **diagnosis** that names the crux, a **guiding policy** that makes a hard choice, and **coherent action** that carries it out. Catches the most common failure, where a "strategy" is really a goal, a vision, or a wish list with no diagnosis and no hard choice. The work is in finding the crux and ruling things out, not in stating ambitions.

The kernel, the crux, the sources of power, and the four hallmarks of bad strategy live in [references/strategy-kernel.md](references/strategy-kernel.md). Load that file before working and apply the kernel and the bad-strategy audit exactly.

## When to use

The user wants a strategy for an organization, business unit, product, or initiative, or wants to know whether something already labeled a strategy holds up. The skill both builds a kernel from a challenge and critiques an existing statement against the four hallmarks. Prefer a sharper tool when the question is narrower:

- For a broad qualitative read of position before strategy, use [swot-analysis](../swot-analysis/).
- For industry profit structure and competitive pressure specifically, use [porters-five-forces](../porters-five-forces/).
- To break out of head-to-head competition by redefining the market, use [blue-ocean-strategy](../blue-ocean-strategy/).
- To deploy a chosen strategy through the organization, use [hoshin-kanri](../hoshin-kanri/).
- To turn a strategy into measurable near-term commitments, use [okr](../okr/).

The kernel decides *what the strategy is*; those tools feed it or carry it out.

## Language

Conduct the session and write the report in the language the user is writing in. The reference file is English; keep the framework keyed to it regardless of output language.

## Inputs

- **ORGANIZATION** (required): the company, unit, product, or initiative the strategy is for.
- **CHALLENGE** (required): the strategic challenge or situation, and what is at stake in getting it right. A kernel is built against a specific obstacle; without one there is nothing to diagnose, so ask for it before starting.
- **EXISTING STRATEGY** (optional): any current strategy statement, mission, or plan to be critiqued. If given, the bad-strategy audit checks it as well as the new kernel.
- **CONTEXT** (optional): competitors, market, constraints, resources, and time horizon. Sharpens the diagnosis and the hard choice.

## Orchestration map

```
Stage 1  Capture               ── inline, 1 pass ──────────────────────┐  (organization, challenge, stakes, existing strategy)
Stage 2  Competing Diagnoses   ── 4 diagnostician subagents IN PARALLEL ┤  (name the crux from distinct angles)
Stage 3  Kernel + Audit        ── 1 agent, needs all 4 ────────────────┘  (sharpest diagnosis, guiding policy, coherent action, bad-strategy audit)
```

Tell each subagent its final message is the return value: structured data, not prose for a human. Subagents should use available retrieval tools to ground claims about the market, competitors, and the organization in real evidence.

## Stage 1: Capture (inline)

Pin down what the strategy is for so every diagnostician works the same target:

1. **The organization.** What it is and what it does, in a line.
2. **The challenge.** The strategic obstacle or situation, stated concretely, and what is at stake in getting it right.
3. **The existing strategy, if any.** The current statement, mission, or plan to be critiqued, captured verbatim where possible.

If the challenge is vague or stated only as a goal ("we want to grow"), press for the obstacle in the way of it before continuing. A diagnosis needs a real challenge to name.

## Stage 2: Competing Diagnoses (PARALLEL)

The diagnosis decides everything downstream, so generate several rather than committing to the first reading. Dispatch four diagnostician subagents at once, each working from a distinct angle: **competitive / market**, **internal capability**, **structural / economic**, and **customer / demand**. Each independently names the crux as it looks from its angle.

**Shared framing (send to each diagnostician):**

> Diagnose the strategic challenge facing **[ORGANIZATION]** from the **[assigned angle]** angle. The challenge: **[CHALLENGE]**. Context: **[CONTEXT]**.
> Find the crux: the part of the challenge that is both most important and addressable, where focused effort would actually pay off. Cut through the noise to the single fact or dynamic that is doing the work. Return:
> - **What is really going on**: the situation from your angle, in two or three sentences, naming the dominant fact or dynamic
> - **The single obstacle that matters most**: the crux as you see it, in one sentence
> - **Why this is the crux**: why this obstacle, not the others, is the one that decides the outcome
> - **The leverage point**: where applied effort would release the most effect, and which source of power it draws on (focus, anticipation, pivot point, chain of effect, coherent design)
> - **Confidence** (high, medium, low), lowered when the evidence is thin
> Ground your reading in evidence where retrieval allows. Do not propose solutions; name the crux.

Collect all four structured diagnoses before continuing. Re-dispatch any diagnostician that fails rather than synthesizing with a gap.

## Stage 3: Kernel Build and Bad-Strategy Audit (SEQUENTIAL, needs all 4)

One agent turns the competing diagnoses into a kernel and tests it:

1. **Pick or synthesize the sharpest diagnosis.** Compare the four crux candidates. Choose the one that best survives the evidence and most concentrates the challenge, or merge two that name the same underlying knot. State the **crux in a sentence or two**, what is really going on, and what the diagnosis deliberately simplifies away. Say why this is the obstacle that matters over the others.
2. **Craft the guiding policy.** A directional approach aimed straight at the crux. It must make a **hard choice**, lean on a named **source of power**, and state **what it rules out**. If the policy is compatible with every action, it is not a guiding policy; sharpen it until it forecloses options.
3. **Design coherent action.** Three to six coordinated commitments that carry out the guiding policy. Each is tied explicitly to the policy. Then run a **coherence check**: do the commitments reinforce one another, or does any pair pull in opposite directions? Resolve conflicts; coordination is where the power is.
4. **Audit against the four hallmarks.** Test the result (and the existing strategy, if one was given) against each hallmark from the reference file, and fix whatever fails:
   - **Fluff:** any gluey abstraction or jargon standing in for a real claim? Replace it with the concrete statement.
   - **Failure to face the challenge:** is the challenge actually named and diagnosed, not stepped around?
   - **Goals as strategy:** has any statement of desire ("grow 20%", "be the leader") been smuggled in where a method belongs?
   - **Bad objectives:** is the action a scramble (a long list with no concentration) or are any objectives blue-sky (the challenge restated as a goal)? Cut the scramble down to the coherent few; rewrite any blue-sky objective as a real commitment.
5. **Verdict.** Whether the result is a real strategy by the kernel's test, and the single hard choice it rests on.

## Report structure

Write a thorough markdown report and save it to `strategy-kernel-<subject-slug>-<YYYY-MM-DD>.md` (today's date) in the working directory unless the user names another location.

1. **Header.** The organization, the challenge the strategy addresses, the date, and any context (competitors, horizon, the existing strategy under critique).
2. **Diagnosis.** The crux in a sentence or two; what is really going on; what got simplified away; and why this obstacle is the one that matters, over the alternatives the competing diagnoses raised.
3. **Guiding policy.** The directional approach; the hard choice it makes; the source of power it leverages; and what it explicitly rules out.
4. **Coherent action.** The three to six coordinated commitments, each tied to the guiding policy, with a coherence check showing they reinforce rather than conflict.
5. **Bad-strategy audit.** The result (and the existing strategy, if given) checked against all four hallmarks: fluff, failure to face the challenge, goals-as-strategy, scramble/blue-sky objectives. Name what was caught and the fix applied.
6. **Verdict.** Whether this is a real strategy by the kernel's test, and the one hard choice it rests on.
7. **Caveats.** A kernel is a hypothesis, not a guarantee; the diagnosis can be wrong, and the rest falls with it; coherence on paper still needs execution to be real; and a strategy that avoids hard choices is not a strategy, however polished it reads.

## Principles

- **Diagnosis first.** Name the crux before reaching for any answer. A strategy with no diagnosis cannot be evaluated, argued with, or improved.
- **A guiding policy rules things out.** If it is compatible with everything, it steers nothing. The hard choice is the strategy.
- **Coherence over completeness.** A handful of mutually reinforcing actions beats a long list that cancels itself out. The power is in the coordination.
- **A goal is not a strategy.** "Grow 20%" names a destination, not a route. Run the four hallmarks and cut what fails before calling it done.
