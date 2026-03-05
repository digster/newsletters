---
subject: "How Shopify Built Its Live Globe for Black Friday"
from: "The Pragmatic Engineer <pragmaticengineer+deepdives@substack.com>"
to: ""
date: 2024-12-17 17:17:03
labels: ["CATEGORY_PERSONAL", "INBOX", "The Pragmatic Engineer", "UNREAD"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_6413324878686416177", "UNREAD"]
---
👋 Hi, this is Gergely with a subscriber-only issue of the Pragmatic Engineer Newsletter. In every issue, I cover challenges at Big Tech and startups through the lens of engineering managers and senior engineers. If you’ve been forwarded this email, you can
|
Black Friday and Cyber Monday (jointly known as “BFCM”) are when e-commerce businesses make the most money in the year: up to 10x more than any other day. Obviously, this means the period is extremely important for:
E-commerce platforms like Shopify, Amazon, and others
Payment providers like Stripe, Adyen, Block, and others which process far more payments than usual
High street and online retailers that receive more inquiries than usual
Delivery services that transport orders from e-commerce companies and face delivery challenges
Shopify is one of the biggest challengers in the e-commerce segment, and is unusually transparent about what happens on its platform on BFCM. For a few years now, the company [has made](https://substack.com/redirect/5e24f478-4425-412c-adc7-9cd45fd898f3?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) a special “Black Friday Cyber Monday” portal for anyone to inspect, and the latest one is a pretty mesmerizing visual experience: in real time, you can inspect sales and software engineering stats like database queries and edge requests per minute, in a fun, interactive spaceship environment.
I reached out to Shopify to find out how they built their interactive dashboard. We talked with BFCM tech lead, [Daniel Beauchamp](https://substack.com/redirect/3a46042f-6b99-4091-a5ff-9508373d58f9?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), and head of engineering, [Farhan Thawar](https://substack.com/redirect/c16a906c-6d84-4f0a-940a-33bf9f838c7a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), who shared plenty of new details. This article covers:
Kickoff. Background of “Live Globe,” and how it began with a 2 month deadline and a team of 6.
Design process. From idea, through design inspiration and prototypes, to the final version.
Stats. Business and infrastructure details about Shopify’s Black Friday traffic. At peak, the platform had nearly 30M database reads and 3M writes per second; all served with a Ruby on Rails backend.
System architecture. Relatively straightforward, with a React SPA app, a Go event server, and a custom data pipeline.
Tech stack. React Three Fiber, server-sent events, Go, Rails, Kafka and Flink.
Easter eggs. A music synthesizer that sends music to instruments, a bobblehead, an emergency shutdown sequence, and the whole thing broadcast live on new Last Vegas landmark, The Sphere.
Building it. The challenge of the annual project, optimizing performance, handling oncall, and the question: “what’s the ROI?”
Check out related articles:
[Shopify’s ‘mastery’ framework](https://substack.com/redirect/c5a0f5d9-28c8-4545-80c0-cf8d2212d68a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o): a new approach to career growth and promotions. More details about how this change started in[Inside Shopify’s leveling split](https://substack.com/redirect/e1b9c3a2-82e6-4ed7-adbe-30c4c8601a55?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).[The Tech Behind Stripe’s Realtime Cyber Monday Dashboard](https://substack.com/redirect/1834234e-2bdf-4181-954b-8bd3f2a5e170?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o): an overview into how Stripe built its dashboard in 2023[Other real-world engineering challenges](https://substack.com/redirect/29cc702b-447f-4dca-84d1-c5793d054c21?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), similar to this deepdive
The bottom of this article could be cut off in some email clients. [Read the full article uninterrupted, online.](https://substack.com/redirect/0a66ebeb-623d-4fde-8005-f4b9c2aa7a32?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
With that, let’s jump in:
Shopify has been running an internal Black Friday / Cyber Monday live dashboard since 2014. Initially, it served as a way to track what was happening on important days for the business. And since 2018, the company has made a version of its “Globe” available to the world
Here’s what the 2023 version looked like:
The Shopify team previously shared details on [how they built the 2023 version](https://substack.com/redirect/c14377a2-5530-4f4d-9b5e-38268abe81f8?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).
Daniel Beauchamp is a principal engineer for AR/VR at Shopify, and has headed the Live Globe project for the past few years. He says that this time, they wanted to make it more special than ever:
“The Live Globe has become a tradition at Shopify, even “just” as a sphere with some arcs showing orders being made in real time, and some additional touches to make it more jazzy.
A big learning last year was that visitors love an easter egg. The easter egg was called “airplane mode”; when you switched it on, instead of just seeing the globe with arcs representing orders, you kind of zoomed in as if flying a little plane, and the plane circled the Earth while the arcs zoomed around you. There were also fireworks, each one representing a merchant’s first sale of the period.
When we built this easter egg, we assumed a few people might find it and smile. Instead, it was what people talked about and shared the most!
We wondered why this feature was so liked and realized that while the Live Globe tells the story of entrepreneurship and of Shopify, these fun and delightful moments are really important for people. We took this learning and wrapped it away for the next iteration.
Early this year, we decided that we wanted to take the Live Globe to the next level. Within Shopify, usually all projects have concrete, measurable goals that make the project a success. In the case of the Live Globe 2024 project, the only success metric defined was to make it as fun as possible”.
With 6 people and 2 months to achieve that this year, the site was rebuilt from scratch. The team consisted of two software engineers, one 3D artist, and three data engineers, plus a few folks helping out with SEO and some design/logo work.
The Live Globe works very well from a user’s point of view because it’s visually appealing, set inside a spaceship near a cabin window. So how was this project designed?
Daniel – the project lead – has a long interest in 3D games and programming, and became the go-to person for all things 3D at Shopify. In 2015, he launched an augmented reality (AR) team in the company. The team’s mission was to make Shopify spatially enabled, and enable merchants to use 3D, VR, or AR. It was natural for this team to be involved in the initial versions of Live Globe, and they drive major updates for the project.
As a start, the team explored different concepts of globes and futuristic environments, merged with retro car dashboards. They collected dashboards and panels from the interiors of spaceships in the Alien movie franchise:
There were also futuristic, functional engineering concepts by hardware maker [Teenage Engineering](https://substack.com/redirect/1fd3f0ba-23cf-4cd4-aea1-222ae72086aa?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), and designer, [Peter Tarka](https://substack.com/redirect/60f7cadf-4af6-4b1f-b6e4-7d9e8c354aff?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o):
AI concept art was also employed, using image generation models to create graphics for the creative process:
And some concept art for the UI was AI-generated:
Then the team started creating 3D model prototypes. During this phase, they had to figure out two things:
#1: Appearance of the Globe. As the centerpiece of the experience, it matters what the globe looks like. Here are some prototypes of the globe and its environment:
The team spent a lot of time honing the appearance. The globe has a glass-like visage and oscilloscopic lines. Initially, the team added topological features, but those didn’t make the final version.
#2: Environment and interactions. With the globe design finalized, the next challenge was to create the environment it exists in, and figure out what visitors could do beyond interacting with the globe. Prototype versions of the environment:
And here’s what one of the final prototypes looked like:
The prototypes had a lot of detail, much of which ended up being stripped out. When prototyping, the team wanted to see how much they could cram into the user interface and what that was like for users.
During the development process, the team removed details that were distracting, like too many wires, screens or buttons, and parts with no function. After plenty of refinement, they achieved the final design:
The functional goal of the site was to share real time statistics on the load that Shopify’s platform was handling during BFCM. Below are some numbers from that weekend.
$108: the average order size during BFCM.
76M customers: the number of people purchasing from a Shopify-powered store
91M: packages sent and tracked in Shopify’s Shop App
$4.6M per minute: peak sales processed by the platform. This happened at midday EST on Black Friday (29 November)
$11.5B: sales on the platform during the 4-day period; around half of the annual GDP of a country like Albania ($23B
[in 2023](https://substack.com/redirect/1a33dc64-033e-4466-a729-fc0302d79a2f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)), and 24% more than during the same period in 2023.
Here are some peak load figures that might interest engineers:
2.4M CPU cores across Kubernetes operated at peak load. Shopify relies on Google Cloud as their cloud partner, so it’s safe to assume most CPU cores were spun up as virtual ones from Google Cloud regions and zones.
45M database queries per second (QPS): peak database queries, and 1.4 billion row operations per second. Over the 4 days, 10.5 trillion (10,500 billion) queries were served. This is an extremely high load! Shopify used MySQL 8 as their database technology.
3M database writes per second. Shopify had a roughly 10:1 database read/write ratio during this time, and a total of 1.17 trillion database writes in this period, compared to 10.5 trillion database reads. From the data, we can assume peak database write was around 3M QPS. Database writes are more resource intensive than reads, so the infra team had their work cut out to handle this load smoothly.
Edge: 4.7M RPS (requests per second) at peak (284M edge requests per minute). The total was 1.19 trillion (1,190 billion) edge requests over 4 days.
[Edge computing](https://substack.com/redirect/88bb9160-63b7-45bb-8049-29292aecea7c?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)means optimizing request response time by serving requests on nodes close to the user; it can be thought of as a kind of smart caching. Edge computing is becoming increasingly important with large-scale, frontend applications.CDN: 2.1M RPS at peak (128M requests per minute). 97% of CDN requests were served from cache, which is a win-win: faster responses for customers, and less resource strain on Shopify’s servers.
App servers: 1.3M RPS at peak (80M request per minute). This stat shows that while Edge was able to absorb most of the load, the backend infra still needed to handle a fair amount!
Client connections: 1.9M per sec at peak (117M per minute): the number of new client connection requests initiated to the backend, coming from websites or apps.
Data: 200GB/sec pushed: pushed at peak to clients (12 TB per minute). A total of 57PB data was pushed over 4 days.
1.1M Kafka messages/sec at peak (66M per minute.) Kafka messages are the lifeblood of communication across systems within Shopify, and used by the Live Globe, as covered below.
Logs: 108GB/sec logged at peak logged (6TB per minute); a huge amount of logging happening across Shopify’s systems!
Caching: 145M/sec commands sent at peak in caching commands (8.7B per minute)
These numbers are truly impressive and require significant infrastructure to serve reliably. It’s safe to assume they set new records at Shopify. It’s also safe to assume they might become “business as usual” if the platform keeps growing.
Finally, I asked the Live Globe team about stats on the microsite that updated in real time during BFCM. Some details:
271,620: visitors over the 4 days
140,325: times the ship’s gravity was turned off, causing objects to float
81,089: times that bobblehead was bobbled
78,425: times the emergency shutdown switch was turned on, which should have self-destructed the ship!
75MB per second: data processed by Flink to serve the Live Globe
Compared to the Shopify platform, the load on Live Globe was trivial; the challenge was not in keeping up with demand, it was building all the features on time and ensuring the data was streamed in as close to real time as possible.
Become a paying subscriber of The Pragmatic Engineer to get access to this post and other subscriber-only content.
| Full articles every Tuesday and Thursday | |
| Access to resources and templates for engineering managers and engineers | |
| Access to the complete archive, see all comments and comment on articles |