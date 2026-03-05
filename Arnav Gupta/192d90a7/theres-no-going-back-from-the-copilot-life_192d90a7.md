---
subject: "There's no going back from the \"Copilot Life\""
from: "Arnav Gupta from system bashing <systembashing@substack.com>"
to: ""
date: 2024-10-29 16:09:41
labels: ["Arnav Gupta", "CATEGORY_PERSONAL", "INBOX", "STARRED", "YELLOW_STAR"]
label_ids: ["Label_2739595779997728054", "CATEGORY_PERSONAL", "INBOX", "STARRED", "YELLOW_STAR"]
---
|
A year back, [Github announced](https://substack.com/redirect/7c478c16-b421-42df-b57b-91a277a56be1?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) that they are ‘re-founding the company on top of Copilot’. A bit of marketing hyperbole. And possible for a long time Github will still continue to make more money off storing code and running CI pipelines, than from suggesting the next line of code. But the Copilot way of writing (and not just Github’s Copilot™️), has become the new reality. Definitely so for me.
There are 3 key things which I do now, which I absolutely cannot do without GenAI going forward, and all 3 of them more of “sprinkling genAI into existing things” and less of “the killer app”.
AI generated thumbnails/images for articles, courses, videos etc
Writing, documenting, explaining code using
[Continue.dev](https://substack.com/redirect/fd772eb5-ee89-46ea-8824-42594ddfafba?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)and Github CopilotWriting, searching, editing and talking to my notes inside
[Obsidian](https://substack.com/redirect/f00de8a5-2e66-41a5-b616-4c2047d6be17?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
I’ll describe a little about the coding and writing/notetaking flow here that I have found myself most comfortable now.
If you are not much into coding, you can skip over the next section to the notetaking and writing part.
[Github Copilot](https://substack.com/redirect/71467fc8-31b0-4602-83b3-7af3cd4f7cc3?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)forin-line autocomplete
code-to-code actions (translate this python script to Kotlin)
[Continue.dev](https://substack.com/redirect/ced3bc9b-4ff9-4cc0-99d1-a74a328682f2?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)for everything elsedocumenting code
explaining code (often useful to dive into new codebases)
a chat-bot inside my IDE to help plan some tasks, rubber-duck the low-level design etc
NOTE: Before anyone asks, why not x, y, z… I have tried out Cursor, and some other Copilot alternatives like Jetbrains AI, Cody etc. The autocomplete quality of Copilot is what I like most (this probably just a taste issue), and along with Jetbrains, most value for money too with the annual plans. For non-autocomplete usage, I just prefer using my own API keys as that’s much cheaper than paying to a wrapper.
I am not writing LeetCode all day, but as a contrived example, it can solve most Easy/Medium questions 0-shot in a single suggestion.
If you actually start typing though, it understands you do not want a 0-shot answer, and suggests only line-by-line.
And if you want to write something different from its original suggestion (here it suggested DFS approach first, and I would like to use BFS instead), then it readily helps you with that too.
And then, when you want to get the code explained (esp, if you took a Copilot suggestion that you cannot fully comprehend quickly), you can switch to the Continue side-drawer and ask that to be explained. I usually circle between one of these models.
Claude 3.5 Sonnet (really good after the 20241022 update)
For very small tasks I use Haiku
Gemini 1.5 Pro (sometimes really structured output)
For really small tasks like generating JSON samples, I use Flash
GPT 4o
4o-mini is faster for smaller things
You can easily send your code into the prompt by quick @file
or @codebase
shortcuts. Or you can even send your @terminal
output into it.
Some of the stuff I truly love having AI to do is - generate test or sample data. This example here - took AI 5 seconds to generate, and if I had to manually or script it, it would definitely would have been either a) a waste of time; or b) I would have skipped generating this and testing my code for this scenario.
Apoligies for a bit of a shameless self-plug, but I have a small community on Telegram of early-mid stage software engineers -
[http://t.me/better_sde2]. Sometimes we do sessions on live coding there, and if you want to see more of me using these AI tools in more real-world projects you can join one of those sessions.
People have been calling their note-taking paraphernelia (Roam, Obsidian, Notion etc etc) as their “second brain” ever since Tiago Forte dropped that damn book. I always felt like it is just a loosely organised personal Wiki at best and just a dumpyard of notes at worst. Until LLMs and GenAI came along.
[Obsidian](https://substack.com/redirect/b7834e9f-4bdf-48a4-9ded-e7cbf8b25562?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)- final ‘workbench’ for my notes, thoughts, drafts[Readwise](https://substack.com/redirect/1391748e-5496-47e2-b32b-8c3836a0fc8b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)- all links, highlights, bookmarks go here. great set of integrations to do it. I try to use the Reader app, but mostly have not been able to - I am not much of ‘ruminating reader’[Obsidian Copilot](https://substack.com/redirect/d01597bc-0df1-4abe-a1ba-cc452da1dad2?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)- This gives a chat window on the side, very similar to Continue workflow.[Text Generator](https://substack.com/redirect/82cd8295-7e29-4d42-9f9e-2f44abd0c273?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)- Another Obsidian plugin - this is less for chatting with, but more useful for long-form writing. It also allows extracting information from PDFs and audio recordings (using Whisper). So I use it for recording rambling things and then turning it into structured text often.[Copilot Autocompletion](https://substack.com/redirect/770b1c69-34f1-4033-8c1a-d36c69d10d18?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)- (ugh, 3 different plugins? well…) this one does what Github Copilot completions does best - generate the next line. Helpful for small autocomplete, not helpful for generating entire paragraphs.
For the last 3 plugins, all of them can be used with any model you like. I have Gemini 1.5 Pro, GPT 4o and Claude 3.5 Sonnet configured with my API keys. Using via APIs is much cheaper. Thus I never actually use the consumer websites ([chatgpt.com](https://substack.com/redirect/f6bfdabb-b12d-4b1e-bddb-ecc628913a30?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) or [claude.ai](https://substack.com/redirect/812eaa59-6f5c-494e-9138-ad1c4c4850e3?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) or [gemini.google](https://substack.com/redirect/2b677065-cdcb-465c-8d3b-f1b5201d04ef?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o))
Part of why my vault in Obsidian is so useful after the advent of GenAI tools has a lot to do with the setup I have had for many years now (even before I started using Obsidian itself).
Readwise app and browser extension for capturing highlights on articles, newsletters, essays
Pocket for capturing all my bookmarks from Firefox
eBook highlights from Kindle go to Readwise as well
Tweets, Twitter Threads are sent to
@readwise
as DMs
Readwise dumps all of this to my Obsidian. (It now also dumps it to Google Drive to be used by NotebookLM)
The Copilot Autocompletion is good for generating “next line” type of things like this
But to actually generate the 10-tweet thread, best to use Text Generator. Here see what it generated.
mai aur meri tanhAI aksar ye baatein kiya karte hai
The best use of these tools inside Obsidian for me has been via the Copilot Chat window. You can either type chats directly into the window, or you can also keep your own elaborate prompts saved as notes.
Something I love doing is comparing my own notes (about situations that have happened or conversations I have had, or some plans I have made), against highlights from books or articles. Here is an example - where I am comparing my management strategy against some highlights I made from a couple of engineering management related books.
Depending on the model used, and how much context was available in the notes and the highlights, the output can be fairly good!
Again, these are contrived examples because I would rather not share too personal examples (for privacy reasons). But on more real use cases, the usefulness is, in fact, much more! I cannot imagine going back to a world where I will not have help from an AI agent.
I have also been exploring how much of these can I run in a diminished capacity locally, as I realise, I’ll feel handicapped while coding and writing in the near future without internet access (like on flights) as I get more dependent on these tools.
The good news is, on a laptop like mine (I am currently on a M3 Max with 48GB of VRAM and a really powerful GPU), using something like Ollama, a good bit of it works. Not the ~100B parameter models (even they work via quantisation at painful speeds), but the ~10B models work fairly well! Things which can be done by GPT 4o-mini or Gemini Flash or Claude Haiku can be replicated at a usable speed locally via open-source models.
Llama 11B VI (vision, image), Deepseek Coder 7B (code autocomplete), Gemma 2 9B (general purpose) are some that I have tried to be fairly useful for local usage. They are not as good as the trio of frontier models I have used as examples earlier, but these can do 70-80% of the job locally. Local usage is $0 which is also a great thing!
Please feel free to comment about your genAI setup in your work tools, if you have started using them yet, and how has your experience been so far!
system bashing is free today. But if you enjoyed this post, you can tell system bashing that their writing is valuable by pledging a future subscription. You won't be charged unless they enable payments.