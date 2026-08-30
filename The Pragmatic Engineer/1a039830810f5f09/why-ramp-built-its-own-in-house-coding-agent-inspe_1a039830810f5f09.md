---
id: "1a039830810f5f09"
subject: "Why Ramp built its own in-house coding agent, Inspect"
from: "The Pragmatic Engineer <pragmaticengineer+deepdives@substack.com>"
to: ""
date: 2026-08-25 15:20:24
labels: ["CATEGORY_PERSONAL", "INBOX", "The Pragmatic Engineer"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_6413324878686416177"]
---
👋 Hi, this is Gergely with a subscriber-only issue of the Pragmatic Engineer Newsletter. In every issue, I cover challenges at Big Tech and startups through the lens of engineering managers and senior engineers. If you’ve been forwarded this email, you can
|
At a select few tech companies, they write most of their code with their own, custom-built, internal AI coding agents. This is different from most of the industry which uses AI coding agents and harnesses like Codex, Claude Code, Cursor, OpenCode, GitHub Copilot, etc. At Ramp, their own version is called [Inspect](https://substack.com/redirect/691d0818-96f6-4f89-a190-d6681f327ec6?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), while at Block it’s [Goose](https://substack.com/redirect/642ee680-497c-465f-87a8-5bd785c88efc?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) (open source), at Stripe it’s [Minions](https://substack.com/redirect/0f027cf2-12ed-432f-b296-4c3f0cbb8e71?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), and [River](https://substack.com/redirect/06fd5b19-260a-4b6d-91f8-3174db306a88?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) at Shopify.
But why not just use what frontier labs and coding harness AI startups already offer; why take the time and effort?
We reached out to Ramp, a fintech company big on building its internal AI infrastructure, and sat down with the founding team of Inspect and engineering leadership. We talked with CTO [Rahul Sengottuvelu](https://substack.com/redirect/ca9ea722-970c-45cf-b993-8e158284c1c4?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), head of engineering [Hamid Dadkhah](https://substack.com/redirect/ef7c252b-9cda-4532-8956-c34bb490e571?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), and [Zach Bruggeman](https://substack.com/redirect/34f9b884-d2cb-4cd6-9bfa-fe7548ab8025?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), principal engineer and founding engineer of Inspect.
Today, we cover:
What is Inspect? Imagine an AI coding agent running on remote sandboxes with access to most internal data sources, and verifying all backend and frontend changes on the remote machine.
Why build your own background coding agent? Engineers and designers at Ramp were dissatisfied with third-party harnesses: they wanted to run more than a few agents in parallel – which local machines don’t support – to have better frontend tooling, and also faced demand for remote development environments.
How Ramp uses Inspect: coding, bugfixing in Slack, debugging, and building internal agents like code review and incident management on top of the Inspect platform
Tech stack and architecture: React/Vite, Cloudflare Durable Objects, SQLite, Cloudflare Agents SDK, Modal sandboxes.
What makes Inspect so popular? The machine in the cloud is a developer machine, plus it has access to numerous internal integrations via API and MCP.
Inside the sandbox. OpenCode, services for development (e.g. Postgres, Redis, RabbitMQ, Temporal), Chromium, and VS Code Server. Plus, we check out smart tricks to make sandboxes spin up in five seconds or less(!!)
Collaboration & feedback. All Inspect sessions are public and open to collaboration, with no opt-outs allowed. More than 150 people at Ramp have contributed to the project.
If you’re like us, you might wonder what the point would be of building your own harness and investing the time and resources in it, given all the choices already out there. This article sets out to answer that question, to understand why other places chose a similar path, and how a non-AI frontier lab can build more efficient tooling than what the frontier AI labs offer. It looks like the “buy, don’t build” tooling convention might not apply to AI tools!
Let’s get into it.
The bottom of this article could be cut off in some email clients. [Read the full article uninterrupted, online.](https://substack.com/redirect/e665577b-5521-46f4-bd7d-692bf907a9d1?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
Inspect is Ramp’s internal background coding agent, shipped and opened internally last November. Engineers at Ramp can use any tool they want, but 75% of merged PRs are now raised by Inspect; a clear indication that many engineers prefer the tool over others:
A couple of things make Inspect different from coding agents like Claude Code and Cursor:
Remote sandboxes: Inspect spins up a sandboxed remote development environment which unlocks unlimited session concurrency, centralized setup configuration, and cross-functional session collaboration.
Internal integrations: Inspect is integrated across the org with the same tools and context that a Ramp engineer has; the only constraint on agents’ ability is model intelligence, not missing tools or access.
Inspect verifies all its changes. As a remote development environment with full tooling access, it can “close the loop” and confirm the changes it makes work:
Backend verification: Inspect runs tests, reviews telemetry and queries feature flags
Frontend work verification: Inspect visually verifies its own work by providing screenshots and live previews to users.
At present, most third-party AI harnesses cannot do these kinds of verifications ‘out of the box’ because they lack internal integrations with things like telemetry and feature flag systems. Also, almost a year ago, Ramp built screenshot verification before it was supported by third-party vendors. Things like this placed Ramp months ahead of nearly all AI coding harnesses, and they could also build a far better feedback loop in their own harness.
The v1 of Inspect was a Chrome extension for designers to prompt AI to make minor website changes. A few months later, the v2 version with background agents followed.
By January of this year, just two months after the v2 launch, around 60% of PRs at Ramp were authored by Inspect, which increased to 75% by May. At Anthropic, Claude Code won rapid adoption after an internal release, as covered in the deepdive [How Claude Code is built.](https://substack.com/redirect/c9433739-bd0f-4d8e-87d9-6e0fd745c2f2?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
Then Inspect hit a neat milestone in July, crossing the one million total sessions mark:
There are a few reasons why Ramp decided to turn down tried-and-tested products and create their own:
Local machines are limited in how many agents they can run. Ramp found third-party products below expectations; they liked Claude Code on day 1, but were constrained by only being able to run one or two sessions on local machines.
Better frontend tooling. The web engineering team wanted to improve their frontend tooling so designers could make small UI tweaks. There was an opportunity to use AI to automate themselves out of that loop.
Need for remote dev environments. As Ramp scaled, so did the complexity, and with it there was more work at the intersection of systems, like debugging backward compatibility, and broken API contracts. The solution was to create remote dev environments.
Inspect started as a designer’s frontend tool, and a good part of its team were frontend engineers with interests in UX and speedy performance. The v1 was a Chrome extension for visual edits, where a user could highlight an area and tell the AI what minor website changes to make, like copy edits and button placements. The task of building a tool for making UI edits with AI was given to two frontend engineers, Zach Bruggeman and Jason Quense, who aside from their frontend domain knowledge, brought a welcome adversarial perspective, as they were less than fully convinced by AI at that time.
People liked v1 but it wasn’t adopted because engineers already knew how to go to a file and edit a single line of code, so didn’t have a reason to use it, and it also required setting up a local development environment, making it too complicated for non-devs.
For the current iteration of Inspect (released November 2025) the team pivoted. They built Inspect v2 as a remote development environment with a coding agent on top. Setting it up as a remote environment that they could configure centrally removed the need for local setup on each machine. They were also encouraged by seeing that OpenCode, the open-source coding agent which serves as Inspect’s harness, exposed an HTTP API which made it straightforward to set up, and was open-source, good enough, and importantly, offered model agnosticism.
Check out the episode of The Pragmatic Engineer podcast [with OpenCode creator, Dax Raad](https://substack.com/redirect/a8eb1ca4-ac39-4baf-a989-8ffdafc0803d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).
After pivoting, adoption skyrocketed to where it is today:
Adoption numbers today:
75% of all merged PRs come from Inspect sessions
~90% share of PRs merged into the Inspect repo come from an Inspect session
Under 5 seconds to spin up a fully provisioned remote dev environment
5.5 people in the Inspect team: four engineers, a director, and part-time PM
150+ engineers at Ramp who have contributed to the Inspect codebase
Having built it, Ramp uses Inspect for a few things:
Coding: obvious use case; engineers prompt Inspect with small and medium-sized coding tasks that can often be one-shot passes. For larger, more complex tasks, devs often use Inspect to kick-start an idea and then take over developing it locally.
Bugfixing in Slack: the @inspect fix this prompt in Slack. Inspect reads all the thread context and raises a pull request (PR) with a fix.
Debugging: Inspect can do things like debug the code (stepping through the code in debugger mode), query the sanitized read-only prod DB replica, find business logic/data mismatches.
Using Inspect to build Inspect: Inspect is used to build itself, and more than 80% of Inspect is written in Inspect sessions.
Platform for agents: Engineers at Ramp have built more than 200 agents running on top of the Inspect platform
Here’s an example of how debugging works. Devs can ask the agent to investigate an issue, and Inspect goes off and pulls data from the correct sources:
The tool goes and makes database or Snowflake queries when helpful:
The debug agent can be long-running while it gathers data from various sources. Finally, it presents its findings:
This debugging example illustrates how much more capable agents can be with the correct access to tools, data, and context.
Some internal agents built on top of Inspect:
ReviewBuddy: Ramp’s own code review system, customizable per team. The difference from third-party AI code review tools is that it’s very aware of Ramp’s context, and the team found it to work better than third-party tools. Built by a single engineer in a week.
Oncall Assistant: connected to all production and observability systems. When the agent detects an incident, it gathers all relevant context and tries to determine the cause. The oncall engineer can choose to join the Inspect session and prompt against this proposed fix.
Testo: a frontend QA tool and browser-based agent that clicks around like a user would, and creates
[Playwright](https://substack.com/redirect/a8357bd3-2197-47f4-9b3b-8239cc766e10?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)tests.Ramp Research: the company’s agentic “data analyst” is connected to all Ramp’s data sources, like
[Looker](https://substack.com/redirect/b47cc0de-137c-45c7-981c-d2826bf1827f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o),[Snowflake](https://substack.com/redirect/7586a758-e807-4c1c-a59a-d79cc97722b0?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)and[dbt](https://substack.com/redirect/00218f88-c328-4998-9240-f4ec30f1c490?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)tables. Ping it from Slack about any topic and it gets answers. Before Ramp Research, engineers and data analysts had to know which data tables to query and join. Ramp previously shared[more about its Research](https://substack.com/redirect/47a2c822-79e8-4295-affc-fb834595cd6a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).Voice of the Customer: connects to several customer feedback sources like chat, email, App Store reviews, etc. It collects feedback from the last 90 days, and allows prompting against them as a Slack bot
Error automations: automatically create draft pull requests based on alerts from Sentry or Datadog.
Visualized:
It’s clever that the Ramp team extended Inspect into a platform, and made it easy to build additional agentic tools, without engineers having to worry about the cloud backend for those tools. Not bad for a tool that started as a simple Chrome extension almost exactly a year ago!
Inspect’s core principle is that agents should have access to the same context and tools as software engineers. Hooking up Inspect to the data sources that engineers would browse with the same tools seems to be a key difference between Inspect and third-party AI harnesses...
Become a paying subscriber of The Pragmatic Engineer to get access to this post and other subscriber-only content.
| Full articles every Tuesday and Thursday | |
| Access to resources and templates for engineering managers and engineers | |
| Access to the complete archive, see all comments and comment on articles |