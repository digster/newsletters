---
subject: "How Anthropic built Artifacts"
from: "The Pragmatic Engineer <pragmaticengineer+deepdives@substack.com>"
to: ""
date: 2024-08-27 16:26:48
labels: ["CATEGORY_PERSONAL", "INBOX", "The Pragmatic Engineer"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_6413324878686416177"]
---
👋 Hi, this is Gergely with a subscriber-only issue of the Pragmatic Engineer Newsletter. In every issue, I cover challenges at Big Tech and startups through the lens of engineering managers and senior engineers. If you’ve been forwarded this email, you can
|
In the past two months, Anthropic has started to gain momentum among software engineers. The company [released its latest language model](https://substack.com/redirect/bc6aac54-3253-4c8c-b2aa-5854d165eb54?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) – Claude 3.5 Sonnet – on 20 June, which works noticeably better than other large language models (LLM) for coding-related work – and gives better results than ChatGPT models, which is [wowing many developers](https://substack.com/redirect/fa7b69ec-891d-4cb4-9703-f6c11431063b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). We touched on this observation [in The Pulse #101](https://substack.com/redirect/fa7b69ec-891d-4cb4-9703-f6c11431063b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o): it’s the first time a company other than OpenAI potentially leads in LLM capability.
Anthropic also released a new feature, [Artifacts](https://substack.com/redirect/bc6aac54-3253-4c8c-b2aa-5854d165eb54?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), alongside Claude 3.5 Sonnet. It allows the creation of things like websites (single page React or HTML), code snippets, documents, diagrams, and more, with only a prompt. It’s surprisingly helpful for a variety of tasks, and also fun. For example, I gave Claude this prompt:
“Create a web application that allows me to tweak the color of The Pragmatic Engineer Logo. This logo is three rectangular bars that increase in height, and are in the color red.”
The result was what I asked for: a mini-web application with an interactive color picker:
This small feature feels like it could be a big leap in using LLMs for collaborative work. Curious to learn how this product was built, I contacted the Anthropic team. Today, we look at the reality of building such a well-received feature, covering:
From the drawing board to shipping Artifacts. A scrappy prototype demonstrated on “WIP Wednesdays” kicked off what became Artifacts.
Tech stack. Streamlit, Node.js, React, Next, Tailwind, and Claude.
Using Claude to build Artifacts faster. The team not only dogfooded Claude, but used their LLM to build software faster, including Artifacts.
Timeline and team. A tiny team built and shipped this feature in just 3 months.
AI products and security. Security is part of everything Anthropic does. An explainer on how model security works, and the product security approach for Artifacts.
When is an idea a winner? Not even the engineers building this feature expected it to be as successful as it is.
GenAI paradigm shift? Artifacts is not a massive feature in itself, but it could pave the way for GenAI becoming a much more collaborative tool.
It just so happens that Artifacts is enabled by default for all users on web and mobile, [starting today (27 August)](https://substack.com/redirect/74cdba68-ad5a-423a-a807-e952da42062a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). So you can [try out](https://substack.com/redirect/74cdba68-ad5a-423a-a807-e952da42062a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) this feature straight away!
The bottom of this article could be cut off in some email clients. [Read the full article uninterrupted, online](https://substack.com/redirect/06cce4ec-53aa-402e-ad4b-8a80839e26f8?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).
Let’s jump into how Artifacts was built. For this, I talked with five current Anthropic employees involved in its creation:
Research scientist, Alex Tamkin, who built and demoed the first prototype
Product designer, Michael Wang, who joined iteration efforts early
Product engineer, Florian Scholz, who helped productionize Artifacts
Security engineer, Ziyad Edher, who helped evaluate security for Artifacts
Brand, Sam McAllister, who created several launch materials for Artifacts
In March 2024, research scientist Alex Tamkin was testing the website generation capabilities of Anthropic’s newest model, using these steps:
Prompt model to generate HTML code for a website
Copy generated code into an editor
Save file as an HTML
Open a web browser to view HTML file
The overhead wasn’t too bad from doing this once or twice. But Alex did it dozens of times, he recalled:
“This whole round-trip process was taking a lot of time. I kept thinking:
‘What if I could just see it right away?’
You know that feeling when you're cooking and you want to taste the sauce straight away, not wait for it to simmer? That's what I was after. I just wanted it to render on the screen immediately.”
So Alex put together a janky side-by-side interface, with Claude on the right and the realtime output on the left. He then showed this rough-around-the-edges demo to his team at a regular catchup session called “WIP Wednesday”:
The demo was a turning point, he says:
“I think this demo was when a lot of us realized: ‘oh wow, there's something here.’
Seeing it immediately on the screen, something sort of... clicks. You know how sometimes you don't realize you need something until you see it? That's what happened.
It wasn't just about making the process faster. It was about changing how we interact with Claude, making it more tangible, more immediate, more collaborative.”
One demo participant was product designer Michael Wang, who then helped make the rough demo into a more production-ready experience. He says:
“I just kept replaying this demo from Alex over and over again in my head. So I started building a prototype, mainly to see how much we could actually pull off with some basic prompt engineering and instructions for Claude. Turns out, quite a bit. I had a proof of concept working much faster than I expected. And it just got my mind racing. Eventually, I felt like I had a pretty solid idea, and I posted it to Slack.”
Posting to internal Slack was a great idea, as it got the attention of many colleagues, including Anthropic’s CEO, Dario Amodei, who offered encouragement. After this, things moved quickly, says Michael:
“In about a week and a half, we had it ready for internal dogfooding. The entire company could start using it. It was a bit surreal seeing something go from an idea to a tool that everyone was experimenting with in such a short time. But that's often how it goes when you're working with Claude – sometimes things just click, and you find yourself building something you didn't even know was possible a week ago.”
As a more polished version took shape, Michael shared the demo internally, gathering even more feedback and encouragement from colleagues:
Engineers at Anthropic have a lot of autonomy, and are expected to take advantage of it. Product engineer Florian Scholz was just getting started at the company, when he saw the demo and decided to help ship the new feature. He recalls:
“Alex's first demo of Artifacts happened in my second week at Anthropic. I was still onboarding in the San Francisco office and adjusting to a very new environment, so I put it on the back burner at the time. Later, when Michael showed a working prototype, I jumped right in.
We all had a common realization that this feature was a step change. My immediate focus was on getting our infrastructure to a place where it was secure. We were concerned about preventing any issues that might arise from untrusted code generated by Claude. It was a pretty great introduction to the kind of fun challenges we face on product engineering at Anthropic.”
With the product ready to ship in beta, there was one last thing to do: create launch materials to showcase Artifacts, and how people can use it. This is where Sam McAllister came in, who leads Brand communications for Claude. After seeing the first prototype of Artifacts, he realized this feature was a truly differentiating UI layer. He’d been using Artifacts as it was built, and put together a demo to showcase the feature: generating an 8-bit game featuring a crab called [“Claw’d:”](https://substack.com/redirect/a257f867-d811-4c91-8168-b18c74bbb4a2?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
First version: When Alex built the early version of Artifacts – one that he showed to a few of his colleagues internally – he used [Streamlit](https://substack.com/redirect/b59ade1d-7f23-4e89-8f6f-6898e8c98816?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). This is a tool to turn Python data scripts into shareable web apps, quickly – to build a prototype for the team.
Using a dedicated prototyping framework to build a “visual proof of concept” turned out to be a helpful approach. It enabled quick feedback, and served as a reminder that the prototype was not (yet) production ready. Of course, not all prototypes become production features, and frameworks that allow research scientists to showcase their ideas are useful, as this case shows.
Second version: Node.js. After getting good feedback, Alex was ready to share the feature with the whole company to try out. For this stage, he decided to migrate the backend from Streamlit. He wanted to use a technology that would work better with more broader usage. Alex explains the reasoning:
“I migrated the app to a Node.js setup and implemented a side-by-side layout for rendering, which I felt improved user experience.
We hold ‘WIP Wednesdays’ meetings at Anthropic, where we share our works in progress with the wider team. Sharing work at a WIP Wednesday like this was a really nice forcing function. I worked late the night before in the office, super focused and just jamming on the prompt and the overall interaction pattern. I paired with Michael too, and he helped me debug what ended up being a simple CORS issue that I was having trouble with. At this point, Claude 3 Opus couldn't actually fix the issue on its own.”
The technology used to build Artifact is a common-enough frontend stack used by many web teams:
[React](https://substack.com/redirect/80d1e78b-fa16-4655-8db7-a5bf2daddfda?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o): frontend framework used to build the interface[Next.js](https://substack.com/redirect/32b70f37-c909-4f95-8ad3-b30211f149ae?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o): a React framework with performance and developer efficiency improvements that many React teams use[Tailwind CSS](https://substack.com/redirect/4ec6aaf0-fcfa-4b2f-b5c8-b132c9cf8cb9?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o): a utility-first CSS framework to design delightful user interfaces
Using sandboxing primitives was a notable difference from how most web apps are built. Artifacts needs to isolate untrusted code in the sandbox; the team calls this approach a “secure playground.” As product engineer Florian Scholz puts it:
“This sandboxing approach gives us a clearly defined environment so we can deploy confidently. It's not a static sandbox, we're constantly pushing and expanding on its capabilities. Having this secure playground was instrumental in enabling us to ship so quickly.”
But how exactly did Anthropic build its sandbox; does it use browser sandboxing primitives like [the Chrome V8 sandbox](https://substack.com/redirect/d77f062b-755d-4715-a3d9-f797822432ad?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)? Security engineer Ziyad Edher reveals details:
“We're not using any actual "sandbox" primitive per se.
We use iFrame sandboxes with full-site process isolation. This approach has gotten robust over the years. This protects users' main Claude.ai browsing session from malicious artifacts. We also use strict Content Security Policies (
[CSPs]) to enforce limited and controlled network access.These approaches protect user data from being exfiltrated through malicious artifacts. We're continuously working on hardening these environments as the browser ecosystem changes.”
Evolution has reduced the need for a more traditional backend, at least for something like Artifacts. Michael says:
“Our models have gotten so capable that a lot of what you'd normally build as backend logic, you can now just ask for! You give Claude the instructions, lay out the parameters, and get back exactly the structured data you need, formatted just the way you want.
A lot of people looking at Artifacts probably assume there's this incredibly complex backend system running the show.
The reality is, a huge chunk of Artifacts is ‘just’ presentational UI. The heavy lifting is happening in the model itself. It's not that traditional backend work disappears entirely, but the balance shifts. I think we're just scratching the surface of what this approach can do. As these models continue to evolve, who knows?”
The team behind Artifacts leaned on Claude heavily to build Artifacts. Here’s how research scientist Alex Tamkin used Claude 3 Opus:
“Claude 3 Opus was, at the time, our most intelligent model. The process was straightforward: I'd describe the UI I wanted for Claude, and it would generate the code. I'd copy this code over and render it. I’d then take a look at what I liked or didn't like, spot any bugs, and just keep repeating that process.
It was a really quick way to iterate on ideas!
When you can see something immediately on the screen, there's this moment where things just ‘click’. That's what I was aiming for with this approach – trying to get to those "a-ha!" moments faster.”
Florian Scholz, product engineer on the Artifact team, used Claude extensively, too. He says:
“Claude proved particularly useful as I went digging into the depths of obscure browser APIs and capabilities. I was using it to figure out how to implement specific interaction patterns, like configuring content security policy options, iFrame interactions, and DOM selection APIs. I used it for lots of areas where documentation can be thin or pretty complicated.
Since the launch of Sonnet and Artifacts, I've been using them to jam on experimental versions of new features and get them up and running. Claude usually gives me a good starting point and I can then pair with Claude and iterate from there. I find these tools helpful to avoid the “blank page” problem.”
Within Anthropic, Sonnet 3.5 was seen as a “game-changer,” and pushed the Artifacts team to be more ambitious. Product designer Michael Wang, shares:
“I'm almost always using Claude in my development process. Claude has become such an integral part of my workflow that I'm honestly not sure what I'd do if I couldn't use it anymore. I use it to scaffold out my code, have ongoing conversations about implementation details, and transform code as needed.
Claude 3.5 Sonnet wasn't ready to test during the initial prototyping phases of Artifacts. So at the time, I was primarily using Claude 3 Opus.
When we got an early peek at 3.5 Sonnet, it was a game-changer. Internally, folks were demoing entire Three.js or WebGL apps created by Sonnet in one shot. That's when I knew we could be a lot more ambitious with what we were building. Sonnet had a huge impact on our feature set in the month leading up to the launch. It really pushed us to expand what we thought was even possible with Artifacts.”
Artifacts is one of the most talked-about releases from Anthropic this year, in software engineering circles, anyway! I asked product design engineer Michael Wang about the team size and timeline, from an idea all the way to production. This is how it played out:
“After Alex’s demo, I started working on the prototype on the main claude.ai repository on March 21 2024.
There was one person working on it full time, another part-time contributing on a regular basis. We had a few other helpful hands contributing at strategic points, and a bunch of other Anthropic employees dogfooding along the way.
The project shipped 3 months after the first demo on June 20. We
[shipped Artifacts]alongside our most capable model yet,[Claude 3.5 Sonnet].The whole project felt kind of like a scrappy operation. But that's how some of the best stuff comes together, right?”
Previously in The Pragmatic Engineer, we covered small teams shipping impactful products – such as [the dozen engineers who shipped Meta’s Threads app in 6 months](https://substack.com/redirect/2463518f-b5b4-4d1b-bac2-1ef3f03b7749?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). Still, Artifacts might be the scrappiest, high-impact product I’ve encountered! Congrats to everyone at Anthropic who helped build it.
Become a paying subscriber of The Pragmatic Engineer to get access to this post and other subscriber-only content.
| Full articles every Tuesday and Thursday | |
| Access to resources and templates for engineering managers and engineers | |
| Access to the complete archive, see all comments and comment on articles |