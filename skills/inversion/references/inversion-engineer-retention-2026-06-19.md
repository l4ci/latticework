# Inversion: keeping our best engineers

> _Illustrative example output for the `inversion` skill. The company, team, and every detail below are fictional and invented to demonstrate the report's shape, not researched. Do not cite any of this as fact._

- **Goal (forward):** Keep our strongest engineers (the top ~15% the org depends on) for the next three years.
- **Inverted question:** How would we guarantee that every one of our best engineers quits within three years?
- **Date:** 2026-06-19
- **Context:** Series-B startup, ~40 engineers, post-hypergrowth slowdown. Two strong engineers left last quarter. Compensation is roughly market. The founders fear a slow drain more than a sudden exodus.

---

## 1. Failure paths

Each path is a concrete way to drive the best engineers out. **Plausibility** (1 to 5) is how easily a team actually falls into it; **Damage** (1 to 5) is how directly it costs us our strongest people. **Severity = plausibility x damage.** Bands: 20 to 25 critical, 12 to 19 high, 6 to 11 medium, 1 to 5 low.

| # | Failure path | Plaus | Dmg | Sev | Band | Lens(es) |
|---|---|---|---|---|---|---|
| 1 | Let the best engineers' work turn into thankless toil: assign them all the firefighting, on-call, and cleanup, none of the interesting builds | 5 | 5 | 25 | Critical | Self-inflicted, People |
| 2 | Reward output we can count, not the hard work that holds the system together, so the people doing the load-bearing work feel invisible | 4 | 5 | 20 | Critical | People, Process |
| 3 | Promote the loudest or most political over the strongest, so the best engineers watch worse work get the title and the raise | 4 | 5 | 20 | Critical | People |
| 4 | Bury them in meetings and process until they cannot ship; let real engineering time fall toward zero | 5 | 4 | 20 | Critical | Process, Self-inflicted |
| 5 | Freeze comp and equity refresh while the market moves, so staying becomes a measurable pay cut | 3 | 5 | 15 | High | External, People |
| 6 | Ship a slow, quiet erosion: small indignities (no growth path, ignored proposals, a manager who never advocates) that no single quarter flags | 5 | 3 | 15 | High | Second-order |
| 7 | Tie them to a rotting codebase with no time to fix it, so every day is more painful than the last | 4 | 4 | 16 | High | Process, Second-order |
| 8 | Hire weak engineers fast to fill headcount, dropping the bar so the best lose their peers and their reason to stay | 3 | 4 | 12 | High | Self-inflicted, Second-order |
| 9 | Let a toxic high-performer or a bad manager go unchecked, and let the best vote with their feet | 3 | 4 | 12 | High | People |
| 10 | Pivot strategy every two quarters so nothing they build survives, killing any sense of progress | 3 | 3 | 9 | Medium | Self-inflicted |
| 11 | Get out-recruited: a competitor ships a better mission and pay and we never give people a reason to say no | 3 | 3 | 9 | Medium | External |
| 12 | Mishandle a layoff or a public stumble so trust in leadership cracks and the most marketable leave first | 2 | 4 | 8 | Medium | External, People |

Cross-lens agreement clusters on the top four: making the work miserable and unrewarded (1, 2, 4) and rewarding the wrong people (2, 3). That convergence is itself a signal: the surest ways to lose great engineers are about daily experience and fairness, not headline pay.

---

## 2. Bright lines

The absolute "never" rules. Each is catastrophic even once, so they sit apart from the scored tradeoffs.

- **Never let a known toxic person or failing manager stay in the path of a strong engineer.** One unaddressed bad actor can clear out a team; tolerating it once teaches everyone what we actually reward (path 9).
- **Never promote on politics or volume over demonstrated strength.** A single visibly unfair promotion tells every strong engineer the game is rigged, and the best have the most options to act on it (path 3).
- **Never quietly let a top engineer's comp fall a full band below market and hope they don't notice.** They will notice, and the discovery converts a retention problem into a trust problem (path 5).

---

## 3. Avoid-list to action

Each top failure path turned into a concrete constraint or move.

| Path | Avoid-rule / action |
|---|---|
| 1. Thankless toil | **Ensure** the load of firefighting, on-call, and cleanup is shared and visible, and that every strong engineer has a real share of the work they find worth doing. Audit who is actually getting the interesting builds. |
| 2. Counting the wrong output | **Ensure** the work that holds the system together (mentoring, hard debugging, design, glue work) is named and rewarded in reviews and promotions, not just countable shipped features. |
| 3. Politics over strength | **Do not** promote on visibility or politics. Tie advancement to demonstrated technical strength and impact, with criteria a skeptical strong engineer would call fair. |
| 4. Meetings over shipping | **Ensure** senior engineers keep large, protected blocks of maker time. Treat a drop in real engineering hours as a leading indicator, not a side effect. |
| 5. Comp drift | **Do not** let a top engineer's comp silently fall below market. Refresh equity and benchmark proactively; surface it before they do. |
| 6. Slow erosion | **Ensure** each strong engineer has a named growth path, an advocate manager, and a channel where their proposals get a real answer. Run skip-levels to catch the indignities no quarter flags. |
| 7. Rotting codebase, no time | **Ensure** there is standing, funded time to pay down the debt the best engineers work in daily, so the job gets better over time, not worse. |
| 8. Bar-dropping hiring | **Do not** trade the hiring bar for speed. Protect the peer quality that is half the reason strong people stay. |
| 9. Unchecked toxicity | **Do not** tolerate a known toxic high-performer or a failing manager in a strong engineer's path. (Bright line.) |

---

## 4. Verdict

Inverting "keep our best engineers" makes the real threat clear, and it is not the one the founders feared most. The fear was a competitor poaching with better pay (paths 11, 5). The inversion puts those mid-pack: out-recruiting and comp drift hurt, but the surest ways to lose great engineers are the ones we do to ourselves, every day, for free. The four critical paths are all self-inflicted: hand them thankless toil, reward the wrong output, promote the wrong people, and bury them in process until they cannot ship.

What this changes about how we run the team: the highest-leverage retention work is not a comp adjustment, it is an audit of daily experience and fairness. Who is getting the interesting work versus the cleanup, whether the load-bearing work shows up in promotions, whether maker time is protected, and whether the last promotion would survive a skeptical strong engineer's read. The avoid-rules that matter most are paths 1 through 4: get those right and most of the drain closes. The bright lines (no unchecked toxicity, no rigged promotions, no silent comp decay) are the cliffs to never walk near while doing it.

---

## 5. Caveats

- Inversion shows what would drive the best engineers out, not the positive program that makes them thrive. Avoiding every failure here leaves a team that is not actively losing people; building one they are excited to stay at is a separate, forward exercise. Pair this with that.
- Avoiding all risk is its own failure. Some attrition is healthy, and refusing every change that might unsettle anyone would freeze the company. The point is to avoid the stupid, self-inflicted losses, not all loss.
- The plausibility and damage scores are judgment, not measurement. The honest move is to validate the top paths against what departing engineers actually said in exit conversations before acting on the ranking.
- All details here are illustrative for documentation purposes and were not researched.
