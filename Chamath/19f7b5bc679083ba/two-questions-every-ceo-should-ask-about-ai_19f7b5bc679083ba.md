---
id: "19f7b5bc679083ba"
subject: "Two questions every CEO should ask about AI"
from: "Chamath Palihapitiya <chamath@substack.com>"
to: ""
date: 2026-07-19 15:06:35
labels: ["CATEGORY_PERSONAL", "Chamath", "INBOX", "UNREAD"]
label_ids: ["CATEGORY_PERSONAL", "Label_4017391144830520384", "INBOX", "UNREAD"]
---
|
As intelligence becomes abundant, knowing what questions to ask will matter more than ever.
This week, I want to share two: one I have discussed recently, and another that prompted some interesting responses from others (my What I Read This Week is still below).
If you find this useful, let me know in the comments, and we will do more every week.
As always, don’t just take my answers or anyone else’s. Think and then answer these questions for yourself.
Share your answer in the comments; we will repost the sharpest take.
Question 1) With massive AI bills hitting enterprises, how should companies think through maximizing ROI for their token costs?
Most CEOs and CFOs have no idea how much[ tokenmaxxing](https://substack.com/redirect/6545f81c-33ec-4191-8354-18bec9a0041c?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) is happening within their own companies, and it will show up in the numbers.
At 8090, my CTO told me our token costs are doubling roughly every 45 days, and the incremental productivity we get from that doubling is maybe 5-10% at most.
Now run that against a Fortune 500 company that said it is all in on AI. The spend can quietly compound inside OpEx, and suddenly a quarter gets missed by a few pennies of EPS. The CEO would ask the CFO where the money went, and they would likely trace it back to the $56-per-million tokens of intelligence, when a $0.50 version could have done the job.
So how do you not become that company?
First, stop paying for the flagship where you don’t need it. The cheap models are now 80% to 95% as good as the frontier models on most tasks. If Pepsi is a fraction of the price of Coke and tastes almost the same in the dark, you at least have to manage that as a risk. Pick the model per task, route it through a control plane that gives you optionality, and pay frontier prices only for the few jobs that genuinely need frontier intelligence.
Second, watch where your data goes. When you pipe your proprietary workflows and your competitive logic through a closed frontier model, you are renting intelligence and giving away your edge to providers that may also want to compete with you.
Measure the output you get, and treat intelligence like any other input cost.
Question 2) If every smart enterprise starts to pull its AI in-house to protect its edge, who’s left to pay for the $1.4T buildout?
Gavin Baker’s answer:
Replit CEO Amjad Masad’s answer:
|
1) Open-Weight AI Reaches the Coding Frontier
On July 16, Chinese lab Moonshot AI released Kimi K3, a 2.8-trillion-parameter model that[ took first place on the Frontend Code Arena](https://substack.com/redirect/6bfe4f9b-9a77-405e-895c-6bf8e58cf3d3?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), a leaderboard scored by blind developer votes on the web apps models generate. [K3 reached 1,679 points](https://substack.com/redirect/d2ed0cf6-4576-4948-8fc2-401b3327eb3e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), ahead of the closed flagships Claude Fable 5 and GPT-5.6 Sol, and led six of the seven frontend categories.
On broader intelligence tests it still trails both, but at $3 and $15 per million input and output tokens it undercuts Fable 5’s $10 and $50, and Moonshot plans to release the full weights by July 27, which would make it the largest open-weight model yet. Until then, every K3 spec is Moonshot’s own claim.
The same push is coming from US startups selling the means to build and own AI rather than rent it.
On July 15, Thinking Machines Lab, founded by former OpenAI CTO Mira Murati, released[ Inkling](https://substack.com/redirect/a48433e0-42b3-4a7c-93f2-078dd3d5446b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), its first model, with open weights under an Apache license that lets anyone download and modify it.
Inkling is a 975-billion-parameter mixture-of-experts model that activates only about 41 billion parameters per request, which makes it cheaper to run. Thinking Machines describes Inkling as a base for customization rather than the strongest model available, and its full weights are free to download. The company’s paid product is Tinker, a fine-tuning tool that adapts models to a customer’s data. [Bridgewater’s AIA Labs published a study](https://substack.com/redirect/e72cfb03-e6c4-468d-a85a-dc5e6ea2ee42?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) that used Tinker to fine-tune an open model for financial document triage. The custom version scored 84.7% accuracy, compared to 78.2% for the best frontier model tested, at roughly one-fourteenth of the cost per task.
A week earlier, on July 8,[ Prime Intellect raised a $130 million Series A](https://substack.com/redirect/01660347-b18a-43d1-a8fc-bfabbcdae7c5?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) at a $1 billion valuation. Prime Intellect rents decentralized computing and open-source software that let a company train its own agents, reporting a $100 million annualized revenue run rate. [A case study with Ramp](https://substack.com/redirect/2b0baea6-efdb-4529-8eb9-6bec1f2f21c1?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) showed their post-trained model beating Opus at spreadsheet search, and running 27% faster and far cheaper than Haiku.
2) Ex-SpaceX Engineers Raise $115M to Revolutionize Construction
On July 14, TerraFirma [raised about $115 million](https://substack.com/redirect/321528d6-a73d-4657-bc9b-dbc3baff523e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), including a $100 million Series A led by Kleiner Perkins, and said it will hire 300 people and build a Texas factory. It was founded in 2024 by former SpaceX engineers Noah Schochet and Noah McGuinness, who met at Princeton and worked on Starlink and Starship.
The company retrofits heavy construction machinery, such as excavators, dozers, and loaders, into robots that a skilled operator operates from a screen rather than climbing into the machine. Using an interface it calls[ “click to dig](https://substack.com/redirect/b0e305fc-f349-4db1-9abb-a864bb22a160?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)”, an operator sketches the required work as a 3D model in about 60 seconds, and the machine runs the task for more than 20 minutes on its own, with an Xbox controller kept as a manual backup. One operator can currently handle three to five machines, which TerraFirma says makes each operator up to 300% more effective and the work safer, since no one has to sit in the machine.
US construction labor productivity has[ fallen about 0.6% every year since 1965](https://substack.com/redirect/a3a0b298-d762-4424-aad9-c6aa60a87507?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) even as productivity across the broader economy has grown at roughly 1.6% annually. It’s estimated that the industry needs 349,000 more workers in 2026 just to keep pace. TerraFirma runs its own projects rather than selling the technology, which gives it live job sites and field data. The field is heating up as Caterpillar and Komatsu already offer remote control, and Bedrock Robotics raised $270 million to field operatorless excavators this year.
[Making Fable Cheaper Than Opus](https://substack.com/redirect/c7c84d71-b434-4b9e-ba7f-8a786c80d6d4?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)(Joon Lee)[You Just Hired a Million Bad Employees](https://substack.com/redirect/d67cfb18-ebf1-4289-8633-84bf733a00ae?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)(George Sivulka)[A Framework for Frontier AI and the Dawning of a New Age](https://substack.com/redirect/0932d04a-30ea-4ca1-9b63-5f28ff7d3499?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)(Demis Hassabis)[The Reverse Information Paradox](https://substack.com/redirect/4c9eaeac-0b32-492c-8854-74bfaaaf923b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)(Satya Nadella)
|
|
|
|
|
|
|
|
|
|