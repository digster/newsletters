---
subject: "An educational side project"
from: "The Pragmatic Engineer <pragmaticengineer+the-scoop@substack.com>"
to: ""
date: 2023-06-01 17:00:21
labels: ["CATEGORY_PERSONAL", "INBOX", "The Pragmatic Engineer"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_6413324878686416177"]
---
|
👋 Hi, this is [Gergely](https://substack.com/redirect/baa09a72-5986-4121-a975-d75444f35fa1?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) with a bonus, free issue of the Pragmatic Engineer Newsletter. We cover one out of four topics in today’s subscriber-only [The Scoop issue](https://substack.com/redirect/1bb4f9d5-905f-4039-822b-a256b783d5ab?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). If you’re not yet a full subscriber, you missed this week’s deep-dive on [Agoda’s private cloud setup](https://substack.com/redirect/179af736-0eb2-43a8-a2aa-9e23128b87c2?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). Subscribe to get the full issues, twice a week 👇
I’d like to share a story about an educational side project which could prove fruitful for a software engineer who’s seeking a new job.
[Juraj Majerik](https://substack.com/redirect/5a01026f-a09f-4c26-ac70-c675a265e779?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) is an Amsterdam-based software engineer who decided to improve his applied knowledge of containerization, multiprocessing and observability. So he built a “clone” of a ridesharing app like Uber or Bolt: the app simulates riders requesting trips and drivers picking them up, then repeats this all over again. See it [in action, here](https://substack.com/redirect/825f9ac6-9bcf-49e1-8294-08dc47bb8556?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o):
What grabbed my attention was how this app is much more than just a simulation. Juraj included system monitoring parts which monitor the server’s capacity he runs the app on:
And it doesn’t end here. Juraj created [a systems design](https://substack.com/redirect/59ad7493-7400-46e1-b154-ef7ee8954e5f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) explainer on how he built this project, and the technologies used:
The app uses:
Node.js for the simulation engine
Go on the backend
PostgreSQL for the data layer
React and TypeScript on the frontend
Prometheus and Grafana for monitoring and observability
And if you were wondering how all of this was built, Juraj documented his process in an incredible, 34-part blog series. You can [read this here](https://substack.com/redirect/5a01026f-a09f-4c26-ac70-c675a265e779?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).
This “Uber clone” offers a nice blueprint on how to tackle a complicated project. Thanks to the detailed documentation of Juraj’s progress, we can reconstruct how he built the project. This is educational, as it shows one possible way to tackle a complicated project, and one for which the creator could only devote time to on the side, and at weekends. Here’s how Juraj approached the undertaking:
Phase 0: make a plan (Oct). Instead of starting with coding, Juraj kicked off by sketching. He sketched out what he wanted the final product to look like:
And he sketched how he envisioned the observability part to work:
Phase 1: Infrastructure (October-November).
Before diving into coding, Juraj set up the infrastructure. I assume he did this to familiarize himself with infrastructure which he hasn’t necessarily used in production before. This side project offered a good opportunity to try it out.
Set up a server on DigitalOcean (a virtual machine with 1GB memory and 25GB of disk space)
Set up the domain, and configure the DNS
Set up users on the server
Set up SSH keys for more secure authentication
Install Go on the server, which will power much of the backend
Set up a HTTP server using Go
Deploy for the first time, doing so manually, for now
Enable HTTPS by registering a certificate
Utilize environment variables to be used for configuration, instead of hardcoding configuration or secrets into the source code. Hardcoding secrets in production is poor practice. We
[covered](https://substack.com/redirect/81510533-13c9-40af-bc61-db43f0e35b9e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)how Stack Overflow learned this the hard way, a few months back.Serving a web page. This is the point where the app reached the “Hello world!” stage
Improve deploys. Change deploys to be a one-command process, instead of multiple steps
See [blog posts #1-11](https://substack.com/redirect/5a01026f-a09f-4c26-ac70-c675a265e779?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) for details on all the steps.
Phase 2: some business logic, and more infra (December-January)
Draw a map using JavaScript to map onto an
[SVG](https://substack.com/redirect/bec33be8-3f2b-452c-a565-b7050d1c4600?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)formatBuild a graph and traverse it.
[Here’s a video](https://substack.com/redirect/a39cb1a0-de71-4841-8dba-ac6f33a0cfbe?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)of Juraj demonstrating this traversal.Set up Docker to package the application into containers
Use Docker in production, and modify the deploy script to deploy using Docker
Set up PostgreSQL to persist data on drivers, riders and trips
Connect the Go backend to the PostgreSQL database
Connect the backend and the database containers
[Docker Compose](https://substack.com/redirect/ec0496e4-1fc8-4362-89f7-31b046133186?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)in production
See [blog posts #12-20](https://substack.com/redirect/5a01026f-a09f-4c26-ac70-c675a265e779?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) for details on all the steps.
Phase 3: a basic UX (February)
Migrate to React
Design a car, from a vector image
Move a car with animations. Including adding unit tests.
Turn a car using rotations
Tidying up the project: refactoring the files now, that the project’s structure is more clear
Server-generated data
Animation fixes
See [blog posts #21-27](https://substack.com/redirect/5a01026f-a09f-4c26-ac70-c675a265e779?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) for details on all the steps.
Phase 4: “hardcore” coding (March)
This was the first phase where Juraj did no more infrastructure work, and focused only on “pure” business logic.
Simulation engine: this component simulates the behavior of drivers and customers
Multiprocessing for Node.js, to avoid blocking the event loop
Generating destinations, and making sure the start point is not too close to the destination
Matching drivers with customers: doing this similarly to how a service like Uber does
Route planner: tell the driver which route to choose to collect a customer
See [blog posts #28-32](https://substack.com/redirect/5a01026f-a09f-4c26-ac70-c675a265e779?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) for details on all the steps.
Phase 5: finalizing and monitoring
Finalizing the simulation
Setting up monitoring & logging
See [blog posts #33 & 34](https://substack.com/redirect/5a01026f-a09f-4c26-ac70-c675a265e779?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) for details of all the steps.
There are several things that I’ll highlight about this side project.
1. Persistence. Juraj built this project on the side, between October 2022 and April 2023, which is 7 months.
2. Documenting the steps. Every time Juraj made progress, he documented what he did, and how. This likely helped him to learn, and it also helps others wanting to understand, too.
3. Incremental progress. The project looks like a tough one to build from scratch on the side. But looking at the incremental steps, it is not nearly so daunting. Here are a few of the steps, taken directly from the blog:
Monday:
[installing Go](https://substack.com/redirect/0b9d591c-2786-4537-a87f-ff40dc3e30dd?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)on the server (17 Oct)Wednesday:
[setting up the HTTP server](https://substack.com/redirect/0b9d591c-2786-4537-a87f-ff40dc3e30dd?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)using Node’s native http module (19 Oct)Friday:
[the first deploy](https://substack.com/redirect/a4de1839-5a36-44f0-9205-b1273b36db2f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)(21 Oct)Saturday:
[enabling HTTPs](https://substack.com/redirect/b16d30e3-305d-4c77-bb52-e105ba2315d6?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)(22 Oct)Sunday:
[setting up environment variables](https://substack.com/redirect/ac5026f4-4fd2-4321-bb85-7568b8c7bffe?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)(23 Oct)(Step away from the side project for a week)
…then do another burst of tasks, making more progress
4. You won’t get the layout of a project right, the first time. So refactor! Juraj was about 70% done with the project, when he went back to refactor the structure of the project. This wasn’t for the lack of planning: but because as you set up new infrastructure, things turn out a bit different than you expected.
This is just the way of software engineering, and there’s nothing to be embarrassed about it. As you learn more about the project, don’t be afraid to go back and change the project structure – or do other refactorings – to help your work, going forward. See [the project structure](https://substack.com/redirect/9cec20f3-cec2-4e5f-87e2-c2d76638e7a9?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) Juraj set up at the end of Phase 3.
5. Infrastructure is important, and setting it up right can be a consuming task! In the first 3 phases of the project, Juraj spent a lot of time on infrastructure setup. It was only in Phase 4 that he was able to focus “purely” on the coding part.
I really like how this project showcases just how much time can go into infrastructure setup. At companies with dedicated platform teams, those teams take exactly this kind of load off other teams building greenfield projects.
Both as an engineer, and especially as an engineering manager, don’t forget there’s a real cost to setting up and then maintaining infrastructure. Much infrastructure work is invisible as it does not involve commits, and most engineers won’t document the time they spend on these tasks, like Juraj has. But this is work that still needs to be done!
Here are the learnings Juraj had with this project. I reached out to Juraj to ask how this project helped him. His answer:
“I've touched on many topics I haven't been exposed to in my day-to-day job, such as server configuration, setting up a deployment pipeline, animations in JavaScript, or using Docker.
I decided to get better at algorithms and data structures a few months ago, and this project complemented it nicely. For example, I implemented the map and its associated methods (e.g. path-finding) from scratch.
I also wanted to get better at setting up a full-stack project from scratch and understand why certain technologies are used. Docker is a good example - I didn't use it because I ‘wanted to’, but because the necessity for it arose. I was surprised how much time all of the infra work took me before I was able to start with the actual simulation logic!”
And how did Juraj find the time to work this much on the project?
“While I was at my previous job, I dedicated 1-2 hours a day, usually after work. After leaving in March due to a layoff, I decided not to start my job search immediately, but spent some more time finishing and polishing this project. That's when I really ramped up my effort on it and started seeing a lot of progress.”
If you are thinking of doing a side project with the goal of learning new technologies – and, to also be able to share those learnings, and show off the side project – I can recommend taking inspiration from this methodological approach Juraj took. Of course: don’t copy the exact approach, as-is. But planning first, documenting steps, and building a “production simulation” are all ideas that you could use in your own side projects as well. If you do: your side project will surely stand out from many of the other ones.
Your own projects often seem less impressive to you than they are to others. I was impressed by the implementation and attention to detail for this project – for example, going the extra mile for adding in monitoring for the server components: typical for a production service, but rarely seen in a side project. When I shared that I’m impressed with the execution with Juraj, his response was surprising, as he told me:
“Working on this side project every day, it no longer feels that impressive to me (as I think is common with software projects). But having read your fresh perspective, it certainly gives a lot of encouragement!”
When it’s day-to-day work, most engineers don’t think they’re doing anything complex, or special. And, in all fairness: no single step in Juraj’s project was complex. The complexity comes from the combination of simple steps. This is the beauty of software engineering: that everything that seems complex can be broken down to simple to understand – and simple to implement – steps.
Thanks a lot to Juraj for sharing this project with me. View the complete source code [here](https://substack.com/redirect/bff5c44a-a4b3-45dc-9ee9-5f4e58523c7a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). If you are hiring for full-stack engineers, Juraj is on the market – at least for now! Connect with him via [his website](https://substack.com/redirect/5a01026f-a09f-4c26-ac70-c675a265e779?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), [on LinkedIn](https://substack.com/redirect/6293c165-338f-4368-b269-6f142d51c8bc?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) or [on Twitter](https://substack.com/redirect/d4e40902-d1d6-449b-b641-31c76bdcd9b7?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).
This was one out of the four topics covered in this week’s The Scoop. A lot of what I share in The Scoop is exclusive to this publication, meaning it’s not been covered in any other media outlet before and you’re the first to read about it.
The full The Scoop edition additionally covers:
Why are many Snap employees selling their stock as soon as it vests, and not a day later? Snap is a very strange publicly traded company, where shareholders have precisely zero votes. I’ve talked with engineers and discovered a surprising level of distrust within the company. Is this tied to the governance model, or something else? Exclusive.
Analyzing the split of cuts at Lyft. How much were software engineers impacted by ride-hailing service Lyft’s large-scale cuts? I went through data based on Lyft’s talent directory; it looks like tech functions were hit harder than other areas. Exclusive.
Robinhood is no longer a remote-first company. Few companies were as vocal about becoming a remote-first company than Robinhood. But less than 18 months later, the company has made a u-turn. What can founders and leaders take from this avoidable policy reversal? Analysis.
If you’re hiring software engineers or engineering leaders, join [The Pragmatic Engineer Talent Collective](https://substack.com/redirect/423707f2-f2bc-4bbe-a014-381663163d52?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). It’s the #1 talent collective for software engineers and engineering managers. Get weekly drops of outstanding software engineers and engineering leaders open to new opportunities. I vet every software engineer and manager - and add a note on why they are a standout profile.
Companies like Linear use this collective to hire better, and faster. [Read what companies hiring say](https://substack.com/redirect/124e6144-9c42-4ebe-8e0c-7554c9b333ca?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). And if you’re hiring, apply here:
If you’re open for a new opportunity, join to get reachouts from vetted companies. You can join anonymously, and leave anytime:
[Senior Software Engineer](https://substack.com/redirect/13bf915a-88bb-4858-9c8c-a31d91248d3a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)at AI Build. London or Remote (Europe).[Senior DevOps Engineerr](https://substack.com/redirect/c1b568a3-3aa3-4d10-a484-c8cf098dba8a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)at AI Build. Remote (US).[Full-Stack Engineer](https://substack.com/redirect/b155dca0-600f-4de3-bbd0-83b46284d96e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)at Farmlend. £85-95K + equity. London.[Senior Backend Engineer](https://substack.com/redirect/8a7d5e74-4374-4248-acff-220d1432527d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)at Farmlend. £85-95K + equity. London.[Senior Full Stack Engineer](https://substack.com/redirect/b2f41600-db9d-4462-9e48-e8f9419e05a5?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)at Perfect Venue. $150-180K + equity. San Francsico or Remote (US).[Full-Stack Engineer](https://substack.com/redirect/130b8d44-a099-43f1-9804-147d37402f52?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)at Vital. $70-120K + equity. Remote (Global, within 5 hours of GMT).[Backend Engineer](https://substack.com/redirect/40bfc9e0-f6c1-445c-9d47-d852db05317f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)at Vital. $70-120K + equity. Remote (Global, within 5 hours of GMT).[Technical Lead - Platform](https://substack.com/redirect/a93fb384-ecd9-4e43-b1cc-5d7cdcd926e6?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)at Vannevar Labs. Remote (US).[Senior Software Engineer, Fullstack](https://substack.com/redirect/431e66f9-a866-4f6d-9921-d10f1d9032b9?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)at Vannevar Labs. Remote (US).[Computational Geometry Engineer](https://substack.com/redirect/792343e4-355d-46df-9420-5b17bbfb5ab2?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)at AI Build. London or Remote (Europe).[Senior QA Engineer](https://substack.com/redirect/06261589-53f5-4874-97aa-e3e151cc8532?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)at AI Build. London or Remote (Europe).[Lead Backend Developer](https://substack.com/redirect/b2827651-be44-446c-9542-c47e8e22e05d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)at Cineville. €53-79K + equity. Amsterdam.[Senior Software Engineer, Distributed Systems](https://substack.com/redirect/41b03bf3-32bd-44eb-9986-61330edb6a92?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)at Mixpanel. $200-270K + equity. New York, San Franciso, Seattle or Remote (US).[Senior Software Engineer, Fullstack](https://substack.com/redirect/9de11166-e207-48c1-9571-233802cca548?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)at Mixpanel. $200-270K + equity. New York, San Franciso, Seattle or Remote (US).[Principal Engineer](https://substack.com/redirect/a221b625-a508-48e1-a235-9497e25c3e6f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)at Shoplift. $185-205K. New York.
See more senior engineer and leadership roles with great engineering cultures on [The Pragmatic Engineer Job board](https://substack.com/redirect/49b18ddd-651f-4441-bfa8-bd211d4bc7a2?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) - or post your own.
You’re on the free list for [The Pragmatic Engineer](https://substack.com/redirect/2/eyJlIjoiaHR0cHM6Ly9uZXdzbGV0dGVyLnByYWdtYXRpY2VuZ2luZWVyLmNvbT90b2tlbj1leUoxYzJWeVgybGtJam94TkRVMk16TXhPU3dpY0c5emRGOXBaQ0k2TVRJMU16SXpOekUyTENKcFlYUWlPakUyT0RVMk16ZzVPVElzSW1WNGNDSTZNVFk0T0RJek1EazVNaXdpYVhOeklqb2ljSFZpTFRRMU9EY3dPU0lzSW5OMVlpSTZJbkJ2YzNRdGNtVmhZM1JwYjI0aWZRLkRiM3ZrTFJ3VW5FQldPUS1zSE80UVZ6UnA4cWUtSnpMV1ZxbmlqaWU3UWMiLCJwIjoxMjUzMjM3MTYsInMiOjQ1ODcwOSwiZiI6dHJ1ZSwidSI6MTQ1NjMzMTksImlhdCI6MTY4NTYzODk5MiwiZXhwIjoxNjg4MjMwOTkyLCJpc3MiOiJwdWItMCIsInN1YiI6ImxpbmstcmVkaXJlY3QifQ.4hBmY9P4tKXeSa_kTJs9x1UW5U84Ms4tYFpSyMBNjps?). For the full experience, [become a paying subscriber](https://substack.com/redirect/2/eyJlIjoiaHR0cHM6Ly9uZXdzbGV0dGVyLnByYWdtYXRpY2VuZ2luZWVyLmNvbS9zdWJzY3JpYmU_dG9rZW49ZXlKMWMyVnlYMmxrSWpveE5EVTJNek14T1N3aWFXRjBJam94TmpnMU5qTTRPVGt5TENKbGVIQWlPakUyT0RneU16QTVPVElzSW1semN5STZJbkIxWWkwME5UZzNNRGtpTENKemRXSWlPaUpqYUdWamEyOTFkQ0o5LkFtUDhPa0RtcGxyVjZPdi1KOFpNUnMzMEZFU2xTTUZsMVVfbUxpWWhMNTgmdXRtX3NvdXJjZT1wb3N0IiwicCI6MTI1MzIzNzE2LCJzIjo0NTg3MDksImYiOnRydWUsInUiOjE0NTYzMzE5LCJpYXQiOjE2ODU2Mzg5OTIsImV4cCI6MTY4ODIzMDk5MiwiaXNzIjoicHViLTAiLCJzdWIiOiJsaW5rLXJlZGlyZWN0In0.veJL64SYuao7ZD2NJLZ1nkp1nNgorQ1WN--RdnTEC9c?). Many readers expense this newsletter within their company’s training/learning/development budget.
This post is public, so feel free to share and forward it.