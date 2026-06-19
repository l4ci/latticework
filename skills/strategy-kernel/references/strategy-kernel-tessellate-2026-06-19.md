# Strategy Kernel: Tessellate

> _Illustrative example output for the `strategy-kernel` skill. Tessellate is a fictional company; every figure, competitor detail, market claim, and quoted strategy statement below is invented to demonstrate the report's shape, not researched. Do not cite these numbers._

- **Organization:** Tessellate, a mid-size SaaS firm selling product-analytics software to growth-stage tech companies (~$31M ARR, ~900 paying accounts).
- **Challenge:** A venture-subsidized competitor, Nilshift, launched a genuinely free tier that covers most of what mid-market teams use Tessellate for. Net revenue retention has slid from 112% to 97% over three quarters. At stake: the renewal base the whole company runs on.
- **Date:** 2026-06-19
- **Existing strategy under critique:** "Our strategy is to be the leading customer-obsessed analytics platform, grow ARR 40% next year, and win on product velocity."
- **Context:** Nilshift's free tier is subsidized by a recent raise; Tessellate's real strength is deep workflows for embedded data teams; churn concentrates at the low end where the free tier bites hardest; the ~80 enterprise accounts are sticky but a small share of logos.

---

## 1. Diagnosis

**The crux, in a sentence:** Tessellate is being commoditized from below, and the obstacle that decides the outcome is that its pricing and packaging still treat the low-end self-serve segment (the exact segment the free tier now owns) as a business worth defending, which spreads the company thin across customers it can no longer profitably keep.

**What is really going on.** Nilshift did not out-build Tessellate; it changed the price of the bottom of the market to zero. For a team that uses analytics for basic dashboards and event counts, "good enough and free" beats "better and $400 a month," and no amount of product velocity closes a gap against zero. The slide in net revenue retention is not spread evenly: it is almost entirely down-tier accounts shrinking or leaving. Meanwhile the part of the base that is not exposed (embedded data teams running deep, workflow-bound analysis) is still expanding. Tessellate is running one motion, one price book, and one roadmap across two segments that the free tier has just split apart.

**What got simplified away.** The four diagnoses raised real but secondary issues: a thinner brand than Nilshift's, slower onboarding, a sales team built for self-serve volume, and an undifferentiated free-trial funnel. These matter, but they are downstream. Fix every one of them and a free tier still beats a paid one at the low end. The diagnosis deliberately sets them aside to name the one fact doing the work: **the company is defending a segment that economics has already conceded.**

**Why this is the obstacle that matters, over the alternatives.**

- The **competitive/market** diagnostician named the crux as "competing against free," and located the leverage in segment economics: the free tier is unanswerable at the low end but irrelevant where switching costs are high. (Confidence: high.)
- The **structural/economic** diagnostician independently reached the same place by a different route: gross margin per low-tier account is now negative once support and infra are loaded, so every retained low-end customer is a loss, and the retention metric is measuring the wrong thing. (Confidence: high.)
- The **internal-capability** diagnostician named the crux as workflow depth: Tessellate's durable advantage is the embedded-data-team use case Nilshift's free tier does not touch, and the company under-invests in it to chase volume. (Confidence: medium.)
- The **customer/demand** diagnostician split the base into "casual" and "embedded" users and showed the two have diverged: casual demand has collapsed to zero willingness-to-pay, embedded demand is growing and underserved. (Confidence: medium.)

Three of the four arrive at the same knot from different sides: a single market has split into two, and Tessellate is priced and built for the half it is losing. That convergence is why this is the crux and not the brand or the funnel. The competitive and structural readings are merged here, because "competing against free" and "negative margin on retained low-end accounts" are the same fact seen from outside and inside.

---

## 2. Guiding policy

**The directional approach:** Stop defending the commoditized low end and reconcentrate the entire company on the embedded-data-team segment, where switching costs are high, willingness-to-pay is intact, and the free tier is structurally irrelevant. Turn the free tier from a threat into a feeder by treating Nilshift's casual users as a funnel that graduates into Tessellate when their analytics outgrow it.

**The hard choice it makes:** Tessellate gives up the self-serve low end on purpose. It will shed accounts, lose logos, and watch raw customer count fall, in order to move margin, roadmap, and sales effort to the segment it can actually keep. This is the choice the existing "grow 40% and serve everyone" stance refuses to make.

**The source of power it leverages:** **Focus / concentration.** A mid-size firm cannot out-subsidize a venture-funded free tier, so it wins by aiming everything at the decisive point (the high-switching-cost segment) instead of spreading thin. Secondarily it uses a **pivot point**: Nilshift's own free tier becomes Tessellate's top-of-funnel, since the users who outgrow free are exactly Tessellate's ideal customers.

**What it rules out:**
- No free tier of Tessellate's own to match Nilshift. Matching free concedes the company's economics to fight on the competitor's chosen ground.
- No roadmap work aimed at casual / dashboard use cases. That capability is now a commodity given away free; building more of it is spending against zero.
- No retention or sales incentive that rewards keeping low-tier accounts. The metric that drove the company to defend the conceded segment is retired.

---

## 3. Coherent action

Six coordinated commitments, each tied to the guiding policy.

