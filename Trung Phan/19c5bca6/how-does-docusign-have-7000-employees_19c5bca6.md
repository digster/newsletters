---
subject: "How does Docusign have 7,000 employees?"
from: "Trung Phan <trungphan@workweek.com>"
to: ""
date: 2026-02-14 05:55:15
labels: ["CATEGORY_PERSONAL", "INBOX", "Trung Phan", "UNREAD"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_7971156048460647958", "UNREAD"]
---
It’s just a digital signature tool, right? Hell, they keep your autograph and initials on file and all you have to do is click the box. That’s it? Why can’t I just copy and paste a template online in Word?
I ask these questions every time I’m signing a Docusign PDF that I didn’t read and hoped that I wasn’t giving away anything important in my life (TBD).
The meme was really funny when Docusign was worth ~$60B on $1.8B of sales during peak pandemic madness in 2021. It’s now worth a still respectable $10B, but on a much more reasonable multiple on $3B of sales (it went from 33x to 3x trailing-twelve-month sales).
Sufficiently curious about how a software company could employ (maybe) more people than the American federal government, I finally did some digging a few months ago.
I read through financial filings, some analyst reports and forum posts.
Man, was I wrong because Docusign having 7,000 employees is very reasonable.
My favourite explainer comes from a post in the r/WebDev subreddit. The post has since been deleted but I [got a screenshot](https://link.workweek.com/click/44129240.61837/aHR0cHM6Ly94LmNvbS9UcnVuZ1RQaGFuL3N0YXR1cy8yMDA5MzUzMTQ1ODkwMjk2MDgxP3M9MjAmaGFzaGVkX3VzZXI9MGViZWYxMmM0MjkxMTg0NTYyZGFjMDk5NjViY2U4MDg/6520d6df2061f24a7d071f97B7bcc636a) and let’s go through a fun thought experiment:
-
Let’s say most people use Docusign 5x a year. But 1% of power users are signing documents 10x a day. Among American adults, that would be (5 x 250 million) + (10 x 365 x 2.5 million) = 10 billion signatures a year.
- America is probably above average since the country is super litigious and lawyers love to lawyer. So, let’s assume the rest of the world does 25 billion signatures a year.
- So, that’s 35 billion signatures a year…or 95 million a day…or 4 million an hour…or 1,000 every second.
- This system has to work in 180 countries around the world, following local contract laws in each of them (that’s a lot of system administrators and lawyers).
- Docusign builds a hybrid cloud system in every country that keeps all records and a ton of back-ups across AWS, Google Cloud, Azure and its own data centres (that’s a lot of engineers and system administrators).
- In total, Docusign serves 1.8 million paying customers (including 3,000 government agencies and most of the Fortune 500).
- These paying customers are sending signature requests to over 1 billion users.
-
The headcount is about 5,000 employees for sales, marketing and support to serve that customer base. Another 2,000 employees for engineering, system admin and product development.
I don’t think anyone is vibe coding a Docusign product and gaining market share by undercutting current prices. Trust me, I tried for a solid 47 minutes. No bueno.
Nor will any serious company build an internal replacement. A 72-hour Claude Code session won’t be able to handle the required 99.9999999% uptime and semi-network effect with all the people that have a Docusign account.
If none of those numbers convince you of Docusign’s mission critical moat, allow me to share this glorious qualitative rant from the aforementioned Redditor:
So you’ve got to have multiple international teams of [System Admins] managing data centers all over the world. Except you have to be able to lose one of those datacenters without losing all the signatures stored there. So you need backups. And you need backups for those backups. And you need just-in-case code already written for if that data center goes offline for 5 hours.
And you need HR for those employees. And if you aren’t managing your own centers, you need business [execs to] negotiate contracts with whatever company you outsource to. And you need SO MANY f*cking Zendesk drones handling the infinite influx of people who can’t use the app or used the app wrong or got themselves in a weird situation.
Or sh*t man, what if something VERY IMPORTANT was signed, but the person who NEEDS THAT SIGNATURE RIGHT NOW forgot his password? Like really forgot? Lost access to his email?
He can prove that he was the owner of that real estate conglomerate during those years. He can pull up the proper legal paperwork. But you need a team of trained legal professionals able to sort through it and make sure he is who he says he is.
What happens when your signed documents are needed for a court case?
What happens when a judge has a warrant for them? What public-facing service are you going to build and maintain for judges in... oh yeah, every country in the world, using wildly different legal structures.
And they all need access to... potentially thousands of signatures all at the same time.
Nothing. Nothing at “global standard” scale, is simple. You’re looking at the face of it. There’s a monster underneath. Always is.
As fate would have it, Docusign CEO Allan Thygesen — a former top Google marketing exec — went on [The Decoder podcast](https://link.workweek.com/click/44129240.61837/aHR0cHM6Ly93d3cueW91dHViZS5jb20vd2F0Y2g_dj1kSkdUVHRxdWFEcyZoYXNoZWRfdXNlcj0wZWJlZjEyYzQyOTExODQ1NjJkYWMwOTk2NWJjZTgwOA/6520d6df2061f24a7d071f97B48c37b46) a few weeks ago and talked at length about these topics.
Some highlights:
-
How Docusign ensures digital signatures are real: “We do all kinds of IP tracing and other things to validate that you are the intended…signer [and] that you are the intended recipient. That whole trail is then auditable and can be used in a court of law. So, it’s a perfect substitute for a wet signature that you might otherwise have done…We worked on a federated identity strategy to give you all kinds of identity validation at different levels of risk. We let people do knowledge-based authentication…We do biometric-based identification [eg. video]. We can link up with the Apple and Google stuff. We do risk-based assessments…We use the new digital IDs [eg. Clear or ID.me, which is the government one that the IRS uses].
-
Docusign’s customer demographic: “We’re incredibly diversified. We are used by 1.8 million companies. By definition, if you have that many customers, most of them are going to be small. But we are used by over 95% of the Fortune 500 and equivalent in many other international markets. Then, many mid-sized companies, and then a huge long tail of small companies. No one company represent any meaningful share at all of our business. That said, our biggest customers tend to be banks or other large companies that have high volumes of high value agreements. You know, if you have agreements that matter, and you’re entering to them in large volumes, you’re very likely to be a Docusign customer.”
-
The breakdown of Docusign’s employee base: “Sales and marketing is the biggest area. We have about 1,000 account executives that cover everything from SMB accounts, all the way up to enterprises. We’re not a small company. We do over $3 billion in revenue. Our revenue per employee is pretty much in the median of the SaaS businesses. So sales and marketing is the biggest function. It’s everything from pre-sales to account executives to customer success people to help with implementation and support. We have about 1,000 people in engineering…and then there are product managers and designers and so on.
I think if you look at the number of countries and the complexity of the regulatory and compliance environments we’re in, that’s a significant effort.”
Thygesen became Docusign’s CEO in September 2022.
A month before ChatGPT launched. He’s been competing only in the generative AI world and believes it is much more of an opportunity for Docusign…rather than a threat.
Even if a legitimate AI-native competitor was launched, Docusign is sitting on juicy proprietary dataset: 150 million private consented agreements with 10 million being added every month (this legal data set is “orders of magnitude bigger than anybody else”).
Docusign is using this data trove to help customers create legal documents and find value that may have otherwise slipped through the cracks:
[Customers always have a template] for something really complex (like an M&A agreement) or something really simple (like an NDA) or anything in between. [It] could be a master service agreement between company and another company, or a license agreement. But they always have a template.
Then, they tailor it. Some of that is done sort of legal tailoring, right? [They’re] going to have different limitation of liability. [They] want to have a different payment term. Some of it is just mass customization. [They] want to get the data about [customers and previous negotiations].
Then, they want that to flow automatically from whatever the system of record is. Could be Salesforce. Could be Workday. Could be SAP. And [they] want to populate that into the agreement. […]
The other piece is [that Docusign will] take AI and…extract data out of the agreements to run [the] business better. That’s something that was conceptually possible…but it was just too heavy and hard to do with legacy LLMs. Now, [Docusign] can do that in a completely automated way.
So we can go [to customers] and say “Hey, you have 5,000 agreements with me. Would you like to know what’s in them? Let me highlight how these agreements deviate from agreements with peers. You know, your company X is coming up for renewal in 90 days. How can [you review or improve] that?”
Due to the mission-critical (and, errr, legal ramifications) of the work, Docusign creates all of its workflows to keep humans in the loop:
We have a whole queuing system where a sales rep or a procurement rep can trigger the sending of documents for legal. It can get an automatic first review.
Then it gets assigned to a lawyer. The lawyer does a quick edit. Everyone has real time status.
That’s an example of reimagining the legal workflow, which today is totally asynchronous emails, unpredictable and non-transparent. […]
Of course, we benchmark you versus your existing templates or playbooks, as they’re often called inside of companies. And highlight things that deviate from that. And this is true both for agreements that the company prepares themselves and for third-party agreements that they receive from others. Because, of course, most companies are takers of terms from other companies, right? […]
We also don’t fully automate flows. We deliberately put humans in the loop at key decision points. And I think that will persist for a very long time.
The biggest AI challenge may be the new customer habit of asking ChatGPT or Claude or Gemini to query legal documents. Not because it’s an alternative to Docusign. But because Docusign has had to create a chat tool.
Thygesen and his team think this is a valuable feature, especially as they can customize LLM models with the >150 million consented agreements.
However, he acknowledges the models can never be 100% accurate and that’s a risk if the customers believe otherwise and end up making a costly uninformed decision based on the chat tool.
Now, I’m not saying Docusign is perfect. I’m not saying Docusign can’t improve. I’m not saying anything about what the proper Docusign valuation should be. I’m not even saying Docusign couldn’t run a bit leaner.
I’m just saying, “Docusign, I’m sorry for laughing at all those Why Does Docusign Have 7,000 Employees memes. It makes a lot of sense and a one-person AI startup isn’t going to replace you.”
***
Going back to my earlier bullet points about AI and SaaS, Docusign serves a mission-critical task, owns proprietary data and establishes tight customer integrations while taking on legal and regulatory risk.
Docusign is a good example of this reality: most large firms (>1,000 employees) simply don’t want to waste resources building and maintaining random tools that aren’t their core competency.
On that note, a recent piece from The Economist shared this striking chart.