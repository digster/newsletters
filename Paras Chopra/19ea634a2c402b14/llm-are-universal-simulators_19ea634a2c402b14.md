---
id: "19ea634a2c402b14"
subject: "LLM are universal simulators"
from: "Inverted Passion Community <invertedpassion@substack.com>"
to: ""
date: 2026-06-08 07:47:15
labels: ["CATEGORY_PERSONAL", "IMPORTANT", "INBOX", "Paras Chopra"]
label_ids: ["CATEGORY_PERSONAL", "IMPORTANT", "INBOX", "Label_6668903435596043419"]
---
Saying that LLMs are just next token predictors is underselling these beasts to a mind numbing degree. First, LLMs aren’t just predicting the next token. They plan ahead - the loss function is the average of cross entropy across all future tokens in a context window and the attention has access to all previous tokens. So, at a particular token, the LLM is planning what could be relevant far ahead and not just at the immediate next token. Second, LLMs are trained to predict sequences across all texts on the internet that contain not just human generated text but things like weather forecasts, financial series, code, bash dumps, satellite pings and so on. To be able to do this prediction well, LLMs have to infer the physics / dynamics for all such domains (e.g. to predict weather patterns in data, you need to develop a model of earth coordinates, sunlight patterns, monsoon cycles and so on). (Just think how hard this prediction problem is, given the diversity of texts in the pretraining corpus.) So, instead of saying LLMs are next token predictors, a much better way of framing them is that these things are universal simulators. You prompt them with a hint, and they simulate physics of whatever domain your hint is about. It’s crazy scary that this works but somehow it does! |