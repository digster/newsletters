---
subject: "Developer productivity with Dr. Nicole Forsgren (creator of DORA, co-creator of SPACE)"
from: "The Pragmatic Engineer <pragmaticengineer@substack.com>"
to: ""
date: 2025-02-19 17:01:28
labels: ["CATEGORY_PERSONAL", "INBOX", "The Pragmatic Engineer", "UNREAD"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_6413324878686416177", "UNREAD"]
---
|
Available now on [YouTube](https://substack.com/redirect/397e3fbc-82b1-4724-bb42-8d46760fb92b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), [Apple](https://substack.com/redirect/2194e3f8-ab4a-4f90-b200-28f476f1bf2b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) and [Spotify](https://substack.com/redirect/70e8a7c3-fc7e-480b-9d59-da0a9587dce3?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). See the episode transcript at the top of this page, and a summary at the bottom.
• [DX](https://substack.com/redirect/18f3ea72-fb9f-4019-bcff-19828ad7a1b8?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) — An engineering intelligence platform designed by leading researchers.
• [Sentry](https://substack.com/redirect/8b122e06-b1c6-4900-8bf5-74ae4f524e89?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) — Error and performance monitoring for developers.
—
We’ve previously covered a lot on the surprisingly slippery topic of developer productivity: from how [Uber measures it](https://substack.com/redirect/886fb392-9d90-4750-b0bd-77957ac1c663?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), how [LinkedIn does it](https://substack.com/redirect/4e06c460-05b1-448d-a03f-a85f4e6624fe?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), an overview of the [innovative DevEx framework](https://substack.com/redirect/d817a9f6-1cec-4c3c-aef8-622ac3aa488c?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), and a deepdive of dev productivity metrics [used by Google, LinkedIn, Peloton, Amplitude, Intercom, Notion, Postman, and 10 other tech companies](https://substack.com/redirect/d9bb1315-c309-42d2-ad14-c279d322e75b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).
Every time developer productivity comes up: DORA and SPACE are almost certainly mentioned. So I could not be more excited to have Dr. Nicole Forsgren on the podcast. Nicole is the creator of the widely adopted DORA and SPACE frameworks, co-author of the award-winning book Accelerate and the DevOps Handbook (2nd edition), and author of the State of DevOps reports. She is currently a Partner at Microsoft Research, leading developer productivity research and strategy, and is currently working on a book about developer experience with Abi Noda. It’s safe to say that Nicole is one of the foremost experts in developer productivity — if not the foremost expert.
In this episode, we discuss:
Why PRs and Diffs are incomplete as a solo metric and how to view them in context
The importance of a holistic set of metrics for evaluating productivity
An overview of DORA’s four key metrics, its strengths, and its limitations
The evolution of processes and tools since DORA, including SPACE
What developer experience is—and concrete ways to improve it
Common characteristics of highly productive engineering teams
How faster onboarding might challenge Brook’s Law
How AI tooling is impacting developer productivity and best practices for experimentation
And much more!
My biggest takeaways from this episode:
1. Measuring the number of PRs is controversial for a good reason. Measuring any single one “output” can be misused: and when devs know it is being measured, they will optimize for it.
However, measuring PRs is important: but to do it well, don’t look at it as an individual performance metric. Instead, use it to understand how well (or not well) systems across the team and company are working. For example, what systems are getting in the way of PRs taking long to merge?
2. DORA and SPACE both have their own limitations. DORA is very well-defined in the metrics it measures. However, a massive limitation it has is how it only measures from commit to production.
SPACE can be used to measure the complete developer workflow – including e.g. planning, coding, and even post-release. In turn, it is a more vague framework where you need to put in more effort to make it useful for your envirnment.
3. AI developer tools don’t change DevEx fundamentals. DORA and SPACE are still relevant. AI tools might be able to improve iteration speed, or make certain tasks more helpful. It’s really an open question how exactly this will play out. There’s a fair chance these tools significantly change how we do development. So if you’re a dev: experiment with them!
4. Developer experience (DevEx) is not necessarily great at large companies and poor at startups. Google is known to have standout developer experience thanks to so much investment it put into systems – but not all large companies are like this!
Startups have less resources to invest specifically in improving DevEx: but then again, they have less infrastructure in-place! The more custom infrastructure you have, the more painful DevEx tends to be (and the more in-house tools need to be built to mitigate this)
([00:00](https://substack.com/redirect/fc5d76e7-5262-4378-9d54-87b187c042a0?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Intro
([02:03](https://substack.com/redirect/f2fa2cce-ff20-4913-9d2b-cb0934e6a50b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) PRs and Diffs and how to view them in the right context
([07:42](https://substack.com/redirect/d7d792bb-b18e-4291-921e-2c38e801f829?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) EngThrive at Microsoft
([10:26](https://substack.com/redirect/2b4979ce-d4f1-41d2-9aac-0882e892f034?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The importance of having a holistic set of metrics in evaluating productivity
([17:00](https://substack.com/redirect/20dd9e50-fa6e-483c-9dcc-8b19bb2922f9?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The four key metrics of DORA
([23:57](https://substack.com/redirect/e732918a-0f1d-43d6-9d4b-64b72945d081?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The evolution of processes and tools since DORA, including SPACE
([26:40](https://substack.com/redirect/7e533175-6fbc-4fa8-bfd8-2025e66beac1?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) An explanation of developer experience — and ways to improve it
([30:44](https://substack.com/redirect/87e1782f-5a24-4f0d-a2c6-4d16c8357088?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Devex at startups vs. larger companies
([34:20](https://substack.com/redirect/40837874-cbff-4164-ada5-cf32a56f842a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Why measuring developer productivity is so difficult
([39:05](https://substack.com/redirect/4aafa67d-6d54-4d5d-a64b-f7c11c4b56f1?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) How to make a case for platform teams
([44:34](https://substack.com/redirect/b5a43a17-aa3e-4ba5-80ea-068b234a65b1?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Common characteristics of highly productive teams
([51:01](https://substack.com/redirect/9c1e45b6-fa41-43aa-8fa8-552c779afa09?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Brook’s law and how faster onboarding might make it irrelevant
([52:49](https://substack.com/redirect/5f1eb959-edbf-4a6d-b8bf-d3d2724d9df7?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Onboarding for internal transfers
([54:18](https://substack.com/redirect/4da002c9-1066-4be5-bdc1-701636cafdc3?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Shifting culture towards technology first
([58:36](https://substack.com/redirect/667b164b-490c-4f13-b2ba-2139053bca15?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) How middle management can improve engineering culture
([1:03:36](https://substack.com/redirect/05f26b1c-f666-41bc-a66f-67f610c12096?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) How AI tooling is impacting developer productivity
([1:06:42](https://substack.com/redirect/a353cac2-5767-4414-8e02-161630d60d19?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Potential use cases for AI
([1:08:40](https://substack.com/redirect/a8f5cf67-bec4-4c97-8b54-ead8bdb45be2?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) A case for experimenting with AI coding tools and how to maintain flow state
([1:15:30](https://substack.com/redirect/0fbb4f5c-52f3-4f44-92b3-ee1edb59c922?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Rapid fire round
PRs and diffs can be both good and bad signals when measuring developer productivity. Many leaders focus on the traditional economic definition of productivity: the rate of output or output per input.
PRs can give a view into the work being done, but senior engineers may have lower PR output due to other responsibilities like unblocking others, architecture, mentoring, and recruitment. It's important to consider the context and who is being measured.
A constellation of metrics is better than a single metric for a holistic view. So yes: it can be helpful to get data on PRs – as long as you get a lot more other data points as well!
Microsoft's EngThrive: this framework (which Nicole works on) uses multiple metrics across dimensions, inspired by the SPACE framework, alongside qualitative feedback.
Easy-to-operationalise measures can be useful. However, they only show a few things and may ignore important aspects.
SPACE: a framework that groups metrics into:
Satisfaction
Performance
Activity
Communication
Efficiency.
Nicole is a co-author of the framework. It’s one that is getting a lot wider adaptation. See
[an overview of the SPACE framework](https://substack.com/redirect/9e3fdae0-1df8-4c3f-bb31-d10274d92c60?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
Absent engineering leadership is unhelpful. No matter what metrics you use: if engineering leadership is not connected with the work, outcomes are likely to be a lot worse.
Metrics collected in a holistic way, on the other hand, can guide decisions about company-wide blockers.
Nicole is the co-creator of DORA
DORA can refer to the entire research program. More frequently though, people tend to refer to the 4 DORA metrics:
Deployment frequency
Lead time for changes
Change failure rate,
Time to restore service
These 4 metrics are a good indicator of how well a development pipeline is working
DORA can be adapted for different environments, such as air-gapped systems, by redefining the scope of the deployment pipeline.
DORA does not show the full picture. DORA metrics serve as a signal for how well a team is doing, but it does not show the complete picture. DORA focuses on commit to production. This is a part of the engineering process that can be made pretty efficient.
Fast feedback is important, as is the ability to set up environments and provision resources quickly.
SPACE evolved from DORA. SPACE considers the entire end-to-end toolchain. SPACE metrics can be applied to specific components, like PRs. DORA is essentially one of many instances of SPACE.
Developer experience is a developer's lived experience. This can be “good” – it can also be “bad!”
A good developer experience minimises friction, blockers, and confusion
Security and compliance: these are important! However, automation can minimise manual processes for developers. A secure and compliant dev process does not need to be cumbersome.
Delays and cognitive load from inefficient processes negatively affect developer experience.
Both large and small companies can have good or bad developer experiences. Large companies have more resources but may struggle with legacy systems and bureaucracy. Startups can move fast but lack infrastructure. Google has an exceptional developer experience because they invest in it and don't tolerate friction.
Most work in software is invisible, and systems are increasingly complex.
Leaders and executives often don't feel the pain of developers.
To make a case for investment in tooling: use both data and stories. Present the trade-offs realistically.
Acknowledge that there's a tipping point where further investments won't deliver much more progress.
Frame requests in terms of trade-offs and potential for repurposing teams.
High-performing teams:
Exhibit psychological safety, curiosity, and openness to better ways of doing things.
Onboarding time is a great indicator of team efficiency.
A “dummy pull request” early during the onboarding phase (e.g. day 1!) can significantly increase productivity. Try it!
If onboarding is slow: adding people to a late project can backfire. But if onboarding is fast: this can actually work!
Engineering culture transformations:
These require changing the entire company culture, not just the tech culture.
Changing how people do their work can lead to cultural impacts.
Introducing faster tools and ways of working changes people's lived experience.
To improve the engineering culture, summarize observations, seek feedback, and involve others in finding improvements.
Aim for quick wins with visible impact, like hack days to address paper cuts.
DORA and SPACE relevance:
DORA metrics should remain relevant
SPACE is still applicable for assessing satisfaction, performance, activity, communication, and efficiency.
Changes AI is likely to bring:
There’s some chance that AI tools einvent development and software engineering, particularly in IDEs and testing.
Coding assistants: AI-powered ones can improve code readability and unit test success rates
PR reviews: an obvious place for AI to help
Support roles like release engineering and deployment: could be a use case
Experiment with AI!
Experimenting with AI tools and adapt to your workflows.
Assess AI tools to see what works, and focus on problem-solving and architecture.
When you find the workflows where AI is helpful: you might be able to preserve flow better
Turn off autocomplete and autosuggestions if they are an interruption!.
Consider AI as a different way to work, such as "driving and reviewing" or "guiding".
LLMs are changing software engineering rapidly.
Nicole recommends reading:
[Inspired](https://substack.com/redirect/7fa6cdb2-2db7-463b-86d1-3daa17f5a69f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)by Marty Cagan[Outlive](https://substack.com/redirect/2873b029-73d0-415c-8750-bbd51e1c9633?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)by Peter Attia[Ender's Game](https://substack.com/redirect/21c84e39-9347-4671-90e2-a7f8a6457322?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)for some good fiction reading
Where to find Dr. Nicole Forsgren:
• LinkedIn: [https://www.linkedin.com/in/nicolefv/](https://substack.com/redirect/cee3b18e-06c5-40ab-b9a7-c7f2c697c592?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Website: [https://nicolefv.com/](https://substack.com/redirect/91cd1684-d86b-428e-aa9c-710835bb37c2?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
Mentions during the episode:
• Microspeak: Sats: [https://devblogs.microsoft.com/oldnewhttps://newsletter.pragmaticengineer.com/p/developer-productivity-a-new-frameworkthing/20100914-00/?p=12873](https://substack.com/redirect/2ddaee3d-b812-4c80-9e4b-c0e519bdd4c8?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Measuring Software Engineering Productivity: [https://newsletter.pragmaticengineer.com/p/engineering-productivity](https://substack.com/redirect/6c50ba62-de2f-4f0c-8173-e001b1dbc53d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Hawthorne effect: [https://en.wikipedia.org/wiki/Hawthorne_effect](https://substack.com/redirect/47cc7dc6-4d61-46e2-b528-55ff7170c3fa?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Accelerate: The Science of Lean Software and DevOps: Building and Scaling High Performing Technology Organizations: [https://www.amazon.com/Accelerate-Software-Performing-Technology-Organizations/dp/1942788339](https://substack.com/redirect/d40ace69-2d12-4b69-a768-4428b9a667bc?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• What is an Air Gap?: [https://www.ibm.com/think/topics/air-gap](https://substack.com/redirect/4a95ae97-2e0f-40a2-9d3e-f7715a4b672e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• DORA: [https://dora.dev/](https://substack.com/redirect/28126b9f-5c5a-47e7-ab15-ae68d55d1931?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Quantifying the impact of developer experience: [https://developer.microsoft.com/en-us/developer-experience](https://substack.com/redirect/2a18ea9a-cbdd-437b-bcad-a6e4993819e1?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• A new way to measure developer productivity – from the creators of DORA and SPACE: [https://newsletter.pragmaticengineer.com/p/developer-productivity-a-new-framework](https://substack.com/redirect/d817a9f6-1cec-4c3c-aef8-622ac3aa488c?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Ciera Jaspan on LinkedIn: [https://www.linkedin.com/in/ciera/](https://substack.com/redirect/4efac46f-791a-469f-a31f-6e389e46c60d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Emerson Murphy-Hill on LinkedIn: [https://www.linkedin.com/in/captainemerson/](https://substack.com/redirect/f3bb4ceb-bee1-414e-9d90-cbe8e52314d3?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Inside Stripe’s Engineering Culture - Part 1: [https://newsletter.pragmaticengineer.com/p/stripe](https://substack.com/redirect/fc1ebeca-5cdf-4f74-839a-1ee9e3debebc?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Inside Stripe’s Engineering Culture: Part 2: [https://newsletter.pragmaticengineer.com/p/stripe-part-2](https://substack.com/redirect/1fa8a456-0c69-4085-9d9b-3c6a352330df?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• David Singleton on LinkedIn: [https://www.linkedin.com/in/davidpsingleton/](https://substack.com/redirect/190ec8ce-7ab1-4978-b3f9-1e7dc021820e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Courtney Kissler on LinkedIn: [https://www.linkedin.com/in/courtney-kissler/](https://substack.com/redirect/7138659b-006c-4864-a735-2be03d9b1cc7?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Brian Houck on LinkedIn: [https://www.linkedin.com/in/brianhouck/](https://substack.com/redirect/31757efe-7176-47b9-aaf9-b6ba1bba4ce6?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Brook’s law: [https://en.wikipedia.org/wiki/Brooks%27s_law](https://substack.com/redirect/b7b364b9-d533-4938-b77b-7aafb9ab82b2?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Satya Nadella on LinkedIn: [https://www.linkedin.com/in/satyanadella/](https://substack.com/redirect/519c96b3-ff56-4cf5-9272-33fc79045780?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Steve Ballmer on LinkedIn: [https://www.linkedin.com/in/steve-ballmer-7087a8157/](https://substack.com/redirect/70e82dba-6962-4c8e-b5bd-2016afdfa4f2?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• John Shook: [https://www.lean.org/about-lei/senior-advisors-staff/john-shook/](https://substack.com/redirect/145ba8ec-3814-47d2-80b5-fcea9815b304?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Does GitHub Copilot improve code quality? Here’s what the data says: [https://github.blog/news-insights/research/does-github-copilot-improve-code-quality-heres-what-the-data-says/](https://substack.com/redirect/f3809f9b-b8f0-46f3-a4e7-d40fbb074d3b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• [Two developers built a game that sold 1M copies. How?](https://substack.com/redirect/7d2c10e2-6a00-47ef-9780-06f8d91261f8?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Reading Between the Lines: Modeling User Behavior and Costs in AI-Assisted Programming: [https://www.microsoft.com/en-us/research/publication/reading-between-the-lines-modeling-user-behavior-and-costs-in-ai-assisted-programming/](https://substack.com/redirect/35bb9ec5-1a6b-4b3f-a5d4-0c644ebca27a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Abi Noda on LinkedIn: [https://www.linkedin.com/in/abinoda/](https://substack.com/redirect/95595ce7-1c6d-44f5-877e-7ee34263af22?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Jason Entenmann on LinkedIn: [https://www.linkedin.com/in/jason-entenmann-06146875/](https://substack.com/redirect/625de493-901b-46fb-9fff-3a1c5142208b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Claude: [https://claude.ai/new](https://substack.com/redirect/711029b6-8bb3-4a17-a48e-aae85dc0912f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Anthropic: [https://www.anthropic.com/](https://substack.com/redirect/e0fa7db4-b55a-4a9e-a846-3ac83bf40c5f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• OpenAI: [https://openai.com/](https://substack.com/redirect/bd15f373-2d58-4cab-a015-bd3dd24caafd?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Sonnet: [https://www.anthropic.com/news/claude-3-5-sonnet](https://substack.com/redirect/5942fbea-f122-4e46-8365-622201270e9c?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Inspired: How to Create Tech Products Customers Love: [https://www.amazon.com/INSPIRED-Create-Tech-Products-Customers/dp/1119387507](https://substack.com/redirect/807c0a9b-fd96-4df6-af0d-801977c8e5dc?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Outlive: The Science and Art of Longevity: [https://www.amazon.com/Outlive-Longevity-Peter-Attia-MD/dp/0593236599/r](https://substack.com/redirect/7c05e5a9-a556-4535-99e3-15015f54dc33?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Ender’s Game: [https://www.amazon.com/Enders-Game-Ender-Quintet-1/dp/1250773024](https://substack.com/redirect/21c84e39-9347-4671-90e2-a7f8a6457322?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Tressie McMillan Cotton’s website: [https://tressiemc.com/](https://substack.com/redirect/86cc2757-0929-4748-a36f-f2fe46e3612e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Anne Helen Petersen’s newsletter: [https://substack.com/@annehelen](https://substack.com/@annehelen)
• Can You Really Measure Individual Developer Productivity? - Ask the EM: [https://blog.pragmaticengineer.com/can-you-measure-developer-productivity/](https://substack.com/redirect/2fa67377-2739-4470-9f52-356d268f9a28?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Measuring Developer Productivity: Real-World Examples: [https://newsletter.pragmaticengineer.com/p/measuring-developer-productivity-bae](https://substack.com/redirect/d9bb1315-c309-42d2-ad14-c279d322e75b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Measuring developer productivity? A response to McKinsey: [https://newsletter.pragmaticengineer.com/p/measuring-developer-productivity](https://substack.com/redirect/2ce938be-2ab7-4b42-8805-f5615d931ab6?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Measuring developer productivity? A response to McKinsey, Part 2: [https://newsletter.pragmaticengineer.com/p/measuring-developer-productivity-part-2](https://substack.com/redirect/e9f797b4-17a7-4a18-99de-59a6c231506e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• The Full Circle on Developer Productivity with Steve Yegge: [https://newsletter.pragmaticengineer.com/p/steve-yegge](https://substack.com/redirect/46795a3d-7151-425d-ad27-4a6c981ba243?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Measuring Software Engineering Productivity: [https://newsletter.pragmaticengineer.com/p/engineering-productivity](https://substack.com/redirect/6c50ba62-de2f-4f0c-8173-e001b1dbc53d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Platform Teams and Developer Productivity with Adam Rogal, Dir. Developer Platform at DoorDash: [https://newsletter.pragmaticengineer.com/p/platform-teams-with-adam-rogal](https://substack.com/redirect/34b62e51-94dd-4eda-9e68-6d95b1d0a405?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
—
Production and marketing by [Pen Name](https://substack.com/redirect/8d88190d-7228-4978-bd5f-537d1724bb93?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). For inquiries about sponsoring the podcast, email podcast@pragmaticengineer.com.
You’re on the free list for [The Pragmatic Engineer](https://substack.com/redirect/2/eyJlIjoiaHR0cHM6Ly9uZXdzbGV0dGVyLnByYWdtYXRpY2VuZ2luZWVyLmNvbT91dG1fY2FtcGFpZ249ZW1haWwtaG9tZSZyPThvNTRuIiwicCI6MTU3MjEyNDMwLCJzIjo0NTg3MDksImYiOnRydWUsInUiOjE0NTYzMzE5LCJpYXQiOjE3Mzk5ODQ2NjQsImV4cCI6MTc0MjU3NjY2NCwiaXNzIjoicHViLTAiLCJzdWIiOiJsaW5rLXJlZGlyZWN0In0.MkjZdSXQ17-hTsQtNvr7F68VHl_3UJZZC7rkcBzYsRs?). For the full experience, [become a paying subscriber](https://substack.com/redirect/2/eyJlIjoiaHR0cHM6Ly9uZXdzbGV0dGVyLnByYWdtYXRpY2VuZ2luZWVyLmNvbS9zdWJzY3JpYmU_dXRtX3NvdXJjZT1wb3N0JnV0bV9jYW1wYWlnbj1lbWFpbC1jaGVja291dCZuZXh0PWh0dHBzJTNBJTJGJTJGbmV3c2xldHRlci5wcmFnbWF0aWNlbmdpbmVlci5jb20lMkZwJTJGZGV2ZWxvcGVyLXByb2R1Y3Rpdml0eS13aXRoLWRyLW5pY29sZSZyPThvNTRuJnRva2VuPWV5SjFjMlZ5WDJsa0lqb3hORFUyTXpNeE9Td2lhV0YwSWpveE56TTVPVGcwTmpZMExDSmxlSEFpT2pFM05ESTFOelkyTmpRc0ltbHpjeUk2SW5CMVlpMDBOVGczTURraUxDSnpkV0lpT2lKamFHVmphMjkxZENKOS5DMl82OFVsZFpvdS1hRUd3ZldaUUhIRThRWjd5TlBEeVdodUotVy1KQ3Q4IiwicCI6MTU3MjEyNDMwLCJzIjo0NTg3MDksImYiOnRydWUsInUiOjE0NTYzMzE5LCJpYXQiOjE3Mzk5ODQ2NjQsImV4cCI6MTc0MjU3NjY2NCwiaXNzIjoicHViLTAiLCJzdWIiOiJsaW5rLXJlZGlyZWN0In0.x1XqjEu-Hyxy-XFDJeOjd85e1DfrBvutUVgfSvLuIDU?). Many readers expense this newsletter within their company’s training/learning/development budget.
This post is public, so feel free to share and forward it.
If you enjoyed this post, you might enjoy my book, [The Software Engineer's Guidebook](https://substack.com/redirect/980f65a4-3279-4fa8-a2fc-4891812b3f37?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). Here is what Tanya Reilly, senior principal engineer and author of The Staff Engineer's Path said about it:
"From performance reviews to P95 latency, from team dynamics to testing, Gergely demystifies all aspects of a software career. This book is well named: it really does feel like the missing guidebook for the whole industry."