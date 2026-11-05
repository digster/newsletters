---
id: "1a19555651791d70"
subject: "Are LLMs good or bad Bayesians?"
from: "Marginal REVOLUTION <donotreply@wordpress.com>"
to: ""
date: 2026-11-01 04:19:23
labels: ["CATEGORY_PERSONAL", "INBOX", "Tyler Cowen", "UNREAD"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_2466199532210586699", "UNREAD"]
---
Bryan Caplan:
It seems like you and other AIs are bad Bayesians. When presented with counterevidence, you should move toward or against the presenter with roughly equal probability. It depends on whether the argument was better or worse than expected. In fact, you seem to either move toward the speaker or just not change.
ChatGPT:
I think you’ve identified a genuine and important failure mode in AI reasoning: LLMs tend to treat a plausible counterargument as evidence in favor of its conclusion, rather than comparing the counterargument to what they should have expected to hear.
Your Bayesian point is correct, with one qualification: there’s no general theorem that updating toward and away from a speaker should happen with equal probability. But under appropriate calibration assumptions, both directions should occur, and an argument that’s weaker than expected should cause a negative update—even if the argument is perfectly valid as far as it goes.
Here is [the full dialogue](https://marginalrevolution.com?action=user_content_redirect&uuid=95bbf182793b5369ceebc28c592f0b7c55e6769d36874182e51dcf84428077db&blog_id=42693868&post_id=94097&user_id=262258391&subs_id=225460721&signature=da770f99b1eed21e34486b04d17b503d&email_name=new-post&user_email=ishan.mail@gmail.com&encoded_url=aHR0cHM6Ly93d3cuYmV0b25pdC5haS9wL2NoYXRncHQta25vd3MtaXRzLWEtYmFkLWJheWVzaWFuP3V0bV9zb3VyY2U9cG9zdC1lbWFpbC10aXRsZSZwdWJsaWNhdGlvbl9pZD04MjA2MzQmcG9zdF9pZD0yMjIzNDcwODYmdXRtX2NhbXBhaWduPWVtYWlsLXBvc3QtdGl0bGUmaXNGcmVlbWFpbD10cnVlJnI9M285JnRyaWVkUmVkaXJlY3Q9dHJ1ZSZ1dG1fbWVkaXVtPWVtYWls&email_id=897107debc9613d128f09ee040fd40fc). But will they try to fix this? Should they try to fix this? Can you undo this with good enough prompting? The scope and limits of Bayesian are truly at stake here...