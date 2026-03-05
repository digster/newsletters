---
subject: "Opus 4.1 Is An Incremental Improvement"
from: "\"Zvi Mowshowitz from Don't Worry About the Vase\" <thezvi@substack.com>"
to: ""
date: 2025-08-06 19:48:36
labels: ["CATEGORY_PERSONAL", "INBOX", "UNREAD", "Zvi Mowshowitz"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "UNREAD", "Label_3336704411007769646"]
---
Claude Opus 4 has been updated to Claude Opus 4.1. This is a correctly named incremental update, with the bigger news being ‘we plan to release substantially larger improvements to our models in the coming weeks.’ It is still worth noting if you code, as there are many indications this is a larger practical jump in performance than one might think. We also got Tomorrow we get an OpenAI livestream that is presumably GPT-5, so I’m getting this out of the way now. Current plan is to cover GPT-OSS on Friday, and GPT-5 on Monday. Introducing Claude Opus 4.1
They lead with this graph, which does not make the change look impressive.
They also have this chart, which doesn’t look like much. What they probably should have led with is this some combination of this, in particular the report from Windsurf:
A similar jump as Sonnet 3.7 to Sonnet 4 would be a substantial win. The jump is actually kind of a big deal?
Taste improvements? But Garry Tan assured me it would never.
The System CardThe topline report is that it is not ‘notably more capable’ than Opus 4, so the whole system card and RSP testing process was optional.
There has to be some threshold, we don’t want 4.0.1 (as it were) to require an entire round of full testing. I am glad to see that Anthropic chose to do the tests even though their rules did not require it, and ran at least an ‘abridged’ version to check for differences. Given we had just made the move to ASL-3, I would have put extremely low odds on an incremental upgrade crossing important additional thresholds, but I do notice that the criteria above seem a little loose now that we’re seeing them tested in practice. Anthropic presumably agreed. This is a large improvement, cutting failures in half. It comes at the expense of more refusals on benign requests. If those are real percentages in practice, and it does match my experience (I’ve had a total of one refusal, and it led to a ‘oh I see how that happened’) then I think This Is Fine. Worst case is you can switch to extended thinking when it gives you a no, sir.
Mostly we see what look like measurement errors and random fluctuations. These tests mostly don’t meaningfully differentiate, aside from the refusal rates above, between 4.0 and 4.1. The changes were narrowly targeted. Given we’d already triggered ASL-3 protections, the question was whether this rises to needing ASL-4 protections. It seems very clear the answer is no.
The 99.99% uptime is, shall we say, highly aspirational. I would not plan on that.
ReactionsThe problem with reactions to incremental upgrades is that there will be a lot of noise, and will be unclear how much people are responding to the upgrade. Keep that caveat in mind. Also they updated the system prompt for Claude.ai, which may be getting conflated with the update to 4.1.
All of this points in the same direction. This upgrade likely improves practical performance as a coding agent more than the numbers would indicate, and has minimal impact on anything sufficiently distant from coding agents. Except that we also should see substantial improvement on sycophancy, based on a combination of reports of changes plus Amanda Askell’s changes to the prompt. You're currently a free subscriber to |