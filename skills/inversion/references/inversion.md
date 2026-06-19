# Inversion: framework and avoid-rule logic

Inversion attacks a problem backward. Most thinking runs forward: state a goal, then search for moves that reach it. Inversion turns the goal around and searches for what would guarantee the opposite, then avoids those paths. The two searches are not the same. Forward search rewards cleverness and tends to crowd around attractive moves; backward search exposes the obvious, avoidable ways to lose that the forward view skips right past.

## Where it comes from

The mathematician Carl Gustav Jacobi advised "man muss immer umkehren" ("one must always invert"), solving hard problems by restating them in reverse. Charlie Munger made it a decision-making habit: "All I want to know is where I am going to die, so I will never go there." His broader claim is that avoiding stupidity is more reliable than seeking brilliance. You do not have to be clever if you are consistently not stupid, and the not-stupid list is short and knowable. Inversion is how you build that list.

## The move

1. **State the goal forward**, the way it is naturally framed: "achieve X", "protect Y".
2. **Invert it.** Ask the opposite question: "what would guarantee we fail at X, or produce the worst possible outcome?" Write the inverted question out plainly.
3. **Enumerate the failure paths.** Generate concrete, specific ways to cause that bad outcome. Manufacture them on purpose. The aim here is coverage and candor, not judgment.
4. **Rank them** by how easily each path gets taken in real life and how badly it damages the goal.
5. **Convert each top path into an avoid-rule.** Turn "the way we lose" into "do not..." or "ensure...", stated concretely enough to act on. Pull out the few absolute bright lines, the things that are catastrophic even once.

The deliverable is the avoid-list and the constraints it implies, not the raw list of failures.

## Two uses

Inversion runs the same way for both, but the inverted question differs:

- **A goal to reach.** The goal is an outcome you want ("grow revenue", "ship on time", "keep the team"). The inversion is "what would make us fail at it", and the result is a set of failures to design around.
- **A quality to protect.** The goal is a property you want to hold ("users trust us", "the system is safe", "the code stays maintainable"). The inversion is "what would destroy it", and the result is a set of things never to do to it.

Most real goals carry both: a thing to reach and a quality to keep intact while reaching it. Run whichever framing fits, or both.

## The lenses

When generating failure paths, cover distinct sources so the search does not crowd onto one kind of failure. Five lenses span most of the ground:

1. **Self-inflicted (own actions).** The ways you wreck it yourself, through your own choices, neglect, or arrogance. The own goals, the avoidable mistakes entirely within your control.
2. **External (environment).** The conditions outside your control that produce the opposite outcome if you walk into them, ignore them, or fail to plan around them.
3. **People and incentives.** How the people involved and what they are rewarded for drive the result the wrong way. Misaligned incentives, who disengages, who games the metric, who leaves.
4. **Process and execution.** How the day-to-day mechanics, handoffs, and quality of the work produce failure even when the intent is sound.
5. **Second-order and slow-burn.** Failures that build quietly over time, moves that look fine now and rot later, things that "succeed" on the surface while undermining the goal underneath.

## Scoring

Tag each failure path so the list can be ranked rather than left flat:

- **Plausibility** (1 to 5): how easily this path gets taken in real life. A trap people fall into constantly scores high; an exotic one scores low.
- **Damage** (1 to 5): how badly this path wrecks the goal if taken. Irreversible or catastrophic scores high.
- **Severity = plausibility x damage** (1 to 25). Rank by severity. Band: 20 to 25 critical, 12 to 19 high, 6 to 11 medium, 1 to 5 low.

## Bright lines

Separate from the ranked list, name the few absolute "never" rules: the small set of things that, done even once, are catastrophic or irreversible. Bright lines are not tradeoffs to be weighed against benefits; they are the cliffs you do not walk near. Keeping them apart from the scored list stops them from being averaged away. This is the operational form of "I will never go there."

## From avoid-list to action

For each top failure path, write the rule, constraint, or move that neutralizes it:

- A **"do not..."** when the failure comes from an action to refrain from.
- An **"ensure..."** when it comes from an omission, something that must be in place so the path is closed.

State each one concretely enough to act on, tied to the path it neutralizes. An unconverted list of failures is half the method; the constraints are where inversion pays off.

## Limits

Inversion finds what to avoid, not the positive path to win. Knowing every way to lose does not tell you how to succeed, only how not to fail, so pair it with forward planning. Pushed to the extreme, avoiding all risk means achieving nothing: some failure paths are the unavoidable cost of a goal worth pursuing, and the point is to avoid the stupid ones, not to refuse every risk. The plausibility and damage scores are judgment, not measurement.