1. **Repackage around the embedded-data-team use case.** Rebuild the product tiers so the paid plans are defined by workflow depth (warehouse-native modeling, governed metrics, embedded SDKs), not by event volume. *Ties to policy: makes depth, not scale, the thing customers pay for.*
2. **Let the low end go, deliberately and gently.** Move casual accounts to a single low-touch legacy plan, stop discounting to retain them, and publish a clean migration path to Nilshift's free tier for teams that only need basics. *Ties to policy: executes the hard choice instead of bleeding margin defending it.*
3. **Build the graduation funnel from free.** Ship an import tool and a "you have outgrown free" motion that targets Nilshift's heavy free users with the workflows their free tier lacks. *Ties to policy: turns the competitor's pivot point into Tessellate's top of funnel.*
4. **Re-aim sales and success at expansion within embedded accounts.** Shift quota and comp from new-logo volume to net expansion inside the high-switching-cost base. *Ties to policy: points the go-to-market machine at the decisive segment.*
5. **Replace the headline metric.** Retire blended net revenue retention as the company's north star and split it: track embedded-segment NRR (defend and grow) separately from low-tier (managed decline). *Ties to policy: stops the measurement that rewarded defending the conceded segment.*
6. **Reinvest the freed low-end R&D capacity into workflow depth.** Move the roadmap effort off casual dashboards and onto the embedded features that widen the moat the free tier cannot cross. *Ties to policy: concentrates build effort at the crux.*

**Coherence check.** The commitments reinforce rather than fight. Letting the low end go (2) frees the margin, the engineers (6), and the sales capacity (4) that the other moves require, so the retreat funds the advance. Repackaging (1) defines the segment that the funnel (3), the sales re-aim (4), and the reinvestment (6) all target, so they pull the same direction. The metric split (5) is what makes (2) survivable politically: without separating the two NRR numbers, the managed decline of the low end would read as failure and the organization would snap back to defending it. One tension surfaced and was resolved: commitments (2) and (3) both touch casual users, and an early draft had sales chasing low-tier renewals (a holdover scramble item) while marketing pushed those same users toward free, which would have had two teams fighting over the segment the strategy is conceding. Removing the renewal chase (folded into retiring it under the policy's rule-out) resolved the conflict.

---

## 4. Bad-strategy audit

Both the proposed kernel and the existing statement were run against Rumelt's four hallmarks.

**The existing strategy ("be the leading customer-obsessed analytics platform, grow ARR 40%, win on product velocity") fails three of four:**

- **(a) Fluff:** "leading customer-obsessed analytics platform" is gluey abstraction. Every competitor would sign the same sentence. It names no choice. **Caught.**
- **(b) Failure to face the challenge:** the statement never mentions the free tier or the retention slide. It is silent on the one fact that threatens the business, so it cannot be evaluated against the actual situation. **Caught, the most serious failure.**
- **(c) Goals as strategy:** "grow ARR 40% next year" is a destination, not a route. It says where to arrive while the floor is falling out, with no account of how. **Caught.**
- **(d) Bad objectives:** "win on product velocity" is a blue-sky objective. Against a free tier, building faster at the commoditized low end is running harder against zero; velocity restated as a virtue is the challenge dressed as an answer. **Caught.**

**The proposed kernel, audited and corrected:**

- **(a) Fluff:** an early draft of the guiding policy read "pursue a premium, value-led market posture." That is fluff. Rewritten to the concrete claim: concede the low end, reconcentrate on the high-switching-cost embedded segment, name what is ruled out. **Fixed.**
- **(b) Failure to face the challenge:** the diagnosis names the free tier, the segment split, and the margin fact directly. The strategy can be argued with and checked. **Passes.**
- **(c) Goals as strategy:** no growth number stands in for method; the action describes how, and the verdict states the hard choice rather than a target. **Passes.**
- **(d) Bad objectives:** the first action list had eight items, including "refresh brand positioning," "improve onboarding speed," and "expand partner integrations." That was a scramble: every department's wish bolted on, with no concentration. Cut to the coherent six, all tied to the one guiding policy. A weak objective, "improve net revenue retention," was caught and rewritten: it merely restated the symptom as a goal (blue-sky), so it became commitment (5), split the metric and manage the two segments differently, which says *how*. **Fixed.**

---

## 5. Verdict

**This is a real strategy by the kernel's test; the existing statement was not.** The difference is the diagnosis. The old statement stepped around the free tier and named a 40% target; the kernel names the crux (a single market has split in two, and Tessellate is priced and built for the half it is losing) and points everything at the half it can keep.

The strategy rests on one hard choice: **deliberately give up the self-serve low end, including the customer count and the logos that come with it, to reconcentrate margin, roadmap, and sales on the embedded segment the free tier cannot reach.** Everything coherent in the action follows from making that choice, and the strategy is only as good as the willingness to actually make it. A leadership team that wants the reconcentration without the retreat will get neither.

---

## 6. Caveats

- A kernel is a **hypothesis, not a guarantee.** It states a bet on what matters and how to win, precisely enough to be wrong.
- The whole thing **rests on the diagnosis.** If the real crux is, say, a sales-motion failure rather than a segment split, the guiding policy aims at the wrong target and the coherent action coheres around a mistake. The diagnosis is the part most worth pressure-testing with real margin and cohort data before committing.
- **Coherence on paper still needs execution.** Six reinforcing commitments are a plan; whether sales comp actually shifts and engineers actually move is a separate, harder problem.
- **A strategy that avoids the hard choice is not one.** The temptation here is to keep the low end "just in case" while also chasing the embedded segment. That hedge dissolves the focus that is the entire source of power, and turns the kernel back into the wish list it replaced.
- All figures here are illustrative for documentation purposes and were not researched.
