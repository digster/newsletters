---
subject: "Developer Experience at Uber with Gautam Korlam"
from: "The Pragmatic Engineer <pragmaticengineer@substack.com>"
to: ""
date: 2025-03-12 15:57:07
labels: ["CATEGORY_PERSONAL", "INBOX", "The Pragmatic Engineer", "UNREAD"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_6413324878686416177", "UNREAD"]
---
|
Listen and watch now on [YouTube](https://substack.com/redirect/b68b3a27-6db8-4875-a6b9-47246bcf901e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), [Spotify](https://substack.com/redirect/8e5f993b-ba5e-4fdd-ade3-feec9d8b569e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) and [Apple](https://substack.com/redirect/f19b6c02-9101-4bc0-b01e-963b0b119d50?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) . See the episode transcript at the top of this page, and a summary at the bottom.
[Sentry](https://substack.com/redirect/53149849-2f5a-4bee-bcea-aa7ea419b76b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)— Error and performance monitoring for developers.[The Software Engineer’s Guidebook](https://substack.com/redirect/a2fd73ce-04e4-4fe5-b0ff-fe9cb7880a94?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o): Written by me (Gergely) – now out in audio form as well.
—
In today’s episode of The Pragmatic Engineer, I am joined by former Uber colleague, [Gautam Korlam](https://substack.com/redirect/8932d5ff-4618-4786-8653-818c5be44cba?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). Gautam is the Co-Founder of [Gitar](https://substack.com/redirect/7a462652-6d62-481c-b830-446f17e5ac39?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), an agentic AI startup that automates code maintenance. Gautam was mobile engineer no. 9 at Uber and founding engineer for the mobile platform team – and so he learned a few things about scaling up engineering teams.
We talk about:
• How Gautam accidentally deleted Uber’s Java monorepo – really!
• Uber's unique engineering stack and why custom solutions like SubmitQueue were built in-house
• Monorepo: the benefits and downsides of this approach
• From Engineer II to Principal Engineer at Uber: Gautam’s career trajectory
• Practical strategies for building trust and gaining social capital
• How the platform team at Uber operated with a product-focused mindset
• Vibe coding: why it helps with quick prototyping
• How AI tools are changing developer experience and productivity
• Important skills for devs to pick up to remain valuable as AI tools spread
• And more!
Interesting parts of the conversation:
1. Submit Queue: Uber bult a complex merge system to dela with the large number of commits, where each commit had to run long-running CI tests. It’s a problem that smaller and mid-sized companies don’t have, but Uber had: and so they scratched their own itch.
2. Local Developer Analytics (LDA): years ago, Uber started to measure the experience that devs had. Like how long did a build take, locally? How much CPU is used? They used this data to improve internal tooling.
3. Developer experience as a product team. Gautam’s team operated like a classic product team: except their customers were Uber’s internal developers. Gautam believes this is how all successful platform teams should work.
4. AI changing software development: this is happening. “Vibe coding” leads to faster prototyping. Gautam believes junior engineers will thrive with AI tools because they will hit the ground running faster, and will be free of biases that hold back more experienced developers.
([00:00](https://substack.com/redirect/d15c3e2e-368b-4623-bb75-f9d9e9adebac?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Intro
([02:11](https://substack.com/redirect/80da59ef-3f4d-49fa-97f2-4445143a60ae?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) How Gautam accidentally deleted Uber’s Java Monorepo
([05:40](https://substack.com/redirect/a8f89d4d-5dbe-4415-9ba2-6ed930943bf3?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The impact of Gautam’s mistake
([06:35](https://substack.com/redirect/c8b58ebd-a436-42aa-b0d4-a82a62bb977c?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Uber’s unique engineering stack
([10:15](https://substack.com/redirect/1e813581-87ca-45e0-9390-66bdb9ee564e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Uber’s SubmitQueue
([12:44](https://substack.com/redirect/2b6c6390-2cab-4119-b506-63a0dc368c36?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Why Uber moved to a monorepo
([16:30](https://substack.com/redirect/5d1505c3-6b51-4bdc-ad09-486cdf69f285?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The downsides of a monorepo
([18:35](https://substack.com/redirect/3f18b9a1-4129-491a-8f08-561345c0699a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Measurement products built in-house
([20:20](https://substack.com/redirect/060182ae-ba84-4ff0-b376-fac8797cc19e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Measuring developer productivity and happiness
([22:52](https://substack.com/redirect/8039abb6-e07f-49e8-a575-1bf10466c26b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) How Devpods improved developer productivity
([27:37](https://substack.com/redirect/d4d70fba-8ea1-48ea-a5aa-75588363c443?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The challenges with cloud development environments
([29:10](https://substack.com/redirect/75ffbe54-953e-4120-91d2-ace03ec7d27b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Gautam’s journey from Eng II to Principal Engineer
([32:00](https://substack.com/redirect/fdb5c64e-9825-40d0-bd2e-6a5984b6176b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Building trust and gaining social capital
([36:17](https://substack.com/redirect/e26cd902-8196-4d51-86fd-cb3d9c191bf8?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) An explanation of Principal Engineer at Uber—and the archetypes at Uber
([45:07](https://substack.com/redirect/ac30413b-323b-43ce-96af-1159a2948d96?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The platform and program split at Uber
([48:15](https://substack.com/redirect/2f698e52-9087-4215-80c5-dfb8e577cf8c?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) How Gautam and his team supported their internal users
([52:50](https://substack.com/redirect/2ea1016f-20c7-445a-b808-0e4f1cf43ce9?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Gautam’s thoughts on developer productivity
([59:10](https://substack.com/redirect/5c3c93d9-5290-4431-836e-cc2eb8d3a3d7?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) How AI enhances productivity, its limitations, and the rise of agentic AI
([1:04:00](https://substack.com/redirect/cadfcbad-9042-4e3f-afc0-17727f99e0b1?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) An explanation of Vibe coding
([1:07:34](https://substack.com/redirect/a6431e2c-3750-4c6b-a9a6-c9840d22b58e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) An overview of Gitar and all it can help developers with
([1:10:44](https://substack.com/redirect/94a4475e-2aba-4aa8-b011-759c16591419?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Top skills to cultivate to add value and stay relevant
([1:17:00](https://substack.com/redirect/fa49aaf4-3e44-44da-86f6-b20ae760b0de?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Rapid fire round
Gautam joined Uber in 2014 as an Android engineer. Back then, there were not even unit tests. Gautam wrote the first Android test, and set up Artifactory.
Uber built much of its engineering stack in-house because the cloud-native SaaS products were not built for their scale.
Even in the earlier years, Uber saw about one commit every minute – and the platforms at the time could not handle this (especially when considering that CI took 10-30 minutes to run!)
Build time was a problem. During the iOS and Android app rewrite in 2016, build times became very long. Gautam worked on getting it under control.
Submit Queue was a way to guarantee a green main. It serialised incoming commits to ensure they played nicely together. The company
[published a paper](https://substack.com/redirect/4cf10e5e-4ce8-4c64-8209-91246a67bc81?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)on this novel solution. Submit Queue tested changes and considered cross-dependencies between different commits. Machine learning models estimated potential failures and speculatively tried paths that might be green.
Monorepo: after starting as polyrepos, Uber moved to monorepos
Uber started with separate repos for Rider, Driver, and other apps (eg Eats). As the company grew, each team wanted its own repository, resulting in hundreds of repos. It became painful to upgrade and bump libraries.
The iOS team moved to a monorepo, followed by Android. The gains in productivity were massive because there was no need to bump libraries. This move really helped with standardisation.
The biggest initial pushback was that teams could no longer break an API without worrying about the consequences. There was concern about slower builds. In the end, the dev platform team solved for these concerns.
Local Developer Analytics (LDA): an internal Uber system that ran on developers' machines and collected information about their systems. It integrated deeply into CLI tools and IDEs, tracked which files developers accessed most, and identified files with the most bugs. LDA helped identify bottlenecks in the development funnel.
Developer surveys: Uber ran this regularly. The dev tooling NPSwent from negative 50 to positive 8 during Gautam’s tenure.
Things that made for a better developer experience: minimizing time to review code, time to build code, and reducing time spent in meetings.
DevPods: another internal Uber tool. These are basically cloud developer environments. They contain a container of code, build system artefacts and IDE indices in the cloud. DevPods make context switching quick.
Previously, onboarding involved running a bootstrapping script. The script was hard to maintain. Dev Pods moved the development stuff into a container. The containers can be huge.
Going deep: getting into a niche and going deep can help over the long term, especially in areas others may not want to do.
Intropsect regularly: every two years Gautam did some introspection to see if he was doing what he wanted and what could challenge him more.
Social capital and mentorship: these become very important at a big company. It helps to have connections.Helping people builds social capital. Gautam would drop everything to help people with their dev environment problems. He also held office hours on a regular basis, offering to help anyone who showed up.
Understand the business: Principal engineers need to understanding how engineering meets business, rather than just pure coding. It helps if you enjoy diving into this area – as well as if you like talking with people!
More of a peer relationship with your manager. As engineers grow in seniority, they become more like a peer to their manager and help their manager get stuff done. The relationship is more like a “peer” than a “boss”.
Tip for managers of senior+ devs: give them agency, check in often, and make sure they are unblocked.
Autocomplete: an obvious use case. It helps one type less and think more.
“Vibe coding”: AI allows you to explore more paths and experiment faster.
How AI impacts engineers
Controversial, but Gauam believes that junior engineers are going to thrive because they are coming with new knowledge and new ways of working with AI tools. They do not have the biases of working a particular way.
The “generalist engineer” is going to be more in-demand, looking ahead
CS knowledge remains important.
When things go wrong it is important to understand why they went wrong. This requires strong computer science fundamentals and system knowledge.
Where to find Gautam Korlam:
• LinkedIn: [https://www.linkedin.com/in/gautamkorlam/](https://substack.com/redirect/8932d5ff-4618-4786-8653-818c5be44cba?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
Mentions during the episode:
• Bypassing Large Diffs in SubmitQueue: [https://www.uber.com/blog/bypassing-large-diffs-in-submitqueue/](https://substack.com/redirect/bfa8fa86-2de3-4b3d-8da7-7c5bf076d72e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Jenkins: [https://en.wikipedia.org/wiki/Jenkins_(software)](https://substack.com/redirect/c8d0ca55-b592-44b9-b1f1-94810f8edb39?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Devpods: [https://www.uber.com/blog/devpod-improving-developer-productivity-at-uber/](https://substack.com/redirect/5e56521c-2c07-4792-b17f-848f19c56f8f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• JetBrains: [https://www.jetbrains.com/](https://substack.com/redirect/e0c2cc7c-fa5e-4d90-96f0-16951fc2775e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Cloud Development Environments: [https://newsletter.pragmaticengineer.com/p/cloud-development-environments](https://substack.com/redirect/da0b2e26-bf3b-4e37-98c1-67dc7266a3cc?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Why are Cloud Development Environments Spiking in Popularity, Now?: [https://blog.pragmaticengineer.com/why-are-cloud-development-environments-spiking-in-popularity-now/](https://substack.com/redirect/58a0c774-e0ac-41fa-a674-0775469b409e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• “The Coding Machine” at Meta with Michael Novati: [https://newsletter.pragmaticengineer.com/p/the-coding-machine-at-meta](https://substack.com/redirect/13e9462b-3cce-43c9-a0f3-73ac91728e04?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Software Architect Archetypes: [https://newsletter.pragmaticengineer.com/p/software-architect-archetypes](https://substack.com/redirect/d5bba7cf-ede7-4ecf-ac45-cc7205442d15?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• The Platform and Program Split at Uber: A Milestone Special: [https://newsletter.pragmaticengineer.com/p/the-platform-and-program-split-at](https://substack.com/redirect/94424774-a0e5-4467-9e01-4b31412b6d84?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• What is Vibe Coding? How Creators Can Build Software Without Writing Code: [https://alitu.com/creator/workflow/what-is-vibe-coding/](https://substack.com/redirect/e4356b12-f84f-43ec-acc2-b8286e7f7476?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• WhatsApp: [https://www.whatsapp.com/](https://substack.com/redirect/3e009f25-dee6-4719-b8f3-0ef77d440d1a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Rust: [https://www.rust-lang.org/](https://substack.com/redirect/3f01e734-9232-48e4-aab7-250c62f7479e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• I am excited to introduce Jimy by Gitar - The agentic AI for building better software: [https://www.linkedin.com/posts/gautamkorlam_i-am-excited-to-introduce-jimy-by-gitar-activity-7297713117927481344-0G4l/](https://substack.com/redirect/f927fc1e-3a78-4147-abc7-44cae9366453?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Cursor: [https://www.cursor.com/](https://substack.com/redirect/405f1dcb-e228-42d9-b337-d29fec3c4484?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Claude: [https://claude.ai/](https://substack.com/redirect/0c988939-e080-42b4-bc5d-82c6373d8469?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Deepseek: [https://www.deepseek.com/](https://substack.com/redirect/ee8631e1-c86d-46f6-80bd-9dbdde4ee351?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Head First Design Patterns: A Brain-Friendly Guide: [https://www.amazon.com/Head-First-Design-Patterns-Brain-Friendly/dp/0596007124](https://substack.com/redirect/764be9bd-be1a-442e-8225-4663e5d8bbc4?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
—
Production and marketing by [Pen Name](https://substack.com/redirect/194709b5-e358-4ff7-a58e-de73740cb658?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). For inquiries about sponsoring the podcast, email podcast@pragmaticengineer.com.
You’re on the free list for [The Pragmatic Engineer](https://substack.com/redirect/2/eyJlIjoiaHR0cHM6Ly9uZXdzbGV0dGVyLnByYWdtYXRpY2VuZ2luZWVyLmNvbT91dG1fY2FtcGFpZ249ZW1haWwtaG9tZSZyPThvNTRuIiwicCI6MTU4ODkwMjgxLCJzIjo0NTg3MDksImYiOnRydWUsInUiOjE0NTYzMzE5LCJpYXQiOjE3NDE3OTUwNzksImV4cCI6MTc0NDM4NzA3OSwiaXNzIjoicHViLTAiLCJzdWIiOiJsaW5rLXJlZGlyZWN0In0.YSOqLXU8j0lzIEkgalo7SfBfzxC1p-U4zayP9a-N4VQ?). For the full experience, [become a paying subscriber](https://substack.com/redirect/2/eyJlIjoiaHR0cHM6Ly9uZXdzbGV0dGVyLnByYWdtYXRpY2VuZ2luZWVyLmNvbS9zdWJzY3JpYmU_dXRtX3NvdXJjZT1wb3N0JnV0bV9jYW1wYWlnbj1lbWFpbC1jaGVja291dCZuZXh0PWh0dHBzJTNBJTJGJTJGbmV3c2xldHRlci5wcmFnbWF0aWNlbmdpbmVlci5jb20lMkZwJTJGZGV2ZWxvcGVyLWV4cGVyaWVuY2UtYXQtdWJlciZyPThvNTRuJnRva2VuPWV5SjFjMlZ5WDJsa0lqb3hORFUyTXpNeE9Td2lhV0YwSWpveE56UXhOemsxTURjNUxDSmxlSEFpT2pFM05EUXpPRGN3Tnprc0ltbHpjeUk2SW5CMVlpMDBOVGczTURraUxDSnpkV0lpT2lKamFHVmphMjkxZENKOS5CRkxGSTdxb1lmZFJSeFdvYUlldUh3V21sZ0U0dXNjamtoV1pSXzdmeGd3IiwicCI6MTU4ODkwMjgxLCJzIjo0NTg3MDksImYiOnRydWUsInUiOjE0NTYzMzE5LCJpYXQiOjE3NDE3OTUwNzksImV4cCI6MTc0NDM4NzA3OSwiaXNzIjoicHViLTAiLCJzdWIiOiJsaW5rLXJlZGlyZWN0In0.AfxqH1_VoWKr0fQV-Cp46GACvZ_7q14b9G5oB7wePbY?). Many readers expense this newsletter within their company’s training/learning/development budget.
This post is public, so feel free to share and forward it.
If you enjoyed this post, you might enjoy my book, [The Software Engineer's Guidebook](https://substack.com/redirect/3f6956aa-3df4-43eb-86af-a8a60dac4f85?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). Here is what Tanya Reilly, senior principal engineer and author of The Staff Engineer's Path said about it:
"From performance reviews to P95 latency, from team dynamics to testing, Gergely demystifies all aspects of a software career. This book is well named: it really does feel like the missing guidebook for the whole industry."