---
subject: "Building Meta’s Threads App"
from: "The Pragmatic Engineer <pragmaticengineer@substack.com>"
to: ""
date: 2023-09-07 16:35:00
labels: ["CATEGORY_PERSONAL", "INBOX", "The Pragmatic Engineer"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_6413324878686416177"]
---
|
👋 Hi, this is [Gergely](https://substack.com/redirect/42fa7745-ce55-4df7-b617-9f3578a3b8f2?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) with a bonus, free issue of the Pragmatic Engineer Newsletter. In every issue, I cover challenges at Big Tech and startups through the lens of engineering managers and senior engineers.
If you’re not a subscriber, you missed the issue on [Why cloud development environments are spiking in popularity right now](https://substack.com/redirect/f8b15f9c-ad85-4a05-a17d-7c042c126f1c?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) and[ a few others](https://substack.com/redirect/3cbeb080-857c-439a-a42f-7833927982a8?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). Subscribe to get two full issues every week. Many subscribers expense this newsletter to their learning and development budget. If you have such a budget, here’s[ an email you could send to your manager](https://substack.com/redirect/9971a670-fb11-4e7d-8f26-88b855a4202e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).👇
‘Real-world engineering challenges’ is [a series](https://substack.com/redirect/48d27db0-440a-4701-aa59-43ff6f23aa82?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) in which I interpret interesting software engineering or engineering management case studies from tech companies. In today’s issue, we peek behind the scenes of the a major app launch at Meta: that of [Threads](https://substack.com/redirect/02092865-a57e-4955-99a8-6fc574d2c981?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).
In July of this year, Meta launched its latest mobile app, Threads, a microblogging service and new rival to X, formerly Twitter. In the first five days following its launch, the app achieved 100M downloads – a new record for the company by some margin. Meta’s previous record for new app installs in the first 5 days after launch was 1M. Here is how the growth curve looked like, for the number of onboarded users:
These are huge numbers for a new app, even when taking into account that the more than 2 billion monthly active Instagram users were promoted to install this new app. When I learned of these stats, my first thought was wondering how did the engineering team pull off this launch, seemingly without any major hiccups? Especially, when considering that the Threads team moved up the launch, after Twitter [limited free users to viewing 600 posts a day](https://substack.com/redirect/64692fbf-954f-4f29-a1c4-f10f8a5c6863?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o): and this decision created the perfect launch opportunity for a Twitter challenger. Threads launched within a few days after Twitter’s rate limiting: and it seems like the app seized that moment well.
But what was it like, from the inside, for engineers building the app? For answers, I reached out to the Threads engineering team, who were open to sharing behind-the-scenes details. [Jesse Chen](https://substack.com/redirect/68f1a550-3afc-41f5-8369-f0874bd25c2d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) (engineering manager on Threads) and [Zahan Malkani](https://substack.com/redirect/10010bfb-e856-410e-b0d9-42b623f274a9?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) (server engineer lead on the app) told me the story on how Threads was built. The details they shared fit nicely into the [Real-World engineering challenges](https://substack.com/redirect/48d27db0-440a-4701-aa59-43ff6f23aa82?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) series.
In today’s issue, we dive into:
Building Threads
Technology choices and engineering approaches
Planning for the launch
The launch
Learnings and next steps
In this article, my questions are in italic and answers from the Threads engineering team are in normal font. With that, it’s over to Jesse and Zahan, to lift the lid on how the app was built.
How “typical” was Threads as a project, compared to other app launches?
Threads was different from most launches. Usually when there is a new, exciting top-down priority, we lean into our open internal culture to rally the company around the initiative and get folks excited to join and bootstrap the team.
In this case, however, we kept the team deliberately small and confidential. We tapped the shoulders of some of our strongest engineers, product managers, and designers within Instagram to work on this, and had regular reviews with Adam Mosseri, the head of Instagram. We knew time to market was a priority, and wanted to shield the team from noise.
How large was the initial team, and what portion of it was engineering?
The team was lean, flat and engineering-heavy, which was an intentional organizational design choice. We had a tight deadline and we wanted to maximize quick decision making and minimize bureaucracy.
We believed a leaner organization could help us build higher quality products faster, and this proved correct. We started with a very small team, with around a dozen people in total. The vast majority of the whole team came from Instagram. Everyone joining the Threads building towards launch was an internal transfer: so they were working at Meta beforehand..
The peak staffing on the team was a week before launch. At this time the team consisted of:
3 product managers
3 designers
About 60 engineers
I (Jesse) worked with engineering leads across the Instagram org to identify key senior engineers to pull onto this project. The experience level of the team skewed senior, since we had a relatively small team and needed engineers who could operate autonomously, and own their respective pieces of the app with little oversight needed.
How formal or informal was the planning, versus jumping straight to prototyping/coding?
There was some high-level planning in the beginning, as we debated how much to reuse Instagram’s codebase. However, for the most part, we jumped straight into prototyping and coding.
We evoked one of Meta’s early mantras, “code wins arguments.” We aligned heavily with this principle. Even before we received the official greenlight, engineers were already prototyping the idea of a text feed, to prove feasibility!
How much did you work with/rely on other internal teams within Meta – such as infra, platform, or product teams?
One unique collaboration we had was a “Bug Bounty” program where we invited security researchers to probe the app for bugs before launch. The goal of this program was to help protect people’s data, and uncover any security or privacy bugs we might have early on. We discovered a few notable bugs thanks to this program.
We worked in secrecy. Pre-launch, the core engineering team was isolated from the rest of Instagram’s engineering org. Working in secrecy, we added our code to the shared codebase discreetly and only looped in partner teams when we faced issues which required their expertise.
Still, we could not have launched this app in the time it took by working in isolation. We relied heavily on our internal tooling and frameworks. We leveraged several things from other internal teams, like:
UI frameworks
APIs
Login, privacy, security, integrity infrastructure
Server infrastructure
… and much more!
We reused as much code as we could to move as quickly as possible. Our speedy development speed and stability during launch is a testimony of how awesome our engineering organization is. Our platform/infra teams make it look easy when we quickly scale and build new products, standing on their shoulders.
We wrote the first line of code for the standalone app late January 2023. We submitted the final launch candidate to the app store in June 2023.
The engineering effort from start to launch took 5 months.
Which technologies did you choose for the backend and the mobile apps?
The backend is running on Instagram’s stack – our custom Python running Django speaking to a custom REST API. We also talk to Meta’s bigger monolithic backend over GraphQL which is on [HHVM](https://substack.com/redirect/a9a872ef-2e45-4fa8-807d-0b3f34581c9f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) – a virtual machine for executing programs written in the Hack, PHP-like language.
The apps are largely native, using a mix of Swift on iOS (and a little Objective C), and Jetpack Compose on Android (with Kotlin and Java as languages). There are some shared server-rendered screens for some simple experiences, but native is the norm.
Which choices did you make in reusing existing parts of the stack – like libraries and frameworks – versus building your own?
Because time-to-market was a priority, we used the Instagram tech stack wherever possible. Instagram itself is built upon a variety of libraries and frameworks, many of them in house.
We used the latitude afforded by a greenfield opportunity to try out technologies at scale that we hadn’t had the chance to, before. On iOS, all new parts of the app were built with Swift, and on Android we used [Jetpack Compose](https://substack.com/redirect/8ffff459-fb71-43df-b6db-ad3edd8e18bd?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) to a large degree. We credit the new language (Swift) and framework choices (Jetpack Compose) with helping us move as quickly as we did.
We chose to heavily leverage Instagram’s existing tech stack, which is built upon Meta’s infrastructure, which contributed greatly to our dev speed. This choice took the ambiguous scope problem from:
“How do we create a new text-based social network from scratch?”
To this much more focused question:
“How do we use the building blocks of the Instagram feed for posts that are more text-based?”
Threads felt snappy on launch. How much did you prioritize client-side performance, and how did you measure this or test for it, if you did?
Launch performance was not snappy enough! We have internal tools which profile and understand where time is spent, and we had to employ them extensively at launch, when the most popular posts individually started getting the kind of engagement we didn’t expect the entire network would get on launch day.
We have internal frameworks which let us measure a variety of crucial performance metrics. Here are some examples:
“Time to new content” is for cold start to seeing content in feed
Scroll performance is checked through looking for frame drops
How did you go about (or skip) testing; specifically automated tests? There are two schools of thought here:
A) build it and get rapid feedback. Worry about automated tests when there’s a product-market fit (PMF.)
B) build it from scratch assuming a PMF, and put tests in place for maintainability, etc.
We were in camp A, of worrying about automated tests after PMF for frontend / UI tests. Because of how important time to market is, we were disciplined about dropping things which didn’t help us towards that goal.
To be sure, automated tests are important; however, there is no value in writing tests for a UI that is constantly changing. As context, some flows had 3+ redesigns before we landed on something we liked!
Automated tests don’t help a product with no product market fit. Instead, we relied extensively on dogfooding and QA. Dogfooders downloaded master builds that updated every few hours with the latest changes. The quick feedback loop allowed us to go from figma mockups, to a master build deployed onto your phone, within a few hours.
That said, backend business logic followed a test-driven development (TDD) practice that was encouraged through peer review. We have great internal testing frameworks that let you set up state and run through actual business logic fairly easily, without touching production databases. This enabled the backend team to move quicker, since we could make changes with confidence, without having to end-to-end test each change.
What were the biggest load challenges you anticipated for Threads?
A particular feature we knew was going to create scaling challenges was giving users the ability to pull across their graph from Instagram.
One of the difficult parts of starting up a new social network is the “cold start” users face. Every one of your new users needs to find the people they’re interested in on the platform and choose to follow / friend them. In our case, we wanted to make that easier by offering a one tap action to “follow everyone you already follow on Instagram.”
There is a major scaling issue here, though! Think of the more popular accounts joining Threads, with audiences in the order of millions already queued up to follow them. We needed to process such large accounts in a timely manner.
After launch, we realized that the scale we were dealing with far exceeded our expectations. Since the launch, we’ve needed to redesign this system with a totally different set of assumptions.
For how long was Threads dogfooded, and by roughly how many folks? How did the team go about collecting feedback and addressing it?
The app was in constant dogfooding from the start, but we intentionally kept the feedback group small. Our goal was to get high signal feedback without overwhelming the team with bug reports.
We slowly expanded dogfooding from the core team, to all of Instagram. With the smaller dogfooding population, engineers engaged directly and debugged with coworkers, resulting in a really tight feedback loop.
How did you prepare for the launch, and to handle the initial load? For example, did you do load tests in advance, or other testing ahead of time?
Doing extensive tests was certainly the plan of record. However, due to external circumstances, we pulled our launch to earlier than planned.
We had to scale our capacity and support the launch, on the fly. This was due to an earlier than planned launch, and because of this timeline change, we were unable to do load tests beforehand. This was one of the most intense launches we’ve had at the company in a while!
How certain or uncertain were you that you could handle a potentially large load on launch? I found it unusual to do a global launch with no “signup limiting” or waitlist in place, as you did.
We knew we had the expertise of Instagram and Meta behind us, so we were fairly confident for the launch. And we initially thought we’d be a small drop in the bucket at Meta’s scale.
The reality of onboarding so many users, so quickly, was unprecedented at Meta, in hindsight. However, the decade of investment in reliable and performant infra at Meta helped. Investment areas like:
Databases
Graph indexing systems
Ranking systems
Integrity systems
Notification systems
These systems all worked in concert to soak up the load without any major hitches.
From the outside, the launch looked surprisingly smooth, with perhaps a few brief blips during the first week. From the inside, how did it go?
This was an “all hands on deck” situation for the team, starting the week before launch, and for the weeks afterwards. We hosted regular video calls to talk through issues live, and a majority of the team was working around the clock to resolve various issues.
The heartening thing was that it was decidedly not a “Threads team-only” effort. A major part of launch support came from partner teams in Instagram, and across Meta. Devs working on infra components collaborated with production engineers keeping the systems up, who worked with product engineers debugging their features.
A launch like this was one where you see the benefits of an open culture. An open codebase really pays dividends, as new people could quickly ramp up and provide value, even if it’s a new domain.
Which engineering KPIs or measurements did you focus on, to ensure Threads worked as expected?
We used monitoring tools like:
[ODS](https://substack.com/redirect/23248107-53d8-4233-a236-4082373cb9ef?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)– a high-performance time series storage engine – and[Scuba](https://substack.com/redirect/984abd74-92ad-4b70-9ebf-d8be6c9dfdf3?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)– a data management system we use for real-time analysis. These tools help keep track of load and the like in real-time.An evolved warehouse extract-transform (ETL) ecosystem to give us key product metrics hourly.
We heavily used PREQ (performance, reliability, efficiency, quality) tools. Our team leaned on the tremendous experience at Meta of supporting PREQ tools that were built into the client app, and integrated in our server-side frameworks.
Metrics we paid attention to included:
Performance and server-side load
“Time to new content” – our cold start app metric
QPS / success rate on our key endpoints
Queue length on async jobs handling heavy lifting
Our general footprint on the main Instagram backend monolith
Endpoint-level catch-all alarms also notify us when things started to go south for particular endpoints, if we hadn’t accounted for scale properly.
The previous record for the fastest-ever growing app at Meta was 1M users in 5 days. This is how Threads grew:
1M users: in 1 hour
30M: 1 day
70M: 2 days
100M: 5 days
What was a difficult challenge which arose?
Making an engaging feed for Threads was the biggest one. On a microblogging site, the thing that is most relevant is what is happening right now. It needs to capture what everyone is talking about, and present choices for which conversations to dive into.
There’s a balance between immediacy and helping the user find content from someone they’re most likely to engage with. At the same time, other apps in the space have proved you don’t need an extensive graph of connections in order to serve relevant and interesting content.
We’ve talked on the Threads team about how we’d like to reduce our reliance on users manually curating follow graphs. However, to reduce reliance on manual curation, you need to understand what these posts are about, and know what is going on in the world – which are both challenging, to say the least!
What went well, from an engineering point of view in this project and launch?
These two stand out:
The speed at which we were able to build a polished product for launch
The relatively small size of the team which achieved this was viewed favorably both internally and externally.
There was a lot of market interest in this app before it launched, which gave people a good reason to download the app and try it out. Our job as engineers was to get roadblocks out of the way and let them do that. It’s a huge accomplishment that we were able to do so relatively smoothly.
What valuable learnings are there for the engineering team?
Focus: it’s the key differentiator between products set up to find product-market-fit and those which are not. Focus is necessary, although not sufficient by itself. The effort in Threads was to be able to focus by aggressively descoping the product experience to just the basics. Early on, we decided to focus execution on internal milestones.
Each internal milestone meant a fully polished, and shippable app experience, but with reduced functionality built out. These internal milestones forced clarity on what we absolutely needed to build, since there was never time to look at anything else.
What was the most interesting part of this project, as an engineer?
Understanding the breadth of the Instagram codebase. The technical decision to share much of the tech stack with Instagram meant that building this app became an exercise in going through Instagram’s codebase, so we could make targeted changes just to support our use case.
It’s rare to get an excuse to understand Instagram at such a high level, while delving into implementation details on the critical Instagram subsystems! It was almost like a puzzle: we needed to figure out within which Instgram systems to make the most targeted changes that would yield the most dividend, while taking the lowest risk. This challenge ended up being the most interesting part of the project.
What impact could the Threads launch have on how apps get built at Meta?
There have been many folks reaching out internally who are looking at Threads as a case study for future product launches. The sheer speed at which we shipped the first version of Threads is what sets this launch apart – with work on the app having only started earlier this year.
It is a notable cultural change to have a small but senior engineering team ship a standalone app with this sort of public reception in just five months, even at Meta. I’m excited to see other teams take inspiration and build faster, scrappier teams!
What are the next priorities for the team, and the growth plans?
For priorities, aside from building all the core product gaps our users are clamoring for, we are also heavily investing in significant infrastructure upgrades to make it more robust for Threads.
Our actual launch numbers far exceeded projections. Our leadership is optimistic about the trajectory of the app and as a result, we are investing in growing the engineering team.
The Threads started off initially as a small incubator team within the Instagram org. With the launch success, we are excited to see this grow into a more formal initiative.
What are things the engineering team is excited about, looking ahead?
We’ve been working on delivering new Threads features as quickly as possible. One such feature is the highly-requested logged-in web version of Threads, which we shipped last month. Another version is our expansion of the keyword content search test to more users in Canada, the United States, India, and the United Kingdom – which we [are launching today](https://substack.com/redirect/76edecc0-68f1-4fd9-8c34-759d211893dc?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) (7th September).
I'm excited for our team to keep shipping features that will improve people's experience on Threads.
I’m also excited about our commitment to join the Fediverse and support the ActivityPub protocol. At our scale, it’s an incredibly exciting technical and regulatory challenge. Joining the [Fediverse](https://substack.com/redirect/3a341a1c-0d89-4cb1-ba0b-4a34ffff8654?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) and building interoperability with other networks to create a more diverse and thriving public conversation ecosystem is something we remain committed to working towards.
This is Gergely again.
Many thanks, [Jesse](https://substack.com/redirect/68f1a550-3afc-41f5-8369-f0874bd25c2d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), [Zahan](https://substack.com/redirect/10010bfb-e856-410e-b0d9-42b623f274a9?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) and the Threads engineering team, for sharing details on how they built and launched the app. It was interesting to understand how the team pulled off this feat, and how their approaches stack up with what we know [about Meta’s engineering culture](https://substack.com/redirect/d9034223-26a6-40b4-a5c2-12b26b8a5ced?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) – a topic we cover in-depth, [in a two-part series](https://substack.com/redirect/d9034223-26a6-40b4-a5c2-12b26b8a5ced?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).
One last question I had to ask the Threads team is the plans to launch in the European Union. The app is available globally – except for the EU, thanks to regulatory concerns. Here is what the team told me about their plans:
“We are working on launching Threads in more countries and will continue to evaluate whether to launch in Europe, but the upcoming regulatory uncertainty has played into our decision not to launch right now. Europe continues to be an incredibly important market for Meta and we hope to make new products available here in future.“
It will be interesting to note if Meta delaying its EU launch is an exception: or if we can expect new apps and services launched by larger corporations to follow an “EU last” strategy, thanks to the additional privacy implications strict European regulations require.
Read more of my takeaways [in the full article.](https://substack.com/redirect/c521410e-b02f-43d8-9ab1-ca6968524ac3?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
If you’re hiring software engineers or engineering leaders, join [The Pragmatic Engineer Talent Collective](https://substack.com/redirect/fadbb623-f355-4ec3-9261-bd4502b1aecd?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). It’s the #1 talent collective for software engineers and engineering managers. Get weekly drops of outstanding software engineers and engineering leaders open to new opportunities. I vet every software engineer and manager - and add a note on why they are a standout profile.
Companies like Linear use this collective to hire better, and faster. [Read what companies hiring say](https://substack.com/redirect/68414a30-edfe-4b07-aa98-0c270ecd67d0?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). And if you’re hiring, apply here:
[Senior Frontend Developer](https://substack.com/redirect/76fbc8d9-83f0-4e5a-bfaf-7423800e05df?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)at TalentBait. €60-80K + equity. Barcelona, Spain.[Technical Lead](https://substack.com/redirect/54291b8a-3f0b-49c7-9397-c0bfe2bd7d08?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)at Alby. £95-120K + equity. London or Remote (UK).[Senior Software Engineer, Missions](https://substack.com/redirect/7e089f8f-aaa4-43b5-b2e7-476cdc62de56?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)at Ably. £80-100K + equity. Remote (UK).[Senior Software Engineer](https://substack.com/redirect/14540938-d8d1-48f4-bcb2-d381e208f6d5?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)at LatchBio. $120-220K + equity. San Francisco.[Software Engineer](https://substack.com/redirect/1238d7c5-3d7c-4ab1-b1bc-7a7a10b2a3ec?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)at Freshpaint. $130-210K + equity. Remote (US).[Senior Software Engineer, Developer Ecosystems](https://substack.com/redirect/c459f2a9-a53d-4eb0-a774-c1d495da068e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)at Ably. £80-100K. Remote (UK).[Senior Web Engineer, Activation](https://substack.com/redirect/ac2f7075-0f15-489e-b3e0-6d0db04742f3?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)at Ably. £75-85K. Remote (UK).[Web Engineer](https://substack.com/redirect/9f6fbb2c-3d5d-4412-8928-ea624c8ca202?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)at Ably. £70-75K. Remote (UK).[Staff Software Engineer](https://substack.com/redirect/c0be8008-f638-4fcc-b3bb-2f5abe01fc0d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)at Deepset. Remote (US, Europe).
See more senior engineer and leadership roles with great engineering cultures on [The Pragmatic Engineer Job board](https://substack.com/redirect/2cbe4648-1cfe-4cc2-ad9a-d41ea9b0b37a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) - or post your own.
You’re on the free list for [The Pragmatic Engineer](https://substack.com/redirect/2/eyJlIjoiaHR0cHM6Ly9uZXdzbGV0dGVyLnByYWdtYXRpY2VuZ2luZWVyLmNvbT9yPThvNTRuJnRva2VuPWV5SjFjMlZ5WDJsa0lqb3hORFUyTXpNeE9Td2ljRzl6ZEY5cFpDSTZNVE0yT0RJek1UTTBMQ0pwWVhRaU9qRTJPVFF4TURRMU1qZ3NJbVY0Y0NJNk1UWTVOalk1TmpVeU9Dd2lhWE56SWpvaWNIVmlMVFExT0Rjd09TSXNJbk4xWWlJNkluQnZjM1F0Y21WaFkzUnBiMjRpZlEuOGpaR0pKN0JqRzN6MzllQTIxS3N2NWl5V1ZHNXZGRUYzQ0dxdVhJbFVRRSIsInAiOjEzNjgyMzEzNCwicyI6NDU4NzA5LCJmIjp0cnVlLCJ1IjoxNDU2MzMxOSwiaWF0IjoxNjk0MTA0NTI4LCJleHAiOjE2OTY2OTY1MjgsImlzcyI6InB1Yi0wIiwic3ViIjoibGluay1yZWRpcmVjdCJ9.g_JP68wkWddctcBw07OVuqChcwWsFB_gm8MzGjqZcyY?). For the full experience, [become a paying subscriber](https://substack.com/redirect/2/eyJlIjoiaHR0cHM6Ly9uZXdzbGV0dGVyLnByYWdtYXRpY2VuZ2luZWVyLmNvbS9zdWJzY3JpYmU_dG9rZW49ZXlKMWMyVnlYMmxrSWpveE5EVTJNek14T1N3aWFXRjBJam94TmprME1UQTBOVEk0TENKbGVIQWlPakUyT1RZMk9UWTFNamdzSW1semN5STZJbkIxWWkwME5UZzNNRGtpTENKemRXSWlPaUpqYUdWamEyOTFkQ0o5LlNvVlkxOVNnSEZJanRESVpqSnNXWnpxMndQNjRpSHVQOEl6bWd0OTRMNk0mdXRtX3NvdXJjZT1wb3N0JnI9OG81NG4iLCJwIjoxMzY4MjMxMzQsInMiOjQ1ODcwOSwiZiI6dHJ1ZSwidSI6MTQ1NjMzMTksImlhdCI6MTY5NDEwNDUyOCwiZXhwIjoxNjk2Njk2NTI4LCJpc3MiOiJwdWItMCIsInN1YiI6ImxpbmstcmVkaXJlY3QifQ.0ImtnF1UaunfJxyB5XG2CJmzBRjouIRSSR3kNDkuBUI?). Many readers expense this newsletter within their company’s training/learning/development budget.
This post is public, so feel free to share and forward it.