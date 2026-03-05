---
subject: "Design-first software engineering: Craft – with Balint Orosz"
from: "The Pragmatic Engineer <pragmaticengineer@substack.com>"
to: ""
date: 2025-03-05 18:18:32
labels: ["CATEGORY_PERSONAL", "INBOX", "The Pragmatic Engineer", "UNREAD"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_6413324878686416177", "UNREAD"]
---
|
Listen and watch now on [YouTube](https://substack.com/redirect/c6065c69-a857-4b1b-bf00-9ab3f8360929?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), [Apple](https://substack.com/redirect/318d7598-3ee5-4d19-bb81-da1500ac5cfb?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) and [Spotify](https://substack.com/redirect/a76137e0-f726-48fa-bd67-427f05aae1f1?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). See the episode transcript at the top of this page, and a summary at the bottom.
[WorkOS](https://substack.com/redirect/67d2f5f3-8d30-4276-8fa5-c72137954557?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)— The modern identity platform for B2B SaaS.[The Software Engineer’s Guidebook](https://substack.com/redirect/11e686d0-026c-4741-8520-06c66b98af25?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o): Written by me (Gergely) – now out in audio form as well[Augment Code](https://substack.com/redirect/ae96a14e-52a3-4bf5-8b8d-5b7ba4ea4c3e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)— AI coding assistant that pro engineering teams love
—
Not many people know that I have a brother: [Balint Orosz](https://substack.com/redirect/421359e1-3de7-43c3-ad70-f0f08ba7664b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). Balint is also in tech, but in many ways, is the opposite of me. While I prefer working on backend and business logic, he always thrived in designing and building UIs. While I opted to work at more established companies, he struck out on his own and started his startup, Distinction. And yet, our professional paths have crossed several times: at one point in time I accepted an offer to join Skyscanner as a Principal iOS Engineer – and as part of the negotiation, I added a clause to my contrac that I will not report directly or indirectly to the Head of Mobile: who happened to be my brother, thanks to Skyscanner acquiring his startup the same month that Skyscanner made an offer to hire me.
Today, Balint is the founder and CEO of [Craft](https://substack.com/redirect/61157e97-b1cc-4801-ae42-4dd7710ee2c0?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), a beloved text editor known for its user-friendly interface and sleek design – an app that Apple awarded the prestigious Mac App of the Year in 2021.
In our conversation, we explore how Balint approaches building opinionated software with an intense focus on user experience. We discuss the lessons he learned from his time building Distinction and working at Skyscanner that have shaped his approach to Craft and its development.
In this episode, we discuss:
Balint’s first startup, Distinction, and his time working for Skyscanner after they acquired it
A case for a balanced engineering culture with both backend and frontend priorities
Why Balint doesn’t use iOS Auto Layout
The impact of Craft being personal software on front-end and back-end development
The balance between customization and engineering fear in frontend work
The resurgence of local-first software and its role in modern computing
The value of building a physical prototype
How Balint uses GenAI to assist with complicated coding projects
And much more!
Design-focused engineers find it harder to fit in. Engineers who focus on backend and distributed systems can usually verbalize their impact clearer, and could see faster career growth – including getting into leadership positions. This creates a reinforcing cycle: as most engineering executives have a backend engineering background: they will recognize and reward backend contributions more.
Balint didn’t like how he didn’t “fit in” as an engineer focused on design and UI: but he just kept building things he believed in – and years later, building up that “design muscle” helps him build products that backend-focused engineers might struggle in putting together.
Amazing companies cannot have a single engineering culture. Balint observed how every standout company that has a single engineering culture inherently biases towards either a backend-heavy engineering culture (e.g. Google, Amazon) or a UI-heavy one (Amazon). For a company to be truly standout – more so than these Big Tech giants – it needs to have several engineering cultures: prioritizing both backend and UI excellence. This is what Craft is aiming to do internally.
To build something better than most other products: you might need to take a different approach. Craft does not use Apple’s UI components: they don’t use SwiftUI or Autolayout – something that 95% or more of iOS apps all take advantage of.
Craft, instead, built their own components from scratch, and came up with their own layout and animations system. This is a lot more work at first: but it’s how Craft can do smooth animations that most apps are unable to do so – and it’s a reason engineers at Apple have asked the team “how are you able to do such a smooth animation on the navigation bar?” (The native iOS navigation bar cannot be animated like Craft does it) Craft can do all this thanks to building and maintaining their own components. It’s simpler to do than most would assume: in the episode, we look at actual code.
A shared codebase is an underrated advantage for speed, consistency and efficiency. Craft has a total of 4 engineers building the respective apps for:
iOS
iPad
MacOS
VisionOS
They can do this, because it’s a single codebase! A single codebase also means that all features built on one platform immediately work on all others.
([00:00](https://substack.com/redirect/38c2dedf-7d9a-4cd8-83d6-903bc208594e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Intro
([02:13](https://substack.com/redirect/e6396407-3a5f-482f-bd69-f8b657a7eeb3?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) What it’s like being a UX-focused founder
([09:00](https://substack.com/redirect/c5c5f0e5-fd04-4ae9-a2f2-d2b972f39aa7?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Why it was hard to gain recognition at Skyscanner
([13:12](https://substack.com/redirect/45ca4d16-e9bb-4c71-b299-5f87488d3fe6?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Takeaways from Skyscanner that Balint brought to Craft
([16:50](https://substack.com/redirect/d9568770-c4cd-45fe-9f93-16e01452c703?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) How frameworks work and why they aren’t always a good fit
([20:35](https://substack.com/redirect/3c35f489-f32e-4fdd-bf23-3bc70a043e14?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) An explanation of iOS Auto Layout and its pros and cons
([23:13](https://substack.com/redirect/74ca1670-f1e7-468e-8808-27b82b65d961?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Why Balint doesn’t use Auto Layout
([24:23](https://substack.com/redirect/809e666f-6307-4698-aeb1-6a288f410098?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Why Craft has one code base
([27:46](https://substack.com/redirect/bc5c2e89-42d2-4890-8633-efc89d7eec58?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Craft’s unique toolbar features and a behind the scenes peek at the code
([33:15](https://substack.com/redirect/62d245ce-fa10-44ec-95a5-36e737b5cd15?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Why frontend engineers have fear around customization
([37:11](https://substack.com/redirect/f51a7fe1-d52a-4b3d-a09b-f81bd8343d79?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) How Craft’s design system differs from most companies
([42:33](https://substack.com/redirect/9ce6cef2-e920-46b7-af04-c61ce02a0da0?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Behaviors and elements Craft uses rather than having a system for everything
([44:12](https://substack.com/redirect/52052f57-22e6-41a1-b149-736487eef6ed?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The back and frontend architecture in building personal software
([48:11](https://substack.com/redirect/bb971788-1fac-40f2-9bfd-2dacd68b6d5f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Shifting beliefs in personal computing
([50:15](https://substack.com/redirect/e99b7e51-f770-4e84-90fc-f06c42a4be0d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The challenges faced with operating system updates
([50:48](https://substack.com/redirect/3fe1c1b8-3f93-4b11-bd3c-f1ca461615fb?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The resurgence of local-first software
([52:31](https://substack.com/redirect/6f891bd3-3c49-4b2c-a605-2859a7da5dbc?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The value of opinionated software for consumers
([55:30](https://substack.com/redirect/22150684-5bbc-4a76-9cd1-087a3c34f426?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Why Craft’s focus is on the user’s emotional experience
([56:50](https://substack.com/redirect/6e951f49-e701-41b5-9890-638413037847?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The size of Craft’s engineering department and platform teams
([59:20](https://substack.com/redirect/225195ef-f979-4794-aae4-e0830fe8d535?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Why Craft moves faster with smaller teams
([1:01:26](https://substack.com/redirect/c7356e54-bc7c-41a6-b4ed-3ba6cd4022b7?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Balint’s advice for frontend engineers looking to demonstrate value
([1:04:35](https://substack.com/redirect/ceb530a7-d426-4315-ab75-14150ac82f6e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Balint’s breakthroughs using GenAI
([1:07:50](https://substack.com/redirect/20885253-e8ec-40e9-bcb1-1dfd2573b45f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Why Balint still writes code
([1:09:44](https://substack.com/redirect/64e075b2-daef-4212-a97c-4e988059ef3d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Rapid fire round
Balint has been writing code since he was 12. He’s always had a pull towards interactivity, animation, and found himself in the intersection of code and design.
Backend engineering is much easier to quantify than UI/UX work. Balint always felt that backend engineering was easier to quantify in impact – like saving millions in infrastructure costs or scaling to billions of users. How do you quantify that the UI is smooth and delightful?
Balint always felt that "hardcore engineers" did not consider him one of them – as his focus was on UX and UI – like making interactions faster, and animations smoother, and not on distributed systems or scalable algorithms. But designers and product managers also didn’t look at him as equals.
There’s a pull for engineers to move towards the backend and distributed systems. Exactly because these areas are seen as having hard problems to solve and are often more measurable in terms of impact.
Craft started off as a text editor for mobile use. When starting to code the product, Balint didn't believe that established engineering patterns, code coverage, or even design components would be the right approach.
Principles in building craft:
Data principles: efficiency and zero data loss are both non-negotiatble. There’s not much to innovate in this area – it’s very well understood! Just refine the existing state of the art.
Fluency. Craft is designed to be used for hours each day, so it needs to feel snappy and fluent.
Having just one engineering culture is not enough. To create an amazing product, you cannot have either frontend or backend engineering principles dominate:
When the dominant engineering culture is UI-first: Apple is a good example. Apple builds delightful user experiences. However, their backend systems and web products are lacking.
When the dominant engineering culture is backend-first: Amazon and Google are good examples. Both focus on system design and backend engineering principles – in return their UIs don't feel as comfortable.
Craft uses the same codebase across 4 platforms: iOS, iPad, MacOS (desktop), and Vision Pro. 99% of the code is common, with some additional native bindings for each platform. Why the same codebase? Balint wanted the desktop app to always do the same thing as the mobile app, and a shared code base was the best way to do it.
Craft's product engineering team is around 20 people. This includes product engineering, design, and QA.
They are split into a platform team, which means they have a web team, a native app team, and a backend team. Each of those teams has three to four people.
Balint observed that teams with more than 5 people start to have communications issues
Prioritize control over abstractions and trends. Using core language patterns and framework elements gives you more control over what you want to do. High-level abstractions and frameworks require more time figuring out the bugs and what those frameworks allow or disallow.
Everything is a canvas. Craft treats everything as a canvas that they draw on. This allows building toolbars that look exactly like a Mac toolbar on the Mac and an iOS toolbar on the iPhone. However, Craft now has more control over these components than if they used the native ones.
Avoiding AutoLayout and SwiftUI. Every time Craft hires a new iOS engineer, the new joiner inevitably asks them why they don't use new technologies like AutoLayout or SwiftUI. Balint shows them one of their transitions and asks them to implement it with the same performance in AutoLayout – and if they can succeed, they’ll move over. So far, no one has managed: but it’s a good exercise to help understand that decisions are not arbitrary, but are following practical purposes.
AutoLayout promises that you no longer need to think in rectangles; you can just say it should be at the top and it can automatically grow. However, when you keep adding more things, the complexity increases and when you want to do something more sophisticated, it can become very performance-intensive.
With AutoLayout, you are trading off easier definition and work as a developer for more complexity on the device and less control when you want to do more advanced animations.
“How it makes me feel” matters more. When it comes to personal software, consumers choose a lot more on which one they feel resonates with them. Thus the best personal software is a lot more opinionated than B2B software is
Craft is aiming to build what Visual Studio Code is for engineers – Craft aiming to do the same for knowledge workers. Visual Studio Code feels lightweight and is a fresh breath of air because it's responsive, fast, and does everything you need.
A different take on design systems.
Most companies create an “atomic design system:” starting with base colours as atoms, then buttons that combine colors and shapes as components, and then building up from here.
Craft, instead, has systems for animation. They have an animation engine and library that synchronizes everything across everyone and they enforce usage of that.
New technologies emerge on the server side. When you're dealing with personal software, the amount of content you're dealing with can fit on the user's device. A lot of the compute can be done locally.
Craft’s architecture is preparing for local-first approaches. They architected components so they can replace them with local or remote components anytime they decide it’s now possible to do so.
An example is search: instead of having a big elastic search cluster, they are looking at having 2 million search indexes on a disk in the cloud. Every time somebody does a search, they can either download that search index locally and use it there to execute the search, or a Lambda or serverless function can just read the search index.
The industry keeps swinging between cloud and local compute.
There is a new wave of personal computing powered by processors getting faster. The M4 Pro is a faster processor than anything you can buy on an AWS cloud.
Eventually, people will get tired of their personal computers holding them back and they’ll appreciate server-side components working faster. After a while, they will then start to get annoyed about how much the server-side project costs… and the pendulum keeps swinging
Local-first is experiencing a comeback because people are starting to travel again. It gets inconvenient when you need something badly, with poor connection – and you cannot access it.
Where to find Balint Orosz:
• X: [https://x.com/balintorosz](https://substack.com/redirect/9e06eea3-11e0-4a16-91ae-86a03fd4a2b5?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• LinkedIn: [https://www.linkedin.com/in/balintorosz/](https://substack.com/redirect/c64a118d-42e6-4497-8ca2-b9c36b2e9f3c?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
Mentions during the episode:
• Craft: [https://www.craft.do/](https://substack.com/redirect/61157e97-b1cc-4801-ae42-4dd7710ee2c0?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Skyscanner: [https://www.skyscanner.com/](https://substack.com/redirect/2f89505c-9605-4c4d-bd5b-ea842ef5903f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Flash: [https://en.wikipedia.org/wiki/Adobe_Flash](https://substack.com/redirect/5aff538c-92bb-46ea-8d91-c3a278e89e67?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Shader: [https://en.wikipedia.org/wiki/Shader](https://substack.com/redirect/8a5977a2-b812-4233-905c-20db80cdb378?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Understanding Auto Layout: [https://developer.apple.com/library/archive/documentation/UserExperience/Conceptual/AutolayoutPG/index.html](https://substack.com/redirect/b80118c8-fcb3-4415-9efb-0ae25768f04b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Mac Catalyst: [https://developer.apple.com/mac-catalyst/](https://substack.com/redirect/040b1d68-f638-4bc0-8b21-3b996ac7ffde?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Apple M1: [https://en.wikipedia.org/wiki/Apple_M1](https://substack.com/redirect/4dd83572-1611-4305-bac0-8ab933107d10?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Elasticsearch: [https://en.wikipedia.org/wiki/Elasticsearch](https://substack.com/redirect/209eaa5a-a2a0-4045-ad31-83c51efeb6d6?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• The Cloud Is a Prison. Can the Local-First Software Movement Set Us Free?: [https://www.wired.com/story/the-cloud-is-a-prison-can-the-local-first-software-movement-set-us-free/](https://substack.com/redirect/7cd5de4a-6b43-4ea0-ade9-bfa03a33f2b1?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Local-first software: [https://news.ycombinator.com/item?id=31594613](https://substack.com/redirect/093bf668-ff7a-4bec-b4cb-17175cf350e9?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Visual Studio Code: [https://code.visualstudio.com/](https://substack.com/redirect/736ca0b6-2d01-4c2e-968a-7314000c3228?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• ChatGPT 01 model: [https://openai.com/o1/](https://substack.com/redirect/2dc37b9a-dde0-449d-8cda-939c86a7ab54?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• PencilKit: [https://developer.apple.com/documentation/pencilkit](https://substack.com/redirect/68581297-7f67-488e-8bdd-0209d442f865?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Swift: [https://www.swift.org/](https://substack.com/redirect/1c1e9b90-99df-42e2-904a-9fa31954d05f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Objective-C: [https://en.wikipedia.org/wiki/Objective-C#](https://substack.com/redirect/53f95946-1a5b-4bd4-b62b-de2d7a60fbdb?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Tailwind CSS: [https://tailwindcss.com/](https://substack.com/redirect/f509c7e8-1a39-4354-9ecc-1e2c407d7d7d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• The Hard Thing About Hard Things: Building a Business When There Are No Easy Answers: [https://www.amazon.com/Hard-Thing-About-Things-Building/dp/0062273205](https://substack.com/redirect/ef7fc6aa-9935-4db2-a757-74859cdc6f55?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
—
Production and marketing by [Pen Name](https://substack.com/redirect/621d4364-c22f-4404-93c2-c38cb3dee671?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). For inquiries about sponsoring the podcast, email podcast@pragmaticengineer.com.
You’re on the free list for [The Pragmatic Engineer](https://substack.com/redirect/2/eyJlIjoiaHR0cHM6Ly9uZXdzbGV0dGVyLnByYWdtYXRpY2VuZ2luZWVyLmNvbT91dG1fY2FtcGFpZ249ZW1haWwtaG9tZSZyPThvNTRuIiwicCI6MTU4MzQ1MDc3LCJzIjo0NTg3MDksImYiOnRydWUsInUiOjE0NTYzMzE5LCJpYXQiOjE3NDExOTg3NTYsImV4cCI6MTc0Mzc5MDc1NiwiaXNzIjoicHViLTAiLCJzdWIiOiJsaW5rLXJlZGlyZWN0In0.eBQCybh8ocDtHJppN84ASzqu--7bOhKPEAc4fwbg-j8?). For the full experience, [become a paying subscriber](https://substack.com/redirect/2/eyJlIjoiaHR0cHM6Ly9uZXdzbGV0dGVyLnByYWdtYXRpY2VuZ2luZWVyLmNvbS9zdWJzY3JpYmU_dXRtX3NvdXJjZT1wb3N0JnV0bV9jYW1wYWlnbj1lbWFpbC1jaGVja291dCZuZXh0PWh0dHBzJTNBJTJGJTJGbmV3c2xldHRlci5wcmFnbWF0aWNlbmdpbmVlci5jb20lMkZwJTJGZGVzaWduLWZpcnN0LXNvZnR3YXJlLWVuZ2luZWVyaW5nJnI9OG81NG4mdG9rZW49ZXlKMWMyVnlYMmxrSWpveE5EVTJNek14T1N3aWFXRjBJam94TnpReE1UazROelUyTENKbGVIQWlPakUzTkRNM09UQTNOVFlzSW1semN5STZJbkIxWWkwME5UZzNNRGtpTENKemRXSWlPaUpqYUdWamEyOTFkQ0o5LllGYTFHTktjUlVsMVR5cXo2U0ZlbHY4Q0Y4Rm9QLUtIMkRoYXNfMmhTT1EiLCJwIjoxNTgzNDUwNzcsInMiOjQ1ODcwOSwiZiI6dHJ1ZSwidSI6MTQ1NjMzMTksImlhdCI6MTc0MTE5ODc1NiwiZXhwIjoxNzQzNzkwNzU2LCJpc3MiOiJwdWItMCIsInN1YiI6ImxpbmstcmVkaXJlY3QifQ.MLScGE7U2sj1rZV7mbgGhIksmNHactHC3Sd5e1bCikY?). Many readers expense this newsletter within their company’s training/learning/development budget.
This post is public, so feel free to share and forward it.
If you enjoyed this post, you might enjoy my book, [The Software Engineer's Guidebook](https://substack.com/redirect/043da8fc-76b9-4726-b069-d325788e96c5?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). Here is what Tanya Reilly, senior principal engineer and author of The Staff Engineer's Path said about it:
"From performance reviews to P95 latency, from team dynamics to testing, Gergely demystifies all aspects of a software career. This book is well named: it really does feel like the missing guidebook for the whole industry."