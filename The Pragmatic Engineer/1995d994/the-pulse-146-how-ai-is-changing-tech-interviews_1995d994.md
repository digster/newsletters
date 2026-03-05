---
subject: "The Pulse #146: How AI is changing tech interviews"
from: "The Pragmatic Engineer <pragmaticengineer+the-pulse@substack.com>"
to: ""
date: 2025-09-18 16:11:43
labels: ["CATEGORY_PERSONAL", "INBOX", "The Pragmatic Engineer", "UNREAD"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_6413324878686416177", "UNREAD"]
---
👋 Hi, this is Gergely with a subscriber-only issue of the Pragmatic Engineer Newsletter. In every issue, I cover challenges at Big Tech and startups through the lens of engineering managers and senior engineers. If you’ve been forwarded this email, you can
|
Before we start: we are doing research on MCP server best pratices. Do you use MCP servers at work, or did you build one/more? We’d like to hear from you. You can [send details via this form](https://substack.com/redirect/8266d125-a6c3-4748-bdcc-a33daf88672b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). We’ll share findings with people sending details – and, of course, in the newsletter as well, at a later date. Thanks for your help!
The Pulse is [a series](https://substack.com/redirect/818c62c9-756e-4a93-9bc2-6a76d435570d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) covering events, insights, and trends within Big Tech and startups.
Today, we cover:
How AI is changing tech interviews. New details about harder questions for candidates, growing cheating concerns, and the rise of AI-assisted interview processes, from 63 engineers in Big Tech scaleups, and startups, who are interviewers on the mock interviewing platform,
[interviewing.io](https://substack.com/redirect/9733c076-bc8b-42d9-a755-0ca9a2768244?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).New trend: devs vibe coding internal tools. An increasingly popular use case among software engineers is using AI agents to vibe code simple tools that would normally take hours or days to write.
Industry pulse. Security nightmare at npm, Microsoft joins the “three days in the office” club, Klarna goes public, Meta to close down small engineering offices, and more.
The team at interviewing.io has surveyed interviewers on their platform from Big Tech and startups; asking how AI is changing interviews in their workplaces. They received 63 detailed responses, and this newsletter is the first to publish the findings.
Special thanks to Aline Lerner, who shared data with me. Aline is founder of [interviewing.io](https://substack.com/redirect/0fe19adc-27ec-4f5a-b8ed-31e5dd462f52?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), co-author of [Beyond Cracking the Coding Interview](https://substack.com/redirect/3c6e945a-37b7-469c-a9a4-8d61623e4a45?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), and creator of the [Whiteboard Confidential Podcast](https://substack.com/redirect/0d838b2e-0c7c-40c5-8ea1-e81cacdc4a09?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).
Most respondents work in Big Tech (Apple, Google, Meta, Microsoft or Netflix), or in New Big Tech (Uber, Stripe, DoorDash, and others), while others work at startups:
How big a problem is cheating in remote interviews? According to the survey responses, it is widespread:
81% of interviewers at Big Tech and New Big Tech said they’ve suspected candidates of using AI tools to cheat during interviews
31% of interviewers at Big Tech and New Big Tech have caught a candidate cheating in an interview; that is, definitely using AI tools to provide answers which they claim as their own
Meta is the only Big Tech making company-wide changes to combat cheating, based on this research. From a Meta interviewer at interviewing.io:
“Cheating prevention is pretty front-and-center at Meta right now. We now have to mark whether we suspect a candidate of cheating across nearly all interview types/levels, and provide justification if so. Previously, it was only coding interviews. We also are requiring candidates to share their entire screen and turn off all background filters (including blur) in most interviews as well.”
Another interviewer at Microsoft mentioned that their team is taking steps to detect cheating tools, but it’s not company-wide. Other interviewers said their workplaces have not changed anything. One engineer at a New Big Tech giant said:
“My company is moving slowly, despite numerous incidents of cheating and other issues being raised.”
So, why is AI cheating a matter of concern for interviewers, but many companies don’t respond? My take is that this is down to a few things:
At Big Tech, changing company-wide processes like interviewing is slow. Until there are major incidents around cheating, there’s probably no trigger for change
Most Big Tech interviews have worked the same way for 15 years, so reform is inevitably sluggish
Counter-intuitively, it might be easier to bring back in-person interviews than to roll out “anti-cheating” policies. Google is likely getting ready to do more in-person interviews because more candidates are using AI tools in interviews, and Google wants to ensure that “the fundamentals are there”, as CEO Sundar Pichai said
[in June](https://substack.com/redirect/1e74f96b-1092-4fc7-96a2-5247ae52ffbf?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
Meanwhile, Interviewers seem to be taking matters into their own hands and battling cheats with AI tools by asking harder questions. 58% of Big Tech interviewers said they have adjusted the kind of questions they ask in an effort to combat potential AI “cheat tool” usage. Here’s what survey respondents at various companies told us (each point is a single interviewer’s approach):
Meta:
More open-ended questions which probe thinking, rather than applying a known pattern
Add variation to popular questions because this often catches cheats off guard – at least, for now it does
Ask questions with much longer descriptions and more complicated setup steps, which are harder for AI tools to perform well at
Microsoft:
Using coding problems that are more complex, to which LLM solutions often contain clues that reveal their usage
Asking questions that require candidates to explain concepts fluently, for which reading an AI-summarized answer won’t work as well
Testing how candidates can expand on existing logic using class structure, instead of rewriting the entire logic. Again, LLMs are not great at this – yet
More focus on systems-level understanding, and more complex, practical implementation questions
Asking a modified version of a LeetCode question
Setting questions that are worded to trigger wrong responses from popular LLMs like ChatGPT
Amazon:
Fewer copy-pasted LeetCode questions. Instead, questions are based on similar concepts, but with different wordings and outcomes
Some engineers create variants of problems to make it difficult for candidates who only memorize solutions to questions
Google:
Not asking LeetCode-style questions. Instead, asking questions with many sub-parts which are problem-solving heavy, not coding-heavy.
Setting problems that are abstract and not tied to a single answer. Also, asking questions with multiple solutions for which candidates use reasoning skills.
Using different terminology, and wording questions differently in ways that AI tools aren’t trained on. Asking more complex questions which require 2 or more data structures or algorithms
Apple:
Asking more real-world questions and fewer algorithmic ones
Netflix:
No change in questions asked.
As mentioned above, questions are getting harder because of AI cheating tools, and interviewers are making it harder for invisible AI helpers to be useful by:
Asking variations of public LeetCode questions
Asking more practical or more complex questions
Asking more abstract questions
Focusing more on problem-solving, and less on coding
Interviewers are also changing their approach. Interviewers at Big Tech and New Big Tech report that they’re adapting in order to tackle AI cheating by:
Looking for “AI patterns.” There are noticeable patterns in responses provided by AI. When an interviewer notices a candidate using a pattern, they look into it.
Focusing on the “why.” Ask why a candidate made choices, and have them explain in detail.
More follow-up questions. Pushing candidates to explain their thinking, which an LLM struggles to do.
More granular questions. “What does this line of code do, what would happen if we remove this line, what is a different way to do the same thing?”
Ask again. Ask the same question again, later. A candidate not using AI will give the same answer, whereas a candidate relying on AI is likely not to because AIs are non-deterministic.
“Rapid fire” questions. Increasing the pace of questions so there’s not enough time to type them as prompts, and cutting opportunities to recite AI responses from a screen.
Candidates explain their thought process. A good answer is no longer enough; interviewers push candidates to explain their thinking and reasoning, in depth.
Among 53 respondents from Big Tech and New Big Tech, NOBODY said their company has moved away from algorithmic questions.
However, over half of respondents said that in 2-5 years’ time algorithmic interviews will be less prominent than today. In contrast, around 20% of respondents are convinced that algorithmic interviews will never go away.
We cover this topic in the deepdive [How experienced engineers get unstuck in coding interviews](https://substack.com/redirect/f52a9a51-3726-4ccd-9786-be30b48e1a9d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).
An amusing finding: Big Tech companies aren’t changing their interview process much, but startups are:
The most common changes at startups:
No more algorithmic questions. Lots of startups are doing away with these, as they are trivial for AI tools to solve and don’t emulate day-to-day work.
No more takehomes. AI tools are very good at solving takehomes, and candidates increasingly simply input theirs into a tool like Claude Code. Startups used to set takehomes frequently, but AI tools mean they offer close to zero signal these days, and are being dropped.
AI-assisted interviews replacing algorithmic ones and takehomes. More startups are adding an interview to their main loop where candidates need to use AI tools while sharing their screen. They solve more ambitious tasks, while also simulating day-to-day work, as almost every engineer at startups uses AI coding tools!
Shopify has moved to adopt AI-assisted interviews. Here’s what its Head of Engineering, Farhan Thawar, had to say about it (watch the full interview [in this recording](https://substack.com/redirect/5273b79f-3c9a-40c8-a213-cbf9489c64bc?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), [from 41:49](https://substack.com/redirect/5273b79f-3c9a-40c8-a213-cbf9489c64bc?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)):
Gergely: “Hold on. So you're using AI during your interview process?”
Farhan: “Yes.”
Gergely: “You’re not running away from it.”
Farhan: “We're embracing it.”
Gergely: “How's it working? Tell me.”
Farhan: “I love it. Because what happens now is that the AI will sometimes generate pure garbage.
We let candidates use whatever they want. Here's what I'll say:
If they don't use a copilot, they usually get creamed by someone who uses one. So they will have no choice but to use one.
When the candidate does use a copilot, I love seeing the generated code. I ask them: what do you think? Is this good code? Is this not good code? Are there problems?
I've seen engineers, for example, when there's something very easy to fix, they won't fix it. They will try to prompt to fix it. And I say, are you really an engineer? I get the nuance of just prompt and prompt and prompt. But sometimes the fix is right there and they will keep on prompting. I’m thinking: just change that one character – but they won’t change it!
And I think, I don't want you to use AI, 100%. I want you to use it, 90-95%. I want you to be able to go in and look at the code and say, oh yeah, there's a line that's wrong.”
You can [listen to the full interview here.](https://substack.com/redirect/1227b780-e5d4-4936-b4d5-d5487de579cb?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
Here’s the percentage of survey respondents who expect in-person interviews to return to their workplaces:
A caveat: all this data comes from engineers, not decision makers. Bringing candidates onsite has budget implications (e.g., flights and hotels) and logistics ones (meeting rooms need to be freed up for interviews.) Keeping interviews remote saves money and doesn’t require solving the problem of finding spaces in which to hold interviews. For logistical reasons like this, it’s likely that even companies that opt for more in-person interviews will probably keep screening interviews as remote.
My sense is that we’re in the midst of the biggest shakeup of tech interviews in the last 15 years. Since 2010, interviews at Big Tech and “top” startups have been predictable enough: algorithmic interviews, systems design, and behavioural interviews. But today, interviews seem to be changing in different directions:
Big Tech: business as usual, with questions modified due to AI. Interviewers are asking harder algorithmic questions, and modifying their strategies to catch AI cheaters during remote interviews.
Hybrid and in-person companies: return of onsites? For companies where engineers are expected to work 2-3 days at the office per week, bringing back in-person interviews is not a big deal. Plus, if a new colleague will work from the office, why not have candidates come and meet their potential co-workers? It’s still not clear which large companies will bring back in-person interviews, but there’s a sense that Apple, Microsoft, and Google could.
Startups and full-remote companies: embracing AI-assisted interviews. Startups are increasingly making Copilot, Cursor, and other coding tools part of their interview process and setting more complex problems for which AI coding tools are needed. This makes interviews more similar to day-to-day work, and larger full-remote companies like Shopify and Canva are also adopting this approach.
The one group of startups that has not changed how they interview is those using trial days or trial weeks. [Linear](https://substack.com/redirect/f3ea94da-4583-4f14-b2a9-3061d8393d9e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) pays candidates for a few days of their time to work directly with a team on completing a real project. In this setup, using AI tools is a feature, not a bug. The obvious downside is time commitment: candidates need to take off several days, and the company needs to invest nearly a week in evaluating just one candidate! It’s a big ask on both ends.
I hope you enjoyed this overview on how tech hiring is changing – and many thanks to the [interviewing.io](https://substack.com/redirect/9733c076-bc8b-42d9-a755-0ca9a2768244?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) team for their work.
Become a paying subscriber of The Pragmatic Engineer to get access to this post and other subscriber-only content.
| Full articles every Tuesday and Thursday | |
| Access to resources and templates for engineering managers and engineers | |
| Access to the complete archive, see all comments and comment on articles |