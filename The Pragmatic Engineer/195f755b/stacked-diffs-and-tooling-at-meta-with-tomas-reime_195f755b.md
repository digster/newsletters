---
subject: "Stacked diffs and tooling at Meta with Tomas Reimers"
from: "The Pragmatic Engineer <pragmaticengineer@substack.com>"
to: ""
date: 2025-04-02 16:27:07
labels: ["CATEGORY_PERSONAL", "INBOX", "The Pragmatic Engineer", "UNREAD"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_6413324878686416177", "UNREAD"]
---
|
Listen and watch now on [YouTube](https://substack.com/redirect/9ef3724e-275a-43ca-b174-16920fc71a64?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), [Spotify](https://substack.com/redirect/64cb83cb-e61e-4389-b4d2-47857f0919dc?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), and [Apple](https://substack.com/redirect/2921dcf7-7cf4-4158-ae78-203a8393d72e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). See the episode transcript at the top of this page, and a summary at the bottom.
• [Swarmia](https://substack.com/redirect/2a4f3db2-851c-4050-a361-e37cbdd70ca7?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) — The engineering intelligence platform for modern software organizations.
• [Sentry](https://substack.com/redirect/94b125bc-543f-439a-8bc6-cdf645d1fe77?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) — Error and performance monitoring for developers.
—
Why did Meta build its own internal developer tooling instead of using industry-standard solutions like GitHub? [Tomas Reimers](https://substack.com/redirect/720de521-f29d-4cf2-b1d5-ba2d21d1f947?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), former Meta engineer and co-founder of [Graphite](https://substack.com/redirect/25cdd5f2-0bc8-4392-b9cc-7f883b9e870e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), joins the show to talk about Meta's custom developer tools – many of which were years ahead of the industry.
From Phababricator to Sandcastle and Butterflybot, Tomas shares examples of Meta’s internal tools that transformed developer productivity at the tech giant. Why did working with stacked diffs and using monorepos become best practices at Meta? How are these practices influencing the broader industry? Why are code reviews and testing looking to become even more critical as AI transforms how we write software? We answer these, and also discuss:
• Meta's custom internal developer tools
• Why more tech companies are transitioning from polyrepos to monorepos
• A case for different engineering constraints within the same organization
• How stacked diffs solve the code review bottleneck
• Graphite’s origin story and pivot to their current product
• Why code reviews will become a lot more important, the more we use AI coding tools
• Tomas’s favorite engineering metric
• And much more!
My biggest takeaways from this conversation:
“Stacked diffs” makes a lot of sense inside companies. However, it makes less sense when working on, e.g., open source projects. Perhaps this is a reason that GitHub has not added support for this workflow — even though it’s popular inside companies like Meta or Uber. We previously did a deepdive on [Stacked Diffs (and why you should know about them)](https://substack.com/redirect/7bfd1b5e-102a-4e18-b51c-532839b66791?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).
The “trust matrix:” this is a good way to decide how much process/tooling to put in place in a team. If you trust people a lot and are willing to tolerate mistakes, you should lean on culture and not process. If you start to become a team or company where you need to trust people less: this is the time to move more tooling and more process. So, as a small startup you probably don’t need that much tooling and process!
There could be an industry-wide movement to monorepos: at mid-sized and larger scaleups and tech companies. Tomas sees a lot of scaleups they work with the move from polyrepos (several repositories) to monorepos. Moving to a monorepo is still a lot of work and requires custom tooling: and this is why it was limited to the largest tech companies in the past. Interesting to hear about this change!
AI coding tools increase the importance of quality code reviews. We’ll see more code churned out by AI: but an engineer needs to review it before it goes out. It’s a good question how we can stick to thorough code reviews when it is so tempting to just say, “Looks good to me (LGTM)” and have the seemingly correct code merged.
• [Stacked Diffs (and why you should know about them)](https://substack.com/redirect/7bfd1b5e-102a-4e18-b51c-532839b66791?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• [Inside Meta’s engineering culture](https://substack.com/redirect/98df17e6-0d4c-4e72-8985-e687a8d67c5a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• [How Uber is measuring engineering productivity](https://substack.com/redirect/afab655b-3b82-4681-b2e4-02b7a1274834?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
([00:00](https://substack.com/redirect/c78f07f2-c3a5-497c-b9bc-6f5fe5f099ed?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Intro
([02:00](https://substack.com/redirect/7b339c02-e277-4edc-987b-77cee3c9b04a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) An introduction to Meta’s in-house tooling
([05:07](https://substack.com/redirect/ec996f3d-07b8-4ebc-bbd6-cc8f639df0e3?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) How Meta’s integrated tools work and who built the tools
([10:20](https://substack.com/redirect/aaf3e46e-c6af-455c-9002-5d0222785b71?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) An overview of the rules engine, Herald
([12:20](https://substack.com/redirect/df0084b1-8499-41d0-8c7d-d674299a4bee?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The stages of code ownership at Facebook and code ownership at Google and GitHub
([14:39](https://substack.com/redirect/a83ce2f5-e7be-488a-a19c-cfd6f31eb553?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Tomas’s approach to code ownership
([16:15](https://substack.com/redirect/aab5408b-e4e7-485a-a939-221d653097d6?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) A case for different constraints within different parts of an organization
([18:42](https://substack.com/redirect/463003f8-2e67-4c3e-bf98-c4d481c973ea?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The problem that stacked diffs solve for
([25:01](https://substack.com/redirect/0d5bba6c-e37f-471c-af05-22772f9f2168?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) How larger companies drive innovation, and who stacking diffs not for
([30:25](https://substack.com/redirect/70fecebd-9598-4eca-a6aa-886fc7e32849?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Monorepos vs. polyrepos and why Facebook is transitioning to a monorepo
([35:31](https://substack.com/redirect/0106bc31-188f-4bb9-a4ac-fc01e110c034?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The advantages of monorepos and why GitHub does not support them
([39:55](https://substack.com/redirect/59928b3a-f77f-4e64-a509-fadf4a1465fd?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) AI’s impact on software development
([42:15](https://substack.com/redirect/4054ac41-9d38-41ac-8121-1edaac2d77ad?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The problems that AI creates, and possible solutions
([45:25](https://substack.com/redirect/13e2cc6c-ffd4-4f31-9716-06899a4fed3b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) How testing might change and the testing AI coding tools are already capable of
([48:15](https://substack.com/redirect/ea8286a8-fe4a-4e0f-94cd-bae61f1a66a4?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) How developer accountability might be a way to solve bugs and bad AI code
([53:20](https://substack.com/redirect/086bdc74-fb88-4d66-9763-34429a76e333?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Why stacking hasn’t caught on and Graphite’s work
([57:10](https://substack.com/redirect/58c1d639-a11f-4004-9cb6-e6cfd9881597?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Graphite’s origin story
([1:01:20](https://substack.com/redirect/2dd915ed-eda7-454e-bc0b-821744161fb0?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Engineering metrics that matter
([1:06:07](https://substack.com/redirect/adb460be-4a6a-44b7-bf39-8108ed602d57?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Learnings from building a company for developers
([1:08:41](https://substack.com/redirect/b3f397cc-3013-4fce-b8c4-ea36b7fd564a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Rapid fire round
([1:12:41](https://substack.com/redirect/b383901f-60dc-4ee4-bf35-497a76576d81?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Closing
Meta developed Phabricator as its internal tool for code review.
Sandcastle: Meta's internal continuous integration (CI) system, integrating with Phabricator.
OnDemand: internal development environments (dev boxes), linked with Sandcastle.
Landcastle: the tool for deploying code to users, integrated with the preceding systems.
These tools aimed for seamless integration across the entire developer workflow, extending to task management.
Herald, later replaced by Butterflybot: a rules engine that automated actions during code review based on specific events, such as flagging use of deprecated APIs.
We cover more internal tools in the deepdive
[Inside Meta’s Engineering Culture](https://substack.com/redirect/d84b905e-08bc-4347-9623-c3ec1f7d7cbb?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
Meta used a method called stacking for code changes, where developers create a series of dependent changes (think of it as small PRs depending one on another)
This involves building multiple, sequential branches, each representing a smaller part of a larger feature.
The goal: minimize developer wait times associated with lengthy code reviews by submitting smaller units.
Reviewing smaller pull requests is generally faster and more effective.
Meta created internal tools to manage the Git operations, such as rebasing, necessary for maintaining stacked branches.
Meta adopted a monorepo strategy, housing most of its codebase in a single repository.
This approach aimed to simplify collaboration and management of dependencies between different parts of the system.
Initially having multiple large repositories, Meta moved towards consolidating them for greater efficiency.
Tomas observes a trend of more companies adopting monorepos.
Tomas expects the use of AI tools to increase the speed and volume of code generation by developers.
This increase in code will place greater emphasis on the processes of code review and software testing to ensure quality.
AI has the potential to automate certain aspects of the code review process, allowing human reviewers to concentrate on more complex design and integration issues.
AI may also play a role in generating software tests, potentially increasing test coverage.
Still: human understanding and review of code will remain essential for verifying the intended functionality and business logic.
Commonly tracked metrics include the number of pull requests created and the time taken for them to be merged.
Uber implemented a metric measuring the time a pull request spent waiting for review without any action. This aimed to address delays in the review process, particularly in distributed teams.
While measuring developer focus time is challenging, it is recognized as an important factor in productivity.
Where to find Tomas Reimers:
• X: [https://x.com/tomasreimers](https://substack.com/redirect/38d2af37-5f28-4eb0-bd1e-3fd8a81cfe77?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• LinkedIn: [https://www.linkedin.com/in/tomasreimers/](https://substack.com/redirect/720de521-f29d-4cf2-b1d5-ba2d21d1f947?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Website: [https://tomasreimers.com/](https://substack.com/redirect/4b55fcb8-b805-47fd-b3de-38c4401cb2bf?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
Mentions during the episode:
• Graphite: [https://graphite.dev/](https://substack.com/redirect/25cdd5f2-0bc8-4392-b9cc-7f883b9e870e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• GitHub: [https://github.com/](https://substack.com/redirect/953be717-3bde-4166-9cc6-c5996c66d91a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Stacked Diffs (and why you should know about them): [https://newsletter.pragmaticengineer.com/p/stacked-diffs](https://substack.com/redirect/7bfd1b5e-102a-4e18-b51c-532839b66791?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Meta developer tools: Working at scale: [https://engineering.fb.com/2023/06/27/developer-tools/meta-developer-tools-open-source/](https://substack.com/redirect/e25d7518-9dca-49e4-960f-2fec0eb9c677?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• A Meta developer's workflow: Exploring the tools used to code at scale: [https://developers.facebook.com/blog/post/2022/11/15/meta-developers-workflow-exploring-tools-used-to-code/](https://substack.com/redirect/a8540934-dace-4a46-9ef3-dec34bd56365?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• GitHub Actions: [https://github.com/features/actions](https://substack.com/redirect/6f4d5490-ef68-4dbb-92ca-a308da83b30d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Buildkite: [https://buildkite.com/](https://substack.com/redirect/b60d559c-d5e3-4628-a95c-7989cfb4daa3?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Jira: [https://www.atlassian.com/software/jira](https://substack.com/redirect/0c6d9c6a-03f2-4d00-a98c-c2c68305ba33?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Linear: [https://linear.app/](https://substack.com/redirect/4dd1534b-81bc-4fb6-9f62-945fa3097491?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Phabricator: [https://graphite.dev/guides/phabricator-source-code-management-tool](https://substack.com/redirect/8b40d3f0-6924-40ed-8306-989fe0698923?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Supercharging A/B Testing at Uber: [https://www.uber.com/blog/supercharging-a-b-testing-at-uber/](https://substack.com/redirect/32c7c6d8-e4da-4663-be18-515646d443d2?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Dropbox uses Phabricator extensively for all our projects: [https://news.ycombinator.com/item?id=8656701](https://substack.com/redirect/cc9e6ff6-3d44-4683-88fd-6331c8941b3d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Herald User Guide: [https://secure.phabricator.com/book/phabricator/article/herald/](https://substack.com/redirect/d68c6bfd-52ea-42eb-b65f-549dc1f5a871?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• GitHub code owners: [https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners](https://substack.com/redirect/e6f4f689-d568-4cbc-84c0-b3f7d490cfd7?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Stacked Pull Requests: [https://www.gitkraken.com/gitkon/stacked-pull-requests-tomas-reimers](https://substack.com/redirect/6da81bb7-db3c-4a9a-a2c2-3cbab190f899?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Mercurial: [https://www.mercurial-scm.org/](https://substack.com/redirect/ad1f5a3d-b091-4fd1-8154-1a6ff1e6d6bc?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Developer productivity with Dr. Nicole Forsgren (creator of DORA, co-creator of SPACE): [https://newsletter.pragmaticengineer.com/p/developer-productivity-with-dr-nicole](https://substack.com/redirect/738cd8f0-885a-42b2-b30e-b45cdb925bd3?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• How Linux is built with Greg Kroah-Hartman: [https://newsletter.pragmaticengineer.com/p/how-linux-is-built-with-greg-kroah](https://substack.com/redirect/ca1c5c40-478c-4a16-8b53-acafb7c90d1c?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Inside Meta's Engineering Culture: Part 1: [https://newsletter.pragmaticengineer.com/p/facebook](https://substack.com/redirect/98df17e6-0d4c-4e72-8985-e687a8d67c5a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Inside Meta's Engineering Culture: Part 2: [https://newsletter.pragmaticengineer.com/p/facebook-2](https://substack.com/redirect/d84b905e-08bc-4347-9623-c3ec1f7d7cbb?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Shopify: [https://www.shopify.com/](https://substack.com/redirect/83ffc711-f141-4d6d-8b4d-d89b807243f4?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• React: [https://react.dev/](https://substack.com/redirect/c9935e5c-90fa-43a8-8b11-559e90396e62?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Vercel: [https://vercel.com/](https://substack.com/redirect/06b7af71-86b4-44e3-bff5-8aafc44748cc?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Andrej Karpathy’s post on X about vibe coding: [https://x.com/karpathy/status/1886192184808149383](https://substack.com/redirect/eb15ccee-3337-47ee-aedb-862f96fd9b50?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Grammarly: [https://www.grammarly.com/](https://substack.com/redirect/67dec16f-ac43-4a59-8946-41b1eb41d8f4?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Heroku: [https://www.heroku.com/](https://substack.com/redirect/e256c604-936d-472e-a5d5-4df05623776b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Pull requests at GitHub: [https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests](https://substack.com/redirect/06037a44-2ab6-4d0d-ac55-75f53c651411?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• How Uber is Measuring Engineering Productivity: [https://newsletter.pragmaticengineer.com/p/uber-eng-productivity](https://substack.com/redirect/afab655b-3b82-4681-b2e4-02b7a1274834?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Statsig: [https://statsig.com/](https://substack.com/redirect/4e0d0003-83ad-4e13-8a1f-64e17b41968f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Typescript: [https://www.typescriptlang.org/](https://substack.com/redirect/11be2037-e9ec-42b0-83dc-b9cce0d4d43e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Ruby: [https://www.ruby-lang.org](https://substack.com/redirect/d7dbdfd2-8113-4f89-acaf-fb846819d051?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Python: [https://www.python.org/](https://substack.com/redirect/01eb4504-84f5-471c-b759-9e7df40ff68c?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• The Last Days of Night: [https://www.amazon.com/Last-Days-Night-Novel/dp/0812988922](https://substack.com/redirect/b17c4850-9de1-45c6-ba20-e27528eab1f8?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• The Timeless Way of Building: [https://www.amazon.com/Timeless-Way-Building-Christopher-Alexander/dp/0195024028/](https://substack.com/redirect/f6b3e9b5-f2a5-46c4-ab54-c4c7cfae2fd1?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
—
Production and marketing by [Pen Name](https://substack.com/redirect/516edd09-e540-4955-a4a0-f4adebef3b9c?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). For inquiries about sponsoring the podcast, email podcast@pragmaticengineer.com.
You’re on the free list for [The Pragmatic Engineer](https://substack.com/redirect/2/eyJlIjoiaHR0cHM6Ly9uZXdzbGV0dGVyLnByYWdtYXRpY2VuZ2luZWVyLmNvbT91dG1fY2FtcGFpZ249ZW1haWwtaG9tZSZyPThvNTRuIiwicCI6MTYwMjc4OTk5LCJzIjo0NTg3MDksImYiOnRydWUsInUiOjE0NTYzMzE5LCJpYXQiOjE3NDM2MTEzNDIsImV4cCI6MTc0NjIwMzM0MiwiaXNzIjoicHViLTAiLCJzdWIiOiJsaW5rLXJlZGlyZWN0In0.qnHhgGiANoT3ykcMBnaKq5A5rVwJwwsXNeCsxRFiIm4?). For the full experience, [become a paying subscriber](https://substack.com/redirect/2/eyJlIjoiaHR0cHM6Ly9uZXdzbGV0dGVyLnByYWdtYXRpY2VuZ2luZWVyLmNvbS9zdWJzY3JpYmU_dXRtX3NvdXJjZT1wb3N0JnV0bV9jYW1wYWlnbj1lbWFpbC1jaGVja291dCZuZXh0PWh0dHBzJTNBJTJGJTJGbmV3c2xldHRlci5wcmFnbWF0aWNlbmdpbmVlci5jb20lMkZwJTJGc3RhY2tlZC1kaWZmcy1hbmQtdG9vbGluZy1hdC1tZXRhJnI9OG81NG4mdG9rZW49ZXlKMWMyVnlYMmxrSWpveE5EVTJNek14T1N3aWFXRjBJam94TnpRek5qRXhNelF5TENKbGVIQWlPakUzTkRZeU1ETXpORElzSW1semN5STZJbkIxWWkwME5UZzNNRGtpTENKemRXSWlPaUpqYUdWamEyOTFkQ0o5LjlEQmh0WW52UU9kUVR3OFAtUTM2eFZUdjU5WVZOQzE1bTBsMzBoSDBIdTAiLCJwIjoxNjAyNzg5OTksInMiOjQ1ODcwOSwiZiI6dHJ1ZSwidSI6MTQ1NjMzMTksImlhdCI6MTc0MzYxMTM0MiwiZXhwIjoxNzQ2MjAzMzQyLCJpc3MiOiJwdWItMCIsInN1YiI6ImxpbmstcmVkaXJlY3QifQ.exsCBpEqiIXxizYEwvht07NpUk4ibc6DjCP6rT4RvbY?). Many readers expense this newsletter within their company’s training/learning/development budget.
This post is public, so feel free to share and forward it.
If you enjoyed this post, you might enjoy my book, [The Software Engineer's Guidebook](https://substack.com/redirect/e8ded478-2df1-4948-aa3d-2b8c5eedae9d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). Here is what Tanya Reilly, senior principal engineer and author of The Staff Engineer's Path said about it:
"From performance reviews to P95 latency, from team dynamics to testing, Gergely demystifies all aspects of a software career. This book is well named: it really does feel like the missing guidebook for the whole industry."