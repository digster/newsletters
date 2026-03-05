---
subject: "Quality Assurance Across the Tech Industry"
from: "The Pragmatic Engineer <pragmaticengineer@substack.com>"
to: ""
date: 2024-02-06 17:17:24
labels: ["CATEGORY_PERSONAL", "IMPORTANT", "INBOX", "The Pragmatic Engineer"]
label_ids: ["CATEGORY_PERSONAL", "IMPORTANT", "INBOX", "Label_6413324878686416177"]
---
👋 Hi, this is Gergely with a 🔒 subscriber-only issue 🔒 of the Pragmatic Engineer Newsletter. In every issue, I cover challenges at Big Tech and startups through the lens of engineering managers and senior engineers. If you’ve been forwarded this email, you can
|
We [previously dived deep](https://substack.com/redirect/48db61d1-368d-4ad3-9a02-4eaebca83752?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) into how 7 Big Tech companies – Microsoft, Google, Meta, Apple, Amazon, Uber and Netflix – approach quality assurance, covering how Microsoft retired its “dedicated software engineer in test” (SDET) position in 2014, while Apple and Amazon retain a high focus on dedicated QA.
Today, we look beyond Big Tech, and analyze details from 47 tech professionals at different tech companies, who responded to a survey I put out about how companies approach QA. Thank you to everyone who contributed!
In this issue, we cover:
Different forms of QA. QA, SDET, QE, TE, and quality coach roles.
Companies with no dedicated QA. Early-stage startups, mid-sized companies, and Indeed’s recent elimination of the QA role.
Indeed eliminated the QA role. Is quality down? In broad layoffs, Indeed discontinued dedicated QA roles. A software engineer saw a decline in quality, which seems normal after such a change.
Where QA is present, but declining. Cases from the accounting, manufacturing and the security industries.
Where QA still matters. Hardware, firmware, operating systems, infosec, and highly regulated industries, and more.
Mozilla’s approach to testing. The company behind the Firefox browser has test engineers (TE,) and quality assurance (QA) roles. They’re different, but each is important in ensuring the browser’s quality.
Insights from other tech companies. A startup where QA builds load and performance tests, a company producing a desktop app with a 1:1 dev-QA ratio, and different testing approaches among teams, even in one workplace.
The survey results contain interesting insights about QA-related roles, which is often associated with manual testing. At most places, this is what “dedicated QA team” means; people who manually test a product. This is not always the case, but QA can also focus on automation and is usually called something else, like SDET, QE, or TE.
These terms describe roles focused on automated testing.At companies which do very little dedicated manual testing, dedicated roles for quality assurance are often called:
Software Development Engineer in test (SDET)
Quality Engineer (QE)
Test Engineer (TE)
In these roles, the mandate is to support quality-related work. However, the role is not to test software products. The role is about automation, empowering engineering teams to do testing, or both. Common responsibilities include:
Building automated test suites: integration, or end-to-end tests
More sophisticated automated testing: load testing, performance testing
Developing new testing plans pre-release
Usability and accessibility product testing, or creating tools and playbooks for others
Exploratory testing
At companies with SDET, QA, or TE roles, the writing of automated tests is split between devs and SDETs/QEs. Often, there are significantly fewer SDETs and QEs than developers.
A lead engineer working in a quality coach role at an Australian multinational, shared how they used to be a “quality coach” until their company made software engineers responsible for testing products, and formed a small group to support them, comprising:
A couple of QA engineers for products and initiatives
Quality coaches to help teams adopt healthy testing practices
Enablement teams (basically, platform teams) to build and improve tooling for automated tooling
Although this approach isn’t mentioned by more survey respondents, it makes sense for engineers to own quality in a transition from QA doing so. The concept of “quality coaches” seems to mirror agile coaches, common at companies rolling out practices like Scrum. Just as the “agile coach” role is redundant after teams learn the practices, so should the role of “quality coach” slowly disappear as testing becomes part of how engineering teams operate. Indeed, the respondee former quality coach works as a software engineer. We previously covered [how Big Tech runs projects and the curious absence of Scrum.](https://substack.com/redirect/0a5380ef-a364-4696-8741-17eafd7cd58b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
This transition also allows the company to convert QA staff into software engineers, if they’re willing to do more automated testing and software development.
We mention above that most teams and orgs at [Big Tech have no dedicated QA roles](https://substack.com/redirect/48db61d1-368d-4ad3-9a02-4eaebca83752?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), except for Apple and teams with hardware divisions, like Google and Meta. Broadly, there are plenty of businesses with no dedicated QA roles. Here are the most common types I’ve identified.
Unsurprisingly, new companies just starting out rarely hire folks dedicated to quality. This is what a survey respondent who’s a founder at a 3-person SaaS startup producing document storage, says:
“We are too small to have a dedicated QA person. One of our co-founders does most of the QA and Product Management.
Things inevitably slip and we have features deployed to Production which have caused minor outages or issues. But we are good at recovering from such issues. Our main focus is to not lose user data!”
At a 20-person Series A startup, a PM says they have no QAs, and engineers focus on automation:
“Engineers are responsible for the quality of the delivery. I am the only PM, I don't do any official testing. We do get some support from the open source community.
Engineers tend to follow Test Driven Development (TDD) and we have production metrics that feed back for engineers to observe. We also have high-level component integration tests in place.”
Hiring the first QAs as contractors seems to be common. A founder at a 20-person startup shares that they are hiring a freelance QA to help set up the company’s testing foundation.
A product and design PM at a profitable, 200-person, Series A company describes their place’s approach to QA:
“Product writes the specs at our company. Sometimes, those specs have specific paths to test. Engineering is responsible for QA, unless product asks explicitly to be included.
We used to have the expectation that product had to QA everything after it was finished. However, we abandoned this approach, focusing more on ‘speed.’ I added ‘speed’ in inverted commas because I feel we over-corrected;1 we now find bugs in prod that we have to fix immediately after a production launch.”
A chief engineer at a 150-person marketing agency shares that they’ve moved away from relying on QAs:
“We used to have dedicated QA, but now developers are responsible for delivery. They generally deliver behind feature flags and then collaborate with Product and Design before releasing.
I'd say QA is more fast and loose than it was before, but we're making smaller changes and generally in more focussed Greenfield areas.”
It’s neat to learn how this agency works; that testing is present, but that developers own it. From the chief engineer:
“We frequently deliver small pieces of software behind feature flags using continuous deployment. Before merging, we run unit and integration tests – we have a lot of them! Ideally, the team should do some level of pair testing together, but I admit this is frequently skipped.
What I'd like to see more of in our organisation is greater understanding of the business goal engineers are trying to hit. Focusing on this, even before they start writing code.
There should be a healthy amount of upfront design/thinking/questioning at the beginning of a project. Evaluating and testing with users comes at the end. In practice, both of these tend to be forgotten, and this is where most issues creep in!”
A 500-person retail and commerce company made product managers and developers responsible for the product’s quality, putting in place:
A staging environment for pre-production testing
Devs validating features before release
Encouraging, not mandating, automated testing
Surprisingly, a 600-person company with 50 software engineers that manufactures electric vehicle chargers, does not have a QA department, but does have test engineers. A cloud software engineer there says:
“Developers are responsible for writing unit and API tests for any new feature. Devs are also encouraged to add coverage where it’s missing. Each smaller software team within the unit has a developer with additional focus on the team’s test automation effort. These ‘test-focused’ engineers support shared efforts alongside normal duties.
A couple of company-wide ‘shared’ test automation engineers develop and implement different end-to-end test suites. These suites are run in a staging environment before production deployment. These test automation engineers support teams, on the side. We do not have dedicated ‘QA staff.’”
We previously covered how [most of Big Tech approaches QA](https://substack.com/redirect/48db61d1-368d-4ad3-9a02-4eaebca83752?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), often via automated testing. An engineering director at a 4,000-person, publicly traded company summarizes their approach to testing:
“Developers are responsible for testing and automated testing. Product may do user acceptance testing (UAT) on new features.”
This approach chimes with how many large tech companies operate.
Indeed is a job search platform and publicly traded company, employing more than 14,000 staff, of whom the company laid off 15% (2,200) in March 2023. The layoffs resulted in the elimination of the QA role, as most QA engineers were let go. Those not shown the door were given 6 months to pass an interview and transition to an SWE position. Since then, developers are responsible for all QA, manual testing, and automation.
A software engineer at Indeed tells me they’ve seen the quality of testing plummet:
“With the elimination of the QA role, we developers are left with testing solutions that were built by someone who isn't here anymore, so the overall quality of tests has nosedived.”
In fairness, it’s common for quality to dip after a role is suddenly eliminated, and a layoff. What tends to happen is engineers pick up new responsibilities, the testing strategy is adopted, and over the next few months, teams adapt. Without dedicated QA staff, you cannot operate as before! I expect Indeed to go through a similar transition.
It’s not only Indeed eliminating QA roles. A tech company based in Taiwan has done large layoffs, transitioning most former SDETs to developers, a software engineer shares. My hunch is the engineering leadership at that company hoped to have their cake and eat it by reducing the cost of engineering, while keeping quality as high as before. But quality usually drops automatically if employers mandate engineers to do more testing without a well thought-through transition away from dedicated QA.
An interesting group are companies with dedicated, but shrinking, QA teams. Here are groups that came up in this survey...
Become a paying subscriber of The Pragmatic Engineer to get access to this post and other subscriber-only content.
| Full articles every Tuesday and Thursday | |
| Access to resources and templates for engineering managers and engineers | |
| Access to the complete archive, see all comments and comment on articles |