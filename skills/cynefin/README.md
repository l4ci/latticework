# cynefin

## What this is

Cynefin is a sense-making framework from Dave Snowden, developed at IBM in the late 1990s and set out in his 2007 Harvard Business Review article with Mary Boone, "A Leader's Framework for Decision Making". The name is Welsh, roughly "habitat". It sorts a situation by the kind of cause-and-effect that governs it into five domains: Clear, where the answer is obvious and you apply best practice; Complicated, where experts can analyze their way to a defensible answer; Complex, where the answer is not knowable in advance and has to emerge from small safe-to-fail experiments; Chaotic, where you act first to stabilize; and Disorder in the center, where you don't yet know which domain you're in. It is a meta-framework, a dispatcher: it does not solve the problem, it tells you what kind of problem you have and so which approach, and which other tool, fits.

The five domains, their decision models, the diagnostic questions, the cliff between Clear and Chaotic, and the movement between domains are in [references/cynefin.md](references/cynefin.md).

## What it does

The skill runs the analysis in parallel. It first breaks the situation into its constituent issues, because a real situation almost always spans several domains at once. One classifier subagent per issue then places it in a domain with evidence and names the matching action model: sense-categorize-respond, sense-analyze-respond, probe-sense-respond, or act-sense-respond. A synthesis pass maps the whole portfolio across the domains, flags anything sitting on the cliff between Clear and Chaotic or stuck in Disorder, recommends a domain-appropriate move for each issue, and points to which other framework fits which domain. The output is a saved markdown report with the portfolio laid out by domain, the matching actions, and the signals that an issue is moving.

The skill is built around one failure mode: misdiagnosing the domain. Applying a best-practice recipe to a Complex problem fails outright; over-analyzing one fails too, just slower, because the answer is emergent. Most stuck plans are Complex problems being managed as merely Complicated. Every placement names what would go wrong if the issue were treated as belonging to a neighboring domain.

## When to use it

Reach for Cynefin at the start of a hard or messy problem, to pick how to act and which framework to use before committing to either, or when plans keep failing because a complex problem is being handled as if it were complicated. Because it is the dispatcher, it routes you onward rather than competing with the analytic tools:

- To frame and sharpen a fuzzy problem before classifying it, use [tosca-problem-definition](../tosca-problem-definition/).
- To split a problem into clean, separable parts, use [mece-decomposition](../mece-decomposition/).
- For the Complicated issues where expert analysis yields the answer, hand off to a positioning tool like [swot-analysis](../swot-analysis/).
- For the Complex issues, use [scenario-planning](../scenario-planning/) to hold multiple plausible futures rather than forcing one read.

## How to get started

**You provide:** the situation, decision, or mess to make sense of; context on what's been tried and the stakes is optional. Something like "Run a Cynefin analysis on our billing-platform migration."

See [references/example.md](references/example.md) for a worked example.

The procedure is in [SKILL.md](SKILL.md).
