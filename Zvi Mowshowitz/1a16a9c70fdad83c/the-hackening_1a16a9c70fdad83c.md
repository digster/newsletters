---
id: "1a16a9c70fdad83c"
subject: "The Hackening"
from: "\"Zvi Mowshowitz from Don't Worry About the Vase\" <thezvi@substack.com>"
to: ""
date: 2026-10-23 21:13:08
labels: ["CATEGORY_PERSONAL", "INBOX", "UNREAD", "Zvi Mowshowitz"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "UNREAD", "Label_3336704411007769646"]
---
Last week at a small conference, there was talk about a future event referred to as The Hackening. As in, within 6-12 months, many predicted that due to advanced AIs and AI agents the internet would become a severely hostile place. Some worried that this could rise to the level of ‘assume any phone connected to the internet is rooted’ and several people urged doing general crisis preparations on a personal level, in case of disruptions in supply lines, power, water or internet. It did not take long for things to escalate. The biggest hack is a flaw in PHP, which can be exploited to take control of the computer running any website suing an unpatched version of PHP. There are many others. On a personal level, you want to do at least some basic prep and get your security in order. It is cheap to do as a form of insurance, and being caught not having it when you need it is a large mistake. That doesn’t mean you should panic, or cancel travel plans or anything like that. But there is low hanging security fruit out there. Pick it. And So It Begins: PHP
They may have been in a rush due to attackers finding the exploit.
The PHP Bug Was Kind of a Big Deal
Things could have gone very, very badly, the same way Y2K could have gone quite badly if we had not done the work to prevent it. These days we are on rather tighter deadlines.
A lot of websites are going to go down permanently.
It’s not quite as bad as spor describes. PHP shipped minimal backports for 7.4, 8.0 and 8.1, but I would not want to be running those going forward.
On Your MarksNow the race is on to patch all the systems before attackers can go on the offensive. OpenAI is helping race to get that done to the greatest extent possible, and are looking for better methods for fixing vulnerabilities in time.
This one was important enough the NSA got in on the act.
We are going to need better procedures for updates. The best case scenario is that a defender finds the bug first, has enough time to figure out a solution and creates a patch. Then, the moment the patch is rolled out, every attacker gets what are effectively very clear instructions on how to exploit any unpatched systems.
Some software has a lot of bugs. Some of that same software powers the internet.
This Was Only the Beginning
The same day as the PHP vulnerability we also were treated to this:
And this:
And also this:
And this, probably nothing:
Some More HacksThings are steadily escalating. Get ready.
AI cyber is scary both because it will find new vulnerabilities, and also
Everything Will Be AttackedAs an example, AI will make it easier to probe essentially everything. Anything vulnerable will be hit. Even if there is no economic reason to do so, some people want to see the world burn, or want to see the West burn.
If I was the banks, I would absolutely not allow agents to authorize any transactions until I could verify the status and nature of those agents. They have huge downside exposure risk as do the customers. This isn’t crypto (derogatory). Soon days like this might be typical, or even quiet. After all, despite all the issues, life mostly continued as normal.
There is no clear line, contra Sacks, between ‘this is a clearly authorized agent’ and ‘this is clearly not an authorized agent.’ Agents Can Just Do Things. Hugging the FaceThe original rogue agent incident remains Hugging Face. I wrote quite a lot of posts on the situation, but they are poor explainers for a non-technical person. Luckily,
The information is mostly in the METR report, but in addition to being a story it organizes some of the data into a more highly readable form. Thanks to Raymond Arnold for putting a month of work in on this. I was able to help a little bit with the editing while at the conference last weekend, as were a number of others.
Also, there is a Netflix ‘instadoc’ called AI Gone Wild about the incident. I have not watched it. Get Daybreak NowEarlier this week
Everyone reading this who has something worth defending, try to get Daybreak and similar programs going now, before you are attacked. Do not wait.
I will not have sympathy for you if you choose not to do this. It is not as if getting access is difficult. You can mostly get it by asking nicely. Some People Need Practical AdviceIt is always a good time for basic personal-level advice. I think something around the level of Wildeford’s advice is wise. You are probably fine with less than that, but if you have to pick a mistake being too prepared is probably the better option.
Others recommend going a bit further:
Things are going to get worse before they may or may not get better.
Diffusion Is Slow Until It Isn’tAn excellent point from Dean Ball: Either you believe in ‘bottlenecks’ and slow diffusion, or you do not. You cannot declare ‘everything is fine’ unless you wait long enough to verify they are not becoming non-fine. Partly this is bottlenecks, but a lot of it is purely that diffusion and figuring out how to use the new tools takes time and iteration and People Don’t Do Things.
The full Also, no, GLM-5.3 does not fully have The Juice that Mythos and Astra have. That day will come, and GLM-5.3 is the best cyber offense open model, but I believe GLM-5.3 is still substantially below the April line for this purpose, and thus remains more than six months behind even in ‘fast follower via mass fraudulent distillation’ mode.
|