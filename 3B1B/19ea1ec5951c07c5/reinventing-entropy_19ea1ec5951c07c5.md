---
id: "19ea1ec5951c07c5"
subject: "Reinventing Entropy"
from: "3Blue1Brown <3blue1brown@substack.com>"
to: ""
date: 2026-06-07 11:51:07
labels: ["3B1B", "CATEGORY_PERSONAL", "INBOX", "UNREAD"]
label_ids: ["Label_4235920960005303993", "CATEGORY_PERSONAL", "INBOX", "UNREAD"]
---
In April, the next item on my roster of video plans was to explain what cross-entropy is and why it’s used for pre-training language models. Fast-forward two months, and this has turned into a little 3-part mini-series on the foundations of information theory as they pertain to the phrase “compression is intelligence.” It’s not uncommon for me to get excited by a topic and have it grow; it’s something I love about this work. However, it feels especially funny to me in this case because cross-entropy as a feature of LLM training amounts to just one line of code, and a relatively simple one at that. Of course, what’s interesting is not the line of code, but the question of what the term means and why it’s a principled loss function to use. Given that the term has its origins in studying compression, I don’t think any writer could resist being pulled into the gravity well of that provocative phrase, “compression is intelligence”. Also, I’ve been itching to cover information theory properly for a while now, and this was a welcome excuse. This first part begins with the fundamentals, explaining where the formulas for information and entropy come from, in the context of leading a viewer to (hopefully) rediscover the core idea behind Shannon’s Noiseless Coding Theorem. Enjoy, |