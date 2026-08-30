---
id: "1a033069bfed5442"
subject: "Escaping the mode collapse of LLMs"
from: "Inverted Passion Community <invertedpassion@substack.com>"
to: ""
date: 2026-08-24 09:04:48
labels: ["CATEGORY_PERSONAL", "INBOX", "Paras Chopra"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_6668903435596043419"]
---
|
LLMs are known to have mode collapse, i.e. if you have multiple parallel runs on the same prompt, you get very similar responses.
Is there a way to increase diversity?
Yes, it turns out that if you do such multiple runs **sequentially**, instead of in parallel. (Plus for each sequential run, append results from previous runs and instruct the LLM to create something different from before.)
I did this quick experiment to explore parallel v/s sequential runs for diversity. Given the same prompt to build a tower defence game, sequential runs had a much higher diversity and innovation v/s parallel runs.
Check out this (AI-generated) video for gameplay clips. The sequential cohort created interesting new dynamics and visual style, while parallel ones all collapsed to similar colors and orbital style dynamics.