# concise-writing

## What this is

A method for writing or editing text so it is only as long as it needs to be and carries no signs of AI writing. It rests on two ideas. The first comes from [ponytail](https://github.com/DietrichGebert/ponytail), a code-minimalism tool built on the line "the best code is the code you never wrote": turned on prose, the best sentence is the one you never wrote, so the default move is to cut rather than polish. The second comes from Wikipedia's [Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing), which catalogs the specific, nameable tells of machine prose. Underneath both sit the classic concision sources: Strunk and White, Zinsser, Williams.

The parts are a cut ladder (delete whole units before trimming words), a set of short questions to run a text through, a compressed catalog of AI tells, a handful of brevity moves, and a guardrail against over-trimming. They live in [references/concise-writing.md](references/concise-writing.md).

## What it does

A single editor runs a loop. It anchors to the purpose and the reader, then drafts (write mode) or reads the whole text for meaning (edit mode). A cut pass runs the text down the ladder, killing whole sections and sentences before it trims words. A de-AI pass scans against the tell catalog and rewrites each tell around the concrete claim under it. A read-aloud and audit pass fixes anything that stumbles and asks what is still too long or still machine-sounding, optionally sending a fresh reader to answer cold. A restore step puts back any qualifier or specific whose loss changed the meaning, because the floor is the reader, not the word count. A final scan strips em dashes, curly quotes, stray emoji, and boldface spam.

The deliverable is the tightened text, not a report about it, plus a before/after word count and a short note on what did the most work. Long pieces are also saved to a dated file.

The guardrail is the point that separates this from a shrink ray: conciseness is not terseness, and the shortest version is not always the clearest. A cut that drops a real point or a needed qualifier is a worse failure than a few extra words.

## When to use it

Reach for it to write text tight from the start, or to make an existing draft shorter and less machine-sounding: emails, posts, docs, announcements, READMEs, marketing copy, essays. It fits "tighten this", "make it shorter", "cut the fluff", "this reads like AI", and "write a concise X".

If the problem is not length or voice but the order of an argument, where the answer should come first and the logic should be a pyramid, use [scqa-pyramid](../scqa-pyramid/) to structure it first, then this skill to tighten the result.

## How to get started

Hand it the text to tighten, or the brief to draft from, and say what the text is for and who reads it. That last part is the anchor; without it the skill asks one short question before starting. Optionally add a length ceiling, the voice to hold, or a sample of your own writing to match.

See [references/example.md](references/example.md) for a full invocation and [SKILL.md](SKILL.md) for the procedure.
