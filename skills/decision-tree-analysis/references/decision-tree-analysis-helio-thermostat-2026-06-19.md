# Decision tree analysis: Helio One thermostat launch

> _Illustrative example output for the `decision-tree-analysis` skill. Helio is a fictional company; every probability, cost, and NPV figure below is invented to demonstrate the report's shape, not researched. Do not cite these numbers._

- **Decision:** Launch the Helio One smart thermostat now, run a paid market test first, or shelve the product.
- **Payoff measure:** Three-year net present value (NPV) in dollars. Product revenue net of cost of goods is positive; build, marketing, and test spend are negative. All payoffs are net of the costs along that path.
- **Horizon:** Three years from the decision.
- **Date:** 2026-06-19
- **Context:** A full launch costs ~$4M to tool and market. A paid market test costs ~$0.6M and delays a launch by a quarter. Roughly even odds the target segment is strong. Helio holds ~$9M, so a failed launch is a serious but survivable hit.

---

## 1. Tree structure

Read left to right in time order. Squares are Helio's decisions, circles are the market's uncertain outcomes, leaves are three-year NPV.

```
[D0] Root decision
│
├─ Launch now ──────────────( C1 ) Market
│                            ├─ Strong   p=0.45 ──► +$8.0M
│                            └─ Weak     p=0.55 ──► -$3.0M
│
├─ Test first (-$0.6M) ─────( C2 ) Test signal
│   │                        ├─ Positive p=0.50 ──► [D1] decide
│   │                        └─ Negative p=0.50 ──► [D2] decide
│   │
│   ├─ [D1] after Positive ─( C3 ) Market | Positive
│   │     ├─ Launch         ├─ Strong p=0.72 ──► +$8.0M (then -$0.6M test)
│   │     │                 └─ Weak   p=0.28 ──► -$3.0M (then -$0.6M test)
│   │     └─ Shelve ─────────────────────────────► -$0.6M (test cost only)
│   │
│   └─ [D2] after Negative ─( C4 ) Market | Negative
│         ├─ Launch         ├─ Strong p=0.18 ──► +$8.0M (then -$0.6M test)
│         │                 └─ Weak   p=0.82 ──► -$3.0M (then -$0.6M test)
│         └─ Shelve ─────────────────────────────► -$0.6M (test cost only)
│
└─ Shelve ──────────────────────────────────────► $0.0M
```

The $8.0M and -$3.0M launch payoffs are already net of the $4M launch spend. On the test branches the additional -$0.6M test cost is carried into every leaf.

The signal probabilities are consistent with the prior: P(Strong) = 0.50 x 0.72 + 0.50 x 0.18 = 0.36 + 0.09 = 0.45, matching the even-odds prior. The test is informative but imperfect: a Positive signal lifts the strong-market probability from 0.45 to 0.72, a Negative drops it to 0.18.

---

## 2. Branch detail

| Branch | Probability | Payoff (NPV) | Evidence / reference class | Confidence |
|---|---|---|---|---|
| Launch now → Strong | 0.45 | +$8.0M | Segment-size estimate x assumed share, net of $4M launch | Low |
| Launch now → Weak | 0.55 | -$3.0M | Sunk $4M launch minus thin weak-market revenue | Low |
| Test → Positive signal | 0.50 | (to D1) | Past Helio concept tests split ~half positive | Med |
| Test → Negative signal | 0.50 | (to D2) | Same | Med |
| After Positive → Strong | 0.72 | +$8.0M (-$0.6M test) | Posterior from test accuracy assumption | Low |
| After Positive → Weak | 0.28 | -$3.0M (-$0.6M test) | Posterior | Low |
| After Negative → Strong | 0.18 | +$8.0M (-$0.6M test) | Posterior | Low |
| After Negative → Weak | 0.82 | -$3.0M (-$0.6M test) | Posterior | Low |
| Shelve | 1.00 | $0.0M | No spend, no revenue | High |

The two prior probabilities (0.45 strong, 0.55 weak) carry the most weight and the least grounding; they are the inputs the sensitivity section stresses.

---

## 3. Fold-back

Working from the leaves to the root. EV at each circle, best branch at each square.

**C1 (Launch now, market):**
EV = 0.45 x 8.0 + 0.55 x (-3.0) = 3.60 - 1.65 = **+$1.95M**

**C3 (market after a Positive signal):**
EV(launch) = 0.72 x 8.0 + 0.28 x (-3.0) = 5.76 - 0.84 = +$4.92M, then -$0.6M test = **+$4.32M**
EV(shelve) = -$0.6M (test cost only)
**D1 = max(4.32, -0.6) = +$4.32M → launch.**

