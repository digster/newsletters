---
subject: "Notion: going native on iOS and Android"
from: "The Pragmatic Engineer <pragmaticengineer@substack.com>"
to: ""
date: 2024-12-11 18:31:16
labels: ["CATEGORY_PERSONAL", "INBOX", "The Pragmatic Engineer", "UNREAD"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_6413324878686416177", "UNREAD"]
---
|
Available now on [Spotify](https://substack.com/redirect/c2afd835-38d5-472e-879b-9366164f20ef?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), [YouTube](https://substack.com/redirect/9933b5c5-6ba8-456c-85fb-5c0ee4adc007?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) and Apple. See the episode transcript at the top of this page.
[DX](https://substack.com/redirect/971927c2-2ee1-44e5-9501-70866f59d5a9?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) → DX is an engineering intelligence platform designed by leading researchers
—
In today’s exciting episode of The Pragmatic Engineer, I am joined by two founding native mobile engineers from Notion: Austin Louden and Karn Saheb. Austin and Karn joined Notion in 2019 when Notion started to revamp its iOS and Android apps. Today, Notion's mobile apps are used by tens of millions of users.
In our conversation today, we take a deep dive into how the Notion mobile team operates and discuss:
The engineering culture at Notion
Why the mobile team focuses so much on app performance
How the mobile team rewrote the mobile app from webviews and Cordova to a native implementation
Notion’s tech stack and frameworks they rely on
Details on the development process, including four types of environments, approaches to using modules, and practices around feature flags
How the mobile team maintains consistency across iOS and Android
… and much more!
My biggest takeaways from this fascinating conversation:
1. Notion’s underlying data model is both flexible, but also tricky to work with. It was interesting to hear how much work Notion’s underlying data model created for the mobile engineering team. Notion chose a flexible data model that makes it easy to change parts of a document. However, this flexibility means a lot of added engineering complexity for all clients – including on mobile!
2. Notion’s native mobile team is surprisingly small. Notion employs about 600 staff, but the mobile team is only 11 people – including iOS and Android. This team size is very small, especially considering how Notion serves more than 10M users on both iOS and Android. We’re likely talking about one engineer for every ~2M or more users!
While the team is small, it is very senior. It would be hard to see such a small team operate efficiently any other way. How Notion’s mobile team operates – preferring a small and senior team – fits into the trend we discussed previously in[ Is there a drop in native iOS and Android hiring at startups?](https://substack.com/redirect/7d886162-d3b8-4f10-b1fa-46bd2f36ddad?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
3. Moving from web-based to native was an incremental process by necessity. Thanks to a small native team, and the need to keep the mobile apps up-to-date with the latest Notion features, the native mobile engineering team didn’t have the luxury of doing a large mobile app rewrite.
Instead, they did the sensible thing of slowly migrating parts of the app. Today, most of Notion’s apps are fully native, save for the editor. The editor remains one of the most complex parts of Notion.
4. Notion releases their app on a weekly cadence. Native mobile apps need to go through an app review flow from Apple and Google, and so many native apps are released less frequently, to account for this overhead. Notion doing a weekly release cycle is impressive – and it can serve as inspiration for other native mobile teams.
If Notion, with 10M+ native users and a small team, does this, other native teams can as well!
5. Feature flags are a must-have for native mobile apps at the scale of Notion. The Notion team uses feature flags extensively as a way to roll out new features and roll back code that could cause issues. With native mobile apps where code is shipped as binary, feature flags become especially important – as this example also shows.
([00:00](https://substack.com/redirect/4a259144-d0d0-427f-bcdd-5a98e0700069?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Intro
([02:03](https://substack.com/redirect/50f2d5ec-dee7-4804-9c20-4d06f4b3962c?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The RFC process at Notion
([06:00](https://substack.com/redirect/f28ce571-4c87-4d8a-9b01-e42ea3cbb80d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) How Notion uses internal channels to share RFCs
([07:57](https://substack.com/redirect/90cce86f-02ab-4235-9dd0-d1c73ecd6c4e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Some of the unique ways the mobile team works
([11:07](https://substack.com/redirect/efa022bd-0782-428c-ae39-9bf661854777?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Why they don’t do sprint planning at Notion—and what they do instead
([12:57](https://substack.com/redirect/3df7c567-6d06-46c9-8281-aeda46759f42?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) An overview of the size of Notion and teams at Notion
([13:15](https://substack.com/redirect/176e6411-261f-433f-a713-c91162dd67ee?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The beginning of mobile at Notion
([14:40](https://substack.com/redirect/5acd5a6d-e3bf-4a16-932c-3a5d6e953d16?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) A simple explanation of Cordova
([15:40](https://substack.com/redirect/fd5fa054-3c55-4bf4-a4e3-120fb440f699?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Why Notion decided to revamp mobile in 2019 and shift to Native
([18:30](https://substack.com/redirect/682c9c18-f551-40f4-ac53-06c385878277?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) How the mobile team evaluated performance as they made the shift to Native
([22:00](https://substack.com/redirect/9c825cc2-b3bd-42a6-bad4-0bc64a0684a6?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Scaling mobile and iterations of moving to Native
([26:04](https://substack.com/redirect/61c1b4be-fde0-4c14-8788-01d7d0cd968d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Why the home tab project was so complex
([30:59](https://substack.com/redirect/4e35fc31-a545-49e2-a7d0-6c2dc7b3d261?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Why the mobile team saved the editor for last and other future problems
([34:35](https://substack.com/redirect/cdde9dd9-1003-40c2-afd0-f499c39c4eec?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) How mobile works with other teams
([36:50](https://substack.com/redirect/f28bc128-f11b-410b-835d-9562abc70fad?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) How iOS and Android teams work together
([38:28](https://substack.com/redirect/583c8c5d-a0d0-4d58-a62b-fa2624c3471f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The tech stack at Notion
([39:30](https://substack.com/redirect/e3e209b4-43cb-4cf6-a192-f23816045050?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) How frameworks are used
([41:57](https://substack.com/redirect/6c6fee5b-6fde-446d-a522-12e02b2c3858?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Pros and cons of different frameworks and why Swift was the right choice
([45:16](https://substack.com/redirect/d929fbe3-48fd-4616-b079-0d3ca1eb4e42?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) How code reviews work at Notion
([48:23](https://substack.com/redirect/832e1406-a8d3-4183-96a2-57aa627c74cc?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Notion’s mobile team’s testing philosophy
([50:18](https://substack.com/redirect/a171ace9-bf14-4c1b-a720-3c3eae37cc14?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) How the mobile team keeps compile time so fast
([52:36](https://substack.com/redirect/9921eb37-21a9-4475-a731-36f79eed8ecd?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Modules in the iOS app
([54:50](https://substack.com/redirect/78396052-e0cf-4a0e-a299-c5bbc0ea3659?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Modules in the Android app
([56:44](https://substack.com/redirect/9ef7508a-aecf-4e96-ad08-ced309f74b0e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Behind the scenes of an app release and the public beta
([1:00:34](https://substack.com/redirect/59969587-4270-4f60-a4a5-3485412077d8?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Practices around feature flags
([1:03:00](https://substack.com/redirect/f18454dd-ea37-45fd-a0a5-085c359bfca0?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The four dev environments at Notion
([1:04:48](https://substack.com/redirect/20cdf532-240b-488e-ae8e-857791293d42?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) How development apps work
([1:07:40](https://substack.com/redirect/85c38b50-0ba2-46ba-91eb-1b9ffec93fe5?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) How and why you can work offline in Notion mobile
([1:10:24](https://substack.com/redirect/1946ab60-1b90-4941-a2bd-8f8728114d65?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Austin and Karn’s thoughts on the future of mobile engineering
([1:12:47](https://substack.com/redirect/a813797a-44e0-48c3-b2d8-9a640ab5729e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Advice for junior engineers
([1:16:29](https://substack.com/redirect/831cc35d-4526-4a22-ad02-fde7cec2727f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Rapid fire round
The Pragmatic Engineer deepdives relevant for this episode:
•
Where to find Austin Louden:
• GitHub: [https://github.com/austinlouden](https://substack.com/redirect/bfa3d154-573e-41a4-bbc0-751559be67b4?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• LinkedIn: [https://www.linkedin.com/in/austinlouden](https://substack.com/redirect/749ac448-b84e-4836-878b-30e696eefa89?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Website: [https://austinlouden.com/](https://substack.com/redirect/2575899b-06b5-4110-89ba-8a74a02f2df8?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
Where to find Karn Saheb:
• GitHub: [https://github.com/Karn](https://substack.com/redirect/ff75e0e0-aeab-4b00-b183-6b6c2699be5a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• LinkedIn: [https://github.com/Karn](https://substack.com/redirect/ff75e0e0-aeab-4b00-b183-6b6c2699be5a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Website: [https://karn.io](https://substack.com/redirect/5c9757b8-33c2-43b6-b295-752d2339cc11?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
Mentions during the episode:
• How Notion Uses Notion: [https://www.notion.com/blog/how-notion-uses-notion](https://substack.com/redirect/512eabf2-e031-45e1-b54f-bcd93773afee?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Cordova: [https://cordova.apache.org](https://substack.com/redirect/1cd951a1-516b-480f-99e9-a2e843fb0108?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• React Native: [https://reactnative.dev](https://substack.com/redirect/fe079ced-b51b-4a1d-9f21-55b47cc47114?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Coinbase: [https://www.coinbase.com](https://substack.com/redirect/d1e522a4-5413-4644-825d-ee63578a5b3f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• SQLite: [https://www.sqlite.org](https://substack.com/redirect/89909263-fef5-48b8-b820-ee0dd83eb571?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Swift: [https://www.swift.org](https://substack.com/redirect/3251285d-6c23-48ba-a8b7-784028b9690e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Webview: [https://developer.microsoft.com/en-us/microsoft-edge/webview2](https://substack.com/redirect/33c3c92c-ea6e-46e8-83ab-d6571b606f67?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Combine: [https://developer.apple.com/documentation/combine](https://substack.com/redirect/cde17feb-82f6-4365-817b-52a1b8125357?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Compose: [https://www.jetbrains.com/compose-multiplatform](https://substack.com/redirect/5f8a3b03-5d96-4a6f-9b60-509e258b9cfa?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Stacked Diffs (and why you should know about them): [https://newsletter.pragmaticengineer.com/p/stacked-diffs](https://substack.com/redirect/879a52f1-0f46-47ec-a931-0c68eaab0bbd?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Graphite: [https://graphite.dev](https://substack.com/redirect/1fe73644-5455-47d3-a180-f1dcc6f38261?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Bazel: [https://bazel.build](https://substack.com/redirect/ff320fce-8746-4321-ae4c-67f7bf346154?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Buck: [https://buck.build](https://substack.com/redirect/b5d774fc-502b-48e1-8f84-0fad4617ccb0?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Point Free: [https://www.pointfree.co](https://substack.com/redirect/0b8b75ef-a5d4-4e47-8b7a-595a7b2acc4e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Cursor: [https://www.cursor.com](https://substack.com/redirect/980bc906-8d23-48b1-a9e0-37808f3bbf6c?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Objective-C: [https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html](https://substack.com/redirect/49229a8c-6570-48f8-ba0f-d4d0c0e6f61c?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Skunk Works: A Personal Memoir of My Year at Lockheed: [https://www.amazon.com/Skunk-Works-Personal-Memoir-Lockheed/dp/0316743305](https://substack.com/redirect/f7fc6f2e-1d22-4e51-ad80-522aff221473?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Lockheed SR-71 Blackbird: [https://en.wikipedia.org/wiki/Lockheed_SR-71_Blackbird](https://substack.com/redirect/fdf7968b-862f-4d9d-a83d-e60bb095c820?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• A Philosophy of Software Design: [https://www.amazon.com/Philosophy-Software-Design-2nd/dp/173210221X](https://substack.com/redirect/a7ea5678-3a0d-425a-85ad-80016d83d880?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Building Mobile Apps at Scale: 39 Engineering Challenges: [https://www.amazon.com/Building-Mobile-Apps-Scale-Engineering/dp/1638778868](https://substack.com/redirect/410ab6f2-749f-406b-a6f1-c1fa46d11b6b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
Production and marketing by [https://penname.co/](https://substack.com/redirect/049632a9-b1ab-4b2a-ac04-b83616b395ce?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). For inquiries about sponsoring the podcast, email podcast@pragmaticengineer.com.
You’re on the free list for [The Pragmatic Engineer](https://substack.com/redirect/2/eyJlIjoiaHR0cHM6Ly9uZXdzbGV0dGVyLnByYWdtYXRpY2VuZ2luZWVyLmNvbT91dG1fY2FtcGFpZ249ZW1haWwtaG9tZSZyPThvNTRuIiwicCI6MTUyODA3MTQ4LCJzIjo0NTg3MDksImYiOnRydWUsInUiOjE0NTYzMzE5LCJpYXQiOjE3MzM5NDE5MzAsImV4cCI6MTczNjUzMzkzMCwiaXNzIjoicHViLTAiLCJzdWIiOiJsaW5rLXJlZGlyZWN0In0.HJ-Yk4ivsLNLgqIyS0diJC-zgOf-4IxSKRAV82pWBow?). For the full experience, [become a paying subscriber](https://substack.com/redirect/2/eyJlIjoiaHR0cHM6Ly9uZXdzbGV0dGVyLnByYWdtYXRpY2VuZ2luZWVyLmNvbS9zdWJzY3JpYmU_dXRtX3NvdXJjZT1wb3N0JnV0bV9jYW1wYWlnbj1lbWFpbC1jaGVja291dCZuZXh0PWh0dHBzJTNBJTJGJTJGbmV3c2xldHRlci5wcmFnbWF0aWNlbmdpbmVlci5jb20lMkZwJTJGbm90aW9uLWdvaW5nLW5hdGl2ZS1vbi1pb3MtYW5kLWFuZHJvaWQmcj04bzU0biZ0b2tlbj1leUoxYzJWeVgybGtJam94TkRVMk16TXhPU3dpYVdGMElqb3hOek16T1RReE9UTXdMQ0psZUhBaU9qRTNNelkxTXpNNU16QXNJbWx6Y3lJNkluQjFZaTAwTlRnM01Ea2lMQ0p6ZFdJaU9pSmphR1ZqYTI5MWRDSjkuYVE3ZmQ1cXpFd09KZ0hZQkNOckhfU3Z1Y01rVnZmLS1ZcTNoYzFuNFRnUSIsInAiOjE1MjgwNzE0OCwicyI6NDU4NzA5LCJmIjp0cnVlLCJ1IjoxNDU2MzMxOSwiaWF0IjoxNzMzOTQxOTMwLCJleHAiOjE3MzY1MzM5MzAsImlzcyI6InB1Yi0wIiwic3ViIjoibGluay1yZWRpcmVjdCJ9.s-vzBpJVQg0SP-s1S0ytEWpU2xIgAK_htG8GcAl7XVo?). Many readers expense this newsletter within their company’s training/learning/development budget.
This post is public, so feel free to share and forward it.
If you enjoyed this post, you might enjoy my book, [The Software Engineer's Guidebook](https://substack.com/redirect/0f4141ab-d077-4350-a3b9-e701caa8f7be?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). Here is what Tanya Reilly, senior principal engineer and author of The Staff Engineer's Path said about it:
"From performance reviews to P95 latency, from team dynamics to testing, Gergely demystifies all aspects of a software career. This book is well named: it really does feel like the missing guidebook for the whole industry."