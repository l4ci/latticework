# First principles: the 24/7 staffed support desk

> _Illustrative example output for the `first-principles` skill. The company, its product, its ticket data, and every cost and volume figure below are fictional, invented to demonstrate the report's shape, not researched. Do not cite these numbers._

- **Problem:** How should our SaaS product handle customer problems that arrive outside business hours?
- **Goal it serves:** Resolve customer problems fast enough that customers stay, without round-the-clock staffing cost sinking the unit economics.
- **Date:** 2026-06-19

---

## 1. Conventional approach

The received answer is a support desk staffed by humans around the clock: three shifts, agents always logged in, because "real support means a person is always reachable." We do it this way because that is what support has always looked like and what customers are assumed to expect.

The assumptions baked into it, listed plainly:

1. A human must answer every request.
2. Coverage must be continuous (a live agent available every minute of the night).
3. The desk must be staffed by us, in-house.
4. Nighttime request volume is high enough to justify live staff sitting ready.
5. "Support" is defined by reachability (a person picks up), not by resolution (the problem gets solved).

---

## 2. Assumption teardown

Four lenses worked the assumptions: the cost floor, the real requirement, physical/operational constraints, and regulatory/contractual constraints. Each verdict marks whether the assumption is **inherited** (customary by analogy) or **necessary** (a genuine constraint).

| # | Assumption | Inherited or necessary | Test applied | Verdict |
|---|---|---|---|---|
| 1 | A human must answer every request | Inherited | Pulled the night ticket log: ~70% of after-hours tickets fall into the same dozen known issues with documented fixes (password reset, billing date, known outage, integration token). A human reading a script adds nothing a retrieval system cannot. | **Falls** for the routine majority; survives only for the novel ~30% |
| 2 | Coverage must be continuous | Inherited | Tested against the goal. The goal is resolution fast enough to retain, not a person present every minute. What retention needs is a bounded time-to-resolution, not a body on a chair at 04:00. Continuity is a proxy that was mistaken for the target. | **Falls** as stated; reframes to "bounded resolution time" |
| 3 | The desk must be staffed by us | Inherited | No constraint requires the night shift be employees. A follow-the-sun partner or contractor in a waking timezone can cover the live hours we are asleep. The "in-house" requirement is custom, not necessity. | **Falls** |
| 4 | Nighttime volume justifies live staff sitting ready | Inherited | Measured it. After-hours volume runs ~8% of daytime, in spikes around deploys and outages, with long dead stretches. Paying three shifts to sit idle through the dead stretches is the core waste. | **Falls** |
| 5 | "Support" means reachability, not resolution | Inherited | Definitional. Checked what customers actually churn over: surveyed cancellations cite "my problem went unsolved," not "nobody picked up at night." Reachability was standing in for resolution. | **Falls**; the real definition is resolution |
| -- | A genuine human must handle novel, high-severity, or account-security cases | Surfaced, necessary | The novel ~30%, security actions, and contractual incidents cannot be safely closed by automation alone. Some live human capability is irreducible. | **Survives as bedrock** |
| -- | Enterprise contracts carry a response-time SLA | Surfaced, necessary | Regulatory/contractual lens: signed enterprise deals commit to a one-hour response on severity-1 incidents at any hour. That is a hard constraint, not a custom. | **Survives as bedrock** |

---

## 3. Bedrock

The fundamental truths that survived, each flagged **fact** (verifiable or established) or **assumption** (a judgment we could not fully verify):

- **The real goal is resolution within a bounded time, not a person reachable every minute.** _(fact: churn-survey data and the goal as stated)_
- **About 70% of after-hours tickets are known, documented issues with deterministic fixes.** _(fact: night ticket log, this sample)_
- **After-hours live volume is roughly 8% of daytime and bursty, clustered around deploys and outages.** _(fact: measured volume)_
- **A real human is irreducibly required for novel, high-severity, and account-security cases.** _(fact: nature of those cases)_
- **Enterprise contracts impose a one-hour severity-1 response SLA at any hour.** _(fact: signed contracts)_
- **The known-issue mix will stay roughly stable as the product evolves.** _(assumption: extrapolated from current data, not guaranteed; a major product change could shift it)_
- **A follow-the-sun partner can hit our quality bar on the live tier.** _(assumption: plausible, not yet tested with a real vendor)_

---

## 4. Reconstruction

Building only from the bedrock and the real goal, ignoring the inherited shape of "a desk staffed around the clock," the night problem decomposes into three tiers, not one wall of staff:

1. **Deflection tier (the ~70% known issues).** A retrieval-backed self-serve assistant resolves the documented issues instantly, at any hour, with no one on a chair. This is where continuous coverage actually comes from, and it costs almost nothing per ticket once built.
2. **On-call tier (the bursts and the severity-1 SLA).** Instead of three idle shifts, a small on-call rotation is paged only when automation cannot close a ticket or an SLA clock starts. Humans are paid for resolution, not for presence. This satisfies the one-hour enterprise SLA without anyone sitting idle through the dead stretches.
3. **Follow-the-sun tier (the live novel cases).** A partner in a waking timezone covers the live human hours we are asleep, handling the novel ~30% during their normal business day, so the work is never a graveyard shift for anyone.

**The option convention hid:** "continuous coverage" and "always-staffed" were fused in the convention, so the only imaginable answer was bodies on chairs all night. Splitting resolution from presence reveals that continuous *coverage* can be automated while continuous *staffing* is discarded. The desk was never the point; bounded resolution was.

---

## 5. Conventional vs first-principles

| | Conventional | First-principles |
|---|---|---|
| Night model | Three in-house human shifts, always logged in | Automated deflection + thin on-call + follow-the-sun partner |
| What is paid for | Human presence, much of it idle | Human resolution, only when automation cannot close it |
| Cost driver | Idle staff through the dead hours | Build cost of deflection, paid once; on-call paid per page |
| Severity-1 SLA | Met by a body being present | Met by paging on-call when the clock starts |
| Rough cost shape | Three full shifts of salary | A fraction of one shift, plus a built asset |

**What convention cost:** paying for human presence through long dead stretches at night. **The assumption that cost rested on:** that "support" means a reachable person (#1, #2, #5), rather than a resolved problem within a bounded time. Drop that one assumption and the staffed-all-night desk stops being necessary.

---

## 6. Verdict

The round-the-clock **staffed** desk is **inherited, not load-bearing.** What is load-bearing is narrower and survived the teardown intact: a bounded resolution time, an irreducible human for novel and high-severity cases, and a one-hour enterprise SLA. None of those requires three idle night shifts of our own employees. The first-principles read points to a tiered model (automate the known majority, page a thin on-call for the rest, hand live novel cases to a follow-the-sun partner) that meets every surviving constraint at a fraction of the cost. The convention answered the wrong question: it optimized presence when the goal was resolution.

---

## 7. Caveats

- First-principles reasoning is expensive and was worth it here only because the convention (three full night shifts) was costly and suspect. For a routine staffing question, reasoning by analogy would have been fine.
- Two bedrock items are flagged **assumption**, not fact: that the known-issue mix stays stable, and that a follow-the-sun partner can hit our quality bar. The reconstruction depends on both. Verify them (a partner pilot, a re-measure of the ticket mix after the next release) before committing.
- The method surfaced an option; it did not prove it. The deflection build cost, the partner's real quality, and customer tolerance for an automated first touch are untested here. This is a candidate to validate, not a decision to ship.
- All figures and ticket data above are illustrative for documentation purposes and were not researched.