**C4 (market after a Negative signal):**
EV(launch) = 0.18 x 8.0 + 0.82 x (-3.0) = 1.44 - 2.46 = -$1.02M, then -$0.6M test = -$1.62M
EV(shelve) = -$0.6M (test cost only)
**D2 = max(-1.62, -0.6) = -$0.6M → shelve.**

**C2 (test signal), using the D1 and D2 values:**
EV = 0.50 x 4.32 + 0.50 x (-0.6) = 2.16 - 0.30 = **+$1.86M**

**D0 (root):**
- Launch now: **+$1.95M**
- Test first: +$1.86M
- Shelve: $0.0M

**D0 = max(1.95, 1.86, 0) = +$1.95M → Launch now.**

**Optimal path (highlighted):** **Launch now.** The test path is close behind ($1.86M) but its $0.6M cost eats more value than the information it buys returns. Shelving is dominated.

---

## 4. Sensitivity and value of information

**Break-even probability on a strong market.** Launch-now beats shelving while its EV stays positive:
8p - 3(1 - p) = 0 → 11p = 3 → **p = 0.273.**
Below a 0.273 chance of a strong market, shelving wins; above it, launching now wins. The estimate is 0.45, well clear of the 0.273 threshold, so the launch call is not fragile against the prior.

Launch-now also has to beat the test path. Test-first only overtakes launch-now when the prior is weak enough that buying the option to back out is worth its $0.6M, which happens just below the strong-market break-even. At p = 0.45 the gap (1.95 vs 1.86) is small, so a modestly cheaper or more accurate test would flip the recommendation to test-first.

**Payoff swings.** If the weak-market loss is worse than -$3.0M (say -$4.5M once channel and warranty costs are counted), launch-now EV falls to 0.45 x 8.0 - 0.55 x 4.5 = 3.60 - 2.48 = +$1.12M and the test path (which can abort after a Negative signal) becomes the better choice. The downside payoff is the input most able to flip the call.

**EVPI on the market outcome.** With perfect foresight you would launch only when the market is strong and shelve otherwise:
EV(clairvoyance) = 0.45 x 8.0 + 0.55 x 0 = **+$3.60M**
EVPI = 3.60 - 1.95 = **+$1.65M.**
Resolving the market uncertainty before deciding is worth up to $1.65M. The $0.6M test is cheaper than that ceiling, but the test is imperfect: it lifts EV from $1.95M (launch now) to $1.86M (test path), a *negative* gain of -$0.09M once its cost is paid. So while perfect information would be worth $1.65M, this particular test does not earn its price. A cheaper or sharper test could.

---

## 5. Risk note

The fold-back is on raw NPV, which assumes risk-neutrality. The weak-market outcome is a -$3.0M hit against a ~$9M balance sheet: serious, costing a third of cash, but survivable. That is small enough that plain EV is a reasonable objective here.

It is not negligible, though. A risk-averse Helio board might read the -$3.0M as worth more than three times a $1.0M swing (a concave utility), which narrows launch-now's edge over the safer test path and could tip a cautious decider toward testing despite the lower EV. If the weak-market loss were instead near Helio's full balance sheet, the EV ranking should be redone on utilities, not dollars.

---

## 6. Recommendation

**Launch the Helio One now.** Expected three-year NPV is +$1.95M, ahead of the test-first path (+$1.86M) and well ahead of shelving ($0). The launch call holds as long as the chance of a strong market stays above 0.273, and the current estimate (0.45) sits comfortably clear of that line.

Two thresholds should stay on the table before committing:
- **The downside payoff.** If the weak-market loss is worse than about -$3.7M, the test-first path overtakes launch-now. Nail down channel, support, and warranty costs before signing the launch budget.
- **The cost or sharpness of the test.** Perfect information here is worth up to $1.65M, but the $0.6M test buys too little to pay for itself. If a faster or cheaper read on the segment is available for materially under $0.5M, re-run the fold-back; it could flip the recommendation to test-first.

Do not shelve: it is dominated by both other options across the full range of plausible priors.

---

## 7. Caveats

- The +$1.95M is an **expected value**, an average over a launch Helio runs once. The actual outcome is either +$8.0M or -$3.0M, never $1.95M.
- The recommendation is only as sound as its inputs. The two **prior probabilities** (0.45 / 0.55) and the **downside payoff** (-$3.0M) are low-confidence and carry the result; they are the figures to firm up first.
- The fold-back assumes **risk-neutrality**. The risk note covers why that is acceptable here and when it would not be.
- The tree only covers the **three options and two market states** modeled. A staged regional rollout, a licensing deal, or a third "mixed" market outcome was not drawn, and an option left off the tree cannot win.
- All figures here are illustrative for documentation purposes and were not researched.
