---
subject: "Code Freezes: Part 3"
from: "The Pragmatic Engineer <pragmaticengineer@substack.com>"
to: ""
date: 2023-12-05 17:07:53
labels: ["CATEGORY_PERSONAL", "INBOX", "The Pragmatic Engineer", "UNREAD"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_6413324878686416177", "UNREAD"]
---
👋 Hi, this is Gergely with a 🔒 subscriber-only issue 🔒 of the Pragmatic Engineer Newsletter. In every issue, I cover challenges at Big Tech and startups through the lens of engineering managers and senior engineers.
|
It’s the last month of the year, meaning that engineering teams at some companies are preparing to start a “code freeze,” while others have already done so, and at a few places it’s business as usual.
This issue is the final part of a three-part series on the topic of code freezes, resuming almost a year after the last installment. In [Part 1](https://substack.com/redirect/3f1e38fb-308f-42d0-9b2c-d89451b5ef9e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) we covered:
Big Tech and code freeze approaches: Meta, Amazon, Microsoft, Apple, Google, Oracle, Uber
Code freezes at other companies: Spotify, X/Twitter, N26, Auth0, Podia
Code freeze upsides
Downsides of code freezes
Companies which don’t do code freezes
In [Part 2](https://substack.com/redirect/4a7b55fa-ae9f-4d2d-9c8c-62881f7c7ff6?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), we touched on:
Software product categories and code freezes
Informal and formal approaches to mandating freezes
Code freeze trends across industries
Code freeze alternatives: code chills, code slush, business as usual
“Wave and bake” instead of a code freeze; a case study from grocery retailer Ocado
Do you need a code freeze?
Now, we wrap up this subject with:
Dates worth keeping in mind. Apple’s store slowdown, and a 3-day workweek at the end of the year.
Code freezes by funding lifecycle. The later stage a company is, the more likely it puts a freeze in place. Bootstrapped companies seem the least likely to do anything different during the holiday season.
Company size. The smaller the business, the less likely there’s a formal code freeze.
By industry. An analysis of 185 data points on deployment freeze approaches at tech companies, contributed by readers.
Advice for those doing a code freeze. Avoid the “thundering herd” in January!
Advice for those not doing a code freeze. Ensure your engineering team gets a well-earned rest during the holiday.
Interesting code freeze approaches. Inspiration from Monzo, Outreach, LinkedIn, Block/Square, Stick Fix, Atlassian and Klarna.
The survey data. Anonymized responses from 185 data points.
In today’s issue, we analyze data from software engineers and engineering managers across tech on how their workplaces run code freezes. These data points come from a survey I published in Part 1; thank you to everyone who shared insights!
There are a few dates worth circling in your calendar when considering whether or not to mandate a code freeze.
The week of 25th December. This year, for most companies based in the US and Europe, the final week of the year is a 3-day workweek:
Whatever the code freeze approach – including not having one – it’s worth figuring out how many people will be around during the week of 25 December. Will there be enough for oncall? Or will oncall need to be merged across teams? What about people still in the office: should they delay risky production changes, even if there’s no formal code freeze in place, assuming most people will be on holiday?
The first week of January. When will normal work patterns resume? Will some staff take off the first week of January, or will most people return to the office?
iOS and Mac app submissions could take longer between 22-27 December, says Apple. Until 2021, Apple paused app reviews between Christmas and New Year. That’s [been adjusted](https://substack.com/redirect/8add27d6-9881-441c-88d5-4ad7fcb4a6a2?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). This year. Apple writes:
“App Review will continue to accept submissions throughout the upcoming holidays. Keep in mind that we anticipate high volume and reviews may take longer to complete from December 22–27. Plan to submit time-sensitive submissions early.”
Let’s look at the split of companies employing freezes, by funding lifecycle:
Unsurprisingly, the later stage a company is, the more likely it imposes a freeze around this time. And here’s one data point that seems to underscore funding’s role in how risk averse companies are when business is higher than during most of the year, but when more staff than usual are away:
Given there were only 13 data points on bootstrapped companies, I collected the reasons why they did or didn’t do code freezes. The bullet points are quotes provided by survey respondents.
Small bootstrapped companies (50 or fewer employees):
Those implementing a code freeze:
“All code bases have a freeze that lasts two weeks. This gives all team members a solid break without the stress of possible issues. The week leading up to Xmas, when most staff are still around, is used for cleanup and admin tasks, with the last day spent documenting state of play and brain dumping that makes for an easier unfreeze in the new year. Been doing this for 10 years and it’s been pretty much loved across the board.“ – CTO of a 25-person social networking business
“We encourage people to just take time off and rest, and we freeze code so nobody is forced to work. We have a freeze between 23 December and 2 January. Take the time you need, but if you want to work we have some tech debt tickets” – principal engineer at a bootstrapped FinTech company
“The code freeze lasting until 2 January is useful to force myself and my team to take a break. We don’t need to ruin anyone’s holiday because we weren’t thinking clearly before it. Everyone pretty much has the whole of Xmas week off.” – CTO at a startup with 3 developers
Workplaces with no code freeze – at least not on the backend:
“A code freeze makes all deploys around it bigger and therefore riskier. We value a steady risk profile rather than a bursty one.” – head of engineering at a bootstrapped crowdfunding platform
“Our product/stack is solid enough to never need attention, and so we have no oncall. If it does, then myself or the head of engineering will jump in.” – CTO at a security startup with 5 engineers
“Our backend services (Ruby and Python,) and platforms are asked to only do the minimum number of changes during the break. Delay big deployments until after the iOS and Android code freezes end. We do have code freezes for native mobile platforms.” – software engineer at 50-person startup in the food business
Larger bootstrapped companies (50-1,000 employees):
Those with a code freeze:
“We have reduced staff in the week leading up to the New Year, and put a freeze in place from the last working day before Christmas until after New Year’s, which applies to ALL codebases. The goal is to avoid outages and incidents.“ – software engineer at a SaaS company with staff in 6 locations globally
Workplaces with no code freeze – at least not on the backend:
“We make supervisory control and data acquisition (SCADA) and release it every 4 weeks. We expand our week-long QA cycle to 2 weeks at the end of the year.” – engineering manager at an industrial automation business. Sidenote: such a long release cycle renders a code freeze irrelevant.
“If something goes wrong with a deploy, the engineers making the change either roll forward a fix, or revert their changes. Our feature flagging practices are great. Our tests are really solid, our alerts are good. We have 15+ engineers putting out multiple PRs per day, we deploy so often that deploying at the end of the year is not a big deal.” – CTO at a bootstrapped order fulfillment platform
“There's a general (unwritten) rule that we don't typically deploy late on Fridays – unless it's an emergency fix, of course. However, programmers are empowered to make the call. The same view holds for holiday periods. Last year, the final merge to master was Fri 23rd Dec 2022 at 8:05 AM. The next was Mon 26th Dec 2022 at 7:56 PM!” – director of engineering at a 80-person SaaS business
JetBrains is a bootstrapped company, and one of the biggest firms to become a billion-dollar company without external funding. Since Jetbrains ships most of its products as releases, the company doesn’t need a code freeze. It just does not cut any major new releases, says a team lead at the company. Minor releases can happen during the holidays.
Bootstrapped companies have quirks worth noticing, as they must be as practical as possible, and are probably immune to trends of little practical benefit. We previously covered [lessons of bootstrapped companies founded by software engineers](https://substack.com/redirect/fd2b86ae-b4c2-4c85-a650-f0a434c9af3c?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).
Segmenting responses by workforce size:
There’s few surprises in this data. The larger the company, the more likely there’s an end-of-year freeze. This makes sense, as the majority of bootstrapped companies tend to be smaller. Within the group of “massive” companies (10,000+ staff) there tend to be even fewer exceptions to this than at very large workplaces:
Splitting responses by industry yields some interesting findings. There are intriguing – though not unpredictable – patterns:...
Become a paying subscriber of The Pragmatic Engineer to get access to this post and other subscriber-only content.
| Full articles every Tuesday and Thursday | |
| Access to resources and templates for engineering managers and engineers | |
| Access to the complete archive, see all comments and comment on articles |