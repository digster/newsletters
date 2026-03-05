---
subject: "Why are AIs so hard to trust? It’s not just because they hallucinate"
from: "The Ken <info@the-ken.com>"
to: ""
date: 2025-09-24 04:59:32
labels: ["CATEGORY_PERSONAL", "INBOX", "The Ken", "UNREAD"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_8244464457792971031", "UNREAD"]
---
Good Morning Ishan,
It isn’t every day that you see a company’s research scientists bite the hand that feeds them, even if it’s inadvertent.
Here’s part of the abstract of a paper straightforwardly titled “[Why Language Models Hallucinate](https://arxiv.org/abs/2509.04664)”, authored by three researchers at OpenAI along with a scholar at the Georgia Institute of Technology. It was published in the first week of September:
Translation: hallucinations are features, not bugs, in language models, given the way they are currently trained. The authors go on to mathematically prove it. Sure, this was already a widespread belief, but if you’re like me and like to get down in the weeds, then you know how exciting it is to see irrefutable proof.
Anyway, the paper’s authors—Adam Tauman Kalai, Ofir Nachum, Santosh S Vempala (of Georgia Tech), and Edwin Zhang—weren’t solipsising. One of their crucial points is that there could be a stopgap to prevent language models from fabricating answers when the right one isn’t immediately within reach. Their solution is based on “confidence thresholds”, defined like this:
In other words, models would only respond when their internal confidence about an answer is above 50%, 75%, 90%—or whatever level the user defines. Guessing with needless confidence is highly, highly, highly discouraged. It’s a way to give the model an out when it doesn’t have a big enough knowledge base and isn’t sure what to say.
Advocating for a model to express uncertainty in an honest manner sounds a lot like instructing a student how to think or training a junior colleague to communicate clearly. In my experience, that involves high doses of sussing out when they might be trying to bluff their way past a new situation.
Read the full article: “[Hallucinations aren’t the problem. AI companies are losing users’ trust](https://the-ken.com/story/why-are-ais-so-hard-to-trust-its-not-just-because-they-hallucinate/)”