# pdca-cycle

## What this is

PDCA (Plan, Do, Check, Act) is a lightweight, repeating loop for continuous improvement: plan a change and predict its effect, do it on a small scale, check the results against the prediction, and act by adopting, adjusting, or abandoning, then run the next cycle from the new baseline. It is also called the Deming cycle or Shewhart cycle. Walter Shewhart sketched the underlying plan-do-see idea at Bell Labs in the 1930s, and W. Edwards Deming carried it to Japanese industry in the 1950s, where it took its modern four-stage form. Its strength is speed and repetition: small cycles that compound rather than one big project.

The four stages, how to use them, and the common pitfalls are in [references/pdca.md](references/pdca.md).

## What it does

The skill facilitates one cycle end to end and sets up the next, keeping a cycle log. Plan states the objective and a specific small change with an explicit prediction and a measure. Do runs the change on a small scale and records what actually happened. Check compares results to the prediction honestly and captures surprises. Act ends in an explicit adopt, adjust, or abandon decision and updates the baseline, then the loop continues. The output is a saved markdown cycle log with a running record of the current standardized practice.

Two rules make PDCA work, and the skill insists on both: a prediction written during Plan, without which Check has nothing to judge against, and keeping Do small, so a wrong idea stays cheap and the loop stays fast.

## When to use it

Reach for PDCA for quick, frequent, lower-stakes improvement: trying a change, testing a fix, iterating a routine, where heavy measurement is not warranted and speed beats depth.

- For a large, costly problem that needs statistical rigor and verified root causes, use [six-sigma-dmaic](../six-sigma-dmaic/).
- When a Check or Act turns up a stubborn defect whose cause is unclear, use [root-cause-analysis](../root-cause-analysis/).
- To set the objectives and measures a cycle improves toward, use [okr](../okr/).

## How to get started

**You provide:** the problem, opportunity, or change to work on, and optionally the situation and how results can be observed. Something like "Run a PDCA cycle on cutting our ticket response time."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
