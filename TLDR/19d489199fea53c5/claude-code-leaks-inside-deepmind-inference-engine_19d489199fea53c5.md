---
id: "19d489199fea53c5"
subject: "Claude Code leaks 🤖, inside DeepMind 🧠, inference engineering 🧑‍💻"
from: "TLDR <dan@tldrnewsletter.com>"
to: ""
date: 2026-04-01 10:23:14
labels: ["CATEGORY_PERSONAL", "INBOX", "TLDR", "UNREAD"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_795315172960844453", "UNREAD"]
---
[
Entire Claude Code CLI source code leaks thanks to exposed map file (2 minute read)
](https://tracking.tldrnewsletter.com/CL0/https:%2F%2Farstechnica.com%2Fai%2F2026%2F03%2Fentire-claude-code-cli-source-code-leaks-thanks-to-exposed-map-file%2F%3Futm_source=tldrnewsletter/1/0100019d4891966b-86badd23-94fb-4dde-854b-6032cc4db804-000000/ImtGDZugfA6OVDmx0Z-MMSfxiUO8brzrt2N0Y0K1pEQ=451)
Anthropic recently published a version of the Claude Code npm package that included a source map file that could be used to access the entirety of Claude Code's source code. More than 512,000 lines of code were leaked on a public GitHub repository, which has since been forked tens of thousands of times. Developers are already analyzing the code to find out how Claude Code works. Anthropic has publicly acknowledged the mistake.
|
[
Apple Tests Siri Feature That Handles Multiple Commands at Once (3 minute read)
](https://tracking.tldrnewsletter.com/CL0/https:%2F%2Flinks.tldrnewsletter.com%2FDb0bgV/1/0100019d4891966b-86badd23-94fb-4dde-854b-6032cc4db804-000000/F1V-J41h13C51nN1rhkdhoLztKw246wOmINRz_bd7Zg=451)
Apple is testing a feature in Siri that will let it process multiple requests in a single query. Siri currently requires users to make requests individually. The new feature will allow users to combine requests, for example, ask Siri to check the weather, create a calendar appointment, and send a message, all within a single prompt. The new Siri is expected to be released at Apple's Worldwide Developers Conference on June 8.
|
|
Science & Futuristic Technology
|
[
Microbubbles (7 minute read)
](https://tracking.tldrnewsletter.com/CL0/https:%2F%2Fwww.worksinprogress.news%2Fp%2Fthe-cruise-missiles-of-medicine%3Futm_source=tldrnewsletter/1/0100019d4891966b-86badd23-94fb-4dde-854b-6032cc4db804-000000/72ptFjDPSSeUbO6lqPFTfZ0B-XppWeMGZQ5H7AeeD-k=451)
Microbubbles are tiny gas-filled bubbles with a protective outer shell that are capable of carrying drugs or genetic material to cells in the body. They are too large to leave the bloodstream, so they deliver drugs by bursting on command, briefly forcing open biological barriers to allow treatments to pass through. The force of their bursts can be used to break apart kidney stones. These bubbles can be steered, so they can carry therapies through the bloodstream to release precisely where they're needed.
|
[
Quantum computers need vastly fewer resources than thought to break vital encryption (7 minute read)
](https://tracking.tldrnewsletter.com/CL0/https:%2F%2Farstechnica.com%2Fsecurity%2F2026%2F03%2Fnew-quantum-computing-advances-heighten-threat-to-elliptic-curve-cryptosystems%2F%3Futm_source=tldrnewsletter/1/0100019d4891966b-86badd23-94fb-4dde-854b-6032cc4db804-000000/j-RROcuPQtupVKfmTz_6ktVj4onnq98DFcFB_Th-Uoo=451)
Two independently written whitepapers have come to the same conclusion that building a utility-scale quantum computer that can crack elliptic curves requires far fewer resources than anticipated. The papers are the latest sign that cryptographically relevant quantum computing at utility-scale is making meaningful progress. The advances are being driven by new quantum architectures that operate correctly even in the presence of errors, and ever more efficient algorithms. Neither of the papers has yet been peer reviewed.
|
|
Programming, Design & Data Science
|
[
Inside the Claude Code source (9 minute read)
](https://tracking.tldrnewsletter.com/CL0/https:%2F%2Flinks.tldrnewsletter.com%2FsCHaFt/1/0100019d4891966b-86badd23-94fb-4dde-854b-6032cc4db804-000000/vbgr6KwsfqU4K8z9gjAuUANIx-XyfepXKWzv6ne2hog=451)
Claude Code CLI's source code was recently leaked on GitHub. This post breaks down how the system works, where Anthropic made clever engineering choices, and where Anthropic's approach diverges from OpenAI's Codex. Claude Code is about 500,000 lines of TypeScript, with the actual API call comprising maybe 200 of them. Everything else in the harness.
|
[
What is inference engineering? Deepdive (45 minute read)
](https://tracking.tldrnewsletter.com/CL0/https:%2F%2Fnewsletter.pragmaticengineer.com%2Fp%2Fwhat-is-inference-engineering%3Futm_source=tldrnewsletter/1/0100019d4891966b-86badd23-94fb-4dde-854b-6032cc4db804-000000/8zwreYYqd5irIgtwGBnYI9jyQJDq3MuzIBJEe1FKYKg=451)
Inference is when a model takes an input and generates an output, one token at a time. Inference engineering is becoming more widespread as open models become more capable. With closed models, inference engineering is only done by the AI engineers who build the model, but anyone can tinker with open models. This post discusses what inference engineering is and some interesting approaches to inference engineering worth knowing about.
|
|
[
Project Mario (50 minute read)
](https://tracking.tldrnewsletter.com/CL0/https:%2F%2Fcolossus.com%2Farticle%2Fproject-mario-demis-hassabis-deepmind-mallaby%2F%3Futm_source=tldrnewsletter/1/0100019d4891966b-86badd23-94fb-4dde-854b-6032cc4db804-000000/aCB3iCJc8UnzcuU30ImyTNI_mF62CAPilz8Jj43dqmc=451)
Google decided to restructure itself in 2015, spinning out chunks of its operation as semi-independent bets and creating a holding company called Alphabet to preside over them. DeepMind used the opportunity to regain its independence. It planned to create a new DeepMind with a board comprising three people from DeepMind, three people from Alphabet, and three independent members. The ensuing governance talks were dubbed by DeepMind's leaders as 'Project Mario'.
|
[
Meet the Startup That Used AI and OpenClaw to Automate Its Own Developers (7 minute read)
](https://tracking.tldrnewsletter.com/CL0/https:%2F%2Flinks.tldrnewsletter.com%2F6c5pry/1/0100019d4891966b-86badd23-94fb-4dde-854b-6032cc4db804-000000/1-eTpunW4_3ap7a-nIhow-vF7WeZpmUC7foOrkJhekU=451)
JustPaid, a California-based startup, used a combination of OpenClaw and Claude Code to create a team of seven AI agents to grind out code 24/7. The agents have built 10 major features in a month, each of which would have taken a team of human developers a month or more to build. JustPaid plans to eventually replace all its employees with AI. The company currently has nine employees - its latest human hire was trained almost entirely by the AI agent engineers.
|
|
[
The Subprime Technical Debt Crisis (2 minute read)
](https://tracking.tldrnewsletter.com/CL0/https:%2F%2Fblog.happyfellow.dev%2Fthe-subprime-technical-debt-crisis%2F%3Futm_source=tldrnewsletter/1/0100019d4891966b-86badd23-94fb-4dde-854b-6032cc4db804-000000/H6u_HCv_s7eLyVq3q2wxOa9Jsjd0eAkVuDkxuNp0Olw=451)
Businesses are using AI under the assumption that the technology will eventually improve to the point that it will easily solve all of the technical debt currently accruing, but this might not be true.
|
|
|
Love TLDR? Tell your friends and get rewards!
|
|
Share your referral link below with friends to get free TLDR swag!
|
|
|
[Track your referrals here.](https://tracking.tldrnewsletter.com/CL0/https:%2F%2Fhub.sparklp.co%2Fsub_3202f09298cc%2F1/1/0100019d4891966b-86badd23-94fb-4dde-854b-6032cc4db804-000000/7jUJAwKtHmtJAcDa7BdSax86uF3SW0gAxmUa0L-NVM0=451)
|
|
|
|