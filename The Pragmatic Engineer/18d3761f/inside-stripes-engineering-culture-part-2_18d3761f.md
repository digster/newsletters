---
subject: "Inside Stripe’s Engineering Culture: Part 2"
from: "The Pragmatic Engineer <pragmaticengineer@substack.com>"
to: ""
date: 2024-01-23 17:32:15
labels: ["CATEGORY_PERSONAL", "INBOX", "The Pragmatic Engineer"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_6413324878686416177"]
---
👋 Hi, this is Gergely with a 🔒 subscriber-only issue 🔒 of the Pragmatic Engineer Newsletter. In every issue, I cover challenges at Big Tech and startups through the lens of engineering managers and senior engineers. If you’ve been forwarded this email, you can
|
Founded in 2009, Stripe is one of the biggest tech success stories of both Silicon Valley and Europe. It has dual headquarters in San Francisco, US, and Dublin, in the Republic of Ireland, employs thousands of software engineers, and processed $817B of payments in 2022. That’s around $1.5M processed per minute, on average.
But what’s it like to work at Stripe as an engineer? Over the past few months I’ve talked with CTO [David Singleton](https://substack.com/redirect/7cf628c5-07d5-46b9-8431-b80c3d85163a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), and others at the company. This article is the second and final part of a deep dive into how Stripe works; with more previously unshared details of how engineering works there. [In Part 1,](https://substack.com/redirect/1bc29a6e-4adf-48b0-a42d-8b4ba59ec001?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) we covered:
What is Stripe?
Engineering at a glance
The culture
Product architects and engineers spending time with customers
The tech stack
Engineering processes
Today, we round up this topic with:
More unique features of Stripe’s engineering culture. Writing, engineers wearing a “product hat,” and friction logging.
Operational excellence. The FinTech company has an outsized focus on operating reliably and delivering on commercial contracts. How do engineering processes achieve this, while still shipping hundreds of times per day?
Internal tools. Stripe’s “Go” tool, Intranet Home, Trailhead, and Compass.
Internal engineering and FinTech platforms. Sail, Amp, Ruby Code Quality Platform, Treasury Network, and Ledger.
API review. A surprisingly important and central part of Stripe’s culture. Each and every change that modifies Stripe’s API must pass a strict review process, which goes way beyond a “normal” code review.
Developer productivity. Stripe unapologetically measures everything possible about software development processes and practices.
Learnings from the CTO. Adopting modern engineering practices in the heavily regulated finance industry, the importance of team size for modern engineering, the cost of collaboration across time zones, and more.
For this article, Stripe has exclusively shared close to a dozen screenshots of its internal systems, which are marked in the captions as “Source: Stripe.”
Check out other engineering culture deep dives on [Meta](https://substack.com/redirect/45785f28-a117-4ce8-93f9-53d1147be067?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), [Amazon](https://substack.com/redirect/da644870-b86c-4753-9eb3-1c89d67141ce?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), [Linear](https://substack.com/redirect/c98ffb27-7fd2-4b94-ab45-516598064fbf?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), [Figma](https://substack.com/redirect/45f77f17-f8df-4da1-9d35-72900f7045e3?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), [Sourcegraph](https://substack.com/redirect/2fc9ef81-38a5-439c-945a-7d3119102036?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), [Agoda](https://substack.com/redirect/ce7a5202-35c7-4389-933a-4b04655e9653?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), and others. [Read them all here](https://substack.com/redirect/77a1ee45-a971-4af7-a562-6c30e0a83ab3?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).
The second part of this email can be cut off in some email clients. [Read the full article uninterrupted, online.](https://substack.com/redirect/4bd3575e-94b7-4f24-999a-81825e76b264?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
In Part 1, we cover [Stripe’s engineering culture](https://substack.com/redirect/bb2d4786-a025-4bde-8f8d-ccaa8b22eb24?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). But there are more unique things about Stripe which deserve a mention for contributing to its success.
It’s rare to come across a company with such a strong culture of writing, as Stripe. When I talked with David about how this works, he had a document – well, a “Go” link (covered below) for all my questions. I asked him how the writing culture emerged. He said:
“We’ve found engineers love the leverage good writing provides. Investing extra time to communicate an idea through clear, precise writing delivers outsized results because vastly more people consume the writing than produce it.”
But how does Stripe support this writing culture? Undeniably, it's extra effort to write things down, and it’s often tempting to just get to coding, instead. Here’s how David says Stripe does it:
“One of the most prolific publishers to Stripe’s internal blog is [CEO and cofounder,] Patrick Collison. The best way to encourage a writing culture is to contribute directly to it. I personally try to publish more than one internal blog piece per month.
Because we have a culture of sharing great writing; carefully reasoned, well-expressed ideas reach a broad audience quickly at Stripe. This really paid off early: we’ve had remote Stripes since almost the beginning. It especially paid dividends when the pandemic hit and everyone was working from home.”
That the CEO and CTO write regularly, and pretty much all engineers produce longer internal documents, seems to encourage new recruits to do the same. I haven’t discovered anything that would help other companies kickstart a writing culture from scratch, so I asked for inspiration and examples of writing by developers. Here are some external documents that showcase the kind of writing engineers at Stripe produce:
[Engineering section of the Stripe Blog](https://substack.com/redirect/7fa13432-d5ee-44e4-84e2-9abe2cb0a611?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o): almost exclusively written by technologists[How we built it: Stripe Radar](https://substack.com/redirect/e55a4deb-0dfb-4252-b881-4936720b9395?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o): engineering blog post by Ryan Drapeau, an ML engineer working on payment fraud preventionNon-engineering writing is common at the company. For example, here is
[a wine-making tutorial](https://substack.com/redirect/82c6fd80-51d8-4da8-abd9-bb1c6cf1f2fd?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)by David, on his personal blog.
Stripe didn’t have the Product Manager (PM) role for a long time, which has had an impact on engineering.
Engineers participate in all parts of the product development process: figuring out business scope, talking to users, collaborating with designers, lawyers, accountants, etc. They don’t only do software development, as is common at “traditional” companies. I’d compare Stripe’s approach to [product-minded engineers](https://substack.com/redirect/cfe1fbee-0f0c-4a6f-a900-c873bfe706b3?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).
In the early days, this meant engineers did a lot of what PMs do. These days, Stripe has found it’s helpful for engineers to partner with PMs because the number of features and products has grown. Stripe now has many PMs and product folks who add a ton of value. That being said, Stripe still expects engineers to be close to users and involved in the process, end-to-end. Staying close helps the feedback loop stay tight, and ensures Stripe builds things users want.
Stripe encourages engineering leaders to experience being an engineer, in what it calls ‘engineerication’. The idea is that if a manager can “down tools” and go on vacation, they can also down tools to spend a week as an IC engineer, too!
As Stripe’s CTO, David leads by example; embedding himself in an engineering team and working end-to-end on a project. “Engineerication” is very helpful for identifying pain points in developer productivity, and frequently leads to improvements.
My observation is that very few companies explicitly encourage this, and without empowerment from above it’s hard to justify doing zero managerial work for a week, in favor of engineering work of not especially high value.
A friction log documents the end-to-end user flow. The person playing the role of “friction logger” gets in the mindset of a user trying to do something like sign up to use a new product, understand a warning on the portal, or generate a report. They note all friction points they hit, as well as ideas for enhancing the UX.
Based on a summary [from two Stripe engineers](https://substack.com/redirect/b38c08d5-cf7b-4922-983f-4da251098096?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), the typical structure of a friction log is:
Context: describe the persona and what they want to accomplish
Pros and cons: what’s good about the experience, and what can be improved
Detailed stream of consciousness: record what you do while using the feature. A good example of a “stream of consciousness” document is
[Bill Gates documenting his process to try and install Microsoft MovieMaker in 2003](https://substack.com/redirect/70c76f7d-7177-4168-98f8-170fc91a576f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).
Stripe has advice for making the most of friction logs:
Share the size of the friction log upfront (small/medium/large) to set expectations for how long it takes to read
Make the journey clear, and add context where helpful
Highlight joys, not just frustrations
Use visuals where possible
Avoid emotional language; stay objective
Stripe encourages engineers, managers, and everyone else, to produce friction logs at least occasionally. The key is to get deep into the mindset and context of a user.
My own note: friction logging is especially powerful when done – or acted on – by people in authority, like managers, directors, and the C-level. This is because they can advocate effectively for change.
Operational excellence – which means operating systems reliably – is a massive focus at Stripe. This should come as no surprise because reliability is non-negotiable for any payments system. Stripe’s annual letter of 2022 highlighted its API reliability, [stating](https://substack.com/redirect/fdb56619-cbd4-4d4a-aa80-d78a3ff20157?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o):
“Our API reliability is now consistently in excess of 99.999%, and, during the peak week of Black Friday and Cyber Monday, exceeded six nines (that is, 99.9999%,—the equivalent of around 600 milliseconds of unavailability. (It takes about 300 milliseconds for a human to blink.)”
In [Part 1](https://substack.com/redirect/1bc29a6e-4adf-48b0-a42d-8b4ba59ec001?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), we covered [the focus on automated testing at Stripe](https://substack.com/redirect/063815e2-ec5d-4e7f-af66-fcd98f63a991?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). In the same letter, the company reinforces how testing and reliability go hand-in-hand:
“The biggest distributed system at Stripe is our testing system. Stripe now comprises more than 50 million lines of code. Each change is verified within 15 minutes by running a battery of tests that would take 50 days to run on a single CPU. These automated tests detect and prevent problems much better than humans ever could. In 2022, we deployed our core payments APIs 5,978 times, 16.4 times a day, on average. Of this, 1,100 deploys failed to meet our acceptance criteria, and were rolled back automatically.”
The importance of operational excellence is regularly reinforced at CTO-level. In April 2023, David sent an email to all of engineering entitled “Operational excellence.” It started with a reminder of why operational excellence matters so much to a payments company:
“People’s livelihoods depend on Stripe working correctly. We need to make sure we’re available and when we’re not, we need to be able to recover quickly. Our customers put a lot of trust in us and we need to re-earn that trust every day, every request.
We haven’t always deserved that trust. On July 10th 2019, Stripe was down for about 2 hours in total. I responded to hundreds of emails from customers trying to recover in the aftermath. We had many deeply unhappy customers. We and they lost significant future business that day. Our users had to explain it to many of their customers who didn’t have a dang clue what Stripe was.
Fast forward to today, we now frequently sign up new users who migrate to Stripe because their previous provider has had a string of outages (you would too!) Our current availability is a selling point for Stripe. But maintaining this position takes constant effort and vigilance and yes, layers and layers of investment.”
David’s email explained:
“Operational Excellence is systematically keeping our promises to users. An operational failure is any time a user expects our systems to do something for them – handle an API request to create an account, auth & capture a credit card charge, pay out money to their bank account by a specific deadline, etc – and we don’t do what they expect. Maybe we returned an error code, failed to deliver a webhook related to the event, moved the wrong amount of money, or didn’t complete the operation fast enough to meet the needs of their business.
Stripe makes promises to our customers: ‘We promise to attempt this transaction and tell you if it went through or not,’ ‘We promise if it goes through, that you'll get the money in X days’. When we break the promise, we fail.
Operational Excellence is about minimizing the number of operational failures; driving them close to zero, despite the immense complexity of all the systems at Stripe and elsewhere that need to work together in concert to uphold those expectations. Building on that, a little operational excellence is about maximizing the likelihood we keep our promises. And when we don't, knowing that ourselves (not being surprised to hear about it from the customer), communicating the situation, reducing the impact, and mitigating the issue.”
An interesting paradox David ekes out in his email is that changes cause operational failures, but Stripe must ship changes in order to keep moving quickly:
“When we think about our operational failures, the vast majority of them are related to making changes; things we were altering in our API, products, or systems that had unintended consequences. But we’re seeking to move fast for our users, so making changes is something we need to be able to do a lot. Less frequently, issues are latent; we changed nothing but perhaps tripped a certain limit in our infrastructure or triggered a rare condition.”
The best way to ship often and safely is to ensure every change is automatically tested via the CI pipeline, and gradually deployed. This is the default for how all new services at Stripe are built.
Writing good tests. TDD (test driven development) is not mandated at Stripe, but writing good tests is emphasized. Good tests are:
Easy to understand, with accurate descriptions
Repeatable: test can be run multiple times and does exactly the same thing, so it’s easy to debug failures
Clear about what’s tested and why failures happen
Auto-deploying code. Testing alone is not sufficient to prevent failures for users. Stripe used to ask engineers to carefully monitor the deployment of their code to production by watching charts to spot problems.
Today, almost all services are auto-deployed and gradually rolled out. Stripe believes that automatically initiated and monitored deployments are more reliable than those “babysat” by humans. Automated rollout can also proceed more slowly as there’s no impatient engineer waiting to do the next task. We cover [more on Stripe’s deployment tooling in Part 1.](https://substack.com/redirect/0e540166-ef64-42c9-b251-eea48669e26b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
Things can still go wrong. No amount of testing can ensure production has no issues, but it can minimize risk. Latent issues which are unobservable outside production can still occur. A common latent issue is when two changes get released at nearly the same time, and impact one another.
A key principle at Stripe is to design and build defensive systems with failures in mind. Failure engineers are encouraged to think about:
Downstream dependencies: failure or unavailability of lower-level infrastructure which people depend on, the cloud provider’s availability to allocate resources, etc.
Hardware failure: including OS-level bugs
Networking issues: quality of service degradations such as packet loss, networking partition issues; like groups of machines being unavailable
Cloud region failures: preparation for a whole region going offline
Design with fault domain minimization in mind. This principle is commonly known as “reduce the blast radius.” Systems are designed so that failures are isolated, and don’t propagate to impact broad swathes of the user base.
Build scalable systems. Stripe encourages engineers to gather information on how much their systems need to scale in the near future, and to plan proactively; for example, for Black Friday/Cyber Monday loads. We cover the [technology choices behind Stripe’s Black Friday/Cyber Monday dashboard](https://substack.com/redirect/da976954-a6ea-4500-b777-9f49c2b329af?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).
Build systems where the easiest path is the safest, most reliable one. Stripe makes it hard to do things like disable health checks, skip checks when deploying, and override sensible defaults.
There is one dashboard which gives a sense of the service’s health (“detect.”) This allows rapid detection when things go wrong. Every service at Stripe has its live metrics dashboard displaying important operating characteristics, all in one place:
Ensure failures do not repeat (“eliminate.”) Stripe aims to be a “learning organization,” which learns from incidents so they don’t happen again. The company uses incident reviews, asking “why” questions which get to the root of an issue, and aim to fix it and other similar issues.
Stripe runs an Ops Review within each group. This tends to happen weekly, when teams check the operational posture of systems. Topics include:
How do systems measure up to service level agreements in place?
Recent incidents, and what actions were taken in response
What can be learned from major incidents?
Are there patterns in incidents that mean drastic action is needed?
Are teams drowning in noisy alerts?
Is enough progress being made on incident remediation actions?
Like many larger tech companies, Stripe has built plenty of its systems internally. Here are a couple custom-built tools most people working at Stripe (referred to as ‘Stripes’) use on a day-to-day-basis.
When I asked David about a resource within Stripe, he responded that it can be found at “go/{something}.” “Go” is Stripe’s internal URL shortener. For example, go/home resolves to home.corp.stripe.com
On top of being easy to use, Go has the neat feature that when someone makes a “go link,” Go also indexes the content behind this link, making it available to be found via search.
Stripe custom built its intranet home page. This site displays announcements, company events, new joiners, and the latest features shipped and fixed. In a nice touch, people whose birthday it is are also listed!
The intranet home page is search-heavy. I’m told many engineers use it as a gateway to resources, company-wide. One neat feature I found was that the search page autofills suggestions based on your own search profile:
Stripe built this custom intranet portal back in the early 2010s, when there were no vendor solutions for portals. A small team still maintains Home.
Trailhead is Stripe’s internal product and documentation system. The structure is based on that of Stripe’s external docs.
Compass is Stripe’s internal project management tool. It’s custom-built, and pretty popular internally – and with engineering! The tool displays recent updates on a selected project; documents linked to it, helps assess launch readiness, and more:
Compass has several Stripe-specific features:
Slack integration: creates a Slack channel for the project, and links to it.
Running standups: with a click, Compass starts a standup and prompts the next speaker, and asks questions like, “what’s up next on your mind,” and “anything blocking you or stressing you out?”
People and channels involved: lists people involved in a project, relevant email lists, and the Slack channels of the project. At Stripe, all projects have one or two Slack channels, usually a public and a private one.
Stripe uses Slack for conversations, like at many companies. However, the company is very clear that Slack is not meant to be a canonical, long-term repository for important information. If something is posted in Slack, it’s expected it will disappear, or become impossible to find.
Stripe encourages engineers to create longer-term artifacts, instead of relying on Slack. Artifacts like Google Docs or other documents or pages, can be found on portals like the Intranet Home. The importance of archiving important information like details on design decisions is emphasized Stripe’s API review guidelines, which we cover later in this article.
It’s smart that Stripe is explicit about Slack usage, given it’s tempting to dump everything into Slack and assume people will find important documents. If your company hasn’t verbalized guidelines on the long term storage of information, taking inspiration from Stripe could be good!
Stripe has built several platforms that are heavily used by its software engineers:...
Become a paying subscriber of The Pragmatic Engineer to get access to this post and other subscriber-only content.
| Full articles every Tuesday and Thursday | |
| Access to resources and templates for engineering managers and engineers | |
| Access to the complete archive, see all comments and comment on articles |