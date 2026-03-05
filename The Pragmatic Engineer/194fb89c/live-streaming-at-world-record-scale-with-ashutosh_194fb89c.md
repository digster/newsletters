---
subject: "Live streaming at world-record scale with Ashutosh Agrawal"
from: "The Pragmatic Engineer <pragmaticengineer@substack.com>"
to: ""
date: 2025-02-12 19:00:50
labels: ["CATEGORY_PERSONAL", "INBOX", "The Pragmatic Engineer", "UNREAD"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_6413324878686416177", "UNREAD"]
---
|
Available now on [YouTube](https://substack.com/redirect/79e63d8e-2681-4e5c-b339-6646120e34d6?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), [Apple](https://substack.com/redirect/efb14b4a-044e-48f8-85e3-3afedb4e0fd8?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) and [Spotify](https://substack.com/redirect/8ae93a7f-c714-47bf-ad0c-26e2766f8197?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). See the episode transcript at the top of this page, and a summary at the bottom.
• [WorkOS](https://substack.com/redirect/3817bd2c-afc6-4eef-a3dd-14ff04084255?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) — The modern identity platform for B2B SaaS
• [CodeRabbit](https://substack.com/redirect/20a9f453-cd3b-4839-a6d6-73b2840a1c5e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) — Cut code review time and bugs in half
• [Augment Code](https://substack.com/redirect/3cc2049d-86d2-4662-a111-5b68f4efb45c?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) — AI coding assistant that pro engineering teams love
—
How do you architect a live streaming system to deal with more load than any similar system has dealt with before? Today, we hear from an architect of such a system: Ashutosh Agrawal, formerly Chief Architect of JioCinema (and currently Staff Software Engineer at Google DeepMind.) In May 2023, JioCinema set the live-streaming world record, serving 32 million concurrent viewers tuning in to the finale of Indian Premier League (a cricket game.)
We take a deep dive into video streaming architecture, tackling the complexities of live streaming at scale (at tens of millions of parallel streams) and the challenges engineers face in delivering seamless experiences. We talk about the following topics:
• How large-scale live streaming architectures are designed
• Tradeoffs in optimizing performance
• Early warning signs of streaming failures and how to detect them
• Why capacity planning for streaming is SO difficult
• The technical hurdles of streaming in APAC regions
• Why Ashutosh hates APMs (Application Performance Management systems)
• Ashutosh’s advice for those looking to improve their systems design expertise
• And much more!
My biggest takeaways from this episode:
1. The architecture behind live streaming systems is surprisingly logical. In the episode, Ashutosh explains how the live streaming system works, starting from the physical cameras on-site, through the production control room (PCR), streams being sliced-and-diced, and the HLS protocol (HTTP Live Streaming) used.
2. There are a LOT of tradeoffs you can play with when live streaming! The tradeoffs between server load, latency, server resources vs client caching are hard decisions to make. Want to reduce the server load? Serve longer chunks to clients, resulting in fewer requests per minute, per client… at the expense of clients potentially lagging more behind. This is just one of many possible decisions to make.
3. At massive video streaming scale, capacity planning can start a year ahead! It was surprising to hear how Ashutosh had to convince with telecoms and data centers to invest more in their server infrastructure, so they can handle the load, come peak viewership months later. This kind of challenge will be nonexistent for most of us engineers/ Still, it’s interesting to consider that when you are serving a scale that’s not been done before, you need to worry about the underlying infra!
4. “Game day” is such a neat load testing concept. The team at Jio would simulate “game day” load months before the event. They did tell teams when the load test will start: but did not share anything else! Preparing for a “Game day” test is a lot of work, but it can pay off to find parts of the system that shutter under extreme load.
• [Software architect archetypes](https://substack.com/redirect/db66a48c-37dd-4943-abd5-136f27fdfe9f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• [Engineering leadership skill set overlaps](https://substack.com/redirect/e8176195-a516-4ab0-962a-88b4ec855972?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• [Software architecture with Grady Booch](https://substack.com/redirect/a8ca8915-35d4-4b63-a79c-e05bab444f54?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
([00:00](https://substack.com/redirect/b00a2d73-398f-475d-9341-aec402e7ff8a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Intro
([01:28](https://substack.com/redirect/e4460c65-64ed-4823-9e7d-5968f50eb44f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The world record-breaking live stream and how support works with live events
([05:57](https://substack.com/redirect/d3b60851-3b5f-4797-9823-5c850ee87bb0?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) An overview of streaming architecture
([21:48](https://substack.com/redirect/375642b8-122d-4b0c-a565-9db257bb4128?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) The differences between internet streaming and traditional television.l
([22:26](https://substack.com/redirect/a54ba481-ed49-4106-9ec9-929abfbae05b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) How adaptive bitrate streaming works
([25:30](https://substack.com/redirect/9a143a20-0462-4f25-84b0-90338d505a68?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) How throttling works on the mobile tower side
([27:46](https://substack.com/redirect/273b5253-c4fd-4e42-89cd-d28f245ce762?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Leading indicators of streaming problems and the data visualization needed
([31:03](https://substack.com/redirect/4e143cea-24ca-4fc3-bde4-0d38513bddc3?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) How metrics are set
([33:38](https://substack.com/redirect/95196fa8-d07e-4c25-9d0c-8a52828b4f01?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Best practices for capacity planning
([35:50](https://substack.com/redirect/ca3c65b6-9694-48cb-b624-bee5c3f65fdb?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Which resources are planned for in capacity planning
([37:10](https://substack.com/redirect/4ed50b61-b7eb-4e99-85c1-cd56fd1ca74f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) How streaming services plan for future live events with vendors
([41:01](https://substack.com/redirect/0ca69ee4-aefb-40b0-b55c-b881983f7d1d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) APAC specific challenges
([44:48](https://substack.com/redirect/7eb5b15f-5ea6-44a9-b0e0-0dd7dd63bf39?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Horizontal scaling vs. vertical scaling
([46:10](https://substack.com/redirect/859966e1-ddbf-43b5-80dc-d2f5b0fb985c?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Why auto-scaling doesn’t work
([47:30](https://substack.com/redirect/cc28af97-aac5-4eed-89ee-9c5b66e43e72?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Concurrency: the golden metric to scale against
([48:17](https://substack.com/redirect/2e60c3ee-157d-42a3-ab53-f697c7a782fa?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) User journeys that cause problems
([49:59](https://substack.com/redirect/ea982b79-40dd-4114-88b2-0d54d9714a06?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Recommendations for learning more about video streaming
([51:11](https://substack.com/redirect/1c6072f2-34ce-4be8-a8f0-b9b46e4703a4?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) How Ashutosh learned on the job
([55:21](https://substack.com/redirect/d2dac52a-6a9f-492d-b9f2-b432afb28bd6?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Advice for engineers who would like to get better at systems
([1:00:10](https://substack.com/redirect/8579b486-d00c-40c0-b8e5-9b43a0654a42?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)) Rapid fire round
The journey of a live stream starts with the cameras at the event’s venue. These cameras are connected by fiber to a Production Control Room (PCR).
In the PCR, a director selects which camera feeds to use, much like in a movie production.
Source feed (or production feed) is then sent to a contribution encoder. This encoder compresses the high-bandwidth source feed to a more manageable size.
The compressed feed is then transmitted to the cloud using a private peer-to-peer link.
Distribution encoder: prepares the stream in various formats for end-user consumption, such as HLS and DASH.
Over 100 stream variants can be generated for various devices – and up to 500 (!) when different languages are included.
Orchestrator: the one managing the pipeline, from the contribution encoding to the cloud infrastructure. The orchestrator decides which endpoints to push to, the configuration of the distribution encoder, and the CDN endpoints.
Playback URLs: generated by the orchestrator. URLs are specific to the device and format being used.
When a user clicks play, a separate playback system takes over. This system verifies user authorization, deals with encryption, and handles Digital Rights Management (DRM). The playback system then provides the client app with an encrypted URL to stream the content.
Live streaming systems are more complex than Video on Demand (VOD) systems because of the need to manage multiple real-time streams and user authentication and authorization for those streams, all while keeping latency low.
Content delivery relies on Content Delivery Networks (CDNs).
The core technology used is HLS or DASH, where the video is broken down into segments.
HLS uses a master manifest file (e.g., master.m3u8) that lists different video quality levels. Each quality level refers to a child manifest.
Child manifests list individual video segments. These segments are typically between four to six seconds long.
The client player requests a child manifest every segment duration and the segments that it lists.
CDN: works at the segment level rather than at a millisecond level.
Correctly setting up CDN configurations, such as the Time To Live (TTL) values for the cached segments, is crucial to ensure a smooth stream without stale data.
Latency is introduced at various stages of the live-streaming process. This includes encoding, network transmission, and client-side buffering.
Encoding techniques: using a look-back period, or Group of Pictures (GOP) are used to achieve more efficient compression. The GOP might be 1, ,2 or 4 seconds long.
Client-side buffering is used to give a smoother streaming experience, even if there are small network issues. This means the user might be watching the stream a few seconds behind the real-time live point.
There are trade-offs between latency, smooth playbac,k and infrastructure demands. Reducing the segment duration increases calls to the CDN, impacting infrastructure needs.
Adaptive bitrate streaming is used to adjust the video quality in response to the user's network conditions.
The client-side player measures the download speed and chooses an appropriate video quality level, matching the user's network capacity.
If the network speed slows down, the client can switch to a lower-quality video (e.g., from 720p to 240p).
The server can also degrade the user's stream by limiting the number of available video quality options, for example during very high load. The server can also adjust the segment length in response to system load.
The client player is always starting playback a few seconds behind the live point, to avoid any interruption in playback if a segment is missed.
If a segment is missed on a TV, the TV will continue playing at the live point. However, on the internet, the client is using a buffer and will try to avoid missing a segment.
Monitoring is based on leading and trailing indicators.
Leading indicators help to identify potential problems in realtime. Examples include buffer time and playback failure rates. These leading indicator metrics are given priority in the system.
Trailing indicators are used to perform a detailed analysis of issues after they occur.
Client-side metrics are collected and quickly processed by the server in less than a minute or sometimes within 30 seconds.
Server-side metrics, such as bandwidth, the number of requests, and latency, are also tracked.
The frequency of data collection is adjusted based on the system load. When there is higher traffic, the amount of data collected is sampled to manage the volume of data collected and processed.
Capacity planning is a very complex process involving infrastructure, network, and power, and is started at the end of the prior year, for the next year.
Capacity planning involves coordination with several infra providers to make sure they can scale their infrastructure for the events.
The planning focuses on metrics such as compute, RAM, disk, and network usage. The main metric that becomes the limiting factor is vCPUs.
Cloud resources are not infinite at the scale required for major live events. There is a finite amount of resources in a given location – at this scale of streaming, that is!
Providers need to purchase real estate, install links, and deploy servers.
Horizontal scaling is preferred for compute resources as it is easy to add boxes to the pool.
Databases and caches are scaled preemptively to avoid the need to scale them on the fly during events.
Auto-scaling is not effective for live events because it is too slow to respond to the rapid changes in traffic. Custom scaling systems are preferred.
The custom scaling system uses a concurrency metric, that is the number of users watching the stream, to scale services. All systems are scaled against a common concurrency metric.
The custom scaler also looks at user journeys, such as when users press the back button and return to the home page. This can cause a spike in traffic to the home page API.
Mobility is a significant challenge because most users in India watch live streams on mobile devices and are often on the move. This means that users are constantly switching between cell towers.
Battery consumption is also a key factor. Video streaming can quickly drain mobile phone batteries.
The video profile, polling frequency, and encoding algorithms are often chosen to reduce battery consumption.
“Game day simulation”: something Jio did to simulate peak load conditions.
Involved in generating synthetic traffic and the teams needed to scale systems and follow operational protocols in response.
The teams did not have access to the traffic dashboard, so the traffic patterns were unknown to the teams.
Understand this: anything that can fail, will fail. Overconfidence in systems can lead to problems! Most people underestimate or overlook the potential failure modes.
Look at every aspect of your system including configurations and code as even the smallest things can cause problems.
Detailed metrics and measurements are vital. Both to see potential problems and to be able to debug effectively.
Ensure you are measuring metrics correctly. For example, response time should be measured from when the request is queued, not when it enters the processing function.
Do not rely too heavily on APMs. It is better to understand the low-level details and measure and fine-tune every aspect of your code.
To learn more about video encoding: look up documentation on GitHub and online. Look for resources going into how image compression is done, and how images are turned into video.
Most of the learning happens on the job. There isn't a lot of public information about problems at this kind of scale! Hopefully, this podcast was helpful in sharing more details!
Where to find Ashutosh Agrawal:
• X: [https://x.com/theprogrammerin](https://substack.com/redirect/31be5513-2317-476a-9f78-aded2192e822?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• LinkedIn: [https://www.linkedin.com/in/theprogrammerin/](https://substack.com/redirect/211ee499-868a-4cb7-a155-ae4c9040e3fc?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Medium: [https://medium.com/@theprogrammerin](https://substack.com/redirect/1440dd94-15c6-44c0-ac27-3b0f800feeb0?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
Mentions during the episode:
• Disney+ Hotstar: [https://www.hotstar.com/in](https://substack.com/redirect/c15dd1c0-bf11-4f87-b39d-7f2b738152ed?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• What is a CDN: [https://aws.amazon.com/what-is/cdn/](https://substack.com/redirect/17264e86-cf2c-458e-b348-60bbee18f81e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Adaptive bitrate streaming: [https://en.wikipedia.org/wiki/Adaptive_bitrate_streaming](https://substack.com/redirect/022b7ce8-0666-40a9-92fb-26e4853a7b0a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Skype: [https://www.skype.com/en/](https://substack.com/redirect/ed458cfd-73ca-45ba-88bf-d920ef20b942?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
•Millions Scale Simulations: [https://blog.hotstar.com/millons-scale-simulations-1602befe1ce5](https://substack.com/redirect/f2f14647-6ca2-4673-95e3-2e39826d2b5c?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Black Friday: [https://en.wikipedia.org/wiki/Black_Friday_(shopping)](https://substack.com/redirect/af75fecb-184b-4526-b61f-37416d0407c3?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Asia-Pacific (APAC): [https://en.wikipedia.org/wiki/Asia%E2%80%93Pacific](https://substack.com/redirect/4fb93592-0a64-455d-b9e5-46db809409b9?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Distributed architecture concepts I learned while building a large payments system: [https://blog.pragmaticengineer.com/distributed-architecture-concepts-i-have-learned-while-building-payments-systems/](https://substack.com/redirect/5db39ed6-b064-4219-862c-aad2f090f946?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Concurrency: [https://web.mit.edu/6.005/www/fa14/classes/17-concurrency/](https://substack.com/redirect/254f0414-ff30-42c4-a443-128435596ea9?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Video streaming resources on Github: [https://github.com/leandromoreira/digital_video_introduction](https://substack.com/redirect/25f91cf1-6283-4a09-9d2d-3125e7f96cd7?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Murphy’s Law: [https://en.wikipedia.org/wiki/Murphy%27s_Law_(disambiguation)](https://substack.com/redirect/17f91410-adb5-4c6e-9373-bc4a58e42ba1?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Java: [https://www.java.com/](https://substack.com/redirect/8adf89a1-ae09-475f-bed9-800a4fce72c8?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Ruby: [https://www.ruby-lang.org/en/](https://substack.com/redirect/a800b506-acca-47f6-90e2-d6eb1b16c7e0?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Ruby on Rails: [https://rubyonrails.org/](https://substack.com/redirect/2acac85c-5a35-4678-83ff-1c36fe6d1fbe?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
• Hacker News: [https://news.ycombinator.com/](https://substack.com/redirect/35284c66-f094-406c-9e66-9cf474f43114?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
—
Production and marketing by [Pen Name](https://substack.com/redirect/0acd4b82-bd35-4fa9-9856-7bf6b4e9692b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). For inquiries about sponsoring the podcast, email podcast@pragmaticengineer.com.
You’re on the free list for [The Pragmatic Engineer](https://substack.com/redirect/2/eyJlIjoiaHR0cHM6Ly9uZXdzbGV0dGVyLnByYWdtYXRpY2VuZ2luZWVyLmNvbT91dG1fY2FtcGFpZ249ZW1haWwtaG9tZSZyPThvNTRuIiwicCI6MTU2OTc0MzczLCJzIjo0NTg3MDksImYiOnRydWUsInUiOjE0NTYzMzE5LCJpYXQiOjE3MzkzODY4OTksImV4cCI6MTc0MTk3ODg5OSwiaXNzIjoicHViLTAiLCJzdWIiOiJsaW5rLXJlZGlyZWN0In0.7lHbkp4W-bAkP4eNk6Sq_tH2d1TxdlEcKknEGfFtvtk?). For the full experience, [become a paying subscriber](https://substack.com/redirect/2/eyJlIjoiaHR0cHM6Ly9uZXdzbGV0dGVyLnByYWdtYXRpY2VuZ2luZWVyLmNvbS9zdWJzY3JpYmU_dXRtX3NvdXJjZT1wb3N0JnV0bV9jYW1wYWlnbj1lbWFpbC1jaGVja291dCZuZXh0PWh0dHBzJTNBJTJGJTJGbmV3c2xldHRlci5wcmFnbWF0aWNlbmdpbmVlci5jb20lMkZwJTJGbGl2ZS1zdHJlYW1pbmctYXQtd29ybGQtcmVjb3JkLXNjYWxlJnI9OG81NG4mdG9rZW49ZXlKMWMyVnlYMmxrSWpveE5EVTJNek14T1N3aWFXRjBJam94TnpNNU16ZzJPRGs1TENKbGVIQWlPakUzTkRFNU56ZzRPVGtzSW1semN5STZJbkIxWWkwME5UZzNNRGtpTENKemRXSWlPaUpqYUdWamEyOTFkQ0o5LjVrdk9rQlIzWFVvSXZheTF0R2tCNUFYcUxxMDJmUF9kbEhxV1ZfYmsxdzQiLCJwIjoxNTY5NzQzNzMsInMiOjQ1ODcwOSwiZiI6dHJ1ZSwidSI6MTQ1NjMzMTksImlhdCI6MTczOTM4Njg5OSwiZXhwIjoxNzQxOTc4ODk5LCJpc3MiOiJwdWItMCIsInN1YiI6ImxpbmstcmVkaXJlY3QifQ.bplESnEGdGqTWXKXT8Jh9PA4_CIdA6oGQCHUeG7ovWw?). Many readers expense this newsletter within their company’s training/learning/development budget.
This post is public, so feel free to share and forward it.
If you enjoyed this post, you might enjoy my book, [The Software Engineer's Guidebook](https://www.engguidebook.com/). Here is what Tanya Reilly, senior principal engineer and author of The Staff Engineer's Path said about it:
"From performance reviews to P95 latency, from team dynamics to testing, Gergely demystifies all aspects of a software career. This book is well named: it really does feel like the missing guidebook for the whole industry."