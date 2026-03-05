---
subject: "AI Engineering in the real world"
from: "The Pragmatic Engineer <pragmaticengineer+deepdives@substack.com>"
to: ""
date: 2025-03-25 16:57:06
labels: ["CATEGORY_PERSONAL", "INBOX", "The Pragmatic Engineer"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_6413324878686416177"]
---
👋 Hi, this is Gergely with a subscriber-only issue of the Pragmatic Engineer Newsletter. In every issue, I cover challenges at Big Tech and startups through the lens of engineering managers and senior engineers. If you’ve been forwarded this email, you can
|
AI Engineering is the hottest new engineering field, and it’s also an increasingly loaded phrase which can mean a host of different things to different people. It can refer to ML engineers building AI models, or data scientists and analysts working with large language models (LLMs), or software engineers building on top of LLMs, etc. To make things more confusing, some AI tooling vendors use the term for their products, like Cognition AI naming theirs an “AI engineer.”
In her new book “AI Engineering,” author Chip Huyen [defines](https://substack.com/redirect/a760476e-5209-4551-8b7e-d4e88c611914?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) AI engineering as building applications that use LLMs, placing it between software engineering (building software products using languages, frameworks, and APIs), and ML engineering (building models for applications to use). Overall, AI engineering feels closer to software engineering because it usually starts with software engineers building AI applications using LLM APIs. The more complex the AI engineering use case, the more it can morph into looking like ML engineering.
Today, we focus on software engineers who have switched to being AI engineers. These are devs who work with LLMs, and build features and products on top of them. We cover:
What are companies building? An overview of seven companies at different stages and in various segments of tech.
Onboarding to AI Engineering as a software engineer. Approaches that help devs get up to speed faster.
Tech stack. Seven different tech stacks, showcasing variety and some common choices.
Engineering challenges. Problems caused by LLMs being non-deterministic, evals, latency, privacy, and more.
Novel tooling. Several companies build in-house tooling, which pays off with this fast-moving technology. Incident management startup, incident.io, shares their unique, bespoke stack.
Cost considerations. LLMs can quickly get expensive, although costs are dropping quickly. But as this happens, usage tends to grow which causes its own issues. Businesses share how big a deal costs really are.
Learnings from software devs turned AI engineers. Building a prototype is the easy bit, vibes-based development inevitably turns bad, smart teams fail because they get overwhelmed; educating AI users, and more.
Note: I am an investor in incident.io and Wordsmith, which both share details in this deepdive. I always focus on being unbiased in these articles – but at the same time, being an investor means these companies share otherwise hard-to-obtain details. I was not paid by any business to mention them in this article. See [my ethics statement](https://substack.com/redirect/63caffe0-e33e-45db-8eb1-170dc5f5947e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) for more.
Thanks to the engineers contributing to this deepdive: [Lawrence Jones](https://substack.com/redirect/60ff0181-ceda-47eb-a916-17f5ec3c8f53?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) (senior staff engineer at incident.io), [Tillman Elser](https://substack.com/redirect/85d09484-5116-4aba-81e1-7f7c5f0086df?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) (AI lead at Sentry), [Ross McNairn](https://substack.com/redirect/2d33384f-7ee5-4f68-84ab-b68ba923a0f7?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) (cofounder at Wordsmith AI), [Igor Ostrovsky](https://substack.com/redirect/47cedc42-b5da-4ab6-93e0-f895c3ccfcd3?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) (cofounder at Augment Code), [Matt Morgis](https://substack.com/redirect/c9023b97-7e2a-4583-b04d-43aef6ca7cb6?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) (Staff Engineer, AI, formerly at Elsevier), [Ashley Peacock](https://substack.com/redirect/07816e07-82e7-45d3-8966-84518cbe181a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) (Staff Engineer at Simply Business), and [Ryan Cogswell](https://substack.com/redirect/bdc66ec9-945d-4f1a-a540-25b4cae4f6a1?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) (Application Architect at DSI).
The bottom of this article could be cut off in some email clients. [Read the full article uninterrupted, online.](https://substack.com/redirect/80bc3fde-853e-42a3-a7e9-86b923a46e7a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
[Incident.io](https://substack.com/redirect/efe09af9-0af6-4d76-9460-101803831453?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) is a tool to help resolve outages as they happen. A few months ago, the engineering team went back to the drawing board to build features that capitalize on how much LLMs have improved to date. Two of these features:
AI note taker during incidents. This includes live transcription, real-time summaries for people joining a call to get up to speed with, and key decisions/actions to clarify who does what.
Incident investigator: an agent looks into an ongoing incident by checking code, logs, monitoring, and old incidents to identify root causes and share findings, with a responder being paged. More details on
[how this tool is built](https://substack.com/redirect/ac8a4270-ee4a-4ad7-98af-450310740089?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).
Both these features make heavy use of LLMs, and also integrate with several other systems like backend services, Slack, etc.
[Sentry](https://substack.com/redirect/1fe050ce-fd70-4ad7-acc8-5479df6c103b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) is a popular application monitoring software. Two interesting projects they built:
Autofix: make it really fast to go from a problem with code (a Sentry issue) to a fix with a GitHub PR. Autofix is an open source RAG framework that combines all of Sentry’s context/telemetry data with code in order to root cause, fix, and create unit tests for bugs.
Issue Grouping: cut down alerting volume while reducing noise. For this, the team used recent advancements in approximate neighbor search (ANN), plus dramatic recent improvements in embedding quality from the new BERT architecture transformer models.
Both these features are [fair source](https://substack.com/redirect/64faa29a-89d1-4305-98c3-3445549879f8?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), meaning you can see exactly how they work.
[Wordsmith](https://substack.com/redirect/b0eaac4d-a487-4abe-ac6b-00434c3a16f3?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) is building AI tools that legal teams use, including:
Documents workspace: plug into all of a company’s communication streams, including analyzing documents and augmenting their contents, and drafting communications.
[Check out a video of it in action.](https://substack.com/redirect/bc078009-67c4-4431-b3c8-fe70d0747d30?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)AI contract review: A product that can analyse any contract or website, then review it and generate a marked-up word doc,
[here](https://substack.com/redirect/f60d5297-0d34-4a5b-9325-f462a45f4624?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). Basically, it’s a lawyer anyone can use.
[Augment Code](https://substack.com/redirect/3bc2fc0c-c899-43e0-8224-4a49e08b1018?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) is an AI coding assistant for engineering teams and large codebases. This kind of product probably needs little introduction for devs:
AI coding assistant: including IDE extensions for VS Code, JetBrains, Cursor, and Vim, and a Slack extension
Fine-tuning models: for AI coding tools, models make a big difference. The team don’t pre-train models or build their own LLMs, but run extensive post-training and do fine tuning to suit the 4-5 models used for specific coding-related cases.
[Elsevier](https://substack.com/redirect/41a91ece-ca5e-4aad-b152-34a27164272b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) is one of the world’s leading publishers of scientific and medical content. Matt Morgis was an engineering manager at the company when the engineering leadership noticed that several product teams were independently implementing [RAG capabilities](https://substack.com/redirect/d0258485-5d70-40dc-82ef-fe02d1163e99?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o); each sourcing content, parsing it, chunking it, and creating embeddings.
An enterprise-wide RAG platform was the solution Matt and his team built, to enable multiple teams to build AI-powered products for medical and scientific professionals. Their platform consists of:
Database. A content database that centralized and normalized content from various sources.
Embeddings+search: A content embedding & indexing pipeline and vector search API.
LLM API: interfacing to multiple LLM models. This API allows teams to experiment with different models by changing a parameter on the API. It also allowed Elsevier to track the usage of various LLM models based on applications using it.
Products built on top of this platform:
Intelligent tutoring system for medical students
Clinical decisions support tool for doctors
Ashley Peacock is a staff software engineer at the insurer, [Simply Business](https://substack.com/redirect/b09384aa-d6c4-4660-ba5a-ebf21fdc0c23?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), who built a pretty common use case: a chatbot for customers to get answers to questions. This seems like the simplest of use cases – you might assume it just involves connecting documentation for the chatbot to use – but it was surprisingly challenging because:
Industry regulation. The chatbot cannot be inaccurate or make things up, as customers use the information to make decisions about which insurance purchases.
Non-deterministic responses. The business needed to turn a nondeterministic chatbot into one that only produces approved responses.
The team had the idea to create an “approved answers” knowledge base for the chatbot, and faced the challenge of creating the questions for this. The team made the chatbot state when it cannot answer a question, and to then connect with human support, which then updated the knowledge base with their solution. This approach works pretty well after taking a few iterations to get right.
[Data Solutions International](https://substack.com/redirect/cbe27d8c-38cf-44ae-a223-a4da5bccd730?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) (DSI) is a 30-person HR tech company with 5 engineers, selling products that help with performance review processes, assessments, and employee engagement surveys. The company is family-owned, has been operating for 27 years, and is profitable.
Summarizing comments for employee engagement processes was the first feature they wanted to build, as something customers would appreciate, and which the team could learn about working with LLMs from.
During an employee engagement process, there are questions like "what do you like most about working here", and "if you could change one thing about working at Company X, what would it be?", etc. For larger companies with thousands of employees, there may be thousands of comments per question. Individual departmental leads might read all comments relevant to them, but there’s no way an HR team at a very large business could check every single comment.
Before LLMs, such comments were categorized into predefined categories, which were hardcoded, per company and per survey. This was okay, but not great. Data Solutions International’s goal was to use LLMs to summarize a large number of comments, and report to survey admins the broad categories which comments belong in, how many comments per category there are, and to allow drilling down into the data.
So, how do you get started building applications with LLMs as a software engineer transitioning to this new field? Some advice from folks at the above companies who have:
Let’s start with an encouraging story from veteran software engineer [Ryan Cogswell](https://substack.com/redirect/bdc66ec9-945d-4f1a-a540-25b4cae4f6a1?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), at HR tech company, DSI. He joined the company 25 years ago, and was the first engineering hire. When AI tools came along, DSI decided to build a relatively simple first AI feature in their HR system that summarized comments for employee engagement purposes. Neither Ryan nor any of the other 4 devs had expertise in AI and LLMs, so the company contracted an external agency which offered a fixed, timeboxed offer to scope the project. Here’s how it went:
Month #1: the agency goes and builds stuff, and shares LLM outputs with DSI
Month #2: while continuing to iterate on desired outputs, devs at DSI ask the agency for access to how things work. They get access to scripts and notebooks
Month #3: the agency lays out the proposed architecture for the project.
The proposal was for a really complex architecture:
SageMaker: a heavyweight solution from AWS to build, train, and deploy ML models
Langfuse: an open source LLM engineering platform to debug and improve LLM applications
Lambdas: serverless functions to run computations
Database #1: store interim states of data between prompts
Database #2: storing user feedback
Other parts: to support RAG aspects
Pipings: to hold it all together
The agency quoted 6-9 months to build the relatively small feature (!!), and an estimated operational cost higher than DSI’s entire investment in all their infrastructure! This was when Ryan asked how hard it could be to build it themselves, and got to work reading and prototyping, making himself the company’s resident GenAI expert.
In 2 months, Ryan and a couple of colleagues built the feature for a fraction of the cost to operate than the agency’s quote. His tech stack choice:
AWS Bedrock: chosen for cost (vs hosting own models), security, and that the platform doesn’t use their input or output tokens for training
[Cohere Embed v3](https://substack.com/redirect/b9c6af27-ed97-4f0f-b4fb-2a4487b1f330?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o): the model used to generate embeddingsPostgreSQL: to store embeddings and do vector-based database queries, using AWS Aurora PostgreSQL
Java: the backend code runs on this, deployed in AWS
React: the frontend that fetches and displays the data, integrated into the existing web app
Ross McNairn is cofounder and CEO of the startup, Wordsmith, which several software engineers have joined. You need to rethink how to think about things, he says:
“Working with AI requires a totally different way of approaching problems.
For new joiner engineers, there is a major readjustment in the first few weeks while they explore the codebase and participate in discussions. There are so many problems that can be eloquently sidestepped using AI. Understanding the suite of tools available takes some time.
Getting comfortable with evaluations and iterating on non-deterministic outputs is the biggest challenge most devs have. A lot of solutions are more subjective: engineers need to really understand the domain in order to assess if output is high-quality. It takes time to ramp up to the point where you can confidently assess output quality.”
[Matt Morgis](https://substack.com/redirect/c9023b97-7e2a-4583-b04d-43aef6ca7cb6?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) was an engineering manager at Elsevier who decided to transition back to staff engineer, specifically to work on AI:
“The move to go from manager to IC was deliberate: working with AI has rekindled my joy in coding.
For experienced engineers who know how to break problems down, AI tools are an incredible force multiplier. At the same time, when I was a manager, I saw AI coding tools handicap junior engineers’ development. The tools are powerful, but I think they’re best wielded by those who understand good software engineering principles.”
The transition was successful, and today Matt is a staff engineer focusing on GenAI at CVS Health.
Here’s the tech stack which various companies used. There’s no right or wrong tech stack – what follows is for context and inspiration, not a blueprint.
The stack:
Postgres and
[pgvector](https://substack.com/redirect/d798c699-8d87-4ead-b051-017c8a17e513?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)for storing embeddings and searching themChatGPT 4o as the default model, and Sonnet 3.7 for code analysis and technical tasks, as they find this Anthropic model performs better. Built in a way to easily switch between them as needed
Gemini: some models used GCP’s Vertex offering, but less often than other models
GCP using Kubernetes: the infrastructure layer
Go on the backend, running as a monolith
React + Typescript on the frontend, including for the dashboard of their own developers’ custom AI tools (covered below)
In-house LLM agent tooling: the team evaluated and rejected using a tool like the [LangChain](https://substack.com/redirect/3832839e-6f7f-48f0-950d-c5d125627345?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) framework to integrate LLMs with other data sources and into workflows. It was a lot more work to build their own, but the upsides are that the architecture and code are more in-line with abstractions and design patterns in Sentry’s existing codebase.
The company used the following languages and frameworks to build this tooling:
Postgres for database and vector store,
[pgvector](https://substack.com/redirect/d798c699-8d87-4ead-b051-017c8a17e513?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)for similarity search (for Approximate Nearest Neighbor –[ANN](https://substack.com/redirect/38ae8cf0-340c-4117-982d-0d31bb89de9a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)– search)Clickhouse for online analytical processing (OLAP)
Sentry for observability – it would be odd to not use their own product for this
Kubernetes for orchestrating compute resources
Python and
[PyTorch](https://substack.com/redirect/e60fb7b1-b16b-4aaf-b060-8d5eff96beed?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)(machine learning library) for inference
The stack:
Pinecone as their vector database
LangChain as their framework to integrate LLMs into the stack.
[LangSmith](https://substack.com/redirect/76ed29d4-af7e-488d-8420-57bda07ad5c9?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)as their developer platform[LlamaIndex](https://substack.com/redirect/4304fdbb-8d7f-4a22-bd8a-efcedf49b62f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)as orchestration frameworks to integrate data with LLMs
Multi-cloud providers:
AWS for running Anthropic models via Bedrock. AWS offers generous credits for startups, which was a factor in the choice
Azure to access OpenAI services because it allows specifying regions to use, which is important when serving EU customers, for example. Using OpenAI’s services directly would not allow switching of regions.
GCP: for Gemini and Vertex (Google’s search AI).
Azure and GCP each have business models for locking in customers; Microsoft is the only major cloud provider offering OpenAI models, and only GCP offers Gemini.
The company routes to different model by use case:
OpenAI: for reasoning-heavy use cases, where the o1 and o3 models are very strong
Groq: when performance is critical, or the goal is to augment UI. Wordsmith calls their API directly – as the performance of Groq is incredibly fast; a step-change in AI development, according to the WordSmith team. Note:
[Groq](https://substack.com/redirect/784f5137-94c5-4eab-8199-46aa17f3b4ac?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)is a standalone company and product, not to be confused with Grok, the AI assistant on social media site, X.
The stack to build and run LLMs:
Google Cloud: the cloud vendor of choice
A3 Mega 600GPU/75 node cluster: used for LLM training and inference
NVIDIA: the hardware choice for GPUs, and for software (CUDA)
Python and PyTorch: the team wrote training and inference libraries making heavy use of PyTorch
The scientific publisher used this stack to build their in-house RAG platform:
AWS Bedrock and Azure OpenAI for hosting and running LLMs
LangChain for LLM integration
Snowflake as their content data warehouse
Embedding pipelines and vector database:
[Apache Airflow](https://substack.com/redirect/a0cc2599-b80f-4b94-8449-d8944367d97e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)for running embedding pipelines[AWS Fargate for ECS](https://substack.com/redirect/748b90f1-2d71-49a6-bc31-bdca9548612a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)to run containers[AWS OpenSearch](https://substack.com/redirect/659d9b2f-bcd9-4150-99e7-959c57b786f3?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)as the vector search database
[FastAPI](https://substack.com/redirect/2fc0575b-4161-482e-8a66-70b1879c1bb1?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)(a Python-based web framework to build HTTP APIs) for HTTP APIs
A pretty simple stack:
AWS Bedrock to host the model, making use of
[Knowledge Bases and Guardrails features](https://substack.com/redirect/9993ddc6-9999-4ce0-a81f-7383625499eb?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)Anthropic Sonnet 3.5 model
Ruby on Rails as the language and framework, running it on top of
[AWS ECS](https://substack.com/redirect/b93fe4a1-be35-4853-85c3-04c66e3054c3?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
As covered above, Ryan took the initiative at DSI by building a simpler solution than the one an AI vendor proposed. DSI ended up with:
AWS Bedrock for running the models
PostgreSQL: to store embeddings and do vector-based database queries. Using AWS Aurora PostgreSQL, and
[Cohere Embed v3](https://substack.com/redirect/b9c6af27-ed97-4f0f-b4fb-2a4487b1f330?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)for generating embeddings
The seven businesses in this article are all different, but there are some common trends:
AWS Bedrock: the preferred way to host and run Anthropic models
Postgres with pgvector: the database of choice to work with embeddings and vectors at most companies. The exception is Wordsmith, which uses vector database
[Pinecone](https://substack.com/redirect/e1218a97-8564-442f-9229-556b4f0a3360?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)LangChain: a few places use this as the framework to integrate LLMs into their stacks
The bigger the scale, the closer you get to the “metal:” most startups are happy to use cloud providers to run LLMs. However, when starting to get into fine-tuning LLMs and heavy usage, it becomes time to rent larger resources and get close to the hardware. Augment Code using NVIDIA GPUs and CUDA software is an example.
What unusual or new challenges does AI Engineering pose for more “traditional” software engineers? The most common ones mentioned:...
Become a paying subscriber of The Pragmatic Engineer to get access to this post and other subscriber-only content.
| Full articles every Tuesday and Thursday | |
| Access to resources and templates for engineering managers and engineers | |
| Access to the complete archive, see all comments and comment on articles |