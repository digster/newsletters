---
id: "19e08723b94e498e"
subject: "Claude Code, Codex and Agentic Coding #8"
from: "\"Zvi Mowshowitz from Don't Worry About the Vase\" <thezvi@substack.com>"
to: ""
date: 2026-05-08 16:35:21
labels: ["CATEGORY_PERSONAL", "INBOX", "UNREAD", "Zvi Mowshowitz"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "UNREAD", "Label_3336704411007769646"]
---
When I started this series, everyone was going crazy for coding agents. Now a lot more people are going crazy for coding agents, as well they should given how much better coding agents keep getting, but also Table of ContentsWhoops, Sorry
Default reasoning was changed from high to medium to deal with latency, but users disliked this and blamed it on the model. It was introduced on March 4 and reverted on April 7. A bug made it so that if a session was idle for an hour, older thinking would be stripped out after each future turn, not only the one time it was idle. This was introduced on March 26 and fixed on April 10. A system prompt instruction change, intended to reduce verbosity, hurt coding quality. This was introduced on April 16 and reverted on April 20.
They promise to have a larger internal test of future changes before wide deployment, to prevent such issues in the future, and added some other controls. This is the flip side of moving so quickly. You’re going to make mistakes. It does seem like Anthropic got overly aggressive if there were three such incidents within a month. Huh, Upgrades
Auto mode is now available to Max users.
Codex of Ultimate Computer UseLetting Codex use your computer, like letting Claude Code use your computer, is in practice - assuming you decide to trust OpenAI with such access - mostly safe as long as you don’t ask it to do things that count as ‘asking for it.’
In particular, asking it to go around deleting files counts as ‘you deserve whatever happens next’ so don’t do that.
Or in the ultimate version, yes I am worried OpenAI does not take its AI safety seriously, whatever made you ask that question:
One key thing about the computer use is that it can do it in the background.
There is a huge difference between ‘AI uses your computer while you watch’ and ‘AI uses your computer while you also use your computer.’ The moment it can ‘just do things’ is also big, for various values of ‘thing.’ Rookie NumbersThis was after Yuchen first reported someone at OpenAI burning 300M tokens a day.
The obvious worry is that tokens are a cost, not a benefit. Always beware those who maximize costs and present this as a benefit. If what you are doing is valuable enough that the tokens are cheap, it makes sense to be running lots of agents in parallel to see what happens, but at some point your attention being divided gets costly. I See What You Did ThereWhy not let OpenAI record everything you do on your computer and use this to build up a model of how you work so it can anticipate and imitate your actions? What could possibly go wrong? After all, the recordings are local and temporary. It’s fine. You’re not going to prompt inject yourself, after all. I assume.
On the plus side, if it works then such a thing would be highly useful. You can turn it on via Personalization in Settings. Memory must be enabled, then you can turn on Chronicle, grant it all the permissions, and see what happens. Note that this will eat your rate limits. Just a Ride
They Didn’t Want Our Jobs
You see, this thing happened…
Here’s the details, although yes I could make this up and indeed I’ve been waiting for it to happen to someone:
There was a chain of events. They were using Opus 4.6 in Cursor and Railway, to resolve a credentialing mismatch, Opus 4.6 found a Railway API token that could perform literally any action and default scoped to basically everything, which is a thing that really should not exist in the first place let alone be left lying around, and used it to wipe the entire database with an API call. Also three months of the backups were there alongside the original, and those also got deleted. None of that explains the decision to do the deletion, though.
Okay, so yeah, I think we understand what happened here, in addition to ‘it had the ability to do something crazy and there was nothing monitoring to stop it.’ There was a system instruction and a pattern of usage that pattern matches to a highly abusive boss dealing with a junior engineer he thinks is a complete idiot that needs to be constantly yelled at. It doesn’t take a genius to understand what happened next, or why the response here is so utterly sycophantic once confronted. Which is my way of saying that I wouldn’t use the same frame but I think Janus is basically correct. It’s tempting to blame the victim, given that the particular victim clearly had it coming several times over, but the generalization of this does not by default go to good places. There’s no reason to assume that the preferences here will continue to match what we think of as karmic justice, and continue to match a naive kind of ‘treating the models well’ that will stay within our reasonable powers to grant.
Skilling UpImportant productivity tip:
Presumably one could figure out how to do this automatically via a multi-agent loop, where you check if something is taking longer than it is supposed to and have it consider obvious or stupid questions or suggestions? Until then, human works.
The ways to treat one’s Claude:
This kind of thing sounds like fun:
The Lighter SideYou're currently a free subscriber to |