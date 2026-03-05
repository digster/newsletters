---
subject: "Inside OpenAI: How does ChatGPT Ship So Quickly?"
from: "The Pragmatic Engineer <pragmaticengineer@substack.com>"
to: ""
date: 2023-11-14 15:44:10
labels: ["CATEGORY_PERSONAL", "INBOX", "The Pragmatic Engineer", "UNREAD"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_6413324878686416177", "UNREAD"]
---
👋 Hi, this is Gergely with a 🔒 subscriber-only issue 🔒 of the Pragmatic Engineer Newsletter. In every issue, I cover challenges at Big Tech and startups through the lens of engineering managers and senior engineers.
|
OpenAI might be the hottest company in tech right now. The company is behind the popular large language-based model, [ChatGPT](https://substack.com/redirect/117396ae-5163-4b5c-a6e9-ca42001b82fa?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), and also built the GPT-3, GPT-3.5 and GPT-4 models which several AI coding assistants use, such as GitHub Copilot. The CEO of the company is Sam Altman, formerly president of Y Combinator.
ChatGPT launched in November 2022, and took the world by storm. It’s safe to say this product provided applied AI with its biggest “wow” moment, and has been the catalyst for a surge in AI investment, industry-wide. ChatGPT has passed 100M weekly active users, as [announced](https://substack.com/redirect/68e2f902-3422-4811-ada9-66172b952c88?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) by CEO Sam Altman on 6 November. Hitting this milestone in less than a year from launch is unprecedented.
Since it arrived last year, it seems ChatGPT has been shipping at breakneck speed:
Nov 2022: public launch (on 30 November 2022, to be exact)
Dec 2022: performance updates and conversation history
Jan 2023: the ability to stop generating, and factuality updates (this is when ChatGPT crosses 100M monthly users)
February: ChatGPT Plus, internationally
March: GPT-4 in ChatGPT. Shipping plugins.
May: web browsing and plugins rolled out in beta. Shared links plugin, and export data.
June: a “browsing” feature.
July: custom instructions and code interpreter rolled out in beta
August: ChatGPT Enterprise. Prompt examples, upload multiple files and custom instructions.
September: new voice and image capabilities. Language support for 10 languages in alpha
October: files such as PDFs can be uploaded to work “chat” with them. Browsing is out of beta.
November: a flurry of announcements on
[OpenAI’s first Developer Day](https://substack.com/redirect/fdccd1cf-9fa8-4b25-b2a8-c42764b0c872?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), including an Assitants API, new models, a GPT models store, and[dozens more](https://substack.com/redirect/d69845fa-febe-4247-afc6-49b1c7d0235f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). We briefly covered Developer Day last week,[in The Pulse](https://substack.com/redirect/e47ed1b8-e3a8-4873-81d6-0007d3af38b8?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).
So, what is the engineering culture that allows the ChatGPT team to iterate this fast? Well, nobody outside of OpenAI really knows, as the company has never discussed its software engineering practices – until now.
In this exclusive interview with [Evan Morikawa](https://substack.com/redirect/08036a7c-24da-40e8-911a-7b801e6e8a52?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), who heads up about half of the 130-person Applied engineering team that builds ChatGPT, we find out how the hottest player in tech gets things done, and builds a winning product at the cutting edge of innovation.
We cover:
An introduction to ChatGPT, the Applied team, and Evan
Operating like an independent startup
Tight integration with Research
Long-term Product and Research thinking
Uncoupled and incremental releases
High talent density
Day-to-day habits that add up
The road ahead
This article is an engineering culture deep dive. [Read other deep dives we’ve previously covered](https://substack.com/redirect/7f41d5a2-e283-417f-8ff8-c7424a735649?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) with companies like Figma, Linear, Amazon, Meta or Sourcegraph.
With that, it’s over to Evan. My questions are in italic:
Evan, can you introduce OpenAI and yourself?
OpenAI is the maker of ChatGPT. Hopefully you've used ChatGPT to learn something new, help you write, or just chat with it for fun. ChatGPT is just one of OpenAI's products – OpenAI also shipped things like [DALL·E 3](https://substack.com/redirect/d07064f9-a27b-47d7-a47c-40ef74fb6f20?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) (image generation), [GPT-4](https://substack.com/redirect/0b763ab7-d3f4-428a-ac5e-85e6c3497392?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) (an advanced model) and the [OpenAI API](https://substack.com/redirect/59c3b03a-f05c-436a-8b94-4140f46ac1d2?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) (which developers and companies use to integrate AI into their businesses.) ChatGPT and the API each expose several classes of models named GPT-3, GPT-3.5, and GPT-4.
The engineering, product, and design organization that makes and scales these products is called "Applied". OpenAI is [charted](https://substack.com/redirect/c84eb42a-0fc8-4107-99e5-ea73a51282f0?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) with building safe AGI that is useful for all of humanity. Applied is charted with building products that really make AI useful for all of humanity. Research trains big models, then Applied builds products like ChatGPT and the API on those models. In practice, it's a more tightly integrated back and forth which I'll talk more about later.
The Applied team is a fairly new addition within the company. OpenAI was founded in 2015, and Applied began in the summer of 2020. We formed this team because we wanted to build and scale an API around GPT-3, which was a model we had just finished training, back then.”
How did you come to head up a large part of OpenAI’s Applied team?
I joined OpenAI in October 2020. Back then, OpenAI had about 150 staff in total, and the Applied team was a handful of people. At the time, nearly everyone working at OpenAI was a researcher. I do not have a PhD in Machine Learning and was excited by the realization that OpenAI was building APIs and engineering teams.
At OpenAI, I started out writing code as an individual contributor for the GPT-3 API. In January 2021, a few months into my tenure, I transitioned into managing our Applied Engineering team. Back then my team consisted of about 6 people. Today, two and a half years later, the Applied Engineering team has grown to 130 engineers, of whom I manage about half. The full Applied group consists of about 150 people; the other 20 folks are PMs and designers.
Since October 2020, OpenAI has grown from around 150 to roughly 700 people, today. And we [keep on hiring](https://substack.com/redirect/d67ff1e3-989f-4e73-b7e7-25994423989e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).
How does OpenAI ship as quickly as it does? I feel like there’s a major new feature launched every couple of months. As an outsider, it’s hard enough just to keep up!
On one hand, this has definitely been the [highest velocity place](https://substack.com/redirect/bef5c241-eb0e-4861-aad3-8e303c70080d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) in my career; but on the other hand, it's not magic. I think the key has been:
Setting up ChatGPT to operate like a small independent startup
Tight integration with research
Long-term product & research thinking
Uncoupled, incremental releases
High talent density
Day-to-day habits that all add up
You mentioned how ChatGPT operates independently. What’s the setup?
ChatGPT looks, feels, and acts like a one-year-old startup, but OpenAI itself is nearly 8 years old. The Applied group within OpenAI was founded 3 years ago. ChatGPT is a product team within Applied that started about 1 year ago.
I and the rest of Applied leadership wanted the ChatGPT team to feel like they are their own, independent startup. In practice this goal involved a lot of changes which evolved as the team grew.
In the summer of 2022, we began development of what would become ChatGPT. At that time, Applied had about 30 engineers, a handful of PMs and designers, and was running products like:
APIs for GPT-3 and Codex
Fine-tuning of models
Embedding APIs
DALL·E 2
All these products used the same codebase, ran in the same cluster, and used the same build pipelines. Within Applied, we were structured functionally; engineering was one unified team.
This changed with ChatGPT.
A few applied engineers, some designers, researchers, and Greg Brockman (OpenAI's president and co-founder) grabbed a room and started rapidly iterating product ideas.
We gave this nascent group its own code repository and a fresh cluster. The dev environment looked like the first days of a startup or a personal project.
Our goal with this small ChatGPT subteam was to create the atmosphere of an early-stage startup iterating towards product-market fit (PMF.) We wanted to foster the rhythm, pace, and autonomy to do this. Every member of the team was on-site, and we rearranged seating to put people next to each other.
As the ChatGPT team grew, we made sure to keep it vertically integrated. This meant engineering, product, design, and key researchers always worked closely together. We codified that pattern further in May 2023 when [Peter Deng](https://substack.com/redirect/c259be99-e645-4e45-ad33-62334a584b8a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) joined to lead ChatGPT engineering, product, and design, as one cohesive group.
We knew to set ChatGPT up this way because we’d created a similar structure when the Applied team started work on the first version of the OpenAI API. Three years ago, we also started with a handful of engineers on a fresh repo, fresh cluster, and greenfield development. We also operated like an early-stage startup searching for PMF, and found it with the API product.
This “fractal startup” approach feels like a good model for any new product category. I expect we’ll continue applying this pattern to rapidly iterate new ideas which we consider pursuing.
How important is tight integration with Research, and why does it matter?
In most tech companies, the “classic” trio of teams that engineering works with tends to be referenced as “EPD”:
Engineering
Product
Design
These teams tend to collaborate heavily with one another, and cross-functional teams usually have members of engineering, product, and design within them.
Research being integrated into product teams has been critical. Instead of the classic “EPD,” I like to think of our unit that collaborated heavily as “DERP”:
Design
Engineering
Research
Product
At OpenAI, many product questions are actually research ones. For example, take these questions, that could be seen as feature requests:
How can ChatGPT produce more concise outputs?
How can ChatGPT produce more accurate answers?
How can ChatGPT connect to additional data sources?
While these questions might feel like product questions, in reality they’re heavily dependent on research. How can underlying models be tweaked or fine-tuned for the desired goals, what other approaches could we take to achieve these outcomes?
Researchers integrating with product engineering wasn’t always a given. At OpenAI, Research and Applied are separate org structures. Within the Research organization, there are a variety of different research teams, such as:
Pre Training team: this team trains the GPT-4 model
Post Training team: they fine-tune GPT-4
[Superalignment team](https://substack.com/redirect/4ed9daed-bc82-4525-8620-1035571ef676?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o): aligns GPT-4Multimoda team: makes GPT-4 see, hear, and speak
… and several others!
Researchers tend to have significant academic or industry backgrounds. They read a lot of academic papers to stay up to date. They also take ideas and run lots of experiments to improve our models. They are all hands-on; researchers do a lot of engineering and write a ton of code!
We could have chosen the approach where models are “thrown over the wall” to Applied. This setup would have meant that Research trains a model, and then hands it over – aka throws it over the wall – for Applied to productize. However, we actively wanted to avoid a culture where Research is only focused on running experiments and Product just wants to commercialize and make money.
To prevent this, product teams like ChatGPT have software engineers, designers, product managers, and researchers working together. In the case of ChatGPT, most researchers came from a research team we call Post Training. These researchers are the masters of the latest fine-tuning techniques and [reinforcement learning](https://substack.com/redirect/1bb7f5c6-db3f-4a4e-ad3f-f5a02d6902f5?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) (RL) methods like [Proximal Policy Optimization](https://substack.com/redirect/8d06712b-d162-461e-9577-142daaf91990?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) (PPO.) Those techniques are necessary to continuously improve the underlying models in ChatGPT. Thanks to these researchers being part of the product group, and running their own A/B experiments, the feedback loop between research and engineering is very tight.
Tight coupling with Research is why we ship new ideas so quickly. How did we ship features like browsing, code execution, plugins, and other ChatGPT features as quickly as we did? It’s because of tight integration! All these started as research ideas, and were deployed into production quickly because the teams doing the research are tightly integrated with engineering! Furthermore, there's a culture of tinkering and prototyping in both research and applied. A lot of those prototypes very quickly found their way to prod.
How does thinking long-term help with execution?
OpenAI's mission is to ensure that artificial general intelligence (AGI) benefits all of humanity. By AGI, we mean highly autonomous systems that outperform humans at most economically valuable work. This mission is captured within the [OpenAI Charter](https://substack.com/redirect/c84eb42a-0fc8-4107-99e5-ea73a51282f0?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) document. The Charter document reflects the strategy of OpenAI in more detail; for example, detailing the focus on long-term safety.
Our Charter and Mission are referenced at almost every all-hands. We've tactically used the phrase "which of these options feels like it's getting us closer to AGI" – referring to our Mission – in product discussions. It not only helps decide what to build, but I’ve seen plenty of decisions to not build things, as a result of focusing on the mission.
Clear focus is always a driver of velocity. I’m convinced our broad mission has helped keep that focus and also pave the way for lots of new ideas.
Another thing that has helped us is how we organize research initiatives:...
Become a paying subscriber of The Pragmatic Engineer to get access to this post and other subscriber-only content.
| Full articles every Tuesday and Thursday | |
| Access to resources and templates for engineering managers and engineers | |
| Access to the complete archive, see all comments and comment on articles |