---
id: "19da3078b903ceca"
subject: "Went to another AI hackathon! Tried to make 'agentic' code reviews better"
from: "Arnav Gupta from system bashing <systembashing@substack.com>"
to: ""
date: 2026-04-18 23:57:20
labels: ["Arnav Gupta", "CATEGORY_PERSONAL", "INBOX", "UNREAD"]
label_ids: ["Label_2739595779997728054", "CATEGORY_PERSONAL", "INBOX", "UNREAD"]
---
|
I have written a bit about it in the past, that I think code reviews have not really been improved by LLMs properly yet.
You’ll hear in many company stats things like
our diffs per developer went up by 200%
our LoC per diff went up by 130%
AI-generated code is 92% of all code written
From a classical SDLC standpoint, all these are metrics on the left hand side of the code review gate.
The code review gate itself has not been transformed, instead it has been cut from the bottom a bit to make space for some PRs to go through unchecked.
Two things have happened.
‘drive-by’ reviews are done using tools like Greptile, Qodo, CodeRabbit etc. (these are not bad per se, but they only review what is in the diff, so it will not include other context, like something that is not changed in this diff but might be impacted because of this diff.)
Actual proper code reviews have actually become more and more difficult now because the number of diffs itself has increased. More than that, the size of the diff itself has also increased because it’s easier to just generate larger diffs.
I think what really needs to happen with code reviews is that we need to be able to create an agentic code review environment. What that means is that we have agentic coding environments versus example are vibe coding environments like Lovable, where you just speak things and you see a website appear. Then there is Claude Code or Codex, where you actually have an environment where you are writing code. Similar to that, we want to be able to create an agentic code review environment. Unlike a vibe review where you outsource the review to an agent—sending the link of the diff to an agent and saying, “Hey, just review it and let me know”—you are actually sitting inside the code review environment. You have the diff open and are reading it line by line, and asking questions like “why does this line do this?” and each such questions fires off the agent to start diving more into the diff and provide and answer to that.
The project we built at the hackathon today is an attempt to create this environment. As you can see in the video above, you can start a review from the PI coding agent, and it creates a temporary website where you can do this agentic review.
This needs more polish before releasing properly but you can give it a spin from here
system bashing is free today. But if you enjoyed this post, you can tell system bashing that their writing is valuable by pledging a future subscription. You won't be charged unless they enable payments.