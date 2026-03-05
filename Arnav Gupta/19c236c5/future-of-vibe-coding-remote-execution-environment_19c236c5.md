---
subject: "Future of Vibe Coding: Remote Execution Environments"
from: "Arnav Gupta from system bashing <systembashing@substack.com>"
to: ""
date: 2026-02-03 12:04:34
labels: ["Arnav Gupta", "CATEGORY_PERSONAL", "IMPORTANT", "INBOX", "UNREAD"]
label_ids: ["Label_2739595779997728054", "CATEGORY_PERSONAL", "IMPORTANT", "INBOX", "UNREAD"]
---
|
The last few months have been a blur.
First, we had the “autocomplete” era. Copilot, Cursor, the “tab-tab” life. You’d open your IDE, have the chat bar on the side, prompt a bit, edit a bit, and let the ghost text fill in the rest. It was a mix. A partnership.
Then came December 2025.
Opus 4.5. Gemini 3. GPT 5.2.
Suddenly, the game changed. We aren’t just “writing code” anymore. We are Vibe Coding. Andrej Karpathy coined the term a year ago, but only now, with these models, does it feel like the default reality.
You don’t tab-complete your way through a function. You prompt for the whole feature. You get an output. If you don’t like it, you don’t rewrite it manually. You prompt again. “Make this change. Add a test there. Fix that edge case.”
But this shift has introduced a massive, glaring bottleneck.
Here is the problem. You give the agent a prompt.
“Refactor this entire module, write unit tests for it, run the CI locally, and if it passes, raise a PR.”
Then... you wait.
2 minutes. 5 minutes. Sometimes 10 minutes.
While the model is chugging away, doing this long-running 10-minute job, your terminal is busy. Your local environment is locked up.
In those 10 minutes, you could go scroll Twitter or watch Instagram reels. But let’s be real, you want to be productive. You want to multitask. You want to open another project and start prompting a different feature.
But you can’t.
Because your “Gemini CLI” or “Cloud Code” session is hogging your local resources. You run into port conflicts. You run into file lock issues. You can’t easily spin up multiple sessions of these heavy agents on one machine without it turning into a chaotic mess.
Coding is rapidly shifting from an Individual Contributor (IC) activity to an Engineering Manager (EM) type activity.
With these agents, you are effectively the manager or tech lead of a team of 4 or 5 junior engineers. They are fast, they are tireless, but they need your eyes on them. You stand behind their shoulder (metaphorically), watch them work, and correct them when they mess up.
Now, ask yourself this: Would you make 5 different engineers type on your single laptop?
No. That would be insane.
Real engineers have their own laptops. They have their own dev servers. They have their own user accounts. They have their own isolated environments where they can mess up, install dependencies, and run servers without crashing your machine. They make commits from their IDs.
So why are we trying to force 5 AI agents to run on our single localhost
?
This is where the industry is moving. We are going to see an explosion of Cloud-based Agents powered by Remote Execution Environments (REE).
We need isolated environments for development.
When you use ChatGPT (especially on the Pro plan), you are already seeing a glimpse of this. It has a “Code Interpreter” (or whatever they rebrand it to next). It spins up a sandboxed Python environment, executes code, calculates data, and gives you the result. It doesn’t ask to install Python on your Mac.
Look at Manus.im.
The Manus agent is a great example of where this is going. It integrates with your Gmail, your Calendar, your Notion. But to be a true “executive assistant”, it needs to do things.
It needs to fetch data, store it in a temporary folder, parse it, create an output, and send it somewhere. It needs to make API calls. It needs to execute code.
To do this safely and reliably, it uses an execution environment in the cloud.
I hear you already wondering. “What about the Model Context Protocol (MCP)? Isn’t that all you need”
MCP is great. Really, it is. It standardizes how LLMs connect to data sources. It lets the agent “read the manual”, fetch a row from a Postgres DB, or create a ticket in Jira without hallucinating the API schema.
But Context is not Compute.
MCP is a protocol. It defines how to talk to a tool. It does not define where the tool runs.
If you ask an agent to “debug why the build is failing on Node 22,” an MCP server can fetch the logs. It can maybe even read the package.json
. But can it run npm install
? Can it utilize strace
to see what system call is hanging? Can it apt-get a missing library that the build script implicitly relies on? All of that requires your coding “agent” basically runs in --yolo
mode with full terminal access.
Agents need to build their own tools.
In a real engineering workflow, you don’t wait for someone to write an MCP wrapper for kubectl
or the aws
CLI. You just install the CLI and run it.
We are seeing a shift where agents are using Skills and dynamic commands.
They check if
ffmpeg
is installed. If not, they download a static binary.They write a temporary Python script to parse a messy CSV, execute it, and then delete it.
They install a
gemini-skill
or aclaude-tool
on the fly to gain a new capability.
To do this, you don’t just need a “protocol” for function calling. You need a writable file system. You need a shell. You need root
(or at least a very permissive user).
MCP is the menu; the Remote Execution Environment is the kitchen. You can’t cook the meal just by reading the menu.
To understand why we are here, you have to look at the trajectory.
Back in 2023, we were obsessed with Cursor and GitHub Copilot. It was the era of the “Super-Autocomplete”. You typed function fetchUser()
, paused for a millisecond, and the AI filled in the rest. It was magical, but it was still you driving the car. You were the pilot; the AI was the navigator.
Then came early 2025, and Andrej Karpathy dropped the term “Vibe Coding”. The shift was subtle but profound. We stopped caring about the syntax. We started caring about the intent. You’d paste a screenshot of a UI and say “Make it look like this.” The AI wrote the code. You didn’t even read it half the time. You just checked if it worked.
But late 2025 gave us Claude Code and the concept of Agent Swarms.
Anthropic realized something critical: One agent is not enough.
If you ask a single LLM to “refactor the auth system,” it will hallucinate. It will forget edge cases. It will break backward compatibility. It has a limited context window, no matter what the marketing says.
So they introduced Subagents.
Now, when you run a command in your terminal, you aren’t talking to one bot. You are talking to an Orchestrator.
The Orchestrator analyzes your request.
It spins up a Researcher Agent to read the existing docs and code.
It spins up a Plan Agent to draft a change strategy.
It deploys three Coder Agents to work on the backend, frontend, and database migration in parallel.
Finally, a QA Agent writes tests and tries to break the code.
This is the “Agent Swarm” architecture. It reduces hallucinations because tasks are atomized. It increases speed because work is parallelized.
But it kills your laptop.
You cannot run an Orchestrator and 5 sub-agents on a MacBook Air. You can’t have 6 concurrent processes fighting for the same node_modules
folder, the same 3000
port, and the same file locks.
The CLI tools we love today will remain, sure. IDEs won’t die overnight.
But the “Vibe Coding” future is one where your “IDE” is effectively a command center. A dashboard where you dispatch tasks to 15 different agents running in 15 different cloud containers.
You prompt Agent A to refactor the backend. You prompt Agent B to update the frontend tests. You prompt Agent C to research a new library.
And you? You just sit back and review the Pull Requests.
It’s like being a Tech Lead with a team of 15 super-fast juniors.
Does it sound a bit soulless? Maybe.
Is it better than staring at a loading spinner for 10 minutes? Absolutely.
If you are still trying to run everything on your poor MacBook Air, you are doing it wrong. The future is remote, and the future is executed elsewhere.
Get your agents their own laptops.
system bashing is free today. But if you enjoyed this post, you can tell system bashing that their writing is valuable by pledging a future subscription. You won't be charged unless they enable payments.