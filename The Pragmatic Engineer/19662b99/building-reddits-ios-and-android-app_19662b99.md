---
subject: "Building Reddit’s iOS and Android app"
from: "The Pragmatic Engineer <pragmaticengineer@substack.com>"
to: ""
date: 2025-04-23 12:56:23
labels: ["CATEGORY_PERSONAL", "INBOX", "The Pragmatic Engineer", "UNREAD"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_6413324878686416177", "UNREAD"]
---
|
Listen and watch now on [YouTube](https://substack.com/redirect/63d10e61-5000-4712-a3fd-072cd048f28c?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), [Spotify](https://substack.com/redirect/fa4efa6f-52a5-4521-ae1c-6105bc3cd54a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) and [Apple](https://substack.com/redirect/bfddffff-6be0-4342-8285-5a61aebd1908?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). See the episode transcript at the top of this page, and timestamps for the episode at the bottom.
• [Graphite](https://substack.com/redirect/d90b400a-3ff2-4503-a238-dfd618db810b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) — The AI developer productivity platform.
• [Sentry](https://substack.com/redirect/c24c34dc-6364-4ddc-aa93-30c2ce07f772?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) — Error and performance monitoring for developers. Get 150k errors (three months of Team Plan) for free.
—
Reddit’s native mobile apps are more complex than most of us would assume: both the iOS and Android apps are about 2.5 million lines of code, have 500+ screens, and a total of around 200 native iOS and Android engineers work on them.
But it wasn’t always like this.
In 2021, Reddit started to double down on hiring native mobile engineers, and they quietly rebuilt the Android and iOS apps from the ground up. The team introduced a new tech stack called the “Core Stack” – all the while users remained largely unaware of the changes. What drove this overhaul, and how did the team pull it off?
In this episode of The Pragmatic Engineer, I’m joined by three engineers from Reddit’s mobile platform team who led this work: Lauren Darcey (Head of Mobile Platform), Brandon Kobilansky (iOS Platform Lead), and Eric Kuck (Principal Android Engineer). We discuss how the team transitioned to a modern architecture, revamped their testing strategy, improved developer experience – while they also greatly improved the app’s user experience.
We also get into:
How Reddit structures its mobile teams—and why iOS and Android remain intentionally separate
The scale of Reddit’s mobile codebase and how it affects compile time
The shift from MVP to MVVM architecture
Why Reddit took a bet on Jetpack Compose (a declarative UI framework for Android, built in Kotlin), but decided (initially) against using SwiftUI (a declarative UI framework for iOS, built in Swift)
How automated testing evolved at Reddit
Reddit’s approach to server-driven-mobile-UI
What the mobile platforms team looks for in a new engineering hire
Reddit’s platform team’s culture of experimentation and embracing failure
And much more!
If you are interested in large-scale rewrites or native mobile engineering challenges: this episode is for you.
My biggest takeaways from this episode:
1. At a glance: Reddit’s mobile tech stack evolution. From 2021, this is how things have changed:
2. The Reddit app is a lot more complex than one would assume. With around 200 native mobile engineers, Reddit has one of the largest mobile teams working on a single mobile codebase – I’d be surprised if there were more than a dozen similarly large mobile teams focusing on a single, standalone app.
The app has about 20 feature teams working on different parts of it, and to give a taste of the complexity, the Android app has ~800 modules and 580 screens. The complexity of mobile apps is rarely obvious at first glance – a few years ago, I did an explainer on [why the Uber app was hundreds of megabytes in size](https://substack.com/redirect/4f5ce067-b3e4-470f-86a2-66d41c2233f7?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).
3. Poor developer experience can slow down a company – so pay attention! One of the reasons Reddit started investing heavily in modernizing its mobile stack was that the “old stack” was slowing down developers. Reddit’s platform team got proof of this simply by asking native engineers about the biggest development-related challenges they face:
4. GenAI coding tools feel like they are not “there” yet with native mobile. LLMs integrated into IDEs seem to be increasingly helpful with backend, fullstack, web and even cross-platform (React Native / Expo) projects. However, Reddit’s mobile team shared that they get a moderate boost from the Apple and Android Studio LLM additions.
Native mobile development is distinctively different from web, fullstack and backend coding – and it seems that these IDEs with AI functionality have not done much to optimize for the expereince of native mobile engineers. Over time, this will likely change – but it’s a reminder that there are differences between fullstack, backend and native mobile development! (I wrote a book reflecting on more of the challenges unique to native mobile titled [Building Mobile Apps at Scale](https://substack.com/redirect/95376a28-449b-4a3f-b336-1de096d14a82?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o))
From [this part](https://substack.com/redirect/f8d25b07-0a21-48ce-b4ff-346a59e20f15?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o):
Gergely: “What does it take for an iOS or Android engineer to work at a platform team like this? When you're hiring, what are the traits that you're looking for?”
Brandon: “My joke answer is that I don't know why someone would choose to do this [working on a platform team]. I just stumbled into it. It's very stressful and it's very hard. Having said that, I would not choose any other position.
The most important thing for an IC who wants to get a job on a platform team: you need to sit in the consequences of your decisions. You should try to work at a tech company for a year or two and actually see what happens after you ship a system — and then the assumptions change! You then have to figure out how to keep this thing going.
Most things that I've had to write at Reddit are still in the code base (after 5+ years!). I wish they weren't, but you have to understand them.
You get a bunch of software design intuition because you have to like re-evaluate your assumptions for an incredibly long time. If you can do that, you're probably ready for platform stuff.
But take your time! Don’t burn you out before you're ready. Cause this is hard.”
Lauren: “Befriending your platform team is the best way to become a platform engineer someday.
If you have a platform team, befriend them during hackathon weeks or get some mentorship within projects. Almost everyone has done something like that before they end up joining our team. But also we really like having really good partners on the feature teams themselves because they are very honest with us about what their real problems are and they are the best source of that.”
Jump [this part of the episode.](https://substack.com/redirect/f8d25b07-0a21-48ce-b4ff-346a59e20f15?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
([00:00](https://substack.com/redirect/c48521f5-f216-4284-bcfc-539ae91b0287?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Intro
([02:04](https://substack.com/redirect/587540f5-0c71-43c2-95b1-767bb80d2fa4?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The scale of the Android code base
([02:42](https://substack.com/redirect/f0f082b5-25e9-4f2e-97b3-6dfc82bec5a0?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The scale of the iOS code base
([03:26](https://substack.com/redirect/131c437f-72de-43d4-9d8d-6d713560d3bd?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) What the compile time is for both Android and iOS
([05:33](https://substack.com/redirect/cffce686-0fc4-45df-828a-a7da4cf1f926?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The size of the mobile platform teams
([09:00](https://substack.com/redirect/aa5fbe71-aa94-4b96-95d1-9ba37de5854d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Why Reddit has so many mobile engineers
([11:28](https://substack.com/redirect/67aca2ac-976a-4cfb-912b-3f182df30d7d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The different types of testing done in the mobile platform
([13:20](https://substack.com/redirect/ff9b53d6-9306-4e70-9e9b-49ff543b3e58?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The benefits and drawbacks of testing
([17:00](https://substack.com/redirect/aa51e549-a675-4e0f-841d-74923cb139d3?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) How Eric, Brandon, and Lauren use AI in their workflows
([20:50](https://substack.com/redirect/b88a8d79-07b7-48ea-80f1-f4cbac1f99e2?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Why Reddit grew its mobile teams in 2021
([26:50](https://substack.com/redirect/3290ed65-3d7d-4d01-b360-0b0c39e6ec9d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Reddit’s modern tech stack, Corestack
([28:48](https://substack.com/redirect/e3d07e6e-1b53-4d5b-b4c8-486ef0c89971?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Why Reddit shifted from MVP architecture to MVVM
([30:22](https://substack.com/redirect/dd68cb02-36ef-44ac-bf72-9685dce4aa13?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The architecture on the iOS side
([32:08](https://substack.com/redirect/702b7903-3771-4f5e-80d0-ad91f7d8306b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The new design system
([30:55](https://substack.com/redirect/fb2195e5-907e-4e22-b179-2482d9937a29?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The impact of migrating from Rust to GraphQL
([38:20](https://substack.com/redirect/31ad26d0-e03d-43e9-b421-d0a2bd712ddc?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) How the backend drove the GraphQL migration and why it was worth the pain
([43:17](https://substack.com/redirect/09138090-e224-4107-a2d1-15fff1704196?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Why the iOS team is replacing SliceKit with SwiftUI
([48:08](https://substack.com/redirect/471b4a2f-56df-457e-91e7-1519d35c9ea8?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Why the Android team took a bet on Compose
([51:25](https://substack.com/redirect/05e5f305-4b5c-4290-9c6b-dde605dbc580?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) How teams experiment with server-driven UI—when it worked, and when it did not
([54:30](https://substack.com/redirect/cedb2b1c-4013-4089-8e74-2bdf18b8115e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Why server-driven UI isn’t taking off, and why Lauren still thinks it could work
([59:25](https://substack.com/redirect/549d1774-84c1-4484-ab93-6584eda8e9fd?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The ways that Reddit’s modernization has paid off, both in DevX and UX
([1:07:15](https://substack.com/redirect/a1bce511-f478-468e-b033-121871832986?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The overall modernization philosophy; fixing pain points
([1:09:10](https://substack.com/redirect/00ec53f5-3661-42fe-a187-e738fbb6cf22?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) What the mobile platforms team looks for in a new engineering hire
([1:16:00](https://substack.com/redirect/1cc20887-cb5f-4e14-995e-4726448d9c47?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Why startups may be the best place to get experience
([1:17:00](https://substack.com/redirect/7f6a8985-251d-4a14-9f04-07957a90588a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Why platform teams need to feel safe to fail
([1:20:30](https://substack.com/redirect/30a01440-bbab-494c-a53e-db030dd48d76?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Rapid fire round
Where to find Lauren Darcey:
• LinkedIn: [https://www.linkedin.com/in/perlgurl/](https://substack.com/redirect/4ef41144-63c6-4ca2-b215-16cc6d14bdb9?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
Where to find Brandon Kobilansky:
• LinkedIn: [https://www.linkedin.com/in/brandon-kobilansky-45097860/](https://substack.com/redirect/4468e4fd-c25c-4e3f-b3a4-bb644aa71b40?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• X: [https://x.com/bkobilansky](https://substack.com/redirect/fbea39be-eed4-4893-b834-af77b36dbec9?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
Where to find Eric Kuck:
• LinkedIn: [https://www.linkedin.com/in/eric-kuck-3bbb7680/](https://substack.com/redirect/395bfa00-6912-4f72-b915-4f03e20a0b23?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
Mentions during the episode:
• Gemini: [https://gemini.google.com/app](https://substack.com/redirect/a87d6f2e-3b96-4b86-865f-cda42fee06e4?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• GraphQL: [https://graphql.org/](https://substack.com/redirect/51d8c081-a4c4-45f9-a989-224be09105ba?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Rust: [https://www.rust-lang.org/](https://substack.com/redirect/83300b06-fc01-47a3-8898-269bc290f1a7?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• MVVM: [https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93viewmodel](https://substack.com/redirect/d64a9ad3-01f1-4382-b4a5-04121f7952f6?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Compose: [https://www.jetbrains.com/compose-multiplatform/](https://substack.com/redirect/eeeb810d-1bc6-42a7-aac5-fc728cecd1bc?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• MVP: [https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93presenter](https://substack.com/redirect/c1cd22f7-7b21-4f76-8109-385afe8b2da4?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• The SliceKit Series: Introducing Our New iOS Presentation Framework: [https://www.reddit.com/r/RedditEng/comments/v3hpns/the_slicekit_series_introducing_our_new_ios/](https://substack.com/redirect/bfc6f013-8416-4da5-b13d-e549db9ae1cb?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• SwiftUI: [https://developer.apple.com/xcode/swiftui/](https://substack.com/redirect/c2e01eb2-a43a-41f1-8112-e52f62675d1f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• The comic about Google migrations: [https://goomics.net/50](https://substack.com/redirect/eff0e639-3101-46a5-9895-b09597e7834f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• The man behind the Big Tech comics – with Manu Cornet: [https://newsletter.pragmaticengineer.com/p/the-man-behind-the-big-tech-comics](https://substack.com/redirect/a6578440-f415-49f0-8450-d86084b25d39?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Texture: [https://texturegroup.org/](https://substack.com/redirect/acf13c94-667f-4344-b203-7009ca89611f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Reddit Talk: [https://www.reddit.com/r/RedditTalk/](https://substack.com/redirect/14827703-70b4-4ed7-879d-1326df55fb23?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• GraphQL JS: [https://www.graphql-js.org/docs/](https://substack.com/redirect/bf3755ad-8ab6-48b1-95e3-cf65fc6cd8be?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Westrum’s typology: [https://psychsafety.com/psychological-safety-81-westrums-cultural-typologies/](https://substack.com/redirect/5dd98bea-7a4f-499e-9e14-cb2159e46259?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• C Programming Language: [https://www.amazon.com/Programming-Language-2nd-Brian-Kernighan/dp/0131103628](https://substack.com/redirect/de952ca5-4440-45cc-bfa2-30e4c1450409?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Tidy First?: A Personal Exercise in Empirical Software Design: [https://www.amazon.com/Tidy-First-Personal-Exercise-Empirical/dp/1098151240](https://substack.com/redirect/e9e67017-e3f6-48a2-952a-9405da293d98?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Project Hail Mary: [https://www.amazon.com/Project-Hail-Mary-Andy-Weir/dp/0593135202](https://substack.com/redirect/024fc9b8-d6ed-4cec-931f-c8d710e33edf?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
—
Production and marketing by [Pen Name](https://substack.com/redirect/23c15834-34cb-4dc4-b01a-c362fdec2d7a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). For inquiries about sponsoring the podcast, email podcast@pragmaticengineer.com.
You’re on the free list for [The Pragmatic Engineer](https://substack.com/redirect/2/eyJlIjoiaHR0cHM6Ly9uZXdzbGV0dGVyLnByYWdtYXRpY2VuZ2luZWVyLmNvbT91dG1fY2FtcGFpZ249ZW1haWwtaG9tZSZyPThvNTRuIiwicCI6MTYxOTE2MDE2LCJzIjo0NTg3MDksImYiOnRydWUsInUiOjE0NTYzMzE5LCJpYXQiOjE3NDU0MTMwNDksImV4cCI6MTc0ODAwNTA0OSwiaXNzIjoicHViLTAiLCJzdWIiOiJsaW5rLXJlZGlyZWN0In0.SxGidVZ2rvNU4mDtQg4HZS5hYljBq3buWVW1na7PI2M?). For the full experience, [become a paying subscriber](https://substack.com/redirect/2/eyJlIjoiaHR0cHM6Ly9uZXdzbGV0dGVyLnByYWdtYXRpY2VuZ2luZWVyLmNvbS9zdWJzY3JpYmU_dXRtX3NvdXJjZT1wb3N0JnV0bV9jYW1wYWlnbj1lbWFpbC1jaGVja291dCZuZXh0PWh0dHBzJTNBJTJGJTJGbmV3c2xldHRlci5wcmFnbWF0aWNlbmdpbmVlci5jb20lMkZwJTJGYnVpbGRpbmctcmVkZGl0cy1pb3MtYW5kLWFuZHJvaWQmcj04bzU0biZ0b2tlbj1leUoxYzJWeVgybGtJam94TkRVMk16TXhPU3dpYVdGMElqb3hOelExTkRFek1EUTVMQ0psZUhBaU9qRTNORGd3TURVd05Ea3NJbWx6Y3lJNkluQjFZaTAwTlRnM01Ea2lMQ0p6ZFdJaU9pSmphR1ZqYTI5MWRDSjkuVDNlR3Q5VjFFYlN1NWFVSXQ4UFd2RVVKVDI2aDZFQlNyR2Fka3VHcjVuMCIsInAiOjE2MTkxNjAxNiwicyI6NDU4NzA5LCJmIjp0cnVlLCJ1IjoxNDU2MzMxOSwiaWF0IjoxNzQ1NDEzMDQ5LCJleHAiOjE3NDgwMDUwNDksImlzcyI6InB1Yi0wIiwic3ViIjoibGluay1yZWRpcmVjdCJ9.-Q4S0OZzQazFuATAGXbf6jPYbvIXx-Rl3z2FzNzxwz4?). Many readers expense this newsletter within their company’s training/learning/development budget.
This post is public, so feel free to share and forward it.
If you enjoyed this post, you might enjoy my book, [The Software Engineer's Guidebook](https://substack.com/redirect/8c70f723-5ef9-4ec5-b5b0-d9286ed2b4a8?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). Here is what Tanya Reilly, senior principal engineer and author of The Staff Engineer's Path said about it:
"From performance reviews to P95 latency, from team dynamics to testing, Gergely demystifies all aspects of a software career. This book is well named: it really does feel like the missing guidebook for the whole industry."