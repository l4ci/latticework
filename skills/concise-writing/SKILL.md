---
name: concise-writing
description: Use when the user wants to write or edit text so it is only as long as it needs to be and carries no signs of AI writing. Anchors to the purpose and reader, then runs the text down a cut ladder (delete whole units before trimming words), scans it against the compressed catalog of AI tells, and reads it aloud, looping draft to audit to final. Guards against over-trimming: the floor is meaning, not word count. Triggers include "tighten this", "make it shorter", "cut the fluff", "less verbose", "trim this", "de-slop", "this sounds AI-written", "write a concise", "edit for length".
---

# concise-writing

Writes new text, or edits existing text, so it is only as long as it needs to be and reads as human-written. Catches two failures at once: prose that is longer than its job requires, and prose that carries the tells of machine generation. The first is fixed by cutting whole units before trimming words; the second by rewriting the tells, not just striking them. The guardrail against both is the reader: a cut that costs meaning is a bad cut.

The cut ladder, the question set, the compressed catalog of AI tells, the brevity moves, and the over-trimming guardrail all live in [references/concise-writing.md](references/concise-writing.md). Load that file before working and follow it. The "what not to cut" section matters as much as the rest: this skill is not a shrink ray.

## When to use

The user wants text written tight from the start, or an existing draft made shorter and less machine-sounding: emails, posts, docs, announcements, READMEs, marketing copy, essays. Reach for it on "tighten this", "make it shorter", "cut the fluff", "this reads like AI", or "write a concise X".

If the problem is not length or voice but the *order* of an argument (the answer should come first, the logic should be a pyramid), prefer [scqa-pyramid](../scqa-pyramid/) to structure it, then use this skill to tighten the result.

## Language

Work in the language the user is writing in. The reference file is English; keep the framework and the tell-words keyed to it, but apply the spirit to the target language (every language has its own filler, its own throat-clearing, its own machine cadence).

## Inputs

- **MODE** (inferred): *edit* if the user hands you text to tighten, *write* if they hand you a brief to draft from. Do not ask; read what they gave you.
- **TEXT** (edit mode): the draft to tighten.
- **BRIEF** (write mode): what the text needs to say.
- **PURPOSE and READER** (required): what the text is for and who reads it. This is the anchor, the equivalent of an objective. You cannot judge "long enough" without it, so if it is not clear from the request, ask one short question before starting. Everything else is optional.
- **LENGTH** (optional): a hard target (a tweet, 200 words, one screen). Treat it as a ceiling, not a quota to fill.
- **REGISTER** (optional): formal, casual, technical, the voice to hold.
- **SAMPLE** (optional): a piece of the user's own writing to match for voice. If given, mirror its sentence rhythm and word level instead of defaulting to a neutral voice.

## Procedure

A single editor runs the loop; no fan-out is needed. The one optional exception is the audit (step 5), where a fresh reader catches what the author's eye skips.

1. **Anchor.** State, in one line, the purpose, the reader, and the single thing the reader must take away. Keep it in view; every later cut is judged against it.
2. **Draft or read.**
   - *Write mode:* draft the shortest version that does the job. Do not pad to a length.
   - *Edit mode:* read the whole text once for meaning before cutting a single word. (Lazy about words, never lazy about reading.)
3. **Cut pass.** Run the cut ladder over the text, top down: kill whole sections and sentences that the takeaway does not need, then the restatements, then what the context already carries, then the long words and the scaffolding. Whole-unit cuts first; word-trimming last.
4. **De-AI pass.** Scan against the compressed tell catalog. For each cluster you find, rewrite the sentence around the concrete claim underneath it. Do not just delete the trigger word and leave a stump.
5. **Read-aloud and audit.** Read it aloud in your head: fix anything that stumbles or runs out of breath. Then ask the audit question: *what is still longer than it needs to be, and what still reads as AI?* Answer in a few honest bullets and fix them. For a substantial piece, dispatch a fresh reader to answer the same question cold, since the author's eye forgives its own draft.
6. **Restore.** Check that no cut turned a true, qualified claim into a false absolute, and that the specifics, the needed qualifiers, and any wanted voice survived. Put back anything that lost meaning. The floor is the reader, not the word count.
7. **Final scan.** No em or en dashes, no curly quotes, no emoji unless the user asked for them, no boldface spam or Title Case headings. Any hit means the draft is not done.

## Output

The deliverable is the tightened text itself, not a report about it. Deliver the final version inline. With it, give:

- A one-line before/after word count when you cut existing text.
- A short "what I cut and why" note: the few moves that did the most work (whole sections dropped, tells rewritten), not a line-by-line diff.

For a long piece, or when the user asks to keep a record, also save the final text plus the change note to `concise-writing-<subject-slug>-<YYYY-MM-DD>.md` (today's date) in the working directory.

## Principles

- **Length is earned.** Every sentence justifies staying. Stop when the point lands; do not fill to a target.
- **Cut, do not compress.** Delete one whole sentence before you shorten ten. Whole-unit cuts are the highest-leverage move.
- **Read before you cut.** You cannot tighten what you have not understood.
- **Rewrite tells, do not strike them.** A deleted trigger word in a still-generated sentence fixes nothing.
- **Specifics survive, filler dies.** Names, numbers, and examples are the last thing to cut.
- **As long as it needs to be, not as short as possible.** The floor is meaning. Terseness that drops a real point is a worse failure than a few extra words.
- **No em dashes.** Use a period, comma, colon, or parentheses.
