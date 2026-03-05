---
subject: "How Kubernetes is Built with Kat Cosgrove"
from: "The Pragmatic Engineer <pragmaticengineer@substack.com>"
to: ""
date: 2025-05-14 17:06:42
labels: ["CATEGORY_PERSONAL", "INBOX", "The Pragmatic Engineer", "UNREAD"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_6413324878686416177", "UNREAD"]
---
|
Listen and watch now on [YouTube](https://substack.com/redirect/c69403cc-7630-4464-b6a6-1a56795c8fba?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), [Spotify](https://substack.com/redirect/c9b81716-40bf-4656-bddd-65b71f4bcb58?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) and [Apple](https://substack.com/redirect/5f113b26-95fc-4edd-8634-65cc0b8beeb8?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). See the episode transcript at the top of this page, and timestamps for the episode at the bottom.
• [WorkOS](https://substack.com/redirect/7bfcfc89-54f3-43d7-89f3-2d75f0ecf560?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) — The modern identity platform for B2B SaaS.
• [Modal](https://substack.com/redirect/3ac5bb36-4f4f-494d-943e-2796ab7785ed?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)[](https://substack.com/redirect/3ac5bb36-4f4f-494d-943e-2796ab7785ed?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) — The cloud platform for building AI applications.
• [Cortex](https://substack.com/redirect/bc0e8568-bbb7-48bd-aba1-2060b9c2e823?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)[](https://substack.com/redirect/3ac5bb36-4f4f-494d-943e-2796ab7785ed?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) — Your Portal to Engineering Excellence.
—
Kubernetes is the second-largest open-source project in the world. What does it actually do—and why is it so widely adopted?
In this episode of The Pragmatic Engineer, I’m joined by [Kat Cosgrove](https://substack.com/redirect/847069dc-7009-4828-9103-1347d7718c49?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), who has led several Kubernetes releases. Kat has been contributing to Kubernetes for several years, and originally got involved with the project through K3s (the lightweight Kubernetes distribution).
In our conversation, we discuss how Kubernetes is structured, how it scales, and how the project is managed to avoid contributor burnout.
We also go deep into:
An overview of what Kubernetes is used for
A breakdown of Kubernetes architecture: components, pods, and kubelets
Why Google built Borg, and how it formed the basis of Kubernetes
The benefits of large-scale open source projects—for companies, contributors, and the broader ecosystem
The size and complexity of Kubernetes—and how it’s managed
How the project protects contributors with anti-burnout policies
The size and structure of the release team
What KEPs are and how they shape Kubernetes features
Kat’s views on GenAI, and why Kubernetes blocks using AI, at least for documentation
Where Kat would like to see AI tools improve developer workflows
Getting started as a contributor to Kubernetes—and the career and networking benefits that come with it
And much more!
Some of the most interesting topics discussed in the conversation were these:
1. Kubernetes helps with managing large-scale backend applications. Google originally built an in-house tool to manage the tens of thousands (then hundreds of thousands and later millions) of machines: this internal tool is called Borg. The roots of Kubernetes come from Borg: but Google has since donated the project to the Cloud Native Computing Foundation (CNCF) – and today, Kubernetes is the second largest open source project, after Linux. We previously did a deepdive on [How Linux is built](https://substack.com/redirect/2db19f1c-cdaf-4194-ac52-af3e27010ca6?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), and touched on Google’s SRE roots in [What is Reliability Engineering?](https://substack.com/redirect/c6519081-3db6-4a5b-8d5a-2f407524387d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
2. Kubernetes is a very well-structured and organized open source project. The structure of the project and all processes are [well documented](https://substack.com/redirect/08583780-c231-402b-8b7e-6650fbf96b4b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). The project has around 150-200 maintainers, has a few dozen SIGs (Special Interest Groups) and releases run on a 14-16 week cycle.
3. The “lead” and “shadow” concept is a clever one, utilized by Kubernetes. The Release Team within Kubernetes owns releases, and the Release Team has about 20-30 people participating in each release. About half of the participants in the Release Team are “shadows” who get to learn on the job how a release is done – and, hopefully, in a release or two, become leads themselves!
Unlike most open source projects where getting a spot on the release team is based on long tenure and impactful contributions: the Kubernetes team recruits “shadows” people via an application process. Even those with no prior Kubernetes contributions are invited to join and participate. To get notified of [applications opening](https://substack.com/redirect/3a858acb-1c6b-4c5d-8dbe-81d4e7a73bd2?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), subscribe to the [relevant Kubernetes mailing lists](https://substack.com/redirect/3a858acb-1c6b-4c5d-8dbe-81d4e7a73bd2?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). This is a very friendly policy – and another reminder that a project can come up with its own policies: no need to copy existing ones.
From the episode, starting at [29:26](https://substack.com/redirect/99e399b0-df34-4e3b-8c46-4852c6700de4?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
Gergely: “Why did Kubernetes win? What did it do so well?”
Kat: “I think we caught on early because of hype. Because of the Google name brand behind us and the association with Docker, which was already very popular. Google was a familiar company, donating a project that relied on a tool many were already familiar with (Kubernetes / Borg). And that got us an initial hype cycle.
The continued popularity of Kubernetes is at least in part due to our truly exceptional documentation. If Kubernetes does something that you can touch as a user, as a cluster admin, we have documented it. Kubernetes uses something in the release cycle called a Kubernetes enhancement proposal, a
[KEP]. This was inspired by Python's[PEP](Python Enhancement Proposal).One of the things we require for a KEP to be considered complete and thus, includable in a particular release is that it has a user-facing change at all – even if it's just a feature flag! – it must be documented, or we do not allow it in the release.
Today, as we're recording this, this is actually the docs freeze for
[Kubernetes version 1.33]. So today, a lot of KEP owners will either merge documentation, or I will revert their PRs!
([00:00](https://substack.com/redirect/639c4e25-3da2-4016-891f-284257dc2ccb?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Intro
([02:02](https://substack.com/redirect/f0084703-b0fe-410e-96d7-93808a8d062c?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) An overview of Kubernetes and who it’s for
([04:27](https://substack.com/redirect/28ecec83-4ce9-48e5-a2de-49499be843a2?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) A quick glimpse at the architecture: Kubernetes components, pods, and cubelets
([07:00](https://substack.com/redirect/7e7557db-83cd-4606-a938-72f70491f62d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Containers vs. virtual machines
([10:02](https://substack.com/redirect/3928d9ef-3e77-4d2e-8a34-7f300ff2712f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The origins of Kubernetes
([12:30](https://substack.com/redirect/55c19ef8-6a89-412b-91f7-f079c5ebd3bd?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Why Google built Borg, and why they made it an open source project
([15:51](https://substack.com/redirect/fd34e705-c577-47bf-b2d8-ce941b446a0d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The benefits of open source projects
([17:25](https://substack.com/redirect/d9457c84-ac90-4235-88c2-af0f554cf2c0?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The size of Kubernetes
([20:55](https://substack.com/redirect/047ea10c-5952-49c7-82af-21828ca9e31d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Cluster management solutions, including different Kubernetes services
([21:48](https://substack.com/redirect/a9a14501-da5b-4ddd-afae-c86d3e41690a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Why people contribute to Kubernetes
([25:47](https://substack.com/redirect/858d0193-74a2-41e7-8134-95992c01c8ee?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The anti-burnout policies Kubernetes has in place
([29:07](https://substack.com/redirect/cf1a2687-e51f-4d21-97c1-60da0386352c?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Why Kubernetes is so popular
([33:34](https://substack.com/redirect/016254ed-395d-4bc4-a56d-db175af0d490?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Why documentation is a good place to get started contributing to an open-source project
([35:15](https://substack.com/redirect/1653f698-f1ba-4ce8-be72-80893a1383ba?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The structure of the Kubernetes release team
([40:55](https://substack.com/redirect/35c96e73-0f24-4197-9296-3e97c4472564?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) How responsibilities shift as engineers grow into senior positions
([44:37](https://substack.com/redirect/1a166b98-7db0-411f-95f3-d5e9c432eec9?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Using a KEP to propose a new feature—and what’s next
([48:20](https://substack.com/redirect/0b70c3c7-70ad-44d7-a27f-0d8f1a792007?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Feature flags in Kubernetes
([52:04](https://substack.com/redirect/a53bddfe-fcd2-4190-b41d-2acf20e21582?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Why Kat thinks most GenAI tools are scams—and why Kubernetes blocks their use
([55:04](https://substack.com/redirect/f123255e-3e49-4c77-aff1-d973fd3ad4fa?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The use cases Kat would like to have AI tools for
([58:20](https://substack.com/redirect/df39a9a4-454b-4f11-9ecc-4538f8ce4fa2?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) When to use Kubernetes
([1:01:25](https://substack.com/redirect/2f3bdc50-d348-4e8e-b145-60192c284b9f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Getting started with Kubernetes
([1:04:24](https://substack.com/redirect/0d71d101-ec6f-42d4-883d-501786653c1a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) How contributing to an open source project is a good way to build your network
([1:05:51](https://substack.com/redirect/39a97afd-43b9-4cfc-b14c-0537905eb258?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Rapid fire round
Where to find Kat Cosgrove:
• Bluesky: [https://bsky.app/profile/kat.lol](https://substack.com/redirect/dfdb0f43-0bfc-4deb-9018-1496c196a4d8?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• LinkedIn: [https://www.linkedin.com/in/katcosgrove/](https://substack.com/redirect/847069dc-7009-4828-9103-1347d7718c49?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
Mentions during the episode:
• Kubernetes: [https://kubernetes.io/](https://substack.com/redirect/f87a0821-beaf-42d2-a1c8-6a4527033cf9?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Docker: [https://www.docker.com/](https://substack.com/redirect/141058ee-8600-4545-b185-488ffcad9c73?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Mesos: [https://mesos.apache.org/](https://substack.com/redirect/141058ee-8600-4545-b185-488ffcad9c73?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Borg: [https://en.wikipedia.org/wiki/Borg_(cluster_manager)](https://substack.com/redirect/07ab20c2-c224-4d9b-8d88-aadeed445a72?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• The Linux Foundation: [https://www.linuxfoundation.org/](https://substack.com/redirect/e56a5678-65fe-44a7-ae48-6eee2a419333?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Cloud Native Computing Foundation: [https://www.cncf.io/](https://substack.com/redirect/135be81a-6344-49d1-a75b-d0b57f2de818?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Joe Beda on LinkedIn: [https://www.linkedin.com/in/jbeda/](https://substack.com/redirect/0d437404-e8e9-4869-9251-13ae1693c8cb?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Seven of Nine” [https://en.wikipedia.org/wiki/Seven_of_Nine](https://substack.com/redirect/6926feb8-1cbf-4595-868f-6356455b5cdf?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• What is Reliability Engineering?: [https://newsletter.pragmaticengineer.com/p/reliability-engineering](https://substack.com/redirect/c6519081-3db6-4a5b-8d5a-2f407524387d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Dave O’Conner on LinkedIn: [https://www.linkedin.com/in/gerrowadat/](https://substack.com/redirect/705db95d-f317-4549-9b17-316165bb48de?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Spotify for Backstage: [https://backstage.spotify.com/](https://substack.com/redirect/92bc0677-498d-417d-b32d-4d3651e0ccd0?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Azure Kubernetes Service: [https://azure.microsoft.com/en-us/products/kubernetes-service](https://substack.com/redirect/ffda6f3b-8451-4696-8622-db2d9d9e596e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Oracle Kubernetes Engine: [https://www.oracle.com/cloud/cloud-native/kubernetes-engine/](https://substack.com/redirect/b122077a-f25c-4314-a533-7da9d06f53b5?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• RedHat Openshift: [https://www.redhat.com/en/technologies/cloud-computing/openshift/](https://substack.com/redirect/4d61d5f5-b4ed-429b-b6c9-88792a506ca4?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• VMware Tanzu: [https://www.vmware.com/products/app-platform/tanzu](https://substack.com/redirect/870bf794-b88a-4919-b4b9-3d083722b483?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• 2347: Dependency: [https://www.explainxkcd.com/wiki/index.php/2347:_Dependency](https://substack.com/redirect/0e7ec95b-d460-4380-87cb-39c435a72c93?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Inside Linear's Engineering Culture: [https://newsletter.pragmaticengineer.com/p/linear](https://substack.com/redirect/bf415aa3-10e9-4fc8-887e-ae243a3e604f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Linear: move fast with little process (with first engineering manager Sabin Roman): [https://newsletter.pragmaticengineer.com/p/linear-move-fast-with-little-process](https://substack.com/redirect/0762abc1-3481-4cbe-84ba-c03b705fd112?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Linear: [https://linear.app/](https://substack.com/redirect/41b8b267-f505-483c-8dd8-3ba8be6c44d8?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• PEP: [https://peps.python.org/pep-0001/](https://substack.com/redirect/e7298d4e-efc4-4528-aec9-235706e26041?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Google Kubernetes Engine: [https://cloud.google.com/kubernetes-engine](https://substack.com/redirect/7390d30c-e869-4b15-9726-4b594cb492c0?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• How Linux is built with Greg Kroah-Hartman: [https://newsletter.pragmaticengineer.com/p/how-linux-is-built-with-greg-kroah](https://substack.com/redirect/2db19f1c-cdaf-4194-ac52-af3e27010ca6?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• KEPs: [https://www.kubernetes.dev/resources/keps/](https://substack.com/redirect/4e8b3503-00d7-452b-a523-d16d0a79fff3?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• The Philosophy of Software Design – with John Ousterhout: [https://newsletter.pragmaticengineer.com/p/the-philosophy-of-software-design](https://substack.com/redirect/39da45f1-02c7-4e8a-95b0-7190f1c31d8f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Python: [https://www.python.org/](https://substack.com/redirect/b7b53296-de5d-4524-a717-82b2baa2e7e3?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• A Fire Upon the Deep: [https://www.amazon.com/Fire-Upon-Deep-Zones-Thought/dp/0812515285](https://substack.com/redirect/1d0284f5-abf8-4613-8dd8-f6860082ccdd?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Kubernetes on Slack: [https://communityinviter.com/apps/kubernetes/community](https://substack.com/redirect/871c06da-b0b8-4aa8-9b97-c6414913b520?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
—
Production and marketing by [Pen Name](https://substack.com/redirect/0939bc15-cb80-4e47-95d2-24849d4756f3?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).
You’re on the free list for [The Pragmatic Engineer](https://substack.com/redirect/2/eyJlIjoiaHR0cHM6Ly9uZXdzbGV0dGVyLnByYWdtYXRpY2VuZ2luZWVyLmNvbT91dG1fY2FtcGFpZ249ZW1haWwtaG9tZSZyPThvNTRuIiwicCI6MTYzNTA2NTg4LCJzIjo0NTg3MDksImYiOnRydWUsInUiOjE0NTYzMzE5LCJpYXQiOjE3NDcyNDI0NDEsImV4cCI6MTc0OTgzNDQ0MSwiaXNzIjoicHViLTAiLCJzdWIiOiJsaW5rLXJlZGlyZWN0In0.Y1_AyPwUtUXwQ5MjtnDUyo8ywuK6S92D3pPISLLFLZc?). For the full experience, [become a paying subscriber](https://substack.com/redirect/2/eyJlIjoiaHR0cHM6Ly9uZXdzbGV0dGVyLnByYWdtYXRpY2VuZ2luZWVyLmNvbS9zdWJzY3JpYmU_dXRtX3NvdXJjZT1wb3N0JnV0bV9jYW1wYWlnbj1lbWFpbC1jaGVja291dCZuZXh0PWh0dHBzJTNBJTJGJTJGbmV3c2xldHRlci5wcmFnbWF0aWNlbmdpbmVlci5jb20lMkZwJTJGaG93LWt1YmVybmV0ZXMtaXMtYnVpbHQtd2l0aC1rYXQmcj04bzU0biZ0b2tlbj1leUoxYzJWeVgybGtJam94TkRVMk16TXhPU3dpYVdGMElqb3hOelEzTWpReU5EUXhMQ0psZUhBaU9qRTNORGs0TXpRME5ERXNJbWx6Y3lJNkluQjFZaTAwTlRnM01Ea2lMQ0p6ZFdJaU9pSmphR1ZqYTI5MWRDSjkuUDBrZFBubV93dFZSZUhUWWtERno1RW5OWjJaMDd4dnlCRGQ3Mkp5ZFl5OCIsInAiOjE2MzUwNjU4OCwicyI6NDU4NzA5LCJmIjp0cnVlLCJ1IjoxNDU2MzMxOSwiaWF0IjoxNzQ3MjQyNDQxLCJleHAiOjE3NDk4MzQ0NDEsImlzcyI6InB1Yi0wIiwic3ViIjoibGluay1yZWRpcmVjdCJ9.AT4V7bTbEXj6dH_Y8GqZMIfvsiVmheERVgyJPKasyn4?). Many readers expense this newsletter within their company’s training/learning/development budget.
This post is public, so feel free to share and forward it.
If you enjoyed this post, you might enjoy my book, [The Software Engineer's Guidebook](https://substack.com/redirect/da77f2af-9692-47bd-bedc-76b812c30b98?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). Here is what Tanya Reilly, senior principal engineer and author of The Staff Engineer's Path said about it:
"From performance reviews to P95 latency, from team dynamics to testing, Gergely demystifies all aspects of a software career. This book is well named: it really does feel like the missing guidebook for the whole industry."