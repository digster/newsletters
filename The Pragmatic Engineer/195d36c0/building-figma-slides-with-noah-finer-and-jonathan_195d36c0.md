---
subject: "Building Figma Slides with Noah Finer and Jonathan Kaufman"
from: "The Pragmatic Engineer <pragmaticengineer@substack.com>"
to: ""
date: 2025-03-26 17:05:12
labels: ["CATEGORY_PERSONAL", "INBOX", "The Pragmatic Engineer"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_6413324878686416177"]
---
|
Listen and watch now on [YouTube](https://substack.com/redirect/c922542a-f940-4ae2-b791-1b891489fb69?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), [Spotify](https://substack.com/redirect/cffd5615-a4d2-42a4-9460-3469fd1ad673?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) and [Apple](https://substack.com/redirect/8d169aef-53b3-41f1-899a-905c44f72132?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). See the episode transcript at the top of this page, and a summary at the bottom.
[Graphite](https://substack.com/redirect/6d02add1-b8bb-4933-8b82-3a51a14cb049?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)— The AI developer productivity platform.[Sonar](https://substack.com/redirect/37f1ff3d-6c91-4f58-96d1-20698d326d6c?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)— Code quality and code security for ALL code.[Chronosphere](https://substack.com/redirect/96095809-0512-4b6e-9f91-a55fd378705c?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)— The observability platform built for control.
—
How do you take a new product idea, and turn it into a successful product? [Figma Slides](https://substack.com/redirect/4921a3a9-d63a-4a72-a18e-43260a1fd552?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) started as a hackathon project a year and a half ago – and today it’s a full-on product, with more than 4.5M slide decks created by users. I’m joined by two founding engineers on this project: [Jonathan Kaufman](https://substack.com/redirect/e07ea9cf-916c-44c0-9f42-d0cbc26c8b5e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) and [Noah Finer](https://substack.com/redirect/9d300963-901f-44ed-adfe-b3afaec0d021?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).
In our chat, Jonathan and Noah pull back the curtain on what it took to build Figma Slides. They share engineering challenges faced, interesting engineering practices utilized, and what it's like working on a product used by millions of designers worldwide.
We talk about:
An overview of Figma Slides
The tech stack behind Figma Slides
Why the engineering team built grid view before single slide view
How Figma ensures that all Figma files look the same across browsers
Figma’s "vibe testing" approach
How beta testing helped experiment more
The “all flags on”, “all flags off” testing approach
Engineering crits at Figma
And much more!
My biggest takeaways from this conversation:
1. Figma’s web app uses a surprising amount of C++ code. It’s rare for web engineers to need to use C++ — but Figma is an exception, as the design tool built their own rendering engine. This means that frontend engineers need to get into the opinionated C++ codebase to make changes — though rewriting some parts of the code to TypeScript is currently on the way.
2. The “EngCrit” process is an interesting — and unique! — one. Figma’s engineering reviews/discussions are called EngCrit. An engineer presents their plan or idea in a FigJam board, and other engineers join in to give their feedback. This process has parallels with the [RFC or design doc process](https://substack.com/redirect/0c8f029b-49f0-423f-a0b6-193a1a46ce13?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) — but it feels a lot more lightweight. Plus, it dogfoods Figma’s own products!
3. Some of the most straightforward UI parts are the most involved ones. It was interesting to learn that one of the most complicated pieces of the web app was the Single Slide View. This seemingly simple interface:
The reason for the complexity was how this view is actually a zoomed in version of the grid view — this one:
There are several reasons that the team decided to do this “zoomed in trick:” one of them is that when multiple people are editing a slide, zooming in means that the cursors for these other users show up both on the slide view and on the grid view.
This detail is a good reminder that a simple UI can hide a complex implementation.
([00:00](https://substack.com/redirect/786f780f-5470-4ea1-877f-a4403d59aa69?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Intro
([01:45](https://substack.com/redirect/5461faa3-9ffb-4e9f-b87b-38a3a90b2155?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) An overview of Figma Slides and the first steps in building it
([06:41](https://substack.com/redirect/5e3aaf6a-6a86-4255-9f68-811718c36b0e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Why Figma built grid view before single slide view
([10:00](https://substack.com/redirect/6055eae3-0b38-4871-8f73-32bdf405130e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The next steps of building UI after grid view
([12:10](https://substack.com/redirect/0abea002-c9fb-42e3-9ce3-ede5ea14f776?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The team structure and size of the Figma Slides team
([14:14](https://substack.com/redirect/644348d9-22c3-43bf-9bba-f57fb8fdb916?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The tech stack behind Figma Slides
([15:31](https://substack.com/redirect/a5869fc7-baa6-4638-b153-8cd8ea5be045?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) How Figma uses C++ with bindings
([17:43](https://substack.com/redirect/7304a635-f721-47ac-a5e1-26bd10328ef9?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The Chrome debugging extension used for C++ and WebAssembly
([21:02](https://substack.com/redirect/3b8dcfce-5a5e-477f-b8ec-df548b566531?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) An example of how Noah used the debugging tool
([22:18](https://substack.com/redirect/7861dfa1-9336-47bf-a791-00ab23695a85?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Challenges in building Figma Slides
([23:15](https://substack.com/redirect/73d4335f-ebbb-4435-8254-14bc2c0daed7?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) An explanation of multiplayer cursors
([26:15](https://substack.com/redirect/cb96513f-94c3-4160-8b2b-92b05fe95b37?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Figma’s philosophy of building interconnected products—and the code behind them
([28:22](https://substack.com/redirect/17d51ceb-2ad0-47af-b056-f3c263fb6a4a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) An example of a different mouse behavior in Figma
([33:00](https://substack.com/redirect/27d67f96-a506-4221-a689-682ea832d4cd?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Technical challenges in developing single slide view
([35:10](https://substack.com/redirect/e613d02b-51f9-4196-be9f-6e9d38f3913e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Challenges faced in single-slide view while maintaining multiplayer compatibility
([40:00](https://substack.com/redirect/2bd9ee69-1a9f-483c-b89e-4626dc85ba12?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The types of testing used on Figma Slides
([43:42](https://substack.com/redirect/6a71250e-4b4f-4fb8-bb6f-60851d3f7dbd?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Figma’s zero bug policy
([45:30](https://substack.com/redirect/fd26189d-6233-4c8f-9d62-47857d21430d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The release process, and how engineering uses feature flags
([48:40](https://substack.com/redirect/a1fd4da9-c8fd-4499-bb75-0240c09f89c5?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) How Figma tests Slides with feature flags enabled and then disabled
([51:35](https://substack.com/redirect/eca2c6b0-a676-4e8b-bd3b-62d665348f45?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) An explanation of eng crits at Figma
([54:53](https://substack.com/redirect/7141ad63-b27f-4793-bbda-27aab1424426?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Rapid fire round
The initial development took about 6 months, starting at a hackathon in late 2023 and the beta launch in April 2024. The public launch happened a week ago, on 19 March.
Phasing of the project
“Slide grid:” the first concept built on a hack week
The initial development was about getting the two-way navigation right between the grid view and the single slide view.
Single slide view construction happened later, around 6 months into the project.
Single slide view operates by zooming into the infinite canvas and hiding elements, maintaining the 2D space. Clever!
User researcher part of the team: this was surprising to hear! The researcher helped a lot with getting the direction of the project right – building something designers would find intuitive to use
Figma's core editors use a C++ codebase and custom renderer outputting to a <canvas> element via WebGL or WebGPU.
UI elements outside the canvas use TypeScript and React.
A "bindings layer" enables communication between the C++ codebase and the web UI.
The C++ codebase
Some engineers join with C++ experience; others learn on the job.
Both Jon and Noah learned C++ on the job, for the most part!
The C++ codebase has a learning curve, similar to game engine development.
Rewriting some C++ to Typescript
Figma is rewriting parts of the C++ codebase into TypeScript, using the bindings layer.
Interactive elements like plus buttons use TypeScript to interact with the C++ canvas.
Tooling for debugging
A Chrome extension called
[DWARF debugging](https://substack.com/redirect/71cc0f8c-5a8c-4e9e-946b-c1fc552b4ce8?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)is a powerful tool the team usesThis extension debugs C++ code within Chrome Inspector, even as WebAssembly, similar to JavaScript source maps.
Breakpoints can be set in TypeScript/React and C++ WebAssembly for debugging interactions.
This tooling helps find intricate bugs between the UI and the core editor.
Previously, C++ debugging involved running a special build in Xcode.
Figma has an internal "web bisect" tool using commit previews to identify bug-introducing commits. A very helpful tool!
Testing: the team does a lot of this.
They run all unit and interaction tests with flags off and then on. Another clever approach
This practice helps prevent regressions caused by specific feature flags.
Feature flags: extensively used. The product has more than 2,000 of these.
Developers have an internal panel to manage feature flags locally and in staging.
Staging: a dedicated staging environment used for testing. Features in this environment are enabled via flags. Staging is used to get early product feedback
Alpha launch: this was done for Slides by involving select customers
Eng Crits: asynchronous feedback via sticky notes in FigJam, followed by discussion.
Zero bug policy
Figma has a "zero bug policy" for new developments, prioritising fixes after launch
The on-call process triages feedback, and addresses reported issues promptly.
Beta phase: this 11-month long period prioritized critical bugs affecting core experience before the broader launch.
Single slide view implementation as viewport manipulation presented unique challenges.
This approach allows existing multiplayer cursor functionality in both views.
Multiplayer uses a server-side Rust service for edit propagation and conflict resolution via WebSockets.
Ensuring "interop" between Figma products
Ensuring products like Design, FigJam, and Slides work nicely with one another
Supporting interop means new node types must function across editors.
What makes it easier is how the underlying C++ codebase is largely shared across editors.
Differences in interactions use "mouse behaviors", editor-specific implementations for mouse actions. The mouse behavior concept comes from game engine architectures.
Custom text rendering
Figma has custom text rendering for consistency across browsers and operating systems.
This means that in-house development is needed for features like spellcheck – something that comes for free for web apps using the DOM!
Managing a collapsed state in a single slide view without file persistence was a state management problem.
Reordering slides in single slide view with multiplayer
To do so: state mutations needed to be minimized
The solution used existing auto layout nodes, with each slide row as a node within a grid node
Reordering manipulates the "parent index" of row nodes, minimizing mutations
Testing complex multiplayer interactions
This was difficult to do! It’s hard to reproduce problematic multi-user scenarios
Extensive unit tests are put in-place for grid reconciliation. These cover past bug scenarios and assert expected mutations. (This is a clever way to ensure fewer regressions!)
Where to find Jonathan Kaufman:
• LinkedIn: [https://www.linkedin.com/in/jkaufman5/](https://substack.com/redirect/e07ea9cf-916c-44c0-9f42-d0cbc26c8b5e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Website: [https://www.jkaufman.io/](https://substack.com/redirect/fa185e2a-1188-44c6-bd81-7be743841faa?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
Where to find Noah Finer:
• LinkedIn: [https://www.linkedin.com/in/noahfiner/](https://substack.com/redirect/9d300963-901f-44ed-adfe-b3afaec0d021?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Website: [https://noahfiner.com/](https://substack.com/redirect/51a220ca-7911-470b-80dc-4145db174477?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
Mentions during the episode:
• Figma: [https://www.figma.com/](https://substack.com/redirect/88615883-9805-4479-9b41-d4794180b9a4?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Figma Slides: [https://www.figma.com/slides/](https://substack.com/redirect/4921a3a9-d63a-4a72-a18e-43260a1fd552?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Config: [https://config.figma.com/](https://substack.com/redirect/51e219da-152c-4ab4-9a89-d7f13d705bfd?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• FigJam: [https://www.figma.com/figjam/](https://substack.com/redirect/2ecb9969-3d70-4087-9c2a-2f72be0a570d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• C++: [https://en.wikipedia.org/wiki/C%2B%2B](https://substack.com/redirect/79e06f90-3a51-4379-9921-72d4b6bb9f0c?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Typescript: [https://www.typescriptlang.org/](https://substack.com/redirect/f652b6df-06e9-46f3-b575-1bf4a505bd5c?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• React: [https://react.dev/](https://substack.com/redirect/3b35d62e-8997-4de8-8e0c-f4a247a292c2?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Debug C/C++ WebAssembly: [https://developer.chrome.com/docs/devtools/wasm](https://substack.com/redirect/71cc0f8c-5a8c-4e9e-946b-c1fc552b4ce8?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Xcode: [https://developer.apple.com/xcode/](https://substack.com/redirect/11f78617-8da5-4a1d-ad23-f04b46fa14d5?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Multiplayer cursors: [https://www.figma.com/community/file/1267761575266415196/multiplayer-cursors](https://substack.com/redirect/b9b2ca60-c857-4618-b61a-5baa797cac8e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• How Figma’s multiplayer technology works: [https://www.figma.com/blog/how-figmas-multiplayer-technology-works/](https://substack.com/redirect/619ad232-7d53-46f5-943f-df125b89879e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Design-first software engineering: Craft – with Balint Orosz: [https://newsletter.pragmaticengineer.com/p/design-first-software-engineering](https://substack.com/redirect/f28d4622-c0a9-4e9f-8c7a-021f8d1dcb58?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Reconciliation: [https://legacy.reactjs.org/docs/reconciliation.html](https://substack.com/redirect/70598b93-f5cc-4773-ba77-a497a300c048?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Inside Figma’s Engineering Culture: [https://newsletter.pragmaticengineer.com/p/inside-figmas-engineering-culture](https://substack.com/redirect/7691c344-6dd1-4694-9d14-436e54f67391?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• How we engineer feedback at Figma with eng crits: [https://www.figma.com/blog/how-we-run-eng-crits-at-figma/](https://substack.com/redirect/befc927a-20a8-4bd8-932f-92818331bd5c?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Nextjs: [https://nextjs.org/](https://substack.com/redirect/bb807e1b-ca3c-426a-9756-dd9fed872f98?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Hacker News: [https://news.ycombinator.com/](https://substack.com/redirect/b0953169-88c7-4a30-b0f6-bcda5e3b3501?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Refactoring UI: [https://www.refactoringui.com/](https://substack.com/redirect/56139b2c-4213-4378-a2d9-6e81d7dfad58?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Tailwind: [https://tailwindcss.com/](https://substack.com/redirect/d72d3cae-d89b-4179-bf4d-a0af9e1b33ef?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Adam Wathan’s website: [https://adamwathan.me/](https://substack.com/redirect/058073f2-eeaf-4bb6-9287-76cf2ca20b31?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Steve Schoger’s website: [https://www.steveschoger.com/](https://substack.com/redirect/ec4af67c-acdc-421f-90ad-c53a29580f68?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Piranesi: [https://www.amazon.com/Piranesi-Susanna-Clarke/dp/1635577802/](https://substack.com/redirect/67b9edc6-d7be-4f13-bbb1-632e89748e65?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Immune: A Journey into the Mysterious System That Keeps You Alive: [https://www.amazon.com/Immune-Kurzgesagt-gorgeously-illustrated-immune/dp/1529360684](https://substack.com/redirect/a40a3cfe-351d-4973-bca7-2f9bd5b87db8?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
—
Production and marketing by [Pen Name](https://substack.com/redirect/e8fcdffe-4358-4aea-a76f-49cc26f9f6ec?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). For inquiries about sponsoring the podcast, email podcast@pragmaticengineer.com.
You’re on the free list for [The Pragmatic Engineer](https://substack.com/redirect/2/eyJlIjoiaHR0cHM6Ly9uZXdzbGV0dGVyLnByYWdtYXRpY2VuZ2luZWVyLmNvbT91dG1fY2FtcGFpZ249ZW1haWwtaG9tZSZyPThvNTRuIiwicCI6MTU5NzE4MjI2LCJzIjo0NTg3MDksImYiOnRydWUsInUiOjE0NTYzMzE5LCJpYXQiOjE3NDMwMDg4MjYsImV4cCI6MTc0NTYwMDgyNiwiaXNzIjoicHViLTAiLCJzdWIiOiJsaW5rLXJlZGlyZWN0In0.IS3W9AfMxirF4U_wfIIxhu67k3V83_EgWXeQy04F9uE?). For the full experience, [become a paying subscriber](https://substack.com/redirect/2/eyJlIjoiaHR0cHM6Ly9uZXdzbGV0dGVyLnByYWdtYXRpY2VuZ2luZWVyLmNvbS9zdWJzY3JpYmU_dXRtX3NvdXJjZT1wb3N0JnV0bV9jYW1wYWlnbj1lbWFpbC1jaGVja291dCZuZXh0PWh0dHBzJTNBJTJGJTJGbmV3c2xldHRlci5wcmFnbWF0aWNlbmdpbmVlci5jb20lMkZwJTJGYnVpbGRpbmctZmlnbWEtc2xpZGVzLXdpdGgtbm9haC1maW5lciZyPThvNTRuJnRva2VuPWV5SjFjMlZ5WDJsa0lqb3hORFUyTXpNeE9Td2lhV0YwSWpveE56UXpNREE0T0RJMkxDSmxlSEFpT2pFM05EVTJNREE0TWpZc0ltbHpjeUk2SW5CMVlpMDBOVGczTURraUxDSnpkV0lpT2lKamFHVmphMjkxZENKOS5jbUZrSnlpSHFycGd6bVVMUnBKNGRaVFZLaU9sTDcyY0RMbFV6blZ1RWhJIiwicCI6MTU5NzE4MjI2LCJzIjo0NTg3MDksImYiOnRydWUsInUiOjE0NTYzMzE5LCJpYXQiOjE3NDMwMDg4MjYsImV4cCI6MTc0NTYwMDgyNiwiaXNzIjoicHViLTAiLCJzdWIiOiJsaW5rLXJlZGlyZWN0In0.DjrUb07bZWSCXofz42pXq7NL6pVGs3o-QSDKoTIgJAo?). Many readers expense this newsletter within their company’s training/learning/development budget.
This post is public, so feel free to share and forward it.
If you enjoyed this post, you might enjoy my book, [The Software Engineer's Guidebook](https://substack.com/redirect/039bc300-5703-487c-a8b8-bd66ad3a2526?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). Here is what Tanya Reilly, senior principal engineer and author of The Staff Engineer's Path said about it:
"From performance reviews to P95 latency, from team dynamics to testing, Gergely demystifies all aspects of a software career. This book is well named: it really does feel like the missing guidebook for the whole industry."