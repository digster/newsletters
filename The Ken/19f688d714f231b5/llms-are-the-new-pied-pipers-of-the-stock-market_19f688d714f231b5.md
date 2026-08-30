---
id: "19f688d714f231b5"
subject: "LLMs are the new pied pipers of the stock market"
from: "The Ken <info@the-ken.com>"
to: ""
date: 2026-07-16 01:32:06
labels: ["CATEGORY_PERSONAL", "INBOX", "The Ken", "UNREAD"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_8244464457792971031", "UNREAD"]
---
|
|
Ka-Ching!
Thu, 16 Jul 26
A weekly newsletter about how finance is getting supercharged by tech in India, and how you can make money work for you.
Good Morning Ishan,
I spent a summer as an intern on a trading desk once, and realised fairly quickly that I was not very good at it. This was long enough ago that good old public forums like Stack Overflow and Reddit’s r/learnpython were still the “go-to” over ChatGPT for coding advice.
The fun part of my job was making wild hypotheses about the market and hoping they work. All the rest—writing code, fetching data, learning new strategies—made me yawn around a little too much for my manager’s liking. But the same friction that deterred me from turning an idea into an actual trade is also the friction large language models (LLMs) have been easing remarkably fast ever since.
An HSBC survey of about 1,000 affluent Indian investors released in June [found](https://ibsintelligence.com/ibsi-news/ai-becomes-the-top-investing-tool-for-indian-wealth-clients/) that 86% of the respondents are now using AI in their trading flows, which is the highest share of any country the survey covered, above China, Singapore, and the US. 42% of them [counted](https://www.businesstoday.in/personal-finance/investment/story/ai-makes-64-of-affluent-indians-more-willing-to-take-investment-risks-survey-539044-2026-06-25) AI-powered tools among their leading sources of investment ideas, second only to China’s 48%.
But individual investors are not the only invitees to the LLM gala.
“Finfluencers”, or social media content creators who share financial advice, are stacking ChatGPT prompt-packs on top of the tips, courses, and Telegram bots they were already selling. The internet is also flooded with [guides](https://www.scribd.com/document/903739959/50-ChatGPT-Prompts-Short-term-Traders) like “50 ChatGPT Prompts for Intraday & Short-Term Traders”, and entire prompt libraries, almost all of them opening with some [variant](https://www.repleteequities.com/blog/chatgpt-for-stock-market-analysis-in-india-2026) of “Act like you are a professional Indian market analyst”.
And if prompts feel like too much effort, Github, Microsoft’s developer platform, is full of open-source trading bots that plug an LLM into your brokerage account, allowing a simple chat with, say, Claude to drive your trades.
It appears that LLMs are becoming more and more embedded into markets—from every direction.
The premise behind this whole movement is essentially that AI is on its way to leveling the playing field between individual and institutional traders, and that early movers get a short, but glorious window of easy money before the rest of the market catches up and closes it.
But still, there is a catch. LLM usage is almost entirely concentrated within three models—OpenAI’s ChatGPT, Google’s Gemini, and Anthropic’s Claude—and a growing body of academic work has begun documenting something [specific](https://arxiv.org/abs/2507.20957) about what these models tend to do at scale.
LLMs, by design, are non-deterministic. No two answers are ever identical, even to the same prompt. But run the same kind of query enough times, across a large enough sample, and a distribution emerges. When it comes to financial markets, LLMs have been shown to have systematic biases in that distribution. Biases not toward any particular stock per se, but toward stocks with certain characteristics.
They [skew](https://arxiv.org/abs/2507.20957), for example, toward large-cap stocks over small ones, toward technology over other sectors, toward “contrarian setups over momentum”, and toward buying rather than selling. The paper argues that since major LLMs are trained on broadly the same universe of public financial writing, they end up sharing the same systematic biases in the aggregate.
Which is a strange kind of level playing field. The retail trader gets tools that, in the aggregate, make her more predictable to the very institutions she thought she was catching up to.
In a June podcast, Osman Ali, the global co-head of Goldman Sachs’ quantitative investing arm, put it plainly. He said, if you ask the same model the same kind of question, you get the same type of answer, which means investors [pile] into the same type of securities at roughly the same time and prices get pushed away from any sort of fundamental value.
Whether or not retail investors were consciously using LLMs to make their decisions, Ali said, the crowding effect was already visible. Broad LLM use had produced “a different type of predictability and inefficiency in the market.”
Millions of retail investors using, essentially, the same two chatbots may not necessarily democratize markets. Osman claimed that this also makes retail behaviour highly predictable. His team, he added, had begun “spending a lot of time” modelling how retail was using AI, so they could see the trades coming before retail placed them.
An academic [paper](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=6350140) from March takes an especially ingenious approach to this question.
Xiaoxue He wanted to understand what ChatGPT was doing to the US markets, and realised she could study it by studying retail trader behaviour every time the chatbot crashed.
Each crash was, in effect, a natural experiment. If ChatGPT was really substantially shaping how retail investors traded, there would be a discernible change in market behaviour when retail traders lose access to the LLM.
And there was. Retail trading volume dropped by about 6% every time ChatGPT crashed, which was itself striking, because it meant a meaningful share of American retail activity was, in some way, being routed through a single LLM.
Markets, in principle, work because different people show up with different views. Some see a stock as undervalued, some as overvalued, some sell into a rally, some buy into a fall, and it is precisely this disagreement that keeps prices honest.
Xiaoxue found that when ChatGPT was on, that disagreement tended to thin out. Retail investors began interpreting the same stocks the same way, and the small, useful frictions that let a market discover a fair price began to erode.
But what about in Indian markets?
A trader at an Indian proprietary firm told me his desk had been running strategies built around herding behaviour in retail investors, and those strategies had started performing meaningfully better in the last few months. There was no clean way to prove what was causing it, he said, but a good guess was that it came down to LLM-assisted trading.
In fact, SEBI too, in its consultation paper on the responsible usage of AI and ML in Indian securities markets, explicitly flagged the risk of “herding and collusive behaviour” arising from widespread use of common models and datasets by large cohorts of market participants.
Be that as it may, this argument only holds if ChatGPT is the one doing the actual thinking. And that is not necessarily the case. LLMs have also powered a whole new class of infrastructure builders on the ground.
Rajandran R is one of them. A long-time systematic trader, he built Openalgo, a self-hostable, WordPress-style platform that lets a non-programmer build and deploy a trading strategy without writing a single line of code.
Rajandran has watched this shift happen room by room.
At an algorithm trading meet he was hosting recently, he said roughly 400 people between the ages of 25 and 70 had shown up, and “almost 80% of them were already using ChatGPT or Claude to help with their investing journey.”
However, from Rajandran’s vantage, Indian retail is nowhere near the point where the LLM convergence effect would begin showing up in the market.
Most of the retail traders he sees use LLMs for execution, not for idea generation. “I have a design in my mind. I convert that design into code using AI”.
However, the trader at the proprietary firm also offered a warning. “It is only by chance that an LLM will actually come up with a profitable trading strategy all by itself,” he said. “[If] LLMs can find a piece of information, the market has most likely already priced it instantaneously, and any profitable signal has already decayed.”
Still, in the rare case your LLM buddy does hand you a profit-making formula, don’t tell anyone. As an ex-trader friend once told me, “No one who makes money opens their mouth, and no one who opens their mouth actually makes money.”
Words to trade by.
If you have any questions, feedback, or thoughts for the piece, please do comment or write to us at kaching@the-ken.com.
See you next Thursday!
Regards,
Mutasim
Where is your alpha piling up?You use AI every day. Every prompt you write, every draft you fix, every decision you talk through with a chatbot leaves a little of your judgment somewhere. The question nobody stops to ask: where? Somewhere you own or somewhere you rent, on someone else’s servers, or under someone else’s terms? We built a five-minute audit to answer exactly that. It ends with a verdict on how dependent you actually are. |