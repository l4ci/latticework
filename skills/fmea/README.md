# fmea

## What this is

Failure Mode and Effects Analysis anticipates how a process, product, or design can fail before it does, scores each failure mode, and acts on the worst. The method is procedural: break the subject into functions, steps, or components; for each, list every way it can fail, what that failure does and to whom, what causes it, and what currently catches it; then score three things on anchored 1-to-10 scales, how bad the effect is (Severity), how often the cause occurs (Occurrence), and how likely you are to detect it before impact (Detection). FMEA grew out of US military reliability work in the 1940s and 1950s and was carried into the Apollo program by NASA in the 1960s; it is now standard in manufacturing, automotive, and safety-critical software, codified in the 2019 AIAG-VDA standard.

The seven columns, the three anchored scales, the RPN and criticality math, the action-priority rules, and the pitfalls are in [references/fmea.md](references/fmea.md).

## What it does

The skill runs the analysis in parallel. One analyst subagent takes each unit, lists its failure modes with effects, causes, current controls, and S/O/D scores, grounding them in real failure history and specifications where it can rather than inventing data. A synthesis pass computes the Risk Priority Number (S x O x D) and criticality (S x O) for every mode, ranks them, applies an action threshold, and recommends a specific action for each high-priority mode, with a target RPN showing the expected payoff. The output is a saved markdown report: the full FMEA table, the ranking, and a prioritized action plan. It dodges the framework's known traps. RPN tunnel vision (a catastrophic but rare and detectable failure posting a low RPN and getting ignored) is caught by an override where any S >= 9 mode gets action regardless of its number. Over-reliance on detection is countered by favoring actions that cut severity or occurrence and reporting criticality alongside RPN. And because RPN is an ordinal index, not a measured probability, equal RPNs from different score combinations are not treated as equal risks.

## When to use it

Reach for this before launching or changing a process, product, or design where failures carry real cost, safety risk, or regulatory exposure, and where the system decomposes into many failure points worth scoring one at a time.

- It is the scored, enumerative counterpart to [pre-mortem](../pre-mortem/); use pre-mortem when the subject is a one-off plan with a single dominant way to fail, and FMEA when it is a system with many independent failure modes.
- If you are running a defect-reduction project, FMEA often supplies the Analyze and Improve phases of [six-sigma-dmaic](../six-sigma-dmaic/).
- If a failure has already occurred and you need its cause, use [root-cause-analysis](../root-cause-analysis/).

## How to get started

**You provide:** the process, product, or design under analysis and its boundary (what is in scope, what is assumed reliable outside). Type, failure history, and existing controls are optional. Something like "run an FMEA on our vaccine cold-chain delivery process."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
