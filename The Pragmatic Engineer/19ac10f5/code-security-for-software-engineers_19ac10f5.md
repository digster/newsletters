---
subject: "Code security for software engineers"
from: "The Pragmatic Engineer <pragmaticengineer@substack.com>"
to: ""
date: 2025-11-26 16:45:55
labels: ["CATEGORY_PERSONAL", "INBOX", "The Pragmatic Engineer", "UNREAD"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_6413324878686416177", "UNREAD"]
---
Hi – this is Gergely with the monthly, free issue of the Pragmatic Engineer Newsletter. In every issue, I cover challenges at Big Tech and startups through the lens of senior engineers and engineering leaders. If you’ve been forwarded this email, you can Black Friday is coming up this week — and The Pragmatic Engineer is
|
Listen and watch now on [YouTube](https://substack.com/redirect/2cece7f6-d1b6-4061-8fcc-a95032452e6b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), [Spotify](https://substack.com/redirect/a5635842-eefb-4e0c-8930-265ffe6d2285?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), and [Apple](https://substack.com/redirect/677e8638-3330-4d9b-908f-3d9f82742b8b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). See the episode transcript at the top of this page, and timestamps for the episode at the bottom.
• [Statsig](https://substack.com/redirect/87d7fb12-23dc-4246-b048-31572b20fac4?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) — The unified platform for flags, analytics, experiments, and more. Statsig are helping make the first-ever Pragmatic Summit a reality. Join me and 400 other top engineers and leaders on 11 February, in San Francisco for a special one-day event. [Reserve your spot here.](https://substack.com/redirect/4f6ca9dd-8c97-4974-8fe3-a555ca05e2f4?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• [Linear](https://substack.com/redirect/9a7db1ec-c50b-45b9-a1da-48e61071fa4d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) — The system for modern product development. Engineering teams today move much faster, thanks to AI. Because of this, coordination increasingly becomes a problem. This is where Linear helps fast-moving teams stay focused. [Check out Linear.](https://substack.com/redirect/9a7db1ec-c50b-45b9-a1da-48e61071fa4d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
—
As software engineers, what should we know about writing secure code?
[Johannes Dahse](https://substack.com/redirect/a73b1b99-058e-4fe4-923f-124f6c731ed3?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) is the VP of Code Security at Sonar and a security expert with 20 years of industry experience. In today’s episode of The Pragmatic Engineer, he joins me to talk about what security teams actually do, what developers should own, and where real-world risk enters modern codebases.
We cover dependency risk, software composition analysis, CVEs, dynamic testing, and how everyday development practices affect security outcomes. Johannes also explains where AI meaningfully helps, where it introduces new failure modes, and why understanding the code you write and ship remains the most reliable defense.
If you build and ship software, this episode is a practical guide to thinking about code security under real-world engineering constraints.
How code quality and code security are connected:
Gergely: “How does the quality of code relate to security?”
Johannes: “This is an underrated topic in the industry today. We talked about the null pointer exceptions or these slow regular expressions, right? That can lead to security issues. That’s more of the obvious examples of bugs.
Think about unreadable code, not well-maintained code: that’s often like spaghetti code. At first, it’s not so obvious how this is connected to security.
If you think about how code is not easy to comprehend, not easy to review. Then you do pair programming or code reviews in your development team — then in that spaghetti code, you will more likely overlook security problems of your colleague.
Now, maybe someone found an issue or and issue and reports it back to you. As a developer, you have to fix it. But if it’s not maintainable code, you cannot fix the security problem easily. So quality suddenly becomes a security issue in how the attacker window stays open longer!
Your code quality is super related to code security, especially now with AI-generated code. We typically see poor quality of code here. And that becomes a problem for security.”
How AI is introducing new security issues:
Gergely: “How do you think AI is changing code security?”
Johannes: “We see a change in how code and applications are built. Traditionally, you had this backend/frontend split. In the backend, you had a database. Remove that database, then you don’t have a SQL injection risk anymore.
As soon as you add an LLM to the backend, you have to deal with prompt injection vulnerabilities. The attacker can modify the system prompt or manage do some prompt engineering and then mess with the LLM’s logic or the output. It’s taking time both for the attackers to adjust to this, and the industry to adjust in defending against it.”
Gergely: “What about with coding assistance? Are you seeing things change in terms of how we think about code security?”
Johannes: “The big problem [with AI coding assistance] in terms of security is that you produce code much more faster. Writing code is not the challenge anymore. Suddenly, the new bottleneck is how are you verifying all that code, right? And if you don’t verify it:that leads to security issues or quality issues. Quality issues, on the long run, lead to security problems.”
On software composition analysis:
Gergely: “What is
[software composition analysis](SCA)?”Johannes: “It’s a technique where we look at manifest files and your list of dependencies, depending on the package manager you use. This list of dependencies is checked against a database of known security problems. Those are called the
[CVEs]. Then you can - with software composition - map, for example, that this specific Log4j version of your library is vulnerable to the Log4 shell vulnerability that is known. And then it can warn you.”
([00:00](https://substack.com/redirect/e74c8ba6-0cbf-43bf-aed5-55f6c48ecae2?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Intro
([02:31](https://substack.com/redirect/e9e30059-f613-4d88-9bba-4920659a57fe?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) What is penetration testing?
([06:23](https://substack.com/redirect/0e444cf8-30cd-4a16-93ce-85846c1b6e86?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Who owns code security: devs or security teams?
([14:42](https://substack.com/redirect/6fde783d-a0cd-45cc-9feb-1f0dd53532b8?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) What is code security?
([17:10](https://substack.com/redirect/298e28e9-04ab-4b56-9d3d-0d0cbc407f45?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Code security basics for devs
([21:35](https://substack.com/redirect/b0c43816-3ea4-4650-a0c0-6178809b36cc?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Advanced security challenges
([24:36](https://substack.com/redirect/112aac3a-a23e-45cb-a0d4-b55a6107713f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) SCA testing
([25:26](https://substack.com/redirect/8ef71154-3e0c-42a2-94a6-b776308bc25d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The CVE Program
([29:39](https://substack.com/redirect/fbfc1b13-59a8-489d-866f-e84a45b0c988?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The State of Code Security report
([32:02](https://substack.com/redirect/6d93c3ce-15e8-4dd4-9598-741052063794?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Code quality vs security
([35:20](https://substack.com/redirect/026508d9-6b75-4c9a-8dbb-6d9f565725ee?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Dev machines as a security vulnerability
([37:29](https://substack.com/redirect/dc3d1c7d-75d0-4bca-b457-fba1511615eb?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Common security tools
([42:50](https://substack.com/redirect/a74bbc25-2d52-4a51-aed3-d5e9ddcfc74b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Dynamic security tools
([45:01](https://substack.com/redirect/f4305e8c-1dc2-4c51-9918-89fb27dea53e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) AI security reviews: what are the limits?
([47:51](https://substack.com/redirect/0bf83c2c-e5d1-44f6-bffc-a5e1b01fe06d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) AI-generated code risks
([49:21](https://substack.com/redirect/e7200b30-afc5-41ee-8888-326d61d6ae6e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) More code: more vulnerabilities
([51:44](https://substack.com/redirect/2d9609ec-d574-4b8b-a0af-076518c1f16f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) AI’s impact on code security
([58:32](https://substack.com/redirect/83af7115-9c88-433c-b1b4-6cc7751b35ba?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Common misconceptions of the security industry
([1:03:05](https://substack.com/redirect/580f89e7-303f-407f-a849-234d30778a5f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) When is security “good enough?”
([1:05:40](https://substack.com/redirect/24ff1f58-4352-4432-b13a-572a741b71c8?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Johannes’s favorite programming language
Where to find Johannes Dahse:
• LinkedIn: [https://www.linkedin.com/in/johannes-dahse-112b3057](https://substack.com/redirect/a73b1b99-058e-4fe4-923f-124f6c731ed3?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
Mentions during the episode:
• Sonar: [https://www.sonarsource.com](https://substack.com/redirect/45a968b2-0ea6-468e-b94d-ff6a87f03b02?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• State of Code Security Report by Sonar [https://www.sonarsource.com/resources/the-state-of-code-security-report/](https://substack.com/redirect/6cecb79b-469a-4940-a712-115c8c02c807?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• OWASP Top Ten: [https://owasp.org/www-project-top-ten](https://substack.com/redirect/4aeafaa7-5aa9-43a3-a1d2-e438d808da91?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Software Composition Analysis: [https://en.wikipedia.org/wiki/Software_composition_analysis](https://substack.com/redirect/42e00836-5b5c-42de-af89-a818e0108f9e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• CVE Program: [https://www.cve.org](https://substack.com/redirect/6efabc56-fa96-4666-99eb-ca1b44eaf16e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• SAST: [https://en.wikipedia.org/wiki/Static_application_security_testing](https://substack.com/redirect/642c9fbe-17a3-4d97-9af1-2d3bc4978763?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• What is DAST: [https://github.com/resources/articles/what-is-dast](https://substack.com/redirect/3ba2b69a-a4e3-47b8-ba27-674e9037eb0e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Stack Overflow AI survey: [https://survey.stackoverflow.co/2025/ai](https://substack.com/redirect/13fb2e8b-eee5-42b4-9bcc-743e29a13246?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Go: [https://go.dev](https://substack.com/redirect/f1f6d6c8-e041-40c0-9f0e-f62147ee5fed?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Java: [https://www.java.com](https://substack.com/redirect/1fe8ee8a-18df-4792-a5fb-925d21305307?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
—
Production and marketing by [Pen Name](https://substack.com/redirect/b2c22ce2-bbbf-4f24-903c-00519d75847d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).
You’re on the free list for [The Pragmatic Engineer](https://substack.com/redirect/2/eyJlIjoiaHR0cHM6Ly9uZXdzbGV0dGVyLnByYWdtYXRpY2VuZ2luZWVyLmNvbT91dG1fY2FtcGFpZ249ZW1haWwtaG9tZSZyPThvNTRuIiwicCI6MTc5ODM3MzA4LCJzIjo0NTg3MDksImYiOnRydWUsInUiOjE0NTYzMzE5LCJpYXQiOjE3NjQxNzU1OTcsImV4cCI6MjA3OTc1MTU5NywiaXNzIjoicHViLTAiLCJzdWIiOiJsaW5rLXJlZGlyZWN0In0.sdk0tLoFAmi_RWjxUQP6_wOmkMDaTxlBQVhyTT2Zadw?). For the full experience, [become a paying subscriber](https://substack.com/redirect/2/eyJlIjoiaHR0cHM6Ly9uZXdzbGV0dGVyLnByYWdtYXRpY2VuZ2luZWVyLmNvbS9zdWJzY3JpYmU_dXRtX3NvdXJjZT1wb3N0JnV0bV9jYW1wYWlnbj1lbWFpbC1jaGVja291dCZuZXh0PWh0dHBzJTNBJTJGJTJGbmV3c2xldHRlci5wcmFnbWF0aWNlbmdpbmVlci5jb20lMkZwJTJGY29kZS1zZWN1cml0eSZyPThvNTRuJnRva2VuPWV5SjFjMlZ5WDJsa0lqb3hORFUyTXpNeE9Td2lhV0YwSWpveE56WTBNVGMxTlRrM0xDSmxlSEFpT2pFM05qWTNOamMxT1Rjc0ltbHpjeUk2SW5CMVlpMDBOVGczTURraUxDSnpkV0lpT2lKamFHVmphMjkxZENKOS5ubnhFbUVESjJzbFlPdkQxUVJjTlpNWEgyOUVleEtyTDg3T0pyYmhyM3pnIiwicCI6MTc5ODM3MzA4LCJzIjo0NTg3MDksImYiOnRydWUsInUiOjE0NTYzMzE5LCJpYXQiOjE3NjQxNzU1OTcsImV4cCI6MjA3OTc1MTU5NywiaXNzIjoicHViLTAiLCJzdWIiOiJsaW5rLXJlZGlyZWN0In0.LlIplnEiL0afym72BGw9H2nqpF_juz2lOWPKHLdEr7s?). Many readers expense this newsletter within their company’s training/learning/development budget. If you have such a budget, here’s[ an email you could send to your manager](https://substack.com/redirect/f61faf2e-0797-437a-9f00-4ef208b45ac2?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).
This post is public, so feel free to share and forward it.
If you enjoyed this post, you might enjoy my book, [The Software Engineer's Guidebook](https://substack.com/redirect/0955a8d6-a67c-4e35-bffd-96a5f7996f35?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). Here is what Tanya Reilly, senior principal engineer and author of The Staff Engineer's Path said about it:
"From performance reviews to P95 latency, from team dynamics to testing, Gergely demystifies all aspects of a software career. This book is well named: it really does feel like the missing guidebook for the whole industry."