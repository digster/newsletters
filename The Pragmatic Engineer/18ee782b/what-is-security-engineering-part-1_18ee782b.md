---
subject: "What is Security Engineering? Part 1."
from: "The Pragmatic Engineer <pragmaticengineer@substack.com>"
to: ""
date: 2024-04-16 15:23:30
labels: ["CATEGORY_PERSONAL", "INBOX", "The Pragmatic Engineer", "UNREAD"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_6413324878686416177", "UNREAD"]
---
👋 Hi, this is Gergely with a subscriber-only issue of the Pragmatic Engineer Newsletter. In every issue, I cover challenges at Big Tech and startups through the lens of engineering managers and senior engineers. If you’ve been forwarded this email, you can
|
Q: “As a software engineer, I’d like to learn more about security engineering. What’s a good way to understand this vast field?”
Security is so important in our industry. There’s frequently news stories about security incidents, like the authentication provider Okta which was breached, then responded poorly and [got schooled on “Security 101” practices by its own customer, Cloudflare](https://substack.com/redirect/6b2d4a70-d05c-4ada-80d0-9014e191975a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). The criticism that followed for Okta was inevitable and also deserved, as it essentially sells security. But what about engineers who want to build things securely, where do they start?
I figured there’s no better place to find out than by asking a security engineer, so I reached out to [Nielet D'Mello](https://substack.com/redirect/c3a37d41-c985-4bbd-85bf-83ff200d0870?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). She’s a security engineer at Datadog, whose job is incorporating security into products from the very start of the development process. Nielet has been working in the security domain for nearly a decade, and before that she was at Intel, where she worked closely with the security team, as well as at McAfee, in consumer and enterprise security products. Nielet’s also speaks at security conferences – here’s her 2023 talk [on security design and guidance at scale](https://substack.com/redirect/bb086bdf-769e-40d0-a9ee-121bb007f6f0?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).
In today’s issue, Nielet takes us through:
Myths and misconceptions about security engineering. Common misconceptions, like that security is only security engineers' responsibility, or that security through obscurity is sufficient, and other myths.
History of security engineering. Security engineering’s evolution since the 1990s; especially network and perimeter defense up to today.
The present. A transformation to a proactive approach, and a shift to “decentralized security.”
A mental model. Seven core dimensions for thinking about application security, with a close look at each one.
Towards a Secure SDLC. An approach to make all steps of the software development lifecycle (SDLC,) “security-first.”
In next week’s issue, we round up this topic with tactical advice on how to define a service or system’s criticality, preparing for threat modeling exercises, and an overview of popular security strategies and principles like “defense in depth” and “zero trust.”
As a note, throughout this article we cover application security engineering (aka, “AppSec.”) This is the most common type of security engineering at tech companies building software products. Other specializations within security engineering include cloud security (focusing on cloud infrastructure security,) infrastructure security (securing hardware, operating systems, middleware,) and even physical security (physical access controls and surveillance.) These topics are out of scope for this series.
The bottom of this article could be cut off in some email clients. [Read the full article uninterrupted, online.](https://substack.com/redirect/5aed8d84-fd6b-4858-89d4-8014b4043ee4?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
With that, it’s over to Nielet.
Hi! We use three terms frequently in this article, so let’s start by defining them:
Vulnerability: An exploitable flaw or weakness in a system’s design, implementation or deployment
Threat: The potential for a threat actor to exploit a vulnerability
Risk: Loss or damage that could occur when a threat actualizes
How intertwined are security engineering and software engineering?
When it comes to software engineering, there’s nothing too special about security. Yet, its extensive depth, breadth, and nuance, mean the security domain has long felt intimidating to engineers. But it has existed for as long as software engineering; so, why does security engineering still feel like an “emerging” field?
It’s due to software engineering’s ever-increasing complexity: distributed systems, microservices, cloud computing, Artificial Intelligence (AI,) and more. Security engineering aims to stay ahead in this dynamic, ever-evolving threat landscape, and businesses are starting to prioritize it more.
Some statistics reveal why investing in security is increasingly important:
$4.45M: global average
[cost of a single data breach](https://substack.com/redirect/bd243e4e-0421-44dc-8670-b49c7fe4e789?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)in 2023, a 15% rise over 3 years16% more application security attack surfaces. In 2023 alone, this meant
[29,000 new vulnerabilities](https://substack.com/redirect/d9755dc6-a64f-47d7-90a6-e9cab7549c6d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)were identified, which organizations need to defend against.
A security engineering organization is usually tasked with:
Risk prevention and detection: Aim to defend an organization's assets: its data, applications, code, infrastructure, etc.
Response and recovery: react to threats and remediate attacks.
I’ve observed several common misconceptions, and this article seems like a good place to debunk them.
This is surprisingly common, but not exactly true. Security engineers are stewards of the organization's overall security posture, but realistically, they can never keep up with all developments in the product and platform space – just within their organizations!
Security teams also tend to be lean, meaning there aren’t many engineers. If they focus too much on the weeds; like constantly triaging incidents or security findings, this will take away from high-value work that brings company-wide impact. Examples of high-value work include:
Security design reviews done product-wide
Building and running programs and services for a secure software development lifecycle
Relying solely on a security team to make all security design decisions is a common anti-pattern. Amazon Web Services, in its “AWS Well-Architected” guide, recommends against this practice, and instead [suggests](https://substack.com/redirect/8cab23fb-b2b6-4d18-a75f-52a58b5ea343?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o):
“Build a program or mechanism that empowers builder teams to make security decisions about the software that they create. Your security team still needs to validate these decisions during a review, but embedding security ownership in builder teams allows for faster, more secure workloads to be built. This mechanism also promotes a culture of ownership that positively impacts the operation of the systems you build. (...)
Common anti-patterns:
Leaving all security design decisions to the security team
Not addressing security requirements early enough in the development process.
Not obtaining feedback from builders and security people on the operation of the program.”
[Security through obscurity](https://substack.com/redirect/d3c2ad96-332f-4913-bbbf-7efd6b34e24f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) is the assumption that safeguarding certain details or functions of a system's operations can guarantee security. The principle is, “if only we know how this thing works, then it will be secure enough because others won’t be able to figure it out.”
This approach leads to a false sense of security! It can also lead to exploits. For example:
You have a web application with an admin panel, and this panel has features like managing users, managing content, and configuring the system. The admin panel has URL endpoints like /admin/user-management, /admin/content-management, /admin/system-configuration. How do you make these endpoints secure? The obvious way is to add authentication. However, this is a lot of effort. A simpler idea is to use obfuscation, remapping URLs to something hard to guess:
In this case, the developer relies on the obscurity of the URLs to prevent unauthorized access. However, all it takes is for the URL endpoints information to leak, or an attacker to brute-force the URLs, and the website can be exploited.
It’s tempting to believe, right? Unfortunately, in my experience, it’s simply untrue.
Implementing multiple security measures can enhance the overall security posture of software, but it’s essential to strike a balance between security and usability. For each security measure, carefully consider these things:
Effectiveness
Complexity
Performance impact
Management overhead
Your goal should be that collectively, the security measures provide meaningful protection against threats to the product or platform.
So, your system passed all its security reviews and penetration tests, and you have evidence it is secure. Can you now step away, and assume it will continue to be secure? No!
The threat landscape is constantly changing. Over the past year, there’s been a surge in attacks aimed at businesses and organizations around the world. These attacks intended to damage brands’ reputations, steal sensitive data, seek financial gain, and more. They are often done by ransomware groups, such as BlackCat’s attack on [Change Healthcare](https://substack.com/redirect/88be5ee2-d429-4b8f-b3ae-0a0a68181c27?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) and [Reddit](https://substack.com/redirect/24aba14f-c6ea-4032-9ab9-dbdff49cb57e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), or mass account hacking through [credential-stuffing](https://substack.com/redirect/d2838fee-e5a6-4d8b-af21-b21fc92e9cb7?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).
New vulnerabilities and attack vectors emerge regularly. For example, applications built on top of large language models (LLMs) are now susceptible to prompt injection, which is a class of attack against applications built on top of LLMs. They work by concatenating untrusted user input with a trusted prompt constructed by the application’s developer. So, security mechanisms built against existing injection attacks must factor this in, as security measures that used to be effective become obsolete or insufficient against new and advanced threats, rendering software vulnerable.
Things that can introduce vulnerabilities and weaken your overall security posture:
Accumulation of technical debt
Using deprecated components and libraries
Outdated dependencies
Security vulnerabilities in a dependency, framework, library, or service
[Zero-day exploits](https://substack.com/redirect/81f5ed44-bd38-4bfb-a1c6-4459d60f3014?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)are disclosed vulnerabilities for which no patch is available. These are a special kind of vulnerability, unknown to all consumers of the software. Finding such exploits is very challenging, but organizations with large security teams can do it. For example, Google[discovered](https://substack.com/redirect/c9afa225-a844-42c5-9102-a18032196723?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)93 zero-days in 2023.
Regulatory requirements and industry standards often mandate regular security assessments, audits and updates, to ensure compliance with data protection laws and regulations. Adhering to these requirements may necessitate ongoing security improvements, regardless of the software's initial security status.
Penetration testing, aka pen testing, involves simulating real-world security attacks against a system, network, application, or organization's infrastructure. The main goal is to identify and exploit vulnerabilities in a system's security defenses, mimicking the tactics, techniques, and procedures of attacks. Pen testing allows organizations to understand their security posture and to prioritize remediation efforts accordingly.
Downsides of pen testing:
It’s a snapshot of the security posture at a single, specific moment
Costly and labor-intensive
A system deemed secure by a penetration test one day, may become vulnerable the next day to new exploits or changes in the environment. Plus, scoping plays a huge role in the impact of penetration test results. Scoping refers to applications, users, networks, devices, accounts, and other assets that should be tested to achieve the organization's objectives.
When pen tests are incorrectly scoped, broader security issues or systemic weaknesses may be missed, which attackers can exploit. Scoping pen tests correctly means providing enough information for the pen testing team upfront, so they can be productive. Here’s a summary from Jessica La Bouve, Solutions Architect at penetration testing vendor, BishopFox, on [the importance of scoping](https://substack.com/redirect/ebab4836-7fc5-44aa-87b4-2bed6989d863?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o):
“If a criminal has decided to target you, they have infinite time to find your weaknesses. (...) The assessment team has a finite amount of time to identify critical weaknesses. What they’re able to accomplish in that time depends on the amount of information you give them during scoping. (...)
Keeping your pen tester in the dark only makes it harder for them to find weaknesses that you need to fix. Even if an attacker starts from zero, they have plenty of time to conduct reconnaissance and learn a lot about your organization, giving your pen tester a head start means they can get right down to the business of finding the real threats to your systems. Attackers also don’t have any limitations on what they can try. They don’t usually worry about knocking your systems offline, but a pen tester would. To maximize a pen tester’s limited time and balance out the technical limitations placed on them, provide as much information as you can.”
Security engineering teams tend to be lean by design and also by constraints, like the specialized skill sets needed, and budget limitations. This lean approach applies at whatever the scale of a company.
Security teams are much smaller than product/platform engineering teams, and tend to be “two-pizza teams” of between 5-10 application security engineers. As the security org is small, it focuses on projects and initiatives offering high return on investment in value, risk reduction, and impact terms.
If we look at the evolution of security engineering, there’s been significant shifts over the decades due to technological advancement, changes in threat landscapes, and systems’ increasing interconnectedness. Below are some examples.
The widespread adoption of the internet led to the development of various secure protocols (SSL, HTTPS,) and measures like firewalls and antivirus software to protect networks and data. The primary focus of security activities was network and perimeter defense, largely due to the dominance of client server architectures.
Web applications gained popularity and security engineering shifted focus towards securing web applications and the network. As web vulnerabilities like [SQL injection](https://substack.com/redirect/11045fb8-9c89-41a2-84a4-485670f98269?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), [cross-site scripting](https://substack.com/redirect/7204cc48-bcff-4225-8f41-1d753628d11a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) and [buffer overflows](https://substack.com/redirect/9210010a-3aef-4d90-bffe-31cd06b2f5e9?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) became common, so did awareness of and focus on secure coding practices.
Around the same time, compliance and regulatory frameworks like [SOX](https://substack.com/redirect/c7b84c4e-3c82-4959-a24d-d2dd63a893ce?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), [HIPAA](https://substack.com/redirect/8e005c11-19ba-457c-a86b-5355d2fcfe7e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), and [PCI DSS ](https://substack.com/redirect/c55b72bb-261f-4a4f-b704-ca92ce93cbfd?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)came into effect, and led organizations to boost efforts to comply with security requirements and guidelines.
Cloud computing created new security challenges, like data privacy, data encryption, secure authentication, access control, and secure infrastructure configurations. The vulnerability landscape evolved in tandem with rapid technological shifts, and security shifted to efforts to automate security testing and remediation.
The rise of containerization and microservices architecture, the emerging field of AI and machine learning, and a shift to zero-trust architectures. This means security engineering must deal with increased complexity and more attack vectors.
Become a paying subscriber of The Pragmatic Engineer to get access to this post and other subscriber-only content.
| Full articles every Tuesday and Thursday | |
| Access to resources and templates for engineering managers and engineers | |
| Access to the complete archive, see all comments and comment on articles |