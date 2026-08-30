---
id: "19ef51c3db118f3b"
subject: "Slow down to speed up: so much has changed in 6 months’ time"
from: "The Pragmatic Engineer <pragmaticengineer+deepdives@substack.com>"
to: ""
date: 2026-06-23 15:30:26
labels: ["CATEGORY_PERSONAL", "INBOX", "The Pragmatic Engineer", "UNREAD"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_6413324878686416177", "UNREAD"]
---
👋 Hi, this is Gergely with a subscriber-only issue of the Pragmatic Engineer Newsletter. In every issue, I cover challenges at Big Tech and startups through the lens of engineering managers and senior engineers. If you’ve been forwarded this email, you can
|
Scheduling note: there will be no edition of The Pulse on Thursday as I’m in San Francisco for the next week and a half, visiting AI labs and startups, and attending the [AI Engineer World Fair](https://substack.com/redirect/49a521d0-c009-4b20-9a4d-404c26934ae9?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) from next Monday. For the podcast and Tuesday articles, it’s business as usual.
Three weeks ago, at [Craft Conference](https://substack.com/redirect/8c82417a-4307-4632-bc29-efc5d1055141?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), in Budapest, Hungary, I opened the event with a keynote titled ‘Slow Down to Speed Up’.
As with most of my talks, it came together in stages, including with some input from full subscribers to the Pragmatic Engineer, with whom I shared my thinking in advance, in ‘[Ideas: slow down to speed up when working with AI agents](https://substack.com/redirect/e4a1ca8c-7672-497a-97de-9b17100bb308?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)’. Thank you for all the comments!
As fate would have it, just two days beforehand, social media giant Meta appositely provided a real-world case study for my talk, with its [most embarrassing outage of all time](https://substack.com/redirect/9fdf8ddb-8aa9-4c4f-8862-34d0a673f356?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o): users could simply ask the Meta AI to change the email of any account, and the bot happily complied – even if the account belonged to someone else entirely – including a former US president. It was a timely example to kick off the talk with. Check out the full keynote that’s available to [view on YouTube](https://substack.com/redirect/b501699a-ecc2-4462-b2b7-9576a88952f2?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o):
In this article, I summarize the key parts of my Craft Conference keynote in detail, and some responses received at the event. Full subscribers also have access to the slides, [here](https://substack.com/redirect/2def11f1-e030-4f40-866a-8be7416087e2?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), and at the foot of this article.
We cover:
Meta: “AI psychosis” in effect? Meta has been destroying its engineering org, and an obsessive focus on AI seems to be one reason for it. For more on this question, check out this
[deep dive](https://substack.com/redirect/c45a556f-4a3e-4dd3-8d06-675eb843e73b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).Everything’s changed in six months. From around November last year, things changed with a more capable generation of AI agents like Opus 4.5 and GPT-5.4.
How are tech companies changing how they work? Anthropic, OpenAI, Google, Uber, startups, and traditional companies.
Trends. Individual productivity is up, but team productivity’s flat, tokenmaxxing and tooling adoption, vanishing middle management, CEOs and CTOs back to coding, and more.
Trends across software. Falling software quality, GitHub’s constant reliability woes, AI slop overwhelming devs who care about quality, and more.
Advice for software engineers and engineering leaders. Suggestions to help future-proof a career.
Feedback. “It’s happening here too!” is a common theme, and relief for some that it’s not unique to their own workplace.
The bottom of this article could be cut off in some email clients. [Read the full article uninterrupted, online.](https://substack.com/redirect/0bb4ea91-a9c1-4eff-82f2-6ec5b3264119?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
I thought it was a made-up story when I read that Meta had enabled account takeovers via a “zero auth” policy; i.e., simply asking the Meta AI bot was sufficient to change any account’s email address. After all, shipping such a regression would fly in the face of security measures, code reviews, automated testing, and metrics. Plus, the company has dedicated Integrity teams whose mission statement is to ensure something like this never happens… And yet, this bug shipped.
It went undetected by anyone at Meta, and high-profile accounts like that of former US president, Barack Obama, were taken over as a result. Instagram’s dedicated Integrity team seems to have discovered the embarrassing issue via the news.
As mentioned, it was two days before the Craft keynote, so there was enough time to ask around at Instagram and Meta. Engineers at the company there told me this disaster was caused by AI-generated, AI-reviewed code, along with layoffs, and by forced reassignments from Integrity teams and elsewhere onto AI labeling and related duties.
The problem at Meta seems to be that leadership is aggressively pushing AI, while withdrawing resources and headcount from areas responsible for security, quality, and reliability. Since last week’s [deepdive](https://substack.com/redirect/c45a556f-4a3e-4dd3-8d06-675eb843e73b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) into what’s been happening behind the scenes was published, I’ve learned further details:
Integrity teams at WhatsApp
[have been hit hard by layoffs](https://substack.com/redirect/66a1e779-7ad2-4861-b344-e7ca60c1cdbd?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)and enforced data-labeling reassignmentsInstagram’s design team suffered a 44% cut in headcount during layoffs
The Developer Documentation and Support team had a full 95% headcount reduction during layoffs
Data labeling at the ADO group
[goes beyond](https://substack.com/redirect/e027e955-db1a-40cb-b70f-179a25c5bb4f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)“just” labeling; there are many AI training tasks to do. But these are repetitive, unless you get really creative.
Based on everything I heard from talking with Meta folks, AI-induced behavior was indeed at the heart of this outage. AI-generated, AI-reviewed code, and security teams being gutted, were also factors in the beyond-embarrassing incident. As reported in last week’s deepdive:
Instagram’s Trust and Safety Team lost around 50% of its staff to data labeling and layoffs. Some of the most senior folks were drafted onto AI training tasks.
AI-generated changes with zero human input, with just an additional AI code review, have been very common in recent months across the codebase. The change that caused this outage looked like one of these
Normally, the Trust and Safety team would be on top of monitoring and alerting of security breaches, but it is currently in full disarray due to rapid, internal disorganization”.
If major changes like data labeling assignments and staff tracking are undone, then perhaps things at Meta could return to normal. But so far, the most being done is that leadership has boosted budgets for snacks, travel, and events. Hardly the change needed to restore morale and the former culture!
The comparison to the Lumon corporation in the hit show, Severance, was duly made:
Meta’s worst-ever outage can be interpreted as a warning about what happens when there’s so much focus on AI that the basic health of a company’s main – money-spinning – products is neglected. Instagram, WhatsApp, and Facebook generate the bulk of revenue for Meta, but the company is reallocating more engineers to training the coding model, and aggressively cutting the headcounts of vital orgs to do so – up to the point of not having oncall coverage for key services, and security teams being too stretched to do their jobs.
Am I missing some insight about why it’s more important to build a state-of-the-art, likely-closed AI model that’s good at coding, than it is to keep operating revenue-generating businesses with stable infra?
Independent, experienced software engineers with zero affiliation to AI labs have been saying for a few months that how we do software engineering has been transformed.
David Heinemeier Hansson (DHH), creator of Ruby on Rails [in January](https://substack.com/redirect/9f857e09-e344-48cf-95f9-78f193b7a3a1?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o):
”Just [in] summer 2025, I spoke with Lex Fridman about not letting AI write any code directly, but it turns out part of this resistance was simply based on the models not being good enough at the time! I spent more time rewriting what it wrote, than if I’d done it from scratch. That has now flipped.”
Simon Willison, creator of Django, [in May](https://substack.com/redirect/5bbfc438-087b-48e2-9e7b-8177b63ae2be?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) pinpointed the start of the change to late last year:
“The models released in November 2025 elevated agents to being genuinely useful. We’ve had six months to get used to that idea now; it’s no wonder companies are beginning to spend real money on this technology.”
Teams using agents now ship 5x as many pull requests as two years ago. Here’s data from Linear:
Devs using AI harnesses are producing 2.5x as much code versus 18 months ago. Data from Cursor shows that their users, on average, went from adding 3,500 lines of code in January 2025 to 8,600 today:
The size of pull requests is up 3x versus 18 months ago. Also from Cursor:
More AI changes are accepted without human review. Data from Cursor shows a big jump in changes being accepted without human review from around February this year, when Opus 4.7 and GPT 5.5 launched:
We’re seeing a lot more code generated, and less of it than ever being reviewed by devs. In the relatively short time since AI agents became really good last November, there are more pull requests generated by devs, those pull requests are getting better, and code reviews are harder to keep up with. And so, reviews are less stringent and more changes are shipped to production sans human review! As per my discussions with Meta engineers, these kinds of AI-generated, AI-reviewed pull requests [at Meta, they’re called diffs] are what caused the most recent, embarrassing outage at Instagram.
Details from a few larger tech companies:
Anthropic: all-in on AI agents. In March, Boris Cherny, creator of Claude Code, [was on the Pragmatic Engineer podcast](https://substack.com/redirect/658e4078-265c-40f6-b411-cf67bd87544f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) and shared some details:
He personally runs ~5x agents parallel, and ships 20–30 PRs/day
Product requirement documents (PRDs) are dead & prototypes have replaced them inside Anthropic
~100% of Claude Code was generated by Claude in March
~70-90% of code inside Anthropic was generated by Claude
Claude Cowork – another billion-dollar product in terms of revenue potential – was built in just 10 days
Since then, Boris has [shared](https://substack.com/redirect/02a682eb-4d3b-4ca7-ae51-e401c542df7a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) that his workflow has changed to setting up loops to run agents.
OpenAI: moving much faster with AI agents. OpenAI’s Codex team was [on the main stage](https://substack.com/redirect/76adcec9-db99-4850-acd7-7e6759d2de09?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) at The Pragmatic Summit in February. Tibo Sottiaux (head of engineering, Codex, OpenAI) shared interesting details on how software development is done in the Codex team:
There’s a “fix this” button integrated into the internal OpenAI mobile app. It makes one-shot fixes to bug reports, which devs review and can merge
AI code review for all code changes. With a tiered approach, some changes can be merged with just AI review, and more important ones need an extra human review
Most devs run several agents in parallel, often walking around with their laptop lids open, so the machine doesn’t enter sleep mode and suspend agents
Code isn’t really written by hand anymore on the Codex team, and is also less common on other teams too
“Taste” is becoming a core skill for working at the company
Codex improves itself: it runs its own test suite, runs improvement tasks overnight, and during team meetings it takes actions on topics discussed
Google: AI widespread. Gemini is not as capable at coding as Claude or Codex, as acknowledged by Google’s CEO, but it’s widely used companywide. The less capable coding model could be hurting AI adoption compared to other companies.
Uber: in-house AI infra. We covered in-depth [how Uber uses AI for development](https://substack.com/redirect/c99606ba-3a81-457c-858d-e0c84fe44bc0?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), touching on internal systems like:
Uber’s MCP Gateway:
Uber Agent Builder:
The AIFX command line interface:
Minion: background agents
Code Inbox:
Smart Assignments as a neat feature of Code Inbox:
Risk Profiles: another smart feature inside Code Inbox:
uReview, Uber’s AI code review tool:
Autocover and Shepherd for large-scale migrations:
Uber is a good case for learning how much of internal developer infra needs to be rebuilt in order to work well with AI agents. Uber built all the tools above because they needed new, better ways to integrate AI agents into the developer workflow, but couldn’t find anything that worked up to requirements. I’d also point out how much time and effort Uber invested in making code review more efficient. Devs are, indeed, getting overloaded with AI code reviews and Uber’s Code Inbox tries to separate the important pieces of code to review from unimportant ones.
Startups are jumping into using AI agents, although their integrations are more basic. In preparation for the keynote, I talked with several startups about their AI usage. Harnesses like Claude Code, Codex, Cursor, OpenCode and others are popular, and I also noticed most startups are heavily integrating AI agents into Slack, so devs can kick off bugfixes or small feature requests straight from the chat tool.
I observed startups being the most likely to experiment with new AI dev tools; from code review, all the way to AI incident management tools.
“Traditional” companies are also heavily investing in AI dev tools. At the recent Pragmatic Summit in San Francisco, Laura Tacho [shared](https://substack.com/redirect/944ba9c8-9257-48e0-9896-e1ec4501a236?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) interesting details:
In February, 18,000 Cisco developers used Codex for complex migrations, code review, and refactoring. This was very early – Codex was just starting to gain industry-wide adoption!
JP Morgan Chase built a multi-agent framework for annotation, using multiple specialized agents to label customer interaction data, and judge agents to aggregate and rank results. These are pretty advanced use cases!
In general, “traditional” companies do not seem to be lagging behind in using, paying for, and adopting AI agents and AI developer tools.
There are trends I’ve observed around the adoption of AI dev tools:...
Become a paying subscriber of The Pragmatic Engineer to get access to this post and other subscriber-only content.
| Full articles every Tuesday and Thursday | |
| Access to resources and templates for engineering managers and engineers | |
| Access to the complete archive, see all comments and comment on articles |