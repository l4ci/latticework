# scqa-pyramid

## What this is

This skill uses two linked tools from Barbara Minto's *The Pyramid Principle* (1973, revised 2009), the communication method that became standard at McKinsey. SCQA frames the reader's context in four moves (Situation, Complication, Question, Answer) and delivers the governing thought up front. The pyramid is the hierarchy of supporting ideas beneath that answer, where each level summarizes the level below it and the whole structure reads vertically as a question-and-answer dialogue. The central idea is answer first: state the conclusion, then let the structure defend it, rather than making the reader assemble it from clues at the end.

SCQA in full, the pyramid rules, deductive versus inductive grouping, and the pitfalls are in [references/pyramid.md](references/pyramid.md).

## What it does

Because the Question fixed in the introduction decides what the whole pyramid must prove, the skill does not commit to the first framing. Two or three subagents propose competing SCQA framings in parallel, each emphasizing a different complication or reader, which surfaces a different question and answer. A selection pass picks or merges the sharpest, the one whose Question the audience actually has and whose Answer the evidence can support. One pass then builds the pyramid: the answer on top, a MECE key line of supporting arguments beneath it (deductive or inductive, stated), and the evidence under each. Two checkers audit it in parallel, one for whether each level summarizes rather than labels, the other for whether the key line is MECE and stays on the question the answer raises. The output is a saved markdown report with the SCQA introduction, the full pyramid, and a clean prose draft.

One rule bounds it: the skill structures and communicates the message, it does not generate the analysis or make a weak case strong. If the evidence cannot support the answer, the fix is more thinking, not a better outline.

## When to use it

Reach for this when you have something to say and need to say it in an order the reader can follow: an executive summary, a one-pager, a recommendation email, a deck storyline. It runs downstream of the analysis, the step where the result of the thinking becomes a message. If you only need a quick note, this is heavier than necessary.

- To define the problem before any of this, use [tosca-problem-definition](../tosca-problem-definition/).
- To build the issue tree behind the analysis, use [mece-decomposition](../mece-decomposition/); a pyramid's key line must itself be MECE.
- To structure a fuller research effort rather than a single message, use [storm-research](../storm-research/).

## How to get started

**You provide:** the recommendation or findings to communicate plus the material behind it, and ideally who the audience is. Something like "Structure this recommendation for my exec team, answer first."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
