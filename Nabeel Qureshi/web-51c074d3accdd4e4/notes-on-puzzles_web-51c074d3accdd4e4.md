---
id: "web-51c074d3accdd4e4"
subject: "Notes on Puzzles"
from: "Nabeel Qureshi <nabeelqu@substack.com>"
to: ""
date: 2023-07-11 12:30:33
labels: ["Nabeel Qureshi"]
label_ids: ["Label_2768118641859383776"]
source_url: "https://nabeelqu.substack.com/p/notes-on-puzzles"
origin: "backfill"
---
1.
I mostly don’t play chess anymore — it’s too addictive, and tends to take over your brain in a way I don’t like — but one habit I’ve retained is solving puzzles. It’s a mental warm-up, a way of occupying my brain when I don’t want to mindlessly scroll.
Along the way, I came across a fantastic book called [Think Like A Super-GM](https://www.amazon.com/Think-Like-Super-GM-Michael-Adams/dp/1784831670), by Michael Adams and Philip Hurtado. The authors take 100 or so chess puzzles, of varying difficulty, and then ask chess players of different skill levels (amateur to grandmaster) to solve them, while recording their thinking process out loud.
It turns out comparing the thought process of less skilled vs. more skilled players gives you many useful insights! (I’d love to see this concept used for books in other disciplines.)
The lesson I found the most striking is this: there’s a direct correlation between how skilled you are as a chess player, and how much time you spend falsifying your ideas. The authors find that grandmasters spend longer falsifying their idea for a move than they do coming up with the move in the first place, whereas amateur players tend to identify a solution and then play it shortly after without trying their hardest to falsify it first. (Often amateurs, find reasons for playing the move -- ‘hope chess’.)
Call this the ‘falsification ratio’: the ratio of time you spend trying to falsify your idea to the time you took coming up with it in the first place. For grandmasters, this is 4:1 — they’ll spend 1 minute finding the right move, and another 4 minutes trying to falsify it, whereas for amateurs this is something like 0.5:1 — 1 minute finding the move, 30 seconds making a cursory effort to falsify it.
This is a really interesting finding!
Let me explain with an example. (Obviously, you’ll need to understand the rules of chess, and chess notation, to follow all this; skip to section 2 if not.) Here is White to move:
Try and solve it yourself first. (Here’s a [Lichess board](https://lichess.org/analysis/4Q3/5pkp/2Bp1bp1/4p3/1P2P2P/5qP1/5P2/6K1_w_-_-_0_1?color=white) link. Note: the puzzle is rated advanced, and a 2000 ELO person got it wrong in the book).
Here is the difference between an amateur and a good player:
The amateur: “Huh, f7 seems weak, what if I attack it again? Bd5 does that. Ok, so Bd5 and next move I play Qf7+. That’s got to be winning”. At this point the amateur will conclude they’ve solved the puzzle. (Note that they didn’t consider the opponent’s move at all.)
The good player: “Ok, I notice f7’s weak. Let me analyse Bd5. What’s the strongest reply — can I prove this wrong somehow? What would I play if I were Black? Oh wow, there’s Bxh4! Now if gxh4 then Black has a perpetual check (repeat Qg4 - Qd1 forever), and it’s a draw.”
Note that the good player hits on a potential right answer but immediately dives into trying their hardest to prove it wrong, as though they were the opponent, and they find that Bd5 leads to a draw (not a win). This leads them to the correct answer, which in this case is Qd7 -- this covers the g4 square, so that now if black plays Bxh4 white can safely recapture the bishop without worrying about perpetual check.
This skill of finding the best move for your opponent turns out to be very hard in practice. [1]
2.
It’s hard in real life, too: vanishingly few people are meta-rational enough to try really hard to falsify their own ideas. Your brain really wants to find reasons to support what you believe. It’s an unfamiliar and strange mental motion to invert that, and find the strongest arguments against your own beliefs.
But this isn’t a catch-all trick. There are important disanalogies to this in life, too. Many scenarios in life have the following properties:
(1) You have to “try it and see”; there aren’t definitive, computable answers
(2) Your degree of belief partially determines how successful you are
For example, should you launch that risky project - say, a startup?
If you spend 1 hour coming up with the idea and 4 hours coming up with reasons not to pursue it… chances are you’ll probably find some compelling-seeming reason why you shouldn’t bother.
The most effective people seem to be good at accepting the dissonance and going forward with things anyway (after thinking rigorously about them!), knowing that you can always find reasons why a thing won’t work. I think startups are an example of #2: your success is partially determined by how much conviction you have.
The “you have to try it and see” property is also counter-intuitive; it implies that your initial idea often doesn’t matter except as a starting point. This concept is often taken to mean “ideas don’t matter”, which is not what I’m saying here. It’s more like: the idea determines what maze you’re exploring, which is important — if you start out trying to find a cure for diabetes you’re unlikely to end up working on a payroll SaaS company, for example — but it’s going to change as you go along and learn more about reality.
This is another area where I find that the personality of founders diverges from some smart engineers or scientists I’ve known: the scientist/engineers are good at analyzing the idea and finding reasons it won’t work (witness the negative Hacker News comments in virtually every successful startup launch, e.g. [Dropbox](https://news.ycombinator.com/item?id=8863)), because that’s how they’re trained to think. This skeptical mindset is adaptive in the engineering and science context — you have to find all the weak points in a system or theory, or else you’re not doing your job right.
It’s not as simple as “founders are optimists, scientists are skeptics”, though. I once asked a few founder friends what they’d have told themselves about startups, and the most common one was that you know when something isn’t working way before you’re actually able to admit it to yourself, and it’s best to save yourself time by admitting that it’s not working sooner, cutting your losses, and iterating quicker. You want the cycle time to be as fast as possible: the more cycles, the higher your chances of success overall. [2]
3.
Conviction that there is an answer. There’s a cruelty to problem-solving: if you are solving exercises that are collected in a book, it’s implicit that each of those problems has a solution. Puzzle books are a forgiving problem-solving environment in that way. It means that you can bang your head against the problem for hours, because you know that there is a findable answer, and that you will find it if you simply apply enough determination and search hard enough. Unlike real life, where you have to try it (and sometimes waste a lot of time).
This lesson hit home when I was trying the following problem from Larson’s book, “Problem Solving Through Problems” which is a collection of math problems (mostly Putnam or Olympiad):
I beat my head against this one for ages, and couldn’t find any traction. It was very annoying. (You should try and write out the sequence yourself, and see what approaches you’d take to prove that “6” occurs an infinite number of times here. I found it quite slippery. Noting that I’m not a mathematician at all, so I’m probably missing some obvious-to-mathematician techniques here.)
Probably if it wasn’t in a puzzle book I’d have given up; but I knew there must be some trick. Larson groups his problems under various headings, and this one, early in the book, is under “check concrete cases”.
So I wrote a short program that would print out the first 300 items in this sequence, and stared at it:
I noticed there was a pattern – a bunch of 8s, then a bunch of 6/4s, then a bunch of 2/4s, and then a bunch of 8s again. I started playing around with the 8s, noting that 8*8 (=64) contains a 6. If you could show this keeps recurring, you’d have proven that there are an infinite number of 6.
Two 8s peters out (8, 8 -> 6, 4 -> 2, 4 -> 8).
But three 8s:
8, 8, 8 -> 6, 4, 6, 4, 6, 4 -> 2, 4, 2, 4, 2, 4 -> 8, 8, 8...
This is a cycle! It recurs infinitely! And it contains a 6! QED. But I’m not sure I’d have found this without the conviction that there was a possible solution (otherwise, why would Larson have included it in the book?).
Real life is not this clean; frequently you dive into an idea maze and the answer turns out to be “it’s too hard for these structural reasons, and unless you fix these structural reasons there isn’t a sufficiently scalable thing here” or something like that — this seems to be the fate of a lot of startups that tackle sectors like education or health, for example. This can be painful and suck up years of people’s lives.
This is why I think of founders and scientists as courageous in precisely the same way: they are driven by a faith that there’s a findable answer there, and they’re willing to dash themselves against the rocks and risk failure to get to that answer. And in many cases it turns out that there isn’t one, at least not by the paths of the maze that they’ve been exploring.
4.
I think of this when reading [Newton’s notebooks](https://www.newtonproject.ox.ac.uk/view/texts/normalized/THEM00092). They’re not structured, they’re more him writing down questions about literally everything, and sketching out little proofs / thoughts.
They’re breathtaking – the sheer diversity of questions he asks, and the audacious scope of his conjectures. And what’s striking is he wonders – profusely – about very small physical things that a child might wonder about (I modernized the spelling):
“Why is breath or sweat seen in winter more than in summer”
“Why water is clearer than Vapors”
“Why flints do break upon a soft thing sooner than a hard one”
“Why does water freeze first & most next the Air”
-- but in between these very physical questions are questions of much grander scope, like:
Whether the soul is immortal
What the first matter would have consisted of
“Whether Moses his saying in Gen the 1st that the evening & the morning were the first day etc. do prove that God created time.”
It feels weird to read these intertwined, since they seem like very different kinds of question to us. But this is only because we know that the physical questions are answerable in terms of science (because we have pretty good answers to them now -- often thanks to Newton!), and the second type of question isn’t, at least as far as we know.
But it’s possible that from Newton’s perspective, both of these kind of questions were equally mysterious, and for all he knew he could find answers to both kinds by trying really hard! [3] Before Newton, maybe people were more confident about the theological questions – (“yes, obviously the soul is immortal”) – than about the physical kind – (“well, I have no idea what makes the planets move!”). Newton made the mysterious banal.
5.
Another thing I’m struck by, in puzzles, is the role of really wanting to know the answer. You might say, facetiously, that a scientist is someone who really wants to know the answer, to a degree that is pathological (and maladaptive) to a normal person. (Elsewhere I referred to this trait as the ‘[will to think](https://nabeelqu.co/understanding)’, after Shockley).
Complacency afflicts us all, to some extent. Solving chess puzzles makes this blindingly clear, because how good you are at them is inversely related to how complacent you are. Our brains want to stop thinking as soon as possible, probably because thinking hard takes up a lot of energy and if you didn’t curb that impulse… well, you’d get a very impractical scientist or a mathematician, who spent all their time lost in thought. For most of us, you have to actively fight complacency, which comes in the form of “yeah this answer seems good enough”.
There’s a striking passage in Jonathan Rowson’s book “[Chess for Zebras](https://www.amazon.fr/Chess-Zebras-Thinking-Differently-about/dp/1901983854)” where he’s tutoring a student on a puzzle. The student gets the ideas in the puzzle, but doesn’t quite make the leap to the answer. The tutor gets frustrated, because he knows the student can get to the answer (paraphrased):
Tutor: No. You were sort of right about shortcomings. You see this position is about problem-solving, as most chess is. You have to be really persistent if you want to get somewhere...
[Student says something about needing to improve on board vision]
Tutor: Well, to be honest, I think you have that. You can see that White has more space, the better bishop, etc. And you can see that you need to get the king in ... thus far you are up there with the best. You also notice that Bxg6 is an issue.
Student: But it’s how to do it!
Me: Well that’s what we are on about here. What stops you, I think, is a combination of not really believing you’ll get it and not really caring. Is that too harsh – or is it somewhere close to the truth?
Complacency hits especially hard in king and pawn endgames, when king moves that seem “good enough” can in fact be losing or drawing, and you really have to calculate each and every move very exactly to figure out a win. You have to be unreasonably thorough and check every single move, to a degree that seems quite pedantic. [4]
I notice this in people who are good at science, too: they are really, really thorough and check every edge case.
This tendency can, again, be maladaptive in some context. I’ve noticed that sometimes good scientists have trouble when cast into more CEO-like / founder-like roles, including things like:
Going down ‘rabbit holes’, i.e. getting super interested in one particular aspect of the business to the exclusion of all else
Difficulty in making themselves interested in “less interesting” problems (e.g. sales, operations), resulting in e.g. mismanagement of finances because they weren’t willing to get into the weeds of the ‘boring’ area
Wanting more information before making a decision than it’s possible to really get and moving too slowly as a result
I think this is a consequence of what I’ll call “scientist-brain” vs. “founder-brain”. (Yes, I’m generalizing, many exceptions exist and it’s not this clean in real life.)
Scientist-brain is unreasonably thorough and wants to check every single case; is very curious about things and willing to follow that curiosity, but doesn’t have a natural check on this process; and prefers working on things that are interesting to them, finding it extremely painful if this is not the case. This is great when you are doing science, because you need the ‘driver’ to be curiosity, and small details matter.
But it’s often bad in CEO or founder type roles, where you often need to move fast, decide based on imperfect information, maintain context on 10+ workstreams including sometimes intellectually boring ones, and above all not go down rabbit holes unless they’re super critical to the business. The tragedy of CEO roles is that you’re often not spending much time on the most interesting things at all.
(This is also why CEOs/founders want you to be terse in communication and give them the bottom line up front. CEOs are holding so much in their heads already that unnecessary details have a high marginal cost.)
Again, these are very, very broad generalizations! And there are some very successful scientist-founders. But I think these are two very different archetypes, and paired together they often make a stellar team.
6.
Chess players usually end up converging on a consistent thought process for every move. [5] Thought process is useful, and it’s often helpful to have a laundry list of these techniques to apply to the problem at hand. But it’s not as if giving you the thought process is magically going to lead you to the right answer.
One constraint you run up against hard when doing chess puzzles is working memory. The more context you have to hold in your head, the harder it is to make more calculations.
Once, frustrated by my accuracy rate, I decided to allow myself to use a scratch Google Docs page to record all my calculations, as an exercise. My accuracy shot up; I rarely got anything wrong. Being able to write things down freed up ‘mental scratchpad’ space, which made my calculations more accurate overall, and made it easier to check I hadn’t missed anything. [6]
I’m pretty sure people who are great at chess have better working memory than people who aren’t. And it seems like working memory is innate and fixed, though I’d welcome any counter-evidence. [7] Indeed, Adams and Hurtado find that grandmasters have better intuition and identify the right answer very quickly; they calculate far quicker and more accurately than amateurs; in general, it seems that visualizing and thinking far ahead is much easier for them than the amateurs, the result of thousands of hours of practice and probably innate talent. I think this is clearly true of math too: more gifted people traverse the maze faster, and seem to have a preternatural instinct for what’s going to turn out to be a blind alley versus what’s not.
I’ve always been struck by Jonathan Rowson’s account of playing Grischuk, a super-grandmaster, and analyzing the game together with him afterwards:
During the post-mortem I was deeply impressed by the fluency and depth of his analysis, and the sense of balance in his assessment of positions. To be honest, it left me feeling a little deflated. It was abundantly clear to me that he was a different class of player. I could perhaps compete with him in a single game, but not in the long haul. There aren’t many players I feel that way about, but Morozevich made the same impression, and to a lesser extent, Kasimdzhanov, Aronian and Sutovsky. There are some players who just seem to function a few orders of magnitude higher – as if they are qualitatively stronger, speaking a different language. (Jonathan Rowson, Chess for Zebras)
Some people are just different. [8] Still: lean into what you’re good at, practice, and you can always get better!
7.
Anyway, there are other lessons that I didn’t go into here, because I don’t want to spoil the entire book(s). Needless to say, they contain many excellent hacks for problem-solving. So if all of this piqued your interest, I’d highly recommend:
Think Like A Super-GM, Adams and Hurtado ([Amazon](https://www.amazon.com/Think-Like-Super-GM-Michael-Adams/dp/1784831670))
Problem Solving Through Problems, Larson ([Amazon](https://www.amazon.com/Problem-Solving-Through-Problems-Problem-Mathematics/dp/0387961712))
Think Like A Grandmaster, Kotov ([Amazon](https://www.amazon.com/Think-Like-Grandmaster-Alexander-Kotov/dp/0713478853))
How To Solve It, Polya ([Wikipedia](https://en.wikipedia.org/wiki/How_to_Solve_It))
Chess for Zebras, Jonathan Rowson ([Amazon](https://www.amazon.com/Chess-Zebras-Thinking-Jonathan-Rowson/dp/191146583X))
Thanks to [Tyler Cowen](https://marginalrevolution.com/) for feedback on a draft.
Footnotes
[1] In online chess games, a nice hack to make this easier for yourself is to flip the board to the opponent’s perspective when you’re trying to decide if a move works or not. Say you play the move - what would you play if you were the opponent now?
[2] This is one thing that makes founding hard: what drives you to search is blind faith that a solution is possible, but you also have to know when to call off the search, and it’s hard to calibrate when to do this because the feedback signal is sparse. Maybe you gave up two weeks too early, and if you’d simply persisted you’d have struck gold. Didn’t the Airbnb guys persist for a whole year with no traction or signals of success before taking off? Wouldn’t they have been rational to give up after the fifth time it didn’t work? Well, it would have been, but they didn’t.
[3] I originally read this point in a PG essay, “[The Risk of Discovery](http://www.paulgraham.com/disc.html)”.
[4] Two examples of complacency, one from chess and one from math, which I omitted from the main text because they’re wonkish. ([Lichess link](https://lichess.org/analysis/2kr4/ppp1q3/b3prnb/2Np3p/3Pp1pP/Q1P1P1B1/P3NPP1/1R2K2R_w_K_-_0_1?color=white)):
You notice a few things immediately – the open b-file with the white rook pointing at the king, the white knight constraining the king’s escape on d7 – and you start looking for mating moves. The obvious move that comes to mind is Qb4, lining up more pressure along the b-file and threatening Nxa6 followed by Qb7, which “looks winning” -- note the bishop pointing at c7 too.
In an online blitz game, with no time to think, I’d play Qb4 100 times over without thinking twice. It’s the sort of move chess players would call “natural”.
But this is complacency – note that:
(1) I haven’t examined other moves, including more forcing ones
(2) I don’t actually have a concrete winning line. I haven’t bothered to think hard enough to get to the level of working out my opponent’s replies. I’ve hand-waved “this looks winning”.
It turns out Qb4 is a fine move for White, but Black can defend. The best move for White is actually Rxb7!, and after Bxb7 Qxa7 Black can only stop checkmate on b7 by giving up their queen.
Another example of complanency from the math context. Here’s another Larson problem:
Since you want to maximize the product, you can guess intuitively that smaller numbers (2s and 3s) are going to get you to a larger final product, since that gives you more multiplications. A 4 is just 2*2 (and 2+2) so the solution won’t involve any 4s, and anything larger than 4 is going to be too big.
It’s easy – but wrong – to guess from this that the maximizing answer is probably either 3^333 + 1, or 2^500. You can then go down a rabbit hole to figure out which one is bigger, or use a calculator and find that it’s 3^333+1. Complacency would stop here and conclude that that’s probably the answer.
But it’s not! It’s helpful to work out some smaller examples first, such as 10:
5+4+1 = 10, and 5*4*1 = 20
4+3+2+1 = 10, and the product is 24
3+3+2+2 = 10, and the product is 36
Clearly, the right answer never contains a 1. So revisiting the 3^333 + 1 answer, the ‘next’ solution would be 3^332 + 2^2, which is indeed the correct answer.
[5] When doing a puzzle, you’re typically told to examine checks, captures and threats first -- in that order.
The Russian chess player Alexander Kotov wrote a famous book, Think Like a Grandmaster, which he outlines a more general thought process for every move and introduces the concept of the candidate move -- essentially, a plausible move in the position. His point is that you should list out all candidate moves first, before going into analysis of each one. Amateurs tend to find an interesting-looking move, and then dive in and analyze it, but it’s best to list all the plausible moves first so that you have an organized list of all the possibilities.
Larson has a similar set of techniques for math problems too. Unlike chess, it’s hard to have a consistent thought process for all math problems because they’re so different, so these lists tend to look more like a bunch of useful hacks: search for a pattern, draw a figure, modify the problem, choose good notation, consider extreme cases, and so on.
[6] Hence the GTD recommendation to write everything down: “your mind is for having ideas, not holding them”.
[7] [Gwern’s review of dual n-back](https://gwern.net/dnb-faq#n-back-in-general) is interesting here, but as far as I can tell the conclusion is that it’s unclear whether this has any real benefit to working memory.
[8] When you watch interviews with grandmasters about Magnus Carlsen, they usually identify a few traits of his that make him exceptional.
One of these is his insane chess memory (see [this YouTube video](https://www.youtube.com/watch?v=eC1BAcOzHyY&t=105s) for a vivid demonstration of this). Clearly, it’s the result of many hours and days of hard work. But there’s also some innate thing going on here.
Another is his chess intuition, which is chess player speak for “a disturbing knack for getting the right answer without any apparent effort, at sub-second speed”. There’s [a great video showing this at work here](https://www.youtube.com/watch?v=k1SCXb2WA2U) -- most players end up memorizing these endgames, but Magnus doesn’t, he works them out on the spot. At one point, he makes a very weird-looking move, the interviewer asks him why he made it, and Magnus says “That wins because, well honestly I don't know.” Similarly, at around 15:00, the interviewer asks if Magnus found the solution using the ‘key squares’ concept -- which most GMs would study explicitly -- and Magnus says in effect: no, it’s obvious to him on sight.
Another is that he’s insanely competitive, wants to win, and doesn’t get tired or let up even in extremely boring positions.
I’m sure he cultivates all of these things. But I’m also pretty sure they’re innate.