---
subject: "Learnings from yet another 'blitzscaling' stage hiring excercise"
from: "Arnav Gupta from system bashing <systembashing@substack.com>"
to: ""
date: 2023-07-01 07:00:31
labels: ["Arnav Gupta", "CATEGORY_PERSONAL", "IMPORTANT", "INBOX", "UNREAD"]
label_ids: ["Label_2739595779997728054", "CATEGORY_PERSONAL", "IMPORTANT", "INBOX", "UNREAD"]
---
|
So I find myself taking 8-10 interviews a week right now, and whenever you're in a hiring storm - out comes a lot of insights into the interview process, and potential learnings for people (both on hiring and job-searching sides).
So thus starts a thread. 🧵
This is my 3rd time in the middle of a large, long drawn, hiring "campaign" for a big team about to expand into a large team. (Done it twice before at Zomato and Target - where you have a 50-60 headcount to fill, over a period of 2-3 months, across the usual job roles).
Over my time running engineering teams, trying to wrangle with why engineering productivity is low, I have come to the conclusion (that I guess all tech leaders come to) is that the malaise lies in engineers not "aligning" to what the "product" and/or not being able to communicate well to the product/business/design folks.
The other learning has also been about coachable gaps vs non-coachable gaps. (Something that [@jiten](https://substack.com/redirect/132a6c3b-9816-474d-90b1-c4a75de6e7e7?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) talks about a lot - and I picked up when first talking to him on my podcast).
A younger version of me would have rejected candidates on gaps which are coachable, now I don't
The intricate part about 'coachable gaps' is also the context about what are my capabilities *right now* to coach.
At a $200B Fortune 50 company with an internal 'university' that teaches people communication better than a Mass Comm degree, communication is a coachable gap
Hiring for Golang, and finding a candidate who is a excellent backend engineer as such - with solid system design skills, and side projects to show for - written in a scalable manner - but not in Go (maybe Java or Nodejs for eg) - you have to decide whether Go syntax itself is coachable?
The answer lies in whether you already have a few senior Go folks in the team who can handhold people into writing idiomatic Go syntax, setup CI/CD and lint rules and frameworks in place to make sure people do not write Java-style code in Go (happens more than you can imagine)
Anyway after a few rodeos, burning my hands in different ways while managing teams and running recruiting, by now, I have come to one very important aspect each I want to look for, while hiring junior and senior engineers respectively.
For junior engineers - it is typically low level design decisions.
The two red-flag ends of the spectrum are
very un-extendable, use-case specific, hardcoded, hackathon-style code - without the self awareness of its limitations
over-engineered, 'Clean Code' type stuff
So the typical type of way I go about figuring this out is, 10-15 min into the interview, after the exchange of pleasantries, I share an API endpoint which has a bunch of photos or files, and ask them to download those, and sort them into folders based on some parameters.
I usually ask people to turn off camera, mic and for first 30 min, no need to screenshare. Be on the call if you want to ask anything, but code as if no one is looking. Google, Copilot, whatever you want to use is ok.
30 min later share screen, and we pair for what's left
Typically people can get to 60-80% of the requirement implemented in the 30 min, and we get to pair on the remaining parts.
Now (1) is fine, if the person is aware of it. Many give the disclaimer themselves "this is harcoded, but I'll extend if an use case comes" - GREAT!
But more often than not, people aren't aware.
Once the pairing starts - and I ask, what about I want to download the response in pages? And you see them go "oh shit I didn't think of that" - now that's where I get uneasy if that happens across all the design choices.
Otoh, (2) happens much more infrequently. But when it happens, it is quite a ridiculous outcome.
Usually someone would have come with an Adapter, an interface and a decoupled impl, a class to define the response, the file name, an enum for even binary parameters etc
The funny part is - it is more often than not a symptom of people who just *loooove* writing code, even more than running it.
Once you try to run their code, and you find it doesn't run in the first attempt, because not all cases have been thought of, and in 30 min if you focussed more on writing 'Clean Code', you'd have not had much time to actually run it and see if it works.
And it is an absolute red-flag for me to see 50+ lines of code written before even running it once. You have to keep running and seeing after every few lines
Now why are these things I index more on? Because these are more about 'nature' of person and not knowledge gaps.
Jumping the gun and not considering what reqs might change in future, or being so much in love with the process of writing code that you don't test it are not things in my current context, and timeframe, I can consider 'coachable gaps'.
These are not unfixable problems. But the type of coaching it needs, and the time it takes - maybe a coding bootcamp will have, but a small fast-moving product engineering team won't.
system bashing is free today. But if you enjoyed this post, you can tell system bashing that their writing is valuable by pledging a future subscription. You won't be charged unless they enable payments.