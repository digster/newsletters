---
subject: "How AI-assisted coding will change software engineering: hard truths"
from: "The Pragmatic Engineer <pragmaticengineer+deepdives@substack.com>"
to: ""
date: 2025-01-05 16:29:58
labels: ["CATEGORY_PERSONAL", "INBOX", "The Pragmatic Engineer", "UNREAD"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_6413324878686416177", "UNREAD"]
---
|
Hi, this is Gergely with a bonus issue of the Pragmatic Engineer Newsletter. In every issue, we cover topics related to Big Tech and startups through the lens of software engineers and engineering leaders. If you’ve been forwarded this email, you can [subscribe here](https://substack.com/redirect/b7fde7dd-7356-4c5b-9616-f337e435881a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).
Happy New Year! As we look toward the innovations that 2025 might bring, it is a sure bet that GenAI will continue to change how we do software engineering.
It’s hard to believe that just over two years ago in November of 2022 was ChatGPT’s first release. This was the point when large language models (LLMs) started to get widespread adoption. Even though LLMs are [built in a surprisingly simple way](https://substack.com/redirect/fa3695e8-0d21-4c13-a560-24777634e10a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), they produce impressive results in a variety of areas. Writing code turns out to be perhaps one of their strongest points. This is not all that surprising, given how:
Programming involves far simpler grammar than any human language
There is a massive amount of high-quality training data for these LLMs to use, in the form of working source code, thanks to open source software and crawling GitHub and other free-to-access code repositories (this kind of crawling and training is happening, regardless of
[whether it is ethical](https://substack.com/redirect/3a1ed71d-75f8-432d-81dd-160a6c41136b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)or not)
Last year, we saw that about [75% of developers use some kind of AI tool](https://substack.com/redirect/2a55b4b3-9c82-4b5b-981b-323db7b18e15?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) for software engineering–related work, as per our [AI tooling reality check survey](https://substack.com/redirect/2a55b4b3-9c82-4b5b-981b-323db7b18e15?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). And yet, it feels like we’re still early in the tooling innovation cycle, and more complex approaches like [AI software engineering agents](https://substack.com/redirect/7280d3aa-57e5-4f71-aa50-62b38a8a22e5?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) are likely to be the center of innovation in 2025.
Mainstream media has been painting an increasingly dramatic picture of the software engineering industry. In March, Business Insider [wrote](https://substack.com/redirect/43a4d2b9-a308-406a-a13d-af4bb583491c?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) about how “Software engineers are getting closer to finding out if AI really can make them jobless”, and in September, Forbes [asked](https://substack.com/redirect/e2e44dca-da5d-4e8e-ba49-e159ce06d93b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o): “Are software engineers becoming obsolete?” While such articles get wide reach, they are coming from people who are not software engineers themselves, don’t use these AI tools, and are unaware of the efficiency (and limitations!) of these new GenAI coding tools.
But what can we realistically expect from GenAI tools for shaping software engineering? GenAI will change parts of software engineering, but it is unlikely to do so in the dramatic way that some previous headlines suggest. And with two years of using these tools, and with most engineering teams using them for 12 months or more, we can shape a better opinion of them.
[Addy Osmani](https://substack.com/redirect/ad66829e-0589-42ec-9d34-1377c4e56013?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) is a software engineer and engineering leader, in a good position to observe how GenAI tools are really shaping software engineering. He’s been working at Google for 12 years and is currently the Head of Chrome Developer Experience. Google is a company at the forefront of GenAI innovation. The company authored the [research paper on the Transformers architecture](https://substack.com/redirect/82917be7-3959-4762-a033-b98385e2e91a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) in 2017 that serves as the foundation for LLMs. Today, Google has built one of the most advanced foundational models with [Gemini 2.0](https://substack.com/redirect/aa695955-3965-4ba4-8a6f-f1e327d13bb0?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) and is one of the biggest OpenAI competitors.
Addy summarized his observations and predictions in the article [The 70% problem: Hard truths about AI-assisted coding](https://substack.com/redirect/41ba09ca-6c2f-4183-955c-81f26155be28?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). It’s a grounded take on the strengths and weaknesses of AI tooling, one that highlights fundamental limitations of these tools, as well as the positives that are too good to not adopt as an engineer. It also offers practical advice for software engineers from junior to senior on how to make the most out of these tools. With Addy’s permission, this is an edited version of his article, re-published, with more of my thoughts added at the end. This issue covers:
How developers are actually using AI. Very different usages for “bootstrappers” versus “iterators.” Perhaps a reason why one tool is unlikely to work equally well for both groups?
The 70% problem: AI's learning curve paradox. Lesser-talked-about challenges with AI: the “two steps back paradox,” the hidden cost of “AI speed,” and the “knowledge paradox.”
What actually works: practical patterns. AI-first draft, constant conversation, and “trust but verify” patterns.
What does this mean for developers? Start small, stay modular, and trust your experience.
The rise of agentic software engineering. A shift to collaborating with AI, multi-modal capabilities, autonomous but guided approaches, and an “English-first” development environment.
The return of software as a craft? The lost art of polish to return, and the renaissance of personal software.
Additional thoughts. A good time to refresh what software engineering really is, how it has been the dream of needing no developers since the 1960s, and how demand for experienced engineers could increase in the future. Demand for experienced engineers could well increase in the future, rather than decrease.
Addy’s name might ring familiar to many of you. In August, we [published an excerpt](https://substack.com/redirect/d166c7e3-899c-4ec4-b9a0-3b23cc568195?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) from his new book, [Leading Effective Teams](https://substack.com/redirect/d166c7e3-899c-4ec4-b9a0-3b23cc568195?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). Addy also writes a newsletter called Elevate: subscribe to [Elevate](https://open.substack.com/pub/addyo?utm_source=mentions) to get Addy’s posts in your inbox.
With this, it’s over to Addy:
The bottom of this article could be cut off in some email clients. [Read the full article uninterrupted, online.](https://substack.com/redirect/049bb783-b90c-4032-bac8-c9ba632d2392?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
After spending the last few years embedded in AI-assisted development, I've noticed a fascinating pattern. While engineers report being dramatically more productive with AI, the actual software we use daily doesn’t seem like it’s getting noticeably better. What's going on here?
I think I know why, and the answer reveals some fundamental truths about software development that we need to reckon with. Let me share what I've learned.
I've observed two distinct patterns in how teams are leveraging AI for development. Let's call them the "bootstrappers" and the "iterators." Both are helping engineers (and even non-technical users) reduce the gap from idea to execution (or MVP).
Tools like Bolt, v0, and screenshot-to-code AI are revolutionizing how we bootstrap new projects. These teams typically:
Start with a design or rough concept
Use AI to generate a complete initial codebase
Get a working prototype in hours or days instead of weeks
Focus on rapid validation and iteration
The results can be impressive. I recently watched a solo developer use Bolt to turn a Figma design into a working web app in next to no time. It wasn't production-ready, but it was good enough to get very initial user feedback.
The second camp uses tools like Cursor, Cline, Copilot, and WindSurf for their daily development workflow. This is less flashy but potentially more transformative. These developers are:
Using AI for code completion and suggestions
Leveraging AI for complex refactoring tasks
Generating tests and documentation
Using AI as a "pair programmer" for problem-solving
But here's the catch: while both approaches can dramatically accelerate development, they come with hidden costs that aren't immediately obvious.
A [tweet](https://substack.com/redirect/b938cd62-0ff7-4654-96d2-309533bf0d7c?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) that recently caught my eye perfectly captures what I've been observing in the field: Non-engineers using AI for coding find themselves hitting a frustrating wall. They can get 70% of the way there surprisingly quickly, but that final 30% becomes an exercise in diminishing returns.
This "70% problem" reveals something crucial about the current state of AI-assisted development. The initial progress feels magical: you can describe what you want, and AI tools like v0 or Bolt will generate a working prototype that looks impressive. But then reality sets in.
What typically happens next follows a predictable pattern:
You try to fix a small bug
The AI suggests a change that seems reasonable
This fix breaks something else
You ask AI to fix the new issue
This creates two more problems
Rinse and repeat
This cycle is particularly painful for non-engineers because they lack the mental models to understand what's actually going wrong. When an experienced developer encounters a bug, they can reason about potential causes and solutions based on years of pattern recognition. Without this background, you're essentially playing whack-a-mole with code you don't fully understand.
When you watch a senior engineer work with AI tools like Cursor or Copilot, it looks like magic. They can scaffold entire features in minutes, complete with tests and documentation. But watch carefully, and you'll notice something crucial: They're not just accepting what the AI suggests. They're constantly:
Refactoring the generated code into smaller, focused modules
Adding edge case handling the AI missed
Strengthening type definitions and interfaces
Questioning architectural decisions
Adding comprehensive error handling
In other words, they're applying years of hard-won engineering wisdom to shape and constrain the AI's output. The AI is accelerating implementation, but their expertise is what keeps the code maintainable.
Junior engineers often miss these crucial steps. They accept the AI's output more readily, leading to what I call "house of cards code" – it looks complete but collapses under real-world pressure.
The most successful non-engineers I've seen using AI coding tools take a hybrid approach:
Use AI for rapid prototyping
Take time to understand how the generated code works
Learn basic programming concepts alongside AI usage
Build up a foundation of knowledge gradually
Use AI as a learning tool, not just a code generator
But this requires patience and dedication, which is exactly the opposite of what many people hope to achieve by using AI tools in the first place.
Here's the most counterintuitive thing I've discovered: AI tools help experienced developers more than beginners. This seems backward. Shouldn't AI democratize coding?
The reality is that AI is like having a very eager junior developer on your team. They can write code quickly, but they need constant supervision and correction. The more you know, the better you can guide them.
This creates what I call the "knowledge paradox":
Seniors use AI to accelerate what they already know how to do
Juniors try to use AI to learn what to do
The results differ dramatically
I've watched senior engineers use AI to:
Rapidly prototype ideas they already understand
Generate basic implementations they can then refine
Explore alternative approaches to known problems
Automate routine coding tasks
Meanwhile, juniors often:
Accept incorrect or outdated solutions
Miss critical security and performance considerations
Struggle to debug AI-generated code
Build fragile systems they don't fully understand
There's a deeper issue here: The very thing that makes AI coding tools accessible to non-engineers, their ability to handle complexity on your behalf, can actually impede learning. When code just "appears" without you understanding the underlying principles:
You don't develop debugging skills
You miss learning fundamental patterns
You can't reason about architectural decisions
You struggle to maintain and evolve the code
This creates a dependency where you need to keep going back to AI to fix issues, rather than developing the expertise to handle them yourself.
This "70% problem" suggests that current AI coding tools are best viewed as:
Prototyping accelerators for experienced developers
Learning aids for those committed to understanding development
MVP generators for validating ideas quickly
But they're not yet the coding democratization solution many hoped for. The final 30%, the part that makes software production-ready, maintainable, and robust, still requires real engineering knowledge.
The good news? This gap will likely narrow as tools improve. But for now, the most pragmatic approach is to use AI to accelerate learning, not replace it entirely.
After observing dozens of teams, here's what I've seen work consistently:
Let AI generate a basic implementation
Manually review and refactor for modularity
Add comprehensive error handling
Write thorough tests
Document key decisions
Start new AI chats for each distinct task
Keep context focused and minimal
Review and commit changes frequently
Maintain tight feedback loops
Use AI for initial code generation
Manually review all critical paths
Conduct automated testing of edge cases
Implement regular security audits
Despite these challenges, I'm optimistic about AI's role in software development. The key is understanding what it's really good for:
Accelerating the known. AI excels at helping us implement patterns we already understand. It's like having an infinitely patient pair programmer who can type really fast.
Exploring the possible. AI is great for quickly prototyping ideas and exploring different approaches. It's like having a sandbox where we can rapidly test concepts.
Automating the routine. AI dramatically reduces the time spent on boilerplate and routine coding tasks, letting us focus on the interesting problems.
If you're just starting with AI-assisted development, here's my advice:
Start small
Use AI for isolated, well-defined tasks
Review every line of generated code
Build up to larger features gradually
Stay modular
Break everything into small, focused files
Maintain clear interfaces between components
Document your module boundaries
Trust your experience
Use AI to accelerate, not replace, your judgment
Question generated code that feels wrong
Maintain your engineering standards
The landscape of AI-assisted development is shifting dramatically as we head into 2025. While the current tools have already changed how we prototype and iterate, I believe we're on the cusp of an even more significant transformation: the rise of agentic software engineering.
What do I mean by "agentic"? Instead of just responding to prompts, these systems can plan, execute, and iterate on solutions with increasing autonomy.
If you’re interested in learning more about agents, including my take on Cursor/Cline/v0/Bolt, you may be interested in my [recent JSNation talk](https://substack.com/redirect/52eba426-25fd-4ec0-a5f3-a1c87b6ac1ee?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) above.
We're already seeing early signs of this evolution:
Current tools mostly wait for our commands. But look at newer features like Anthropic's computer use in Claude, or Cline's ability to automatically launch browsers and run tests. These aren't just glorified autocomplete. They're actually understanding tasks and taking the initiative to solve problems.
Think about debugging: Instead of just suggesting fixes, these agents can:
Proactively identify potential issues
Launch and run test suites
Inspect UI elements and capture screenshots
Propose and implement fixes
Validate the solutions work (this could be a big deal)
The next generation of tools may do more than just work with code. They could seamlessly integrate:
Visual understanding (UI screenshots, mockups, diagrams)
Verbal language conversations
Environment interaction (browsers, terminals, APIs)
This multimodal capability means they can understand and work with software the way humans do: holistically, not just at the code level.
The key insight I've gained from working with these tools is that the future isn't about AI replacing developers. It's about AI becoming an increasingly capable collaborator that can take initiative while still respecting human guidance and expertise.
The most effective teams in 2025 may be those that learn to:
Set clear boundaries and guidelines for their AI agents
Establish strong architectural patterns that agents can work within
Create effective feedback loops between human and AI capabilities
Maintain human oversight while leveraging AI autonomy
As Andrej Karpathy [noted](https://substack.com/redirect/c3a67fc5-8300-424d-84ba-24d66d93cb97?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o):
"The hottest new programming language is English."
This is a fundamental shift in how we'll interact with development tools. The ability to think clearly and communicate precisely in natural language is becoming as important as traditional coding skills.
This shift toward agentic development will require us to evolve our skills:
Stronger system design and architectural thinking
Better requirement specification and communication
More focus on quality assurance and validation
Enhanced collaboration between human and AI capabilities
While AI has made it easier than ever to build software quickly, we're at risk of losing something crucial: the art of creating truly polished, consumer-quality experiences.
It's becoming a pattern: Teams use AI to rapidly build impressive demos. The happy path works beautifully. Investors and social networks are wowed. But when real users start clicking around? That's when things fall apart.
I've seen this firsthand:
Error messages that make no sense to normal users
Edge cases that crash the application
Confusing UI states that never get cleaned up
Accessibility completely overlooked
Performance issues on slower devices
These aren't just P2 bugs. They're the difference between software people tolerate and software people love.
Creating truly self-serve software, the kind where users never need to contact support, requires a different mindset:
Obsessing over error messages
Testing on slow connections
Handling every edge case gracefully
Making features discoverable
Testing with real, often non-technical users
This kind of attention to detail (perhaps) can't be AI-generated. It comes from empathy, experience, and deep care about craft.
I believe we're going to see a renaissance of personal software development. As the market gets flooded with AI-generated MVPs, the products that will stand out are those built by developers who:
Take pride in their craft
Care about the little details
Focus on the full user experience
Build for the edge cases
Create truly self-serve experiences
The irony? AI tools might actually enable this renaissance. By handling the routine coding tasks, they free up developers to focus on what matters most: creating software that truly serves and delights users.
AI isn't making our software dramatically better because software quality was (perhaps) never primarily limited by coding speed. The hard parts of software development — understanding requirements, designing maintainable systems, handling edge cases, ensuring security and performance — still require human judgment.
What AI does do is let us iterate and experiment faster, potentially leading to better solutions through more rapid exploration. But this will only happen if we maintain our engineering discipline and use AI as a tool, not as a replacement for good software practices. Remember: The goal isn't to write more code faster. It's to build better software. Used wisely, AI can help us do that. But it's still up to us to know what "better" means and how to get it.
Gergely again. Thank you, Addy, for this pragmatic summary on how to rethink our expectations on AI and software engineering. If you enjoyed this piece from Addy, check out his [other articles](https://substack.com/redirect/3ffe699b-a311-49e7-8c01-268e78b3b8af?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) and his latest book: [Leading Effective Engineering Teams](https://substack.com/redirect/d166c7e3-899c-4ec4-b9a0-3b23cc568195?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).
Here are my additional thoughts on AI and software engineering.
Much of the disclosure on AI tooling for software engineering focuses on code generation capabilities, and rightfully so. AI tools are impressive in generating working code from prompts, or suggesting inline code as you build software. But how much of the process of building software is coding itself? About 50 years ago, Fred Brooks thought that it is around 15-20% of all time spent. Here are Brooks’ thoughts [from The Mythical Man-Month](https://substack.com/redirect/bd0b6d5f-a765-43fe-b16f-6a60a6a7e6a8?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o):
“For some years, I have been successfully using the following rule of thumb for scheduling a software task:
⅓ planning
⅙ coding
¼ component test and early system test
¼ system test, all components in hand.”
My take is that today, software engineers probably spend their time like this:
20% planning
40% coding (code + tests)
20% code review (others' code)
20% production readiness + rollout + small fixes during this + monitoring+alerting
At the same time, building standout software has a lot of other parts:
What: Figure out what to build. This can involve brainstorming, designing, user testing, working with product managers and business stakeholders, and so on. For startups, this phase can take very little time (“just build it and see if it works!”). For established companies, it can take up more time than building, though (“we need to make sure what we build doesn’t confuse our existing customers!”).
How: Draw up a plan on how to build the product/feature/service. Think through architecture implications, dependencies, how to test the product, and so on. Again, startups might be able to skip this stage, and the team can jump straight to planning. But for larger companies with more services and dependencies, leaving out planning will come back to bite the team. So most teams are doing some kind of planning using
[Design docs, RFCs, or ADRs.](https://substack.com/redirect/de7f8e5c-a6f5-45f0-8f3d-0e1d9df0c79d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)Build: Implement the feature or product: write the code, and make sure it works.
Verify: Double check that it works as expected before shipping to production. This is especially important in cases where shipping is high-stakes: for example, shipping a regression to a banking app could have financial implications for customers, and the business! We went into details about QA in
[QA across the tech industry.](https://substack.com/redirect/15ffed46-e82e-4135-b4ee-4edebe6536d6?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)Ship it: Merge the change, and ship to customers. There are plenty of strategies to ship changes to production. We covered several of these in
[Shipping to production.](https://substack.com/redirect/d0c7f4fd-b0f0-412f-b250-556d7e20ad89?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)Monitoring and oncall: Detect when something is wrong with the product. If there’s an outage, resolve it as soon as possible, and then make sure a similar outage won’t happen again. We looked at these common approaches in
[Healthy oncall practices](https://substack.com/redirect/fb80fe75-b304-4eaf-8ea5-3580549d85c5?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)and in[Incident review and postmortem best practices](https://substack.com/redirect/d8c8807c-c536-4d84-8c88-6b629cfabef2?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).Maintain: Listen to customer complaints and feedback, and decide which bugs warrant fixing, and which are feature requests to prioritize. And figure out what feedback to disregard.
Migrate: If the product goes under large changes, or if the tech stack sees major changes — like a new framework — there might need to be migrations. We covered more in
[Migrations done well](https://substack.com/redirect/7b4d8c71-f04c-422c-8723-3fa19fc9e1d4?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).
AI tools today can help a lot with the “Build” part. But here is a good question: Just how useful are they for the other 7 things that are also part of software engineering?
Non-technical people creating working software without needing to rely on software developers has been the dream since the 1960s. Coding is about translating from what people want (the customers, business stakeholders, the product manager, and so on) to what the computer understands. LLMs offer us a higher level of abstraction where we can turn English into code. However, this new abstraction does not change the nature of how software is created, – and what software is, – which is this:
GenAI tools don’t change the process, but they do make some of the coding parts more efficient:
Throughout the history of technology, new innovations promised the ability for business folks to collapse or bypass the “tech” part, and get straight to working software from their high-level prompts. This was the aspiration of:
1960s: the high-level programming language
[COBOL](https://substack.com/redirect/e812c328-aaa9-4915-852b-5b78485880a3?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). COBOL stands for “common, business-oriented language.” The[stated goal](https://substack.com/redirect/b14c0a0d-655b-4df3-8fa8-bcd05299e3c4?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)of this language was to allow business people with no programming background to use it.1990s:
[Visual Basic](https://substack.com/redirect/68ac7530-00ef-4dc6-a664-0170e27e24b8?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). A programming language meant to have a very low learning curve, plus a visual environment where forms can be created with drag-and-drop.Late 2010s:
[The no-code movement](https://substack.com/redirect/8219a843-44ac-46b0-ac9c-a9783dcca05c?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). Through templates and visual editing, no-code solutions like[Bubble](https://substack.com/redirect/c765e202-e2ce-4713-a78f-b45a4688a10a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)offer a way to build software applications.
Unsurprisingly, several GenAI coding startups aspire for the same goal: to allow anyone to create software, by using the English language. In the past, we have seen success for simpler use cases. For example, these days, there is no coding knowledge needed to create a website: non-technical people can use visual editors and services like Wix.com, Webflow, Ghost or WordPress.
The higher-level the abstraction, the harder it is to specify how exactly the software should work. No-code solutions already ran into this exact limitation. As advisory CTO Alex Hudson writes in his article [The no-code delusion](https://substack.com/redirect/1294753c-623f-45a6-b118-62784e8f9df2?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o):
“The development of these syntaxes has generally run into the problem of expression: once they are simple enough to pick up quickly, they are no longer expressive enough to use in many scenarios. And vice-versa: some languages have the ability to define a custom language within them, called domain-specific languages (DSLs). Few of these languages have ever been truly successful amongst the development community at large, primarily because they again make things extremely complex.”
For more complex software, it’s hard to see not needing software engineers taking part in planning, building and maintaining software. And the more GenAI lowers the barrier for non-technical people to create software, the more software there will be to maintain.
Two years after the launch of LLMs, many of us have gotten a pretty good handle on how to use them to augment our coding and software engineering work. They are great for prototyping, switching to less-familiar languages, and tasks where you can verify their correctness, and call out hallucinations or incorrect output.
AI agents, on the other hand, are in their infancy. Most of us have not used them extensively. There is only one generally available agent, [Devin](https://substack.com/redirect/cbc46fbd-3c89-4029-bfbc-d4e179550965?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), at $500/month, and early responses [are mixed](https://substack.com/redirect/f2fb16a4-8698-473a-a541-527fa35ead54?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).
A lot of venture funding will be pouring into this area. We’ll see more AI coding agent tools launch, and the price point will also surely drop as a result. GitHub Copilot is likely to make something like [Copilot Workspace](https://substack.com/redirect/038aaff9-85c8-4112-a87d-41c4c87bc78f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) (an agentic approach) generally available in 2025. And we’ll probably see products from startups like what Stripe’s former CTO, David Singleton founded ([/dev/agents](https://substack.com/redirect/66210077-5b8c-4327-9d4b-f5c3f822ec72?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).)
AI agents trade off latency and cost (much longer time spent computing results and running prompts several times, paraphrased by these startups as “thinking”) for accuracy (better results, based on the prompts). There are some good questions about how much accuracy will improve with this latency+cost tradeoff, and what engineering use cases will see significant productivity boost as a result.
Experienced software engineers could be in more demand in the future than they are today. The common theme we’re seeing with AI tooling is how senior-and-above engineers can use these tools more efficiently, as they can “aim” better with them. When you know what “great output” looks like, you can prompt better, stop code generation when it’s getting things wrong, and you can know when to stop prompting and go straight to the source code to fix the code itself.
We will see a lot more code produced with the help of these AI tools, and a lot more people and businesses start building their own solutions. As these solutions hit a level of complexity, it’s a safe bet that many of them will need to bring in professionals as they attempt to tame the complexity: complexity that requires experienced engineers to deal with. Existing tech companies will almost certainly produce more code with AI tools: and they will rely on experienced engineers to deal with the increase of complexity that necessarily follows.
As a software engineer, mastering AI-assisted development will make you more productive, and also more valuable. It’s an exciting time to be working in this field: we’re living through a time of accelerated tooling innovation. It does take time to figure out how to “tame” the current tools in a way that makes you the most productive: so experiment with them!
I hope you’ve found the practical approaches from Addy helpful. For additional pointers, see the issue [AI Tooling for Software Engineers in 2024: Reality Check](https://substack.com/redirect/2a55b4b3-9c82-4b5b-981b-323db7b18e15?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).
You’re on the free list for [The Pragmatic Engineer](https://substack.com/redirect/2/eyJlIjoiaHR0cHM6Ly9uZXdzbGV0dGVyLnByYWdtYXRpY2VuZ2luZWVyLmNvbT91dG1fY2FtcGFpZ249ZW1haWwtaG9tZSZyPThvNTRuIiwicCI6MTU0MjAwODQwLCJzIjo0NTg3MDksImYiOnRydWUsInUiOjE0NTYzMzE5LCJpYXQiOjE3MzYwOTQ2MzksImV4cCI6MTczODY4NjYzOSwiaXNzIjoicHViLTAiLCJzdWIiOiJsaW5rLXJlZGlyZWN0In0.8irS2_x_orkAGQXmxoN1EcjOPYxfnLdavlARfrb1WsU?). For the full experience, [become a paying subscriber](https://substack.com/redirect/2/eyJlIjoiaHR0cHM6Ly9uZXdzbGV0dGVyLnByYWdtYXRpY2VuZ2luZWVyLmNvbS9zdWJzY3JpYmU_dXRtX3NvdXJjZT1wb3N0JnV0bV9jYW1wYWlnbj1lbWFpbC1jaGVja291dCZuZXh0PWh0dHBzJTNBJTJGJTJGbmV3c2xldHRlci5wcmFnbWF0aWNlbmdpbmVlci5jb20lMkZwJTJGaG93LWFpLXdpbGwtY2hhbmdlLXNvZnR3YXJlLWVuZ2luZWVyaW5nJnI9OG81NG4mdG9rZW49ZXlKMWMyVnlYMmxrSWpveE5EVTJNek14T1N3aWFXRjBJam94TnpNMk1EazBOak01TENKbGVIQWlPakUzTXpnMk9EWTJNemtzSW1semN5STZJbkIxWWkwME5UZzNNRGtpTENKemRXSWlPaUpqYUdWamEyOTFkQ0o5Lnd0aXhwU240RXl1SmpaVWp3YlRnQ3VkYW1uRlU5RUZIMmdLdDlkT29hbWciLCJwIjoxNTQyMDA4NDAsInMiOjQ1ODcwOSwiZiI6dHJ1ZSwidSI6MTQ1NjMzMTksImlhdCI6MTczNjA5NDYzOSwiZXhwIjoxNzM4Njg2NjM5LCJpc3MiOiJwdWItMCIsInN1YiI6ImxpbmstcmVkaXJlY3QifQ.YDRK7S6P7MCJVOEgR5UrohAjWDx615RdBZDOe2hsg0s?). Many readers expense this newsletter within their company’s training/learning/development budget.
This post is public, so feel free to share and forward it.
If you enjoyed this post, you might enjoy my book, [The Software Engineer's Guidebook](https://substack.com/redirect/ce12eadd-3262-4f9b-ab0d-6532251da6d1?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). Here is what Tanya Reilly, senior principal engineer and author of The Staff Engineer's Path said about it:
"From performance reviews to P95 latency, from team dynamics to testing, Gergely demystifies all aspects of a software career. This book is well named: it really does feel like the missing guidebook for the whole industry."