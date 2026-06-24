# concise-writing run: product update announcement

A worked run of the skill in edit mode. The input is a draft product-update email, AI-written and three times longer than it needs to be. The job is to make it land in a busy inbox.

## Anchor

- **Purpose:** tell existing users what changed in this release and what they should do.
- **Reader:** current customers skimming an email between meetings.
- **Takeaway:** "Imports are faster and no longer fail on large files; nothing you need to do."

## Original (218 words)

> Subject: Exciting Updates — A New Chapter in Your Experience!
>
> Hi there,
>
> We're absolutely thrilled to share some exciting news with you! At [Company], we've always believed that great products are a testament to listening to our users, and this release marks a pivotal moment in that ongoing journey.
>
> Our team has been working tirelessly behind the scenes to deliver a range of improvements designed to enhance your workflow, streamline your processes, and empower you to do your best work. We've heard your feedback loud and clear, and we're committed to continuously improving.
>
> - 🚀 **Faster Imports:** Import speeds have been significantly improved, reducing friction and saving you valuable time.
> - 💡 **Increased Reliability:** Large files now import more reliably than ever before, ensuring a seamless experience.
> - ✅ **Behind-the-Scenes Polish:** Numerous under-the-hood enhancements contribute to a smoother, more intuitive platform.
>
> It's not just about speed — it's about giving you back the time to focus on what really matters. We can't wait for you to experience these changes for yourself!
>
> As always, we're here for you. Should you have any questions, please don't hesitate to reach out. Exciting times lie ahead!
>
> Warm regards,
> The [Company] Team

## Cut pass

Whole units the takeaway does not need, deleted first:

- The subject-line hype ("Exciting Updates, A New Chapter").
- The opening paragraph: significance inflation ("a testament", "marks a pivotal moment", "ongoing journey"), zero information.
- The "working tirelessly behind the scenes" paragraph: promotional, says nothing the bullets do not.
- The "Behind-the-Scenes Polish" bullet: vague filler, no user action.
- The closing two paragraphs: negative parallelism ("not just about speed, it's about"), false-authority "what really matters", servile sign-off, generic upbeat ending ("Exciting times lie ahead").

## De-AI pass

Tells rewritten in what survived:

- Emoji and bold-header bullets stripped to plain sentences.
- "Import speeds have been significantly improved" (passive, copula-avoiding) to "Imports are faster".
- "import more reliably than ever before, ensuring a seamless experience" (-ing tail, vague) to the concrete fact: large files no longer fail.
- Em dash in the closing line removed with the line.

## Audit

- Still longer than it needs to be? The subject can be plainer; one line of intro is enough.
- Still reads as AI? "valuable time" is brochure filler. Cut.
- Lost meaning? Need to keep "nothing you need to do", the actual takeaway for the reader, which the original buried.

## Final (54 words)

> Subject: Imports are faster, and large files now work
>
> Hi there,
>
> Two changes in this release:
>
> - Imports run faster.
> - Large files no longer fail partway through. If an import used to time out, try it again.
>
> Nothing on your end to do. Reply if anything looks off.
>
> The [Company] Team

## Result

218 words to 54, a 75% cut, with more information than the original carried: the one fact the reader needed ("large files no longer fail", "nothing to do") was missing from the bloated version and is now the point. The voice is plain because the genre is a utility email, not an essay; nothing here wanted personality.
