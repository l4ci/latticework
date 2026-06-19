# six-sigma-dmaic

## What this is

DMAIC (Define, Measure, Analyze, Improve, Control) is the core problem-solving cycle of Six Sigma, a data-driven method for improving an existing process by reducing defects and variation. Six Sigma grew out of quality work at Motorola in the 1980s, where engineer Bill Smith is usually credited with formalizing it around 1986, and it spread widely after General Electric adopted it in the 1990s. The discipline of DMAIC is that you do not jump to solutions: you quantify the problem, prove the root causes with data, fix those causes, then lock in the result. It applies to improving a process that already exists; for designing a new process from scratch, the related DMADV is used instead.

The five phases, their gate questions, and the common pitfalls are in [references/dmaic.md](references/dmaic.md).

## What it does

The skill facilitates the five phases with gate checks, holding each phase until it answers its question (problem clear, baseline trusted, causes proven, pilot working, control real) before the next begins. In Analyze, several analyst subagents generate candidate root causes in parallel through different lenses (the fishbone categories, a 5 Whys chain), then the causes are pooled and verified against data with the user. The output is a saved markdown project document covering all five phases plus a record of the gates.

Two rules keep it honest: causes and effects are tested against data rather than asserted, and Improve targets the proven root causes, not symptoms. Guessing root causes instead of proving them is where DMAIC most often fails, so the Analyze gate does not pass on assertion.

## When to use it

Reach for DMAIC to fix an existing process where data can be gathered: reducing defects, errors, cycle time, or variation, when rigor matters and the problem is costly enough to justify the measurement.

- For a lighter, faster improvement loop without heavy measurement, use [pdca-cycle](../pdca-cycle/).
- To run the deep cause-finding that the Analyze phase needs on its own, use [root-cause-analysis](../root-cause-analysis/).
- To score and rank failure modes by risk rather than fix one process, use [fmea](../fmea/).

## How to get started

**You provide:** the process and what's wrong with it (and, if you have them, the available data, the customer's requirement, and the process owner). Something like "Run a DMAIC to cut the scrap rate on our molding line."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
