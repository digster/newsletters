---
subject: "Hiring software engineers and engineering leaders from Big Tech (Part 1)"
from: "The Pragmatic Engineer <pragmaticengineer+deepdives@substack.com>"
to: ""
date: 2024-10-29 17:30:25
labels: ["CATEGORY_PERSONAL", "INBOX", "The Pragmatic Engineer", "UNREAD"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_6413324878686416177", "UNREAD"]
---
👋 Hi, this is Gergely with a subscriber-only issue of the Pragmatic Engineer Newsletter. In every issue, I cover challenges at Big Tech and startups through the lens of engineering managers and senior engineers. If you’ve been forwarded this email, you can
|
Before we start: the Korean translation of [The Software Engineer’s Guidebook](https://substack.com/redirect/820f04da-f9d2-4ed7-b78f-ade039e48ed8?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) is out! If you are based in Korea, you can get it [from Hanbit Media](https://substack.com/redirect/20b046eb-951a-4cbc-aa93-08d7e4546ac1?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) (the publisher), from [Kyobo](https://substack.com/redirect/6b14a429-1cf9-4e0d-90a4-c70853761351?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), from [YES24](https://substack.com/redirect/6cf346be-3b06-41f0-8afd-f2a0ec00732b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) and from [Aladin](https://substack.com/redirect/1fc16673-b7f8-4400-b962-067ebc038d93?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). This is the first translation of the book – other languages like German, Japanese and Chinese will follow in the coming months!
There are many standout software engineers and engineering leaders in Big Tech, and it’s easy to assume that hiring them is a sure win for any startup and scaleup. But counterintuitively, recruiting techies from Big Tech is often very difficult for startups. Sometimes, it’s simply very hard to get tech professionals interested in a smaller company, even when they’re a good fit.
A few weeks ago, we dug into reasons [why software engineers quit Big Tech](https://substack.com/redirect/d00a5db7-9ecb-436d-ba4f-533524219969?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). In this article, we look into ways to attract folks to startups.
For this piece, I talked with techies in senior roles at startups. Keeping identities anonymous, this deep dive covers:
Why Big Tech hires are often poor fits for startups
When hiring from large companies doesn’t make sense
When it does make sense
Why is it hard to hire from Big Tech?
How to “poach” from Big Tech
Part two of this mini-series will cover how to pitch opportunities to Big Tech folks, with advice from hiring managers at startups about their successful approaches.
The Pragmatic Engineer deepdives related to this topic:
Let’s start with the elephant in the room; it’s a terrible idea to hire someone from a big company into a small, scrappy startup. Here’s the founder of a data startup on their personal experience:
“Some of our hires from Google wanted to replicate all Google’s processes/culture, and completely failed. One staff engineer was the worst hire I can remember; they were so certain of their excellence and Google's superiority, that they ignored what made our company outstanding.”
An ex-Big Tech cofounder of an AI startup offers their experience:
“We've had Big Tech folks consistently fail our interviews on some rather fundamental engineering best-practice questions. We don't ask Leetcode questions and never will, but we found that BigTech candidates (Meta, Google, Stripe) had a particularly hard time with basic system design and coding questions.”
There are other reasons, including:
“Entitlement.” One thing mentioned by a few folks at startups is that some recruits from Big Tech are noticeably pleased about that fact, with a “I worked in Big Tech, therefore I’m awesome” mentality. Of course, it’s understandable to feel pride at having got into Big Tech and gained valuable experiences, as a career achievement. But when joining a startup from Big Tech, it seems sensible to be driven more by curiosity and humility, than judging a new workplace by the old one.
Startups do operate very differently from large companies, and the best way to make a difference and not alienate colleagues is to soak up a new environment, first!
Success in Big Tech is often about managing optics, sometimes without real stakes. A founding engineer shares that there are plenty of seemingly successful engineering leaders in Big Tech who operate well, run great meetings, have excellent project management skills… and still ship lackluster products.
Some characteristics can appear as ownership and agency, when they’re not. So, it’s easy to hire folks who are good at following processes, but not at being owners. Former Stripe product manager Shreyas Doshi describes this in the thread, [“Operators optimizing for optics.”](https://substack.com/redirect/961dd7e5-2376-48a7-a712-09772b2f933a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
Lack broad experience with tools. A founding engineer at a fintech startup shares:
“I came across folks with FAANG experience who did not even know JOINs on SQL! This was because they've only queried their internal non-relational datastore.
I had a friend who bragged about 10x-ing the QPS on a service at Google, but when I asked how they'd approach a Flask app running Postgres, they were completely clueless as to where to even start.
There's real skill in navigating FAANG stacks, but it's frequently using internal tools that someone else wrote for a promo packet, with little bearing on the "stitching together open source tools" of startup-land.
Many ex-FAANG people are unprepared for the upfront cost of learning the ecosystem outside of their silo. Non-technical startup founders or executives don't predict this; they just see the elite job background, and assume all candidates from that background will be strong in a role.
Focus on things startups don’t care about. An ex-Google engineer working at a startup says:
“Most FAANG engineers I've met do years of work without ever talking to a customer. In the ZIRP 2010s especially, they never had to worry about a cost, ever.
In a FAANG environment, there's a lot of focus on things that your early startup shouldn't care about – but which FAANG engineers do!
These include:
A deep engineering ladder and promotion process
Expectations of consistent and/or relaxed working hours
Make most decisions in meetings
Architecture reviews
Restarting work because someone found a technical snag that prevents a hypothetical scaling event
Technical things:
Ceremonies for "clean code" (whatever that means)
Building for future scalability
Copying the tech stack of their previous Big Tech workplace.”
Big Tech talent can have a magnetic pull, but the quotes above indicate there’s plenty of ways that it can not work out in small workplaces. Circumstances when it doesn’t make business sense for a startup to hire for a Big Tech profile, include:
Many startups don’t actually need Big Tech expertise, especially not in leadership. An engineering manager at a startup in San Francisco explains:
“Leadership that has only operated at Big Tech often doesn’t know the realities of operating at a smaller scale. For example, planning years in advance at a startup is usually a waste of time because things change so quickly. But such planning is required in Big Tech!”
Unfamiliar with “startup infra” and pace. A downside of hiring from larger companies is that Big Tech engineers and managers are often used to shipping faster. In some Big Tech companies, they might have mostly been building on top of sophisticated, Big Tech-specific infrastructure, and be unfamiliar with common cloud infrastructures which many startups use, like AWS, GCP, GitHub Actions or similar tools. Outside of Amazon, Big Tech companies almost always use their own infrastructure, not public cloud providers. Google doesn’t use GCP.
A startup founder in Boston says:
“Some Big Tech companies are particularly bad at honing skills that translate to startups. For example, Google engineers usually focus on very small product surface areas, and all the work is on very specific Google infra stack.”
Big Tech companies typically generate around $400,000 to $1,000,000 in revenue per employee, while being extremely profitable. It is thanks to this kind of revenue generation that they can justify paying senior-and-above hires $500,000 a year or more in total compensation (in the US: adjusted to regions, but still paying [top tier compensation](https://substack.com/redirect/71c0ad58-d27a-4d14-8dff-e4ba486bd2bb?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).)
If a startup has a business model to eventually generate this kind of revenue, it means the business fundamentals exist to compete with Big Tech on comp. But if the business isn’t forecast to earn so much revenue, then paying the same kind of compensation as Big Tech isn’t sensible, nor practical.
Pure software startups often have a theoretical business model to get to Big Tech revenues. This is why it makes sense for such startups and scaleups raising venture funding to offer similar base salary and equity. These businesses then need to execute: grow their market and revenue.
Most of Big Tech is used to doing more with lots of resources. For example, it’s impressive that Meta built the social media site Threads in 6 months, got 100 million users in the first week, all with a starting team of 12 people, but this was done by building on top of Instagram’s infrastructure. Things like the storage and compute layer did not need to be built from scratch.
Compare this with the Bluesky team building its social network from scratch: it took much longer, done with very little Big Tech experience. And it’s not a given that all Big Tech engineers can “do more with less” well, which is essential at early-stage startups. But sometimes it does make sense to hire from big places; Bluesky [hired Dan Abramov](https://substack.com/redirect/61a5e3e2-97b8-4fda-92c7-a14f1af361ee?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) from Meta. We cover more about [How Meta built Threads](https://substack.com/redirect/8460cdad-346f-4995-9a6b-6dcfa40ec92b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), and [How Bluesky was built](https://substack.com/redirect/53a5f7ed-470f-454c-8c26-59ca8e4cf038?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) in deep dives.
Among the Big Tech companies, Amazon is typically the closest to operating infrastructure like a startup, by running on AWS services. We cover more about why Amazon is a common source of startup hires, later.
If the goal is to get from zero to one in a difficult problem space by using as few resources as possible, Big Tech probably isn’t the place to do it. The biggest companies are good at solving novel problems with lots of resources, but are getting better at solving common, well-understood problems with fewer resources (headcount). Generally, Big Tech isn’t where a scrappy mentality for building novel solutions on a budget thrives.
A good example is AI companies. Google has an applied AI team that is easily 10x the size of OpenAI. And yet, OpenAI out-executes Google in novel product releases. Google, to its credit, is pretty good at catching up in problem areas that are well understood, such as shipping [enterprise-ready APIs](https://substack.com/redirect/1cd466ad-e269-47d8-bcae-d580fc672abb?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), or [enabling](https://substack.com/redirect/d0d938e9-25e1-4231-995c-8bc6e90d0d07?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) its AI solution (Gemini) for enterprise Google Workspaces. We cover more [on how OpenAI ships so fast in a deep dive](https://substack.com/redirect/4a657eb9-1998-4187-aa54-306f7b67d44a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).
An engineer at an early-stage startup puts it like this:
“In the absence of real stakes, many ex-FAANGers I've met view the focus on code and architecture quality as "doing the job of software engineering" and providing value.
In early-stage startups, the goal is to hit product-market-fit as fast as possible, it’s not to get high-quality code out the door. This difference means the day-to-day work is also different. Software engineers at startups should focus on what customers care about, and much less on what other software engineers care about.”
Related to this last point, here’s a deep dive on [how to thrive as a founding engineer in a startup](https://substack.com/redirect/ef713c11-3036-45c8-b659-0aebf4881ff5?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).
When building a company in a very different style from Big Tech, hiring from those places makes less sense. For example, when building a full-remote workplace, hiring from companies which mandate being in the office for most of the week, isn’t optimal. Of course, there are plenty of people in Big Tech who are tired of how things work there, and would like to try new ways of working. These people can bring valuable experience, without being tied to Big Tech processes.
If there’s no strong reason for hiring from Big Tech, why do so? Startups need a very good story to tell Big Tech folks in order to close them, even with compensation packages that match Big Tech. If that compelling story has yet to be written at a fledgling startup, then why bother paying the top of the market?
Despite the downsides mentioned above, there are naturally plenty of reasons to hire from large, high-performing companies! These include:...
Become a paying subscriber of The Pragmatic Engineer to get access to this post and other subscriber-only content.
| Full articles every Tuesday and Thursday | |
| Access to resources and templates for engineering managers and engineers | |
| Access to the complete archive, see all comments and comment on articles |