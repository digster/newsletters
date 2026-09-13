---
id: "1a081e0789720b5f"
subject: "What is happening with code reviews?"
from: "The Pragmatic Engineer <pragmaticengineer+deepdives@substack.com>"
to: ""
date: 2026-09-08 16:32:01
labels: ["CATEGORY_PERSONAL", "INBOX", "The Pragmatic Engineer", "UNREAD"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_6413324878686416177", "UNREAD"]
---
👋 Hi, this is Gergely with a subscriber-only issue of the Pragmatic Engineer Newsletter. In every issue, I cover challenges at Big Tech and startups through the lens of engineering managers and senior engineers. If you’ve been forwarded this email, you can
|
One question haunting the minds of CTOs and heads of engineering whom I’ve been talking with, is how to deal with large quantities of code review which have only been growing now that AI agents generate most code at many tech companies.
Since the end of 2025, it has seemed that the era of devs writing code by hand [is over](https://substack.com/redirect/bbc70fb9-8e49-4c89-ac39-8fe847c64beb?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) at startups and in Big Tech. AI agents work faster and generate more pull requests (PRs) than devs ever did, and the size of those pull requests is also increasing.
Today’s article summarizes some approaches to code review at various workplaces in this new paradigm, covering:
Humans review the AI code reviews. The most popular approach: AI code review tools go through code changes, and devs review the review itself.
Triage by “blast radius” & decide an approach. Low-risk changes don’t need human review, and high-risk ones do. Adopted by OpenAI, Anthropic, and others.
Review the plan/tests/database schema, but not implementation. Focus on reviewing the “before” and “after” states of an implementation, rather than the implementation itself.
Produce less code. Set up AI agents to produce smaller PRs that are easier to review and reason about.
Review everything by hand. Not everyone has adopted AI code review tools – even those that have sometimes still expect devs to read through all the new code, before allowing it to go to prod.
No human code review? There’s more talk about dropping human code reviews than there is evidence of this actually happening, so far. The most I could find was AI startups doing it and building additional layers for safer production rollouts.
Why do we review code, anyway? Before figuring out whether or not code review should stay, it’s worth going back to the fundamental technical, team, and organizational reasons for code reviews.
Unsurprisingly, it’s clear there’s no one-size-fits-all solution to the question of how to handle a deluge of AI-generated code review. Please leave a comment below about how your team or company deals with this new, pressing issue!
A snapshot of what’s going on in code review at this stage of AI development is provided by the graphic from GitHub, below. The background context it provides is pretty stark. It shows the stats for the number of PRs and commits over the course of three years on the popular platform:
Over that time, the number of PRs opened has increased fivefold, which is a lot! And growth sped up from the end of 2025, when PRs and commits nearly doubled just in that period alone! So, how are teams dealing with this avalanche of extra work? To find out more, I asked around.
The most common approach is to add an AI code review step to every pull request in a variety of ways:
Use one or more vendors to review PRs. There are dozens of vendors offering this functionality – ones like CodeRabbit, Gitar, Greptile, GitHub Copilot Code Review, Qodo, Claude Code Review, Ellipsis and more. Many teams choose one or more, and the bots then review PRs, leaving comments for devs. For example, the Bun project by Anthropic has CodeRabbit, GitHub Code Review, and Claude Code Review
[all generating comments](https://substack.com/redirect/dd69ae2c-38a9-4f51-ba24-064a94663612?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)on PRs.Multi-agent code review. Build a custom solution which triggers several models/agents to review the code and suggest fixes.
Agents update PRs with fixes. Vendors and home-grown solutions can instruct agents to update PRs with fixes and then re-trigger reviews – if you trust agents to make sensible fixes, that is!
Typical processes:
In the above cases, engineers typically review the review itself, and not usually the code. Here’s Etienne Dilocker, cofounder and CTO at AI database software, Weaviate, [explaining](https://substack.com/redirect/564a0ee1-c333-4f8e-a231-dec7c4bd0d05?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) why he likes their approach:
“It’s very hard for agents to get the balance [of the code review] right. If you ignore human code review entirely and leave it to agents, every PR will either suffer from scope creep or ship critical issues. But, of course, you can’t review everything by hand. So my current favorite setup is:
1. an (adversarial) agent does a review
2. a human makes a scope decision
3. an agent implements the feedback
4. either repeat or break the loop (likely a human decision)
So basically, 90% is left to agents, with humans in the loop for critical scope decisions and exit criteria.”
Noise is a big problem with AI code reviews. WeTravel, a Series C travel tech company, [decided](https://substack.com/redirect/65537871-b66c-4b0b-8e8a-7ac496dad6b6?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) to not use AI for code reviews because of the amount of noise it generated. In June, they did an updated evaluation which showed lots of improvement, but still not enough to justify adopting AI for the task.
As things stand, custom tooling is probably needed to reduce code-review noise. Uber built a clever approach for this; an agentic pipeline called [uReview:](https://substack.com/redirect/8eee7233-a8d3-4b75-a2ad-df8b37f1f2c1?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
What uReview does:
Bots generate lots of code review comments
Comments are graded, and low-confidence comments removed
Comments are merged, categorized, and unimportant ones removed
… in the end, the AI review results in important comments being shown to devs
Another common approach is to decide whether to review code by hand or with AI, based on how “risky” a change is:
Low-risk change: only AI, without human review. It can ship to production once AI agents are happy
High-risk change: mandatory human review
This is the approach that Anthropic and OpenAI follow, which I confirmed by talking with both companies. At Anthropic, Jarred Sumner [told me](https://substack.com/redirect/e6f3eb9d-c311-43f2-b5cf-9d6271909b4c?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) that a human merges even low-risk changes, but that their goal is eventually to get another Claude instance to merge low-risk changes.
And it’s not just at leading AI labs: five-person startup, Duckbill Group, a cloud and AI cost management company, changed their process, as [explained](https://substack.com/redirect/5e8dbfb2-e8f3-4e72-be9e-5df1aabac9d1?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) by cofounder and CEO Mike Julian:
“We ditched code review at Duckbill Group (mostly)
About a month ago, we found ourselves with 60 open PRs for a team of five. They had been accumulating for a few weeks and we all had the sudden realization we were looking at two days of just code review.
I had been tossing around the idea for a while about having AI do all code review and so I just asked the team: what if we just didn’t review the PRs?
We decided to do a couple of things:
Switch to a risk-based system. With a risk-based system, we agreed that if your change touched the public API/MCP, auth, design system, non-additive database schema changes, or agent skills, it needed a human review. We then enforced that with a shell script to add a GitHub label.
Improve our guardrails (unit and end-to-end testing, post-deploy observability, stricter linting and type checking, etc). Improving guardrails was pretty easy, just expensive in tokens and attention. We enabled nearly every rule in ruff/prettier/eslint/ty, and we improved our unit test coverage to a floor of 85%.
Results before vs after:
PRs merged: 353 → 684 (80/wk → 154/wk, +94%)
Merged within 1h: 28% → 45%; within 24h: 76% → 80%
Human-reviewed PRs median merge time: 26h
No human-review median merge time: 1h.”
Here’s how I’d visualize this approach:
Some companies have built additional tooling to make it easier for devs to know which reviews to focus on. For example, Uber’s custom-built Code Review Inbox highlights high-impact changes, so devs know to spend more time and effort on them:
Some devs and teams have stopped reviewing the code (the implementation), and instead review the “before” and “after” states:
Review the plan: spend a lot more time on the plan than before, to get a much more detailed spec. Using [The /grill-me skill](https://substack.com/redirect/86776564-7d85-4377-be4d-3b0e271f7f8d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) by Matt Pocock is a popular method, and I’m also a fan of it for thorough upfront planning, [as is](https://substack.com/redirect/99a0d943-83a4-48d3-a11f-dc542c6cab1d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) Andrea Francesco Speziale, Principal Engineer at Musixmatch:
“After 3 hours of /grill-me, it better one-shot the implementation. I’m not spending a single minute on any review!”
Review the tests: via Test Driven Development (TDD) – which is much easier with agents when writing the tests upfront is a chore – or by focusing the review to ensure the software is tested.
One argument for this approach is that customers and users of software usually don’t care about the code. There’s a caveat that automated tests can verify a lot of different software – and are great at verifying business logic – but they don’t do a good job at verifying whether a UI looks and feels good.
Review the database schema. Jackie Luo, cofounder and CEO of AI startup Sigil, and formerly an engineer at Square, says:
“My current take is that all that really matters is the database schema. Speaking from a fast-moving startup perspective:
1. Everything, besides data, is fluid and recoverable.
2. The schema is the “hard” representation of what’s been built and reveals the riskiest changes, so it’s a good attention/impact tradeoff.
3. Business logic only matters because product behavior matters—so ideally align on that before interacting with a coding agent at all. Then, once the code is written, use abstractions to understand any other significant decisions made.
Understand the product over the code. Use abstractions to translate the latter to the former – except in the case of schemas!”
Jackie’s point is that data (that is, the state) is the most “rigid” part of any system. Stateless business logic is now easy to change because it’s “just” code, and code is easy and fast to generate and regenerate. For startups, it’s worth getting the data schema – and thereby your state machine – right. Then, everything else will be easy and fast to iterate on.
My sense is this approach makes perfect sense for a startup iterating to get product-market fit. However, once you have a business, you’ll want to “guard” the business logic with tests: else your product could break, and existing users will be unhappy when this happens!
Become a paying subscriber of The Pragmatic Engineer to get access to this post and other subscriber-only content.
| Full articles every Tuesday and Thursday | |
| Access to resources and templates for engineering managers and engineers | |
| Access to the complete archive, see all comments and comment on articles |