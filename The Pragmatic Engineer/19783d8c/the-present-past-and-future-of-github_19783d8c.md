---
subject: "The present, past and future of GitHub"
from: "The Pragmatic Engineer <pragmaticengineer@substack.com>"
to: ""
date: 2025-06-18 16:21:06
labels: ["CATEGORY_PERSONAL", "INBOX", "The Pragmatic Engineer", "UNREAD"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_6413324878686416177", "UNREAD"]
---
|
Listen and watch now on [YouTube](https://substack.com/redirect/292ad8cd-4522-40d0-8cfa-d8be7182bc80?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), [Spotify](https://substack.com/redirect/49693abb-e80a-49b2-8af7-c52a5ae46c5e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) and [Apple](https://substack.com/redirect/1aa1ab69-3cbd-4a0d-a37f-29a7d824f073?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). See the episode transcript at the top of this page, and timestamps for the episode at the bottom.
[Statsig](https://substack.com/redirect/a511a1ba-4864-45a3-8066-15602c4f8695?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)[](https://substack.com/redirect/933e979b-b2af-4f11-bbbb-88f0f57d40c2?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)—[](https://substack.com/redirect/933e979b-b2af-4f11-bbbb-88f0f57d40c2?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)The unified platform for flags, analytics, experiments, and more.[Graphite](https://substack.com/redirect/e529e93f-0a2f-45db-acc0-42aab2a2d877?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)— The AI developer productivity platform.[Augment Code](https://substack.com/redirect/68688633-c1a5-4785-8c3e-ce14f2f2f001?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)— AI coding assistant that pro engineering teams love.
—
GitHub recently turned 17 years old—but how did it start, how has it evolved, and what does the future look like as AI changes how developers work?
In this episode of The Pragmatic Engineer, I’m joined by [Thomas Dohmke](https://substack.com/redirect/8f1bf53e-9c73-4aa7-b376-62e5aa17990b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), CEO of GitHub. Thomas has been a GitHub user for 16 years and an employee for 7. We talk about GitHub’s early architecture, its remote-first operating model, and how the company is navigating AI—from Copilot to agents. We also discuss why GitHub hires junior engineers, how the company handled product-market fit early on, and why being a beloved tool can make shipping harder at times.
Other topics we discuss include:
How GitHub’s architecture evolved beyond its original Rails monolith
How GitHub runs as a remote-first company—and why they rarely use email
GitHub’s rigorous approach to security
Why GitHub hires more junior engineers than ever before
How Microsoft acquired GitHub
The launch of Copilot and how it’s reshaping software development
Why GitHub sees AI agents as tools, not a replacement for engineers
And much more!
An interesting quote from the episode is how and when GitHub started to build Copilot — during the pandemic, after getting access to GPT-3. And how it all started with [a published paper](https://substack.com/redirect/b40a3b79-c975-4418-a1fe-2fc9e9ef1b98?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o):
Thomas (at
[01:07:03]): So GPT-3 came out right after the BUILD conference in 2020, which was obviously given the pandemic fully remote. But Kevin Scott and Sam Altman did a session about transformers and large language models. And then, after that, GPT-3 got into the preview, and we got access to that through the OpenAI/Microsoft partnership.We realized with OpenAI that GPT-3 was able to write decent code in different programming languages and would not mix up the syntax between Python, Ruby, and JavaScript. Then, OpenAI finetuned a model that was called Codex that was specific for these coding scenarios.
In 2020 and August
[we wrote a paper]with three ideas. We had:
Text to code
Code to text as in describing code
Conversational coding which today is known as Chat.
And those two latter scenarios didn't work well enough. But text to code — as in prompting the model within the editor — ultimately turned into auto completion. That worked so well that quickly we saw our internal Hubbers, adopting the tool, giving it really high scores saying "this is great, I want to keep using this."
It was not the typical “management says you have to use it” and you don't want to. In the early days, it wrote about 25% of the code in the fileswhere it was enabled. Shortly thereafter, that number got to about 46% in early 2023. That was the early days of copilot.
In June, 2021, we went into the public preview and within a few months it had gone to one million users. We saw more and more folks on social media saying "well, I was skeptical that this could ever work, but it actually is good enough that I don't want to work without it anymore.”
We go into several more, previously unshared stories on the evolution of GitHub.
([00:00](https://substack.com/redirect/338f8797-bf9e-47df-90f3-71752ff00b72?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Intro
([02:25](https://substack.com/redirect/5c400c89-26a9-4d5c-a3fa-fe9f80ed74e3?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) GitHub’s modern tech stack
([08:11](https://substack.com/redirect/c20bb663-0e1a-458e-a720-0c0cf89b12a5?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) From cloud-first to hybrid: How GitHub handles infrastructure
([13:08](https://substack.com/redirect/ca3b8248-3178-4f02-969a-557494e97dd1?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) How GitHub’s remote-first culture shapes its operations
([18:00](https://substack.com/redirect/168260f7-bde6-499c-bc93-116ecc19d3b7?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Former and current internal tools including Haystack
([21:12](https://substack.com/redirect/2f3f9767-485c-45a4-85ae-f906220c454e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) GitHub’s approach to security
([24:30](https://substack.com/redirect/84685b0b-d9b3-49cb-be14-49208d5aaabe?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The current size of GitHub, including security and engineering teams
([25:03](https://substack.com/redirect/ba63fb00-4024-4504-b738-4b4bfc4916ba?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) GitHub’s intern program, and why they are hiring junior engineers
([28:27](https://substack.com/redirect/ea40dbdc-c830-42f8-9d30-723531e63475?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Why AI isn’t a replacement for junior engineers
([34:40](https://substack.com/redirect/70e6d7f7-228f-4ed3-b068-2b49e5e8b95d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) A mini-history of GitHub
([39:10](https://substack.com/redirect/0f1297ac-d453-459a-b112-fe33074e65ef?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Why GitHub hit product market fit so quickly
([43:44](https://substack.com/redirect/7f0d219b-68fc-4bce-a328-aef7bdf06394?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The invention of pull requests
([44:50](https://substack.com/redirect/37535a90-9060-40d2-97ff-a8b0bc58f753?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) How GitHub enables offline work
([46:21](https://substack.com/redirect/0ae42371-b15e-4620-90c6-c59e56345732?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) How monetization has changed at GitHub since the acquisition
([48:00](https://substack.com/redirect/866ec854-bbf8-4625-99e1-00516b23588c?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) 2014 desktop application releases
([52:10](https://substack.com/redirect/5626d0d2-828c-4874-b598-218a4ff310bf?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The Microsoft acquisition
([1:01:57](https://substack.com/redirect/a7808386-1518-4c99-b42c-177f9a8b81f4?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Behind the scenes of GitHub’s quiet period
([1:06:42](https://substack.com/redirect/035d8348-41ab-4120-8626-889be146ca73?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The release of Copilot and its impact
([1:14:14](https://substack.com/redirect/3943e657-1bac-4af8-88aa-2198cdf4623a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Why GitHub decided to open-source Copilot extensions
([1:20:01](https://substack.com/redirect/b7b7f733-a801-43d8-ab90-807a03d9679b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) AI agents and the myth of disappearing engineering jobs
([1:26:36](https://substack.com/redirect/57e657ae-4b02-47d4-96e4-64504b5b3fa3?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Closing
Where to find Thomas Dohmke:
• X: [https://x.com/ashtom](https://substack.com/redirect/e977afc4-2953-4942-b9cd-62f7f42b0870?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• LinkedIn: [https://www.linkedin.com/in/ashtom/](https://substack.com/redirect/8f1bf53e-9c73-4aa7-b376-62e5aa17990b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• GitHub: [https://github.com/ashtom](https://substack.com/redirect/8cdacd08-d592-4b95-9415-7cf03a94591f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
Mentions during the episode:
• Ruby on Rails: [https://rubyonrails.org/](https://substack.com/redirect/0c8757f4-3080-4ca6-8e47-3f212c375b83?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• React: [https://react.dev/](https://substack.com/redirect/4df29f74-db4b-4709-a0d0-3f5862ae1938?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Go: [https://go.dev/](https://substack.com/redirect/3c724f4d-3399-4518-a541-5f413178f592?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Swift: [https://www.swift.org/](https://substack.com/redirect/768c3796-6a0b-4c09-af41-9759ee0237c1?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• .NET: [https://code.visualstudio.com/docs/languages/dotnet](https://substack.com/redirect/4e03e4b4-9c6a-4c0b-bd42-efc59dc418a7?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Chris Wanstrath on LinkedIn: [https://www.linkedin.com/in/defunkt/](https://substack.com/redirect/bde6aff6-146d-4e73-9da9-a7a539b8a16f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• PJ Hyett on Instagram: [https://www.instagram.com/pjhyett/](https://substack.com/redirect/4a3d4ff1-5767-4b7e-a74f-0778e6ca3473?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Tom Preston-Werner on LinkedIn: [https://www.linkedin.com/in/mojombo/](https://substack.com/redirect/9d76559c-5307-4522-a44d-d469277e01f6?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Scott Chacon on LinkedIn: [https://www.linkedin.com/in/schacon/](https://substack.com/redirect/737fce06-5506-4115-9438-d9df2612b3d6?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• GitButler: [https://gitbutler.com/](https://substack.com/redirect/03d81a05-b516-4fa8-84e8-335d0f904497?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Working at Amazon as a software engineer – with Dave Anderson: [https://newsletter.pragmaticengineer.com/p/working-at-amazon-as-a-software-engineer](https://substack.com/redirect/d02040e1-1de1-47c2-b87e-20ec1a38717d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Azure: [https://azure.microsoft.com/](https://substack.com/redirect/5ce462c4-9d3f-4402-a4ff-212999673853?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• MYSQL: [https://www.mysql.com/](https://substack.com/redirect/55511dd5-0045-41e9-953e-704783731bb6?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Acquired | GitHub | Season 2, Episode 9: [https://www.acquired.fm/episodes/season-2-episode-9github](https://substack.com/redirect/27a4fae7-b954-40c9-9fe0-2a9e9cc881ca?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Loom: [https://www.loom.com/](https://substack.com/redirect/c21f39a1-ee36-479e-bffa-ab8f91638765?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Sentry: [https://sentry.io/](https://substack.com/redirect/78b3cedd-55fa-4806-b444-10a5fb86a8c2?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Zendesk: [https://www.zendesk.com/](https://substack.com/redirect/c5ccd275-2d2d-48cf-a778-5ede30a33c63?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Atom: [https://atom-editor.cc/](https://substack.com/redirect/33815d48-c511-4d8e-b206-dc59ce6b5e88?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Heroku’s April 2022 Incident Review: [https://www.heroku.com/blog/april-2022-incident-review/](https://substack.com/redirect/9f3579a0-ef90-407e-8d30-31241caaf07d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Mike Hanley on LinkedIn: [https://www.linkedin.com/in/michaelphanley/](https://substack.com/redirect/f0834a88-65a1-4116-ba88-29e75c2d4587?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• GitHub Security Lab: [https://securitylab.github.com/](https://substack.com/redirect/43a762a8-eb25-4df7-a76e-d25eec5ebd8d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• CodeQL: [https://codeql.github.com/](https://substack.com/redirect/c2527120-147a-42ef-aadc-653dd731fc31?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• How Linux is built with Greg Kroah-Hartman: [https://newsletter.pragmaticengineer.com/p/how-linux-is-built-with-greg-kroah](https://substack.com/redirect/7636f812-8177-4fc7-92ff-e5e9d4b50e57?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Two decades of Git: A conversation with creator Linus Torvalds:
• SourceForge: [https://en.wikipedia.org/wiki/SourceForge](https://substack.com/redirect/bc5681dd-7f18-4ab0-adf6-4e923e3fc517?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• The Octocat: [https://github.com/octocat](https://substack.com/redirect/97828a9a-9544-42ff-8475-559f82c49fe7?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Bosch: [https://www.bosch.com/](https://substack.com/redirect/36dc00a3-3f65-482b-a6ed-ed440ca59388?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• RailsConf 09: Chris Wanstrath, "How to become a famous Rails Developer, Ruby Rockstar or Code Ninja":
• Mercurial: [https://www.mercurial-scm.org/](https://substack.com/redirect/28804be8-58ac-44f6-8b8e-959517a177af?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• About pull requests: [https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests](https://substack.com/redirect/cea0978f-26ca-4aa9-ad8a-d9cab3562a05?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Oh yeah, there’s pull requests now: [https://github.blog/news-insights/the-library/oh-yeah-there-s-pull-requests-now/](https://substack.com/redirect/ddbad023-79ce-47a8-8a49-6a1526b0cd3a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• VS Code: [https://code.visualstudio.com/](https://substack.com/redirect/3de66810-2f0a-4bf1-8517-8dd9599e614e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Nat Friedman on X: [https://x.com/natfriedman](https://substack.com/redirect/353708e4-f133-49f8-ba5b-ea7efcb076b8?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Satya Nadella on LinkedIn: [https://www.linkedin.com/in/satyanadella/](https://substack.com/redirect/e9829d16-2944-4ffc-a917-7027e8bba04c?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• 50 Years of Microsoft and Developer Tools with Scott Guthrie: [https://newsletter.pragmaticengineer.com/p/50-years-of-microsoft](https://substack.com/redirect/282512e7-4358-439e-93d7-973f193ce9d3?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Jetbrains: [https://www.jetbrains.com/](https://substack.com/redirect/4052925b-1a7e-4fd6-8de6-e1d9c803dfea?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• JFrog: [https://jfrog.com/](https://substack.com/redirect/fbb58f3f-f17e-4806-a311-f7d78bdc8d5e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Kevin Scott on LinkedIn: [https://www.linkedin.com/in/jkevinscott/](https://substack.com/redirect/17752bec-932d-4bcf-8b87-83ee0f91e5da?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Codex: [https://openai.com/index/introducing-codex/](https://substack.com/redirect/b43cc1ff-1380-44fb-a287-558f5a4ecfdf?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Research: quantifying GitHub Copilot’s impact on developer productivity and happiness: [https://github.blog/news-insights/research/research-quantifying-github-copilots-impact-on-developer-productivity-and-happiness/](https://substack.com/redirect/30a27935-c9b7-4d68-a5fa-69f64a0be34f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Universe 2023: Copilot transforms GitHub into the AI-powered developer platform: [https://github.blog/news-insights/product-news/universe-2023-copilot-transforms-github-into-the-ai-powered-developer-platform/](https://substack.com/redirect/b161ce25-0738-4d27-b83a-e26e3211cd31?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Copilot Extensions: [https://github.com/copilot-extensions](https://substack.com/redirect/b3e4b042-41fe-4ea3-a224-bb7d9af451a4?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Xcode: [https://developer.apple.com/xcode/](https://substack.com/redirect/500ff222-1ca4-484f-9dcf-57bd7c26e26f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Jessica Deen on X: [https://x.com/jldeen](https://substack.com/redirect/74f3b3d1-1ac7-4a28-98b8-25f92c2c6f67?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
—
Production and marketing by [Pen Name](https://substack.com/redirect/6f071bb9-6cb6-4f9f-a4e5-e64e199670c2?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).
You’re on the free list for [The Pragmatic Engineer](https://substack.com/redirect/2/eyJlIjoiaHR0cHM6Ly9uZXdzbGV0dGVyLnByYWdtYXRpY2VuZ2luZWVyLmNvbT91dG1fY2FtcGFpZ249ZW1haWwtaG9tZSZyPThvNTRuIiwicCI6MTY2MDkzNDQ5LCJzIjo0NTg3MDksImYiOnRydWUsInUiOjE0NTYzMzE5LCJpYXQiOjE3NTAyNjM3MDksImV4cCI6MTc1Mjg1NTcwOSwiaXNzIjoicHViLTAiLCJzdWIiOiJsaW5rLXJlZGlyZWN0In0.4zUt-QyIZkA-NjijV2fGGhECKNC4EedAYWhj8SEHhLY?). For the full experience, [become a paying subscriber](https://substack.com/redirect/2/eyJlIjoiaHR0cHM6Ly9uZXdzbGV0dGVyLnByYWdtYXRpY2VuZ2luZWVyLmNvbS9zdWJzY3JpYmU_dXRtX3NvdXJjZT1wb3N0JnV0bV9jYW1wYWlnbj1lbWFpbC1jaGVja291dCZuZXh0PWh0dHBzJTNBJTJGJTJGbmV3c2xldHRlci5wcmFnbWF0aWNlbmdpbmVlci5jb20lMkZwJTJGZ2l0aHViJnI9OG81NG4mdG9rZW49ZXlKMWMyVnlYMmxrSWpveE5EVTJNek14T1N3aWFXRjBJam94TnpVd01qWXpOekE1TENKbGVIQWlPakUzTlRJNE5UVTNNRGtzSW1semN5STZJbkIxWWkwME5UZzNNRGtpTENKemRXSWlPaUpqYUdWamEyOTFkQ0o5Lk1YYlF1cjM0bnhzT00tS1RXcUtlZHFWMUxMLU1SNW1qUnZFcDB2LVF3aEUiLCJwIjoxNjYwOTM0NDksInMiOjQ1ODcwOSwiZiI6dHJ1ZSwidSI6MTQ1NjMzMTksImlhdCI6MTc1MDI2MzcwOSwiZXhwIjoxNzUyODU1NzA5LCJpc3MiOiJwdWItMCIsInN1YiI6ImxpbmstcmVkaXJlY3QifQ.Ekbu_UMg5YWZrnsUIRHiGjgcYMFykkYDcsVWdJgViXU?). Many readers expense this newsletter within their company’s training/learning/development budget. If you have such a budget, here’s[ an email you could send to your manager](https://substack.com/redirect/26a618a6-2ea5-4d2e-939f-23dd80b0f659?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).
This post is public, so feel free to share and forward it.
If you enjoyed this post, you might enjoy my book, [The Software Engineer's Guidebook](https://substack.com/redirect/6689ed9e-95fd-4a91-9431-232f73d23eee?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). Here is what Tanya Reilly, senior principal engineer and author of The Staff Engineer's Path said about it:
"From performance reviews to P95 latency, from team dynamics to testing, Gergely demystifies all aspects of a software career. This book is well named: it really does feel like the missing guidebook for the whole industry."