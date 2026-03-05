---
subject: "What is Security Engineering? Part 2."
from: "The Pragmatic Engineer <pragmaticengineer@substack.com>"
to: ""
date: 2024-04-30 16:10:39
labels: ["CATEGORY_PERSONAL", "IMPORTANT", "INBOX", "The Pragmatic Engineer", "UNREAD"]
label_ids: ["CATEGORY_PERSONAL", "IMPORTANT", "INBOX", "Label_6413324878686416177", "UNREAD"]
---
👋 Hi, this is Gergely with a subscriber-only issue of the Pragmatic Engineer Newsletter. In every issue, I cover challenges at Big Tech and startups through the lens of engineering managers and senior engineers. If you’ve been forwarded this email, you can
|
Q: “As a software engineer, I’d like to learn more about security engineering. What’s a good way to understand this vast field?”
This is the second and final part of exploring this important – and, yet, often intimidating! – topic of security engineering. Giving us an overview of this field is [Nielet D'Mello](https://substack.com/redirect/f63da55b-8cd2-46a5-893a-37c312816fb8?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o): a security engineer at Datadog (previously at Intel and McAfee).
[In Part 1](https://substack.com/redirect/7fabf3f9-9d22-44ee-9ab3-1fcc364154bc?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) we already covered:
Myths and misconceptions about security engineering
History of security engineering
The present
A mental model: seven core dimensions to think about application security
Towards a secure software development lifecycle (SDLC).
In today’s issue, Nielet takes us through:
Defining the criticality of a system. Security dimensions to consider as we talk about a service or systems’s criticality.
Scoring a system’s criticality. The “napkin math” approach for scoring a system’s security criticality, and a case study to bring all it to life.
Threat modeling. A criteria for threat modeling, and pre-work for this exercise.
Security paved roads. For platform teams, building pre-approved security solutions and configurations is pragmatic.
“Defense in depth,” “least privilege,” and “zero trust.” A strategy, a principle, and a security model. Use in combination to build more layered, secure systems.
The bottom of this article could be cut off in some email clients. [Read the full article uninterrupted, online.](https://substack.com/redirect/ea957005-ead5-48ff-8f6f-7c2c4a764e2d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
With that, it’s over to Nielet.
As a brief refresher, we use three terms frequently in this article, so let’s start by defining them:
Vulnerability: An exploitable flaw or weakness in a system’s design, implementation or deployment
Threat: The potential for a threat actor to exploit the vulnerability
Risk: Loss or damage that could occur when a threat actualizes
Do all services and systems need to invest in a security design review? Not necessarily, as the need for a review depends on a service’s or system’s business risk profile. Vulnerabilities will surface as you identify security concerns in a system’s design and architecture. Code reviews and dynamic testing also surface security issues.
For critical systems, it’s worth investing in processes like security design reviews. However, how do you decide just how critical a service or system is? Use the dimensions below for a better sense of this:
Business purpose
Public access
Custom access controls
Users of the system
Deployment environments
Data classification
What are the primary objectives and functions of the service or system within the context of the organization's business operations? Identify how the service contributes to achieving business goals, generating revenue, or providing stakeholder value. To figure out the risks, it’s essential to know:
The nature of business
The industry the business operates in
Regulatory requirements
Sensitivity of data involved. For example, is it restricted, or subject to PII?
Is the service accessible to external users outside of the organization's network, or the general public? Public access systems offer expanded attack surfaces.
For these, you need to assess the potential exposure to security threats and risks associated with providing services over the internet, or other public networks, as these systems are at a much higher risk of automated bot attacks, for example.
All systems need custom access controls for their data, apps and resources to determine who has access to it and in what circumstances. Role-based access control (RBAC,) or attribute-based access control (ABAC,) are two examples of custom access controls. These have specific access permissions defined for users and identities, and restrictions tailored to the service’s requirements and security needs to ensure confidentiality.
The decision to build custom access controls is usually made with the following factors in mind:
Granularity
Dynamic decisions based on real-time information and conditions
Implementation efforts
Simplicity
Flexibility
What different types of users interact with the service? This is key information for defining:
User roles
Authentication mechanisms
Access requirements
User activity auditing
Threat detections associated with anomalous user behavior patterns
Adherence to regulatory compliance
The last one is especially important. Several regulatory frameworks and industry standards mandate the protection of sensitive data through user identification and access controls. Examples of such frameworks include the General Data Protection Regulation ([GDPR](https://substack.com/redirect/ce93d001-94c8-4fdd-8dbd-ca9e8c61a701?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) and California Consumer Privacy Act ([CCPA](https://substack.com/redirect/b132ae72-da6a-4191-a6a3-e55478cd8f87?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)). In these cases, putting these in place is not “just” about making the system secure; it’s about what ensures the system is compliant with privacy and security regulation.
Users include:
Internal users: employees, administrators
External users: customers, partners, third-party vendors.
Development, testing, staging, and production environments in which the service operates. Each environment may have different security requirements and configurations. These varying requirements depend on:
Level of risk tolerance
Need for data protection
Data availability requirements
Compliance with industry standards, regulations, and legal requirements.
For example, a staging environment may have broader internal employee access, meaning it can be accessed by most (if not all) employees. However, the production environment tends to have much stricter access control: only specific employees or groups can access it, and even fewer will have the rights to deploy to it. And while the staging environment is unlikely to have data that is considered confidential customer data: the production environment will! So the production environment will have much more strict data security and monitoring measures deployed on its infrastructure.
It’s pretty common for an environment to be a shared infrastructure for various services. When this is the case, robust security controls (like stricter isolation for applications and databases) are even more important! [Multi-tenant architectures](https://substack.com/redirect/b1a632c4-8ade-4787-84fe-0901acc0beb9?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) are a good example for such “shared infrastructure” where stricter security controls are necessary.
This refers to labeling data based on sensitivity, confidentiality, and regulatory requirements. Understanding the classification of data helps determine:
Appropriate security controls
Suitable encryption methods
Access restrictions for safeguarding sensitive information and preventing unauthorized disclosure or misuse.
It’s helpful to calculate a criticality score for services. For this, I like to assign weights to the security dimensions. Below is a sample of how these scores could look. It’s just an example; simpler than I usually use, and it doesn’t encompass all factors relevant for every system. Just treat it as inspiration:
Now we’ve established the basic factors for understanding risk and criticality, we can do some napkin math with criticality scores, based on characteristics:
A simple way to think about a total risk “score” is to add together the weights for each dimension. So, in this case: Total Risk Score = BP + PA + CAC + US + DE + DC.
Let’s take the example of building a payment system for an e-commerce site. It needs to process a high volume of transactions via credit cards, debit cards, and other payment methods. It also needs to have payment gateway integration, account for fraud prevention, and is subject to PCI DSS compliance.
Let’s do the napkin math for this system’s criticality:
We get the total risk score by adding up the dimensions. In this case, it comes to 15 out of a maximum of 18 points (3 + 1 + 2 + 3 + 3 + 3.) This score indicates we are talking about a critical system from a security standpoint.
All companies have unique risk-scoring and risk-tracking processes. As a software engineer, you need to figure out what a “high” service risk score means, and at what point you should reach out to the security team at your organization, if there is one.
Become a paying subscriber of The Pragmatic Engineer to get access to this post and other subscriber-only content.
| Full articles every Tuesday and Thursday | |
| Access to resources and templates for engineering managers and engineers | |
| Access to the complete archive, see all comments and comment on articles |