---
subject: "AI Tooling for Software Engineers in 2026"
from: "The Pragmatic Engineer <pragmaticengineer+deepdives@substack.com>"
to: ""
date: 2026-03-03 16:05:35
labels: ["CATEGORY_PERSONAL", "INBOX", "The Pragmatic Engineer", "UNREAD"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_6413324878686416177", "UNREAD"]
---
👋 Hi, this is Gergely with a subscriber-only issue of the Pragmatic Engineer Newsletter. In every issue, I cover challenges at Big Tech and startups through the lens of engineering managers and senior engineers. If you’ve been forwarded this email, you can
|
Which AI tools are software engineers using, and what do they really think of them? We asked The Pragmatic Engineer subscribers, and nearly a thousand of you have shared your experiences of using AI tools for work. This article provides a high-level overview of those findings from our latest AI tooling survey. Thank you to everyone who participated!
There are plenty of interesting details, most notably, validation of just how much Anthropic and Claude Code have risen to dominate tooling usage. Claude Code is today nearly as widespread as GitHub Copilot was in [our survey three years ago](https://substack.com/redirect/52dae9a8-273e-4be8-8eab-b90956994f80?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) (in the spring of 2023) – which shows how fast the AI market moves.
In today’s issue, we cover:
Interesting findings: Claude Code has rocketed to #1 in just eight months, AI is fully mainstream with 95% weekly usage among respondents, and more.
Most-used AI tools: Claude Code leads the pack, followed by chatbots and GitHub Copilot. Cursor’s rising fast, and newcomers like Codex and Antigravity are gaining traction. Most engineers juggle two to four tools at once.
Popular models: Anthropic’s Opus and Sonnet models dominate coding tasks by a wide margin, with more mentions than all others combined.
AI trends: mainstream adoption achieved. 95% of respondents report using AI tools at least weekly, 75% use AI for half or more of their work, and 56% report doing 70%+ of their engineering work with AI.
AI agent usage rising: 55% of respondents now regularly use AI agents, with staff+ engineers leading adoption on 63.5% usage in the survey results. Agent users are twice as excited about AI as non-users are.
Company size and tool usage: smaller places overwhelmingly favor Claude Code (75% at the tiniest businesses), while large enterprises default to GitHub Copilot. This popularity is probably down to enterprise procurement preferences – and Microsoft’s enterprise marketing efforts.
Tools engineers love: Claude Code is the most loved tool at 46%, far ahead of Cursor on 19% and GitHub Copilot at 9%. Senior leaders are especially enthusiastic about Claude Code.
Demographics: Overview of who took part in the survey.
Full subscribers also have access to a longer, 35-page report with additional details - linked at the end of this article.
The bottom of this article could be cut off in some email clients. [Read the full article uninterrupted, online.](https://substack.com/redirect/5132579f-8701-46cc-9f9b-7cf4331083b3?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
Here are my ten personal, most-interesting findings from this survey:
Claude Code has gone from zero to be the #1 tool in only eight months. Released in May 2025, it’s already the most-used AI coding tool, overtaking GitHub Copilot and Cursor.
AI is now mainstream. 95% of respondents use AI tools at least weekly, or more often, and 75% use AI for at least half their software engineering work. Among readers of The Pragmatic Engineer, it seems the question is no longer whether to use AI in day-to-day work, but which tools to use.
Cursor is catching up fast on GitHub Copilot. As much as we hear about companies dropping Cursor for Claude Code, Cursor is doing more than fine, growing in mentions 35% since our previous survey nine months ago.
Most engineers juggle multiple AI tools. 70% use between two and four tools simultaneously, while 15% use five or more.
Staff+ engineers are the heaviest agent users. 63.5% use agents regularly; more than regular engineers (49.7%), engineering managers (46.1%), and directors/VPs (51.9%).
Codex is seeing explosive early growth. Despite not existing during the last survey, OpenAI’s Codex already has 60% of Cursor’s usage (!!)
Using agents correlates strongly with being positive about AI. People using agents are nearly twice as likely to feel excited about AI while non-users are twice as likely to be skeptical.
Company size influences tool choice more than preference. Huge companies (10K+) more likely to use Copilot (56%), tiny startups mostly go with Claude Code (75%) and Cursor (42%). It seems like enterprise procurement, not individual preference, is behind this divergence.
A tight chatbot race. ChatGPT, Gemini, and Claude as standalone chatbots have nearly equal numbers of mentions, suggesting there’s no clear winner outside of coding-specific tools among software engineers.
Directors and senior leaders are especially into Claude Code. The survey finds this tool is twice as popular with these folks as it is at less senior levels, while Cursor gets less love as seniority increases.
Let’s jump into some of the data:
Just eight months after its release, Claude Code is already the most-used tool, overtaking both GitHub Copilot and Cursor:
Tools mentioned, in order of popularity:
[Claude Code](https://substack.com/redirect/3c26ee1c-3257-4831-80f9-cb9d69f707ba?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o): a terminal-first coding agent from Anthropic. We cover its history in the deepdive,[How Claude Code is built](https://substack.com/redirect/79b0d775-f2f8-4b24-ba1d-f8bbd05d8bdf?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)Chatbots: ChatGPT, Claude, Gemini, and others
[GitHub Copilot](https://substack.com/redirect/08807caf-6c90-4de3-974f-030f9af17a4b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o): launched in 2021, it’s the “oldest” AI coding tool on this list[Cursor](https://substack.com/redirect/b90c7af4-8f52-4f51-8a54-bcad5f552c49?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o): agent-powered coding IDE. Learn more about it in our deepdive,[Real-world engineering challenges: building Cursor](https://substack.com/redirect/733d4f3f-5c11-468c-a00a-76b7030d01d4?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).[Codex](https://substack.com/redirect/aafea543-5fd9-4e79-bffc-5af5c26af0c4?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o): OpenAI’s AI coding agent. We recently covered[how Codex is built](https://substack.com/redirect/f1168c59-a7af-40e9-9f88-dacde003cf60?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)[Gemini CLI](https://substack.com/redirect/856cfc2b-6ecf-45c7-af01-0b8beee0b189?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o): Google’s command line agent[OpenCode](https://substack.com/redirect/b54827dd-e5f7-4b98-9610-a6cf4c466198?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o): the most popular open source coding agent, where you can swap out the model being used, sidestepping vendor lock-in[Antigravity](https://substack.com/redirect/30f9872a-d3e2-44e1-a982-6f630aaf7e20?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o): Google hired the original team behind Windsurf and launched its own agentic IDE[JetBrains Junie](https://substack.com/redirect/3f1eccae-d7ed-4235-b574-ce5fbbbdc2f0?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o): the AI coding agent by JetBrains[Zed](https://substack.com/redirect/7748d67c-0cec-4b30-84e1-53b04f162dc5?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o): a fast editor with agentic workflows[Windsurf](https://substack.com/redirect/36c40669-4adf-4972-9863-ce410130e57e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o): when Google acquihired the team, it did not buy the product. An AI IDE, now owned and operated by Cognition[Amp](https://substack.com/redirect/b2d0c7af-88b0-41c6-9041-20db8568e513?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o): a model-agnostic coding agent. A free version is supported by ads[Augment Code](https://substack.com/redirect/c9182d5e-ee4d-4aa1-8613-1edf0814dd43?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o): an enterprise-focused coding agent[Factory](https://substack.com/redirect/ef727891-d60c-4e29-9f9d-66bb05dd939d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o): agent-native software development, which calls agents “droids.”
It’s interesting to compare how people answered the same question just nine months ago, last May:
Notable trends:
Claude Code has massive momentum and is already the market leader. Since being released in May 2025, it has become the most-used AI coding tool among survey respondents. Anecdotally, I’ve heard many teams are dropping Cursor for Claude Code.
Cursor has grown circa 35% in nine months and now threatens GitHub’s popularity. In this survey, 35% more respondents mention using Cursor than in our previous research, last May. Such growth is impressive: at this rate, Cursor will have more users than GitHub in 6-9 months!
Chatbot usage remains high. Combined mentions for ChatGPT, Claude, Gemini, Perplexity, and others used outside of coding apps are still higher than for any other tool except Claude Code. For context, the most-mentioned chatbot (ChatGPT, 107 times) only has as many as Gemini CLI (also 107).
GitHub Copilot usage stable. Nine months ago, 46% of respondents said they used GitHub Copilot. Since then, it’s barely risen.
Explosive growth for Codex. OpenAI’s Codex wasn’t available during our last survey. But it now already has 60% of Cursor’s usage(!), and could be
[growing even faster](https://substack.com/redirect/f1168c59-a7af-40e9-9f88-dacde003cf60?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)since this survey.Up-and-coming tools: OpenCode, Gemini CLI, Antigravity. None of these had launched nine months ago, but today they’re used by around 10% of respondents – no small feat!
Tools growing more than before: The likes of Zed, Windsurf, Amp, Augment Code, and Factory appear less often in these results, but all are mentioned more by respondents than they were nine months ago.
Here’s how mentions of chatbot usage line up in our survey:
Most tech professionals use between two and four AI tools. An interesting detail is how many different ones are mentioned by respondents:
Noteworthy details:
70% of survey participants mention using between two and four tools
15% use a single tool
15% are using 5 or more
Anthropic’s Opus and Sonnet dominate the ranking of models used for coding.
This is not even a contest: Opus 4.5 and Sonnet 4.5 (latest models at the start of our survey) come up more often than all other models, combined. Anthropic has become the go-to model developer for coding-related work – for now, that is. When this survey launched, Opus 4.6, Sonnet 4.6, and GPT-5.3 were not yet out.
Around 1 in 8 respondents say they just use whatever model is the default at their company. This is interesting to note: these are likely folks who might not bother changing default settings, and just go with whatever’s available. If the default model is powerful enough, that’s fine, but if the company’s default is a cheaper, less capable model, then these people could face a more frustrating experience than those who get to choose what they use.
In the “other” category of models, some other mentions include:
Cursor’s custom Composer/Composer-1 model, and its “Cursor Auto” auto-select model
Kimi/Kimi K2.5 — Moonshot
DeepSeek model variants like R1, V3.2, Coder
Alibaba’s Qwen/Qwen3
xAI’s Grok
Various Mistral models
How often do people use AI tools? Very often, as it turns out; 95% of respondents are using them weekly, at a minimum:
It’s worth reflecting on this data in relation to insights presented by Laura Tacho [at the recent Pragmatic Summit in San Francisco:](https://substack.com/redirect/2d2b4851-c493-44d4-885b-4d5e833ed2d0?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
It seems that AI is now mainstream in software engineering. Anecdotally, this has been my sense since the beginning of the year: everyone whom I talk with is using AI tooling on a roughly daily basis. Now, there’s data to prove it.
This year, we asked readers to estimate the percentage of their software engineering work that’s done using AI. The results:
The data show that AI is embedded in the workflows of participants in our survey:
Only 25% of respondents use AI for less than 40% of their work
56% do 70% or more of their work using AI
75% use AI for at least half of their software engineering work
Eighteen months ago, AI usage was mostly for code generation and tab completion. There were [one or two respondents](https://substack.com/redirect/a713f978-c84e-423c-a993-68ad71577cd4?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) who experimented with early AI agents in March 2024, as something equivalent to a junior software engineer.
This year, 55% say they regularly use AI agents. This is 507 people, a massive jump!
The most common use cases for agents:
Code review and code validation
Automating manual / annoying tasks
Bug fixing / investigating bugs
Code investigation
Debugging
“Crafting” code, or “weaving” it together with the agent
Below is a typical-enough comment from one software engineer who uses agents at a smaller company:
“I use agents for pretty much all coding work, mostly prompting with Cursor Chat. I use it for code investigation, bug investigation, creating commits and pull requests. It’s my tool for reviewing code, I am always still in the loop. Almost all of my AI-written code is still reviewed and ‘crafted’. When using it for code review, I find it helpful to chat with and gain understanding, rather than letting it loose on code review. So, I use it for everything, but I am still very much in the loop.”
A common arrangement in the survey is the split-screen setup: a terminal with Claude Code open to drive work, and an IDE also open to review changes made by the agent.
The tools mentioned by those who regularly use AI agents split almost identically to the broader survey results:
Staff+ engineers are the heaviest users of agents. Here’s the data on agent usage by experience level:
This data point is slightly amusing because it shows there’s not much difference between the lowest and highest levels: 46% of leads and engineering managers say they use AI agents regularly, while for Staff+ engineers it’s 63%. Does it suggest the most experienced engineers are also the most curious?
The more someone uses AI, the more they also use AI agents. We segmented the data by the percentage of software engineering work that respondents do with AI:
Heavy users have AI for 80% or more tasks, or use AI on an hourly basis
Moderate users have AI for 30-80% of tasks, or use AI on a daily basis
Light users employ AI for 30% of tasks or less, or use AI on a weekly or monthly basis
The more positive someone is about AI, the more likely they are using agents on a regular basis. In contrast, those negative about AI barely use agents:
One question is whether this finding indicates correlation or causation: that is, does starting to use AI agents more, actually cause people to feel more positive about AI?
A couple of details:
Using agents seems to make people nearly twice as enthusiastic about AI (61%) as those who do not use them (36%)
Respondents who don’t use agents are twice as likely to be skeptical (22%) about AI than those using agents regularly (11%)
It looks like that if you don’t use AI agents on a regular basis, you may have a negative opinion about the tools, in general, which could come at the cost of not experiencing what the technology has to offer.
In our results, company size and tooling choice correlate for some tools; for example, the smaller a team or company is, the more likely it is to use Claude Code or Codex:
Claude Code is used by a whopping 75% of the smallest companies and teams. This is a big number, far ahead of any other tools. At the smallest places, the most-used tools are, in order:
Claude Code: 75%
Chatbots: 55%
Cursor: 42%
GitHub Copilot: 35%
Codex: 26%
Gemini CLI: 14%
OpenCode: 13%
GitHub Copilot overtakes Claude Code at large companies. This confirms what was known: Microsoft is very good at enterprise sales, and at bundling GitHub Copilot in its suite of products:
Cursor and OpenCode usage drops at massive companies with similar usage patterns. Across the board, usage is roughly the same, regardless of company size. We only see a drop at the very largest of companies with 10,000+ employees:
One theory for such a drop at massive companies could be that large companies often build their own internal coding agents that engineers use; e.g., at fintech, Block, the agent is called [Goose](https://substack.com/redirect/564a5ca1-a4f1-4dcc-985d-d211b1c84b90?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), Meta has its own agent, as does Google with [Jetski](https://substack.com/redirect/3e8c0bbd-5da3-4187-928a-32e22c387f01?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) (its version of Antigravity) and [Cider](https://substack.com/redirect/3a365d2b-c013-4efc-b63a-42bf52802b6c?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).
Google’s tools are evenly used across the spectrum of company size. Google’s Gemini CLI and Antigravity are the only tools in this survey whose usage is notably stable, regardless of company size. Both tools hover at around 10% from the smallest to largest workplaces:
The feeling among survey respondents that they can experiment at work, correlates with Claude Code being available. We asked if readers experiment frequently with tools. Below are the “yes” responses by company size:
When these responses are mapped to the percentage of people using Claude Code, there’s a very similar distribution. My theory is that Claude Code is new enough at 9 months old to have not yet been approved at companies with bureaucratic processes for approving new tools, and this is partly why some respondents feel their chance to experiment with the range of tooling is being thwarted.
Engineers at places with lots of red tape for tooling are less empowered to experiment with new AI tools; not just Claude Code, but any new, interesting tool.
We asked respondents: “Which AI tools do you love using the most, and why?” Below are the tools which respondents enjoy most, in descending order of number of mentions:
Claude and Cursor stand out in terms of how much they are loved. A whopping 57% of respondents mention either Claude Code (46%) or Claude models (11%) as the tools they are attached to. Cursor was at a respectable 19% – double GitHub on 9%.
Other notable tools with two or more mentions:
[Warp](https://substack.com/redirect/f73e3acf-bb25-4112-85ba-80841641c899?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o): a terminal for building agents[Zed](https://substack.com/redirect/7748d67c-0cec-4b30-84e1-53b04f162dc5?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o): a fast editor with agentic workflows[Amp](https://substack.com/redirect/b2d0c7af-88b0-41c6-9041-20db8568e513?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o): a model-agnostic coding agent. A free version is supported by ads[Cline](https://substack.com/redirect/f432610b-5261-4ef9-8f52-3311b0e22af2?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o): an open source coding agent[RooCode](https://substack.com/redirect/6f99b508-a175-44f4-909f-37ee17049160?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o): an open source, AI-powered coding assistant running in VS Code[Continue.dev](https://substack.com/redirect/b214f924-0244-4601-8863-e661bdd1726d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o): AI checks on every pull request
Claude Code is especially loved by Director-and-above folks. Segmenting the “most loved” responses by level (engineers up to the senior levels of staff+ engineers, leads/eng managers, and Director+ folks):
Both Claude Code and Cursor become less loved – or used! – as seniority goes up, but it’s notable that folks in senior engineering leadership positions are obsessed with Claude Code, but not Cursor.
GitHub Copilot is equally loved by engineering managers as Cursor is — and this is surprising:
Both OpenCode and GitHub Copilot are surprisingly loved by Staff+ engineers. Another unexpected detail is that, despite OpenCode being used about a quarter as much as GitHub Copilot, it rivals the “loved” mentions. For Staff+ engineers, it matches GitHub on those terms:
Finally, when segmenting based on company size, we see the familiar pattern of Claude Code vs GitHub Copilot. Claude Code is less frequently mentioned as a “loved” tool as company size increases.
GitHub Copilot sees the opposite trajectory: it’s more loved within larger companies where it’s likely to be harder to experiment with alternatives.
In closing, below are details about who took the survey, and how the 906 responses came together.
Engineers comprise 55% of respondents, and engineering leadership another 34%:
Respondents are experienced professionals. The median respondent has 11-15 years of experience:
Company size is also a fairly even split across this group:
Region-wise, most respondents are in Europe or the US:
We have compiled additional findings from this survey which did not fit in this article: it’s a 35-page article:...
Become a paying subscriber of The Pragmatic Engineer to get access to this post and other subscriber-only content.
| Full articles every Tuesday and Thursday | |
| Access to resources and templates for engineering managers and engineers | |
| Access to the complete archive, see all comments and comment on articles |