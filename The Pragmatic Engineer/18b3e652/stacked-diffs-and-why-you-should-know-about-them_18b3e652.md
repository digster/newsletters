---
subject: "Stacked Diffs (and why you should know about them)"
from: "The Pragmatic Engineer <pragmaticengineer@substack.com>"
to: ""
date: 2023-10-17 16:05:47
labels: ["CATEGORY_PERSONAL", "INBOX", "The Pragmatic Engineer", "UNREAD"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_6413324878686416177", "UNREAD"]
---
|
👋 Hi, this is Gergely with a 🔒 subscriber-only issue 🔒 of the Pragmatic Engineer Newsletter. In every issue, I cover challenges at Big Tech and startups through the lens of engineering managers and senior engineers.
One of my biggest personal “wow” moments during my time at Uber as a developer, was when I began using stacked diffs. Stacking refers to breaking down a pull request (PR) for a feature into several, smaller PRs which all depend on each other – hence the term “stacked”. It might sound counterintuitive, but this workflow is incredibly efficient by making it easier to review and modify PRs – or “diffs” as we call them at Uber.
The concept of stacking has existed for ages at Google, but Meta was the first company to really popularize this workflow outside the company, by open sourcing its internal developer tool called Phabricator, which supports stacked diffs. To this day, Meta engineers live and breathe stacked diffs.
For today’s issue, I reached out to five former Meta software engineers for their insights on stacking. All are now cofounders, or early employees at the developer tooling startup [Graphite](https://substack.com/redirect/98f92422-1945-42bb-9fde-3b0d19993173?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), which builds this stacking workflow for any company using GitHub. I am a small [investor in Graphite](https://substack.com/redirect/d2ec22e7-dd92-4aa1-b216-9e76822de665?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) – after experiencing the major impact which stacking had on productivity at Uber, and being curious about why this tooling is not more widely available.
Today, we cover:
Stacked diffs: the concept
How Meta uses stacked diffs
Google’s approach to stacking: chaining
Stacking outside of Meta and Google
Meta’s other neat developer tools we’ve previously not covered
The impact of Meta’s developer tools on the industry
Working at Meta versus working at a startup like Graphite
Stacking is a tricky concept that’s much more easily understood by doing it. To help with this, we’ll explain and visualize the process separately.
[Tomas Reimers](https://substack.com/redirect/5845263e-7f60-454d-bb4c-285acdc1ab7e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) worked for 2.5 years at Meta, before cofounding Graphite three years ago. Here’s how he explains stacking:
‘Stacking lets you make many small PRs easily, and without having to wait for review. Traditional git workflows equate every feature with its own PR. A PR has its own branch, and is made up of several commits. The traditional, non-stacking workflow is this:
Finish a feature
Submit a PR
Await PR approval
Merge back into main once approved
‘Once the PR is merged, you want to start work on the next feature. So you branch off of main again and begin building. Even at its most seamless, this process takes a long time! The biggest time waster is that PRs sit waiting for review for hours or days. We analyzed historical data for 15 million pull requests and PRs exist which waited several years to be merged!
‘Stacking makes the unit of change an individual commit, rather than a pull request composed of several commits. With stacking, you break up larger changes into many smaller ones. This change – a commit! – can be tested, reviewed, landed, and reverted individually.
‘These collections of smaller changes, or “stacks,” can be built continuously, one on top of the other, allowing engineers to stay unblocked and to keep moving. To give a practical example, it’s pretty common that once you build a feature, you want to build the next feature using the completed one. With stacking, you don’t have to wait for the first feature to be approved and merged; you just keep working!
‘Stacking as a methodology empowers developers to bypass the delays of main branch dependency and permits continuous parallel development.’
For stacking, a visual explanation is also helpful, and here’s my attempt at one. The traditional pull request flow works as follows:
Productive engineers tend to make small-enough pull requests, which are atomic enough and easy to review. How does an engineer go about creating a series of small PRs? There are two choices:
Create a PR, then wait for this PR to be reviewed, and then create the next PR. This is time consuming!
Create PR, then, while waiting for this PR to be reviewed, start a new branch with a second new PR, to keep working.
The most common approach for productive engineers is #2. Sure, it involves a little more context switching, but it beats waiting and doing nothing, right? So a typical flow when working on several pull requests is:
But this “traditional” pull request flow doesn’t work well when PRs depend on one another. So long as PRs are completely independent, the classic flow works well enough, and you just switch between different branches, locally.
But you are blocked if you want to make changes in PR_2 that depend on changes in PR_1 being in the main branch. Then there’s no choice but to await PR_1 approval and ping reviewers, asking them to speed up the review.
In practice, what devs usually do is add more commits to PR_1, which turns it into a giant code change. This isn’t ideal, but there’s no choice because there’s no good way to “split” a PR into several independent parts. This is where stacked diffs come in.
The idea behind stacked diffs is that you can keep working on your main branch, and worry about reviews later. You check out the main branch and start working on it, make a small change, and commit this as a diff – a very small pull request. You then continue working, creating a second diff, and a third, and so on.
You still need reviews to merge these diffs but these can wait until later. So now, your workflow changes to this:
It might feel like a small change to keep working on your current branch without waiting on reviews. But this adds up to a massive productivity boost when working with small diffs and small pull requests. Let’s visualize the difference:
The real benefit of stacked diffs is that they protect your “coding streak” by ensuring it doesn’t break when completing one code change, and moving to the next:
With stacked diffs, every commit (diff) becomes a code review. And this is the main idea behind stacked diffs. Everything else is a tooling matter.
Most developers work on large and complex pieces of work, and because of this complexity, it is not reasonable to ask engineers to limit a pull request to, say, 200 changed lines at most. Sometimes one, complete piece of work can be as many as hundreds – or even thousands! – of lines long.
Diffs – which are basically commits – make it reasonable to ensure all commits are small in size. A large piece of work that changes 1,000 lines of code can be broken into three separate diffs as follows:
Scaffolding (800 lines): the “boring” but verbose stuff. Perhaps this is auto-generated code.
Core business logic (150 lines): key changes made to the code
Edge cases (50 lines): handling of cases which aren’t part of the core code
Suddenly, it’s easier to review this code and spot issues with it. It also helps better organize your work as a dev!
In theory, stacked diffs seem like a pleasant workflow. However, things get a bit more complicated when a change is made on the main branch or in an earlier diff. Let’s take the latter case, when a reviewer requests significant changes to the first diff.
In this example, we have three stacked diffs which all depend on one another:
After we’ve finished the last code change (diff,) the code review for Diff 1 completes. The reviewer found a couple of issues and significant changes are needed to Diff1. So:
Now what? Diff2 and Diff3 cannot be landed to the main branch while they don’t contain changes from the updated Diff 1. This is exactly why we use [Interactive rebasing](https://substack.com/redirect/0dbf9dae-a1c7-4ae8-b988-7f5beb1875f1?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) – basically, rewriting the local git history. We execute the command git rebase -i. If the changes to Diff1 cause conflicts with Diff2, we manually select the changes we want the updated Diff2 to contain. And we do the same with Diff3:
Working with stacked diffs usually means more frequent rebasing of small diffs. When I started to use stacked diffs with Phabricator, at Uber, rebasing became almost a daily habit. This was not just because it was common to get meaningful feedback for an earlier diff in the chain that required major code changes, but because the main branch changed frequently!
Rebasing is not unique to stacked diffs, though: it’s a pain point that happens any time lots of engineers are working in the same part of the codebase. Stacked diffs actually make rebasing a little easier because the conflicts you need to merge tend to be smaller, since the diffs themselves are smaller. The most risky rebase tends to be merging a branch with hundreds or thousands of lines of changed code and dozens of conflicts.
Getting proficient at rebasing is a helpful skill for any software engineer. Working with stacked diffs forces you to master this practice! My only addition is that when using the stacking workflow, dedicated tooling for stacking — such as within [Phabricator](https://substack.com/redirect/ad9b4a9e-06df-4ad7-8b60-3e3374b71436?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) (now unmaintained as an open source project), or [Graphite](https://substack.com/redirect/98f92422-1945-42bb-9fde-3b0d19993173?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), or [Gerrit](https://substack.com/redirect/08fa54f1-f03a-4c1d-98da-605d555f6d8f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) can make rebasing a bit easer than the native git flow.
[Nick Yan](https://substack.com/redirect/7d3dc6db-dbf2-48f0-9e6d-db5b48521203?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) worked at Meta for 4 years, before joining Graphite as an engineer. When he started at Meta – then Facebook – in 2017, he was surprised that the topic of stacked diffs was covered during onboarding, early on:...
Become a paying subscriber of The Pragmatic Engineer to get access to this post and other subscriber-only content.
| Full articles every Tuesday and Thursday | |
| Access to resources for engineering managers and engineers | |
| Access to the complete archive, and to comment on posts |