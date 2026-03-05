---
subject: "AI plays Pokémon, but so does π. Tesla's \"brand collapse.\" Neuroscience scaling laws. Why do I know all the songs …"
from: "Erik Hoel <erikhoel@substack.com>"
to: ""
date: 2025-02-27 16:18:15
labels: ["CATEGORY_PERSONAL", "Erik Hoel", "INBOX", "UNREAD"]
label_ids: ["CATEGORY_PERSONAL", "Label_2504961760700514996", "INBOX", "UNREAD"]
---
|
Table of Contents
1. Claude plays Pokémon. But so does the number π?
2. Evil numbers turn AIs evil. Great.
3. Researchers observe flies playing on carousels. Actually great.
4. Will Elon Musk get booted from Tesla after “brand collapse?”
5. Why do I know every song on the radio? I’m old.
6. Scaling laws for neuroscience.
7. From the archives.
8. Comment, share what you’ve found interesting lately, ask anything.
1. There I sat, listening to my daughter practice words during her nightly bedtime reading, while on a screen I watched the newest AI, Claude 3.7, live-stream its Pokémon play-through.
“Blue,” said my wife in the background, pointing to a splayed book.
“Boo!” said Sylvia.
“I also noticed that SWIFT’s HP has decreased due to the poison status, which reinforces the urgency of finding the exit,” Claude’s running chain-of-thought said on Twitch. It laboriously moved its character a few spaces to the right.
“Car!” said my wife. “Ar!” said Sylvia.
“Let me continue following this path to explore further eastward,” said Claude.
To explain: this week Anthropic dropped Claude 3.7, arguably tied for the smartest state-of-the-art AI that exists (e.g., it’s going to power [Amazon’s Alexa](https://substack.com/redirect/2781d67c-cb3a-48ce-bc42-e2315c4f9cd1?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)). Apparently Anthropic had been investigating how well Claude plays the old Pokémon Red/Blue [as a side project](https://substack.com/redirect/e2cdf193-b890-4066-95af-d65d1a0a8418?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), the very thing I once played on a gameboy. So they decided to livestream a play-through at launch, one that is still ongoing (you can [watch here](https://substack.com/redirect/171633df-52bf-400e-9e01-05a2517c6484?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)).
You might wonder why. After all, AI has been good at gaming for a long time, right? True. But those models were always fine-tuned for the game. This is just Claude itself, out of the box, using its general intelligence to look at screenshots taken every few seconds and make decisions about what button to press, just as a human would. Its slow gameplay is rendered quaintly adorable because its running “thoughts” are displayed next to what it sees on the screen.
So as my daughter learned to speak from the data in a few dozen children’s books, Claude, which has read the entire internet, played Pokémon, and I watched along with 2,000 other people as it talked to characters and fought battles and explored.
Observing it play, I learned things about AI I never had from reading academic papers, or even using the models myself in shorter sprints. This was a marathon. How modern LLMs will expand into agents was very much on display as Claude oscillated between impressively smart and unbelievably dumb.
How does it work? Normally, AIs can only handle so much context before they start to break down and go insane. The longer you talk to an AI, the more insane it will get, and the more mistakes it will make, and the more things it will forget, until it gets stuck in a loop. This is the main hurdle for AI agents.
Anthropic solves this by simply having Claude go through a summary process of its thoughts—where it is, what its quests are, what pokémon it has—about every 10 minutes. Then it “cleans up my context” (which might be the same as starting up a new chat, implying Claude “dies” thousands of times while playing), and then that summary gets fed to the new instance.
In one forest map, I watched it loop for about three hours between what it thought were exits but were really just tree stumps. This made me question whether the term “reasoning model” is accurate. As Einstein supposedly said, “The definition of insanity is doing the same thing over and over again and expecting different results,” and by this definition Claude is assuredly insane. It is hard to be scared of AI when you watch the smartest existent one get stuck in a corner for several hours, which is what happened. Currently, it has been running loops in Mt Moon for ~23 hours and just re-set the loop as the chat pleaded with it not to go north from a particularly troublesome ladder again.
In some ways, it was endearingly human-like. If it pressed the wrong button, its thoughts would be, “Oh, the game has taken me to this menu via a bug,” and it responded with “Lucky break!” when an attack by an enemy missed.
But it was subtly inhuman: e.g., I noticed it appeared impossible for Claude to stop having particular thoughts. At certain screens, it would always think that there was some visual bug, despite (a) there was no visual bug, and (b) it had had that thought every single time, which a human would stop noticing or caring about.
To me, this silly benchmark felt a lot more substantial and informative regarding “are we at AGI?” than academic questions. Claude is the [third highest scorer](https://substack.com/redirect/6b22888d-9cd6-45c2-a87b-a6b19e8cd5fd?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) on a PhD-level question set ominously titled “Humanities Last Exam” but meanwhile, its record in Pokémon is 3/8 badges.
Claude didn’t pursue fights efficiently, often making mistakes about how best to defeat opponents. People, in comparison, beat these games [without healing](https://substack.com/redirect/e38552b6-75f7-4a70-8e77-7058d3875c86?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) for fun challenges. Although there is a certain terror at its mere indefatigability, while watching I realized it is the forgiving structure of the game, wherein failure is an impossibility (you restart somewhere else should you lose, and all the maps push you in certain directions) that actually propels the model along as much as its own intelligence. E.g., a sign saying “Go Ahead” finally got it out of the 3-hour loop in the forest. It’s like bowling with bumpers.
Did you know the number π also can play Pokémon? Literally just the infinite number 3.14159… mapped onto button presses. It’s unfortunately been playing a different game version (for, oh, a [couple years now](https://substack.com/redirect/2c0c1326-fb53-409b-8faf-8cd11889657e?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)), but there it has gotten out of the starting town a few times and leveled up its characters to ungodly stats via random battles...
Subscribe to The Intrinsic Perspective to keep reading this post and get 7 days of free access to the full post archives.
| Subscriber-only posts and full archive | |
| The Intrinsic Podcast | |
| Open threads, AMA, competitions, etc |