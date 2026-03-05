---
subject: "How experienced engineers get unstuck in coding interviews"
from: "The Pragmatic Engineer <pragmaticengineer+deepdives@substack.com>"
to: ""
date: 2025-08-26 16:33:18
labels: ["CATEGORY_PERSONAL", "INBOX", "The Pragmatic Engineer", "UNREAD"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_6413324878686416177", "UNREAD"]
---
👋 Hi, this is Gergely with a subscriber-only issue of the Pragmatic Engineer Newsletter. In every issue, I cover challenges at Big Tech and startups through the lens of engineering managers and senior engineers. If you’ve been forwarded this email, you can
|
In-person coding interviews are returning to Big Tech and some startups in 2025 now that LLMs are too good at solving coding challenges, and a plethora of tools offer invisible AI “overlays” which help candidates to cheat during remote interviews. As a result, remote coding interviews today serve up more noise and less signal than ever. In response to AI “helper” tools for remote interviews, many employers are returning to the in-person interview format – while others accept AI tools and adapt their processes like [Shopify](https://substack.com/redirect/a5370e0c-fdaf-4122-a801-25416ae53f61?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) has.
Today, the most popular interview type remains the algorithmic coding interview, in which candidates have an algorithmic challenge, a whiteboard, and 30-60 minutes to come up with a solution. So, how do you succeed in this new wave of old-style tech job interviews? For some professionals, the approach may not be crystal clear if remote interviews have been the norm.
To find out, I turned to one of the best people to tackle this question: [Mike Mroczka](https://substack.com/redirect/5c16d1fb-f3fe-47f4-bcfd-5f0c834f6a7d?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), lead author of the book [Beyond Cracking the Coding Interview](https://substack.com/redirect/890b0cf6-b5da-4fec-9e89-a24ff5eb66fd?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). It is the official sequel to the classic coding interview preparation “bible,” [Cracking the Coding Interview](https://substack.com/redirect/03c2d03f-e9be-49f5-b35f-05352a75239b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). Reading the original title first is not a prerequisite for Beyond Cracking the Coding Interview, Mike says. If you are interested in this updated book, you can [read nine chapters for free](https://substack.com/redirect/40992cd0-82d1-4f42-a70d-eadca0db9956?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) (the book has 43 chapters in total).
Mike worked at Google for nearly 4 years, and has been a dedicated interview coach for a decade. In this article, he shares his approach for acing in-person interviews with a framework aptly named “MIKE,” and advice and tactics for getting unstuck in tough coding interviews. We cover:
The reality of interviews at Big Tech Some data suggests so. After all, the process has worked for decades and is well understood, meaning it’s unlikely to have been discarded and forgotten. Also: the interview / reality disconnect
MIKE framework: a framework for getting unstuck during coding interviews
Minimally sketch the naive solution
Identify upper and lower bounds
Keywords in the problem
Employ boosters when stuck
Importance of preparation and practice. Practice makes all the difference: consider recording yourself in mock interviews, then analyse your performance
The bottom of this article could be cut off in some email clients. [Read the full article uninterrupted, online.](https://substack.com/redirect/8fba4e9b-08c0-42f3-842d-a04ec9f5ad76?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
Several companies have started to embrace AI coding tools for interviews, including Meta, which is currently trialing them. Elsewhere, [Canva](https://substack.com/redirect/9444ab47-429f-4e0b-8139-4e7420980634?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) and [Shopify](https://substack.com/redirect/a5370e0c-fdaf-4122-a801-25416ae53f61?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) (as mentioned above), encourage candidates to use AI tools during interviews. But adoption like this is far from being a death knell for tried and true interview formats, according to research.
Data from leading mock interview site [interviewing.io](https://substack.com/redirect/b44a195f-cbce-4a33-b961-8d8416f41c11?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) shows AI has overwhelmingly NOT made algorithmic interviews redundant at Big Tech. It surveyed 53 Big Tech interviewers, mostly at FAANG companies – Facebook, Amazon, Apple, Netflix, and Google – and also at a few large scaleups like Stripe. [Aline Lerner](https://substack.com/redirect/a10de535-0fcf-4abd-a4fb-304260074e8a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), founder at interviewing.io, summarizes the data collected:
“Answering the question of whether AI has changed interview processes:
93% of respondents have confirmed that AI has not driven any changes to their interview process.
Of the 7% who reported changes, these consisted exclusively of adding cheating detection tools to their interviews, rather than modifications to the interview format itself.
None of the interviewers reported that their companies are moving away from algorithmic questions. Some interviewers did note they're no longer asking questions taken verbatim from LeetCode. Others are making modifications to pre-existing algorithmic questions that make those questions harder for LLMs to answer, asking more follow-up questions of candidates, and/or are incorporating additional discussion into interviews.
It looks like algorithmic questions are here to stay – at least for the foreseeable future.”
At search giant Google, they are doubling down on in-person interviews because of AI. In June, CEO Sundar Pichai confirmed Google is bringing back in-person interviews on the Lex Fridman podcast (emphasis mine):
Lex Fridman: “Google has legendary coding interviews, like rigorous interviews for the engineers. Can you comment on how that has changed in the era of AI? The whiteboard interview, I assume, is not allowed to have some prompts.”
Sundar Pichai: “We are making sure we’ll introduce at least one round of in-person interviews for people just to make sure the fundamentals are there. I think they’ll end up being important, but it’s an equally important skill. Look, if you can use these tools to generate better code, I think that’s an asset. So overall, I think it’s a massive positive”.
Alternatives to in-person algorithmic coding interviews have downsides. The most popular other options are:
Remote algorithmic interviews. Unfortunately, invisible “AI helper” software displays answers in realtime, and is slowly rendering this type of interview useless. Plus, there have been incidents of “AI fakers”, where candidates pretend to be someone else, which also reduces trust in this format, as
[we’ve previously covered](https://substack.com/redirect/ff25babb-af77-4b4c-9f58-a0bb32458d97?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).Remote interviews that allow AI coding tools. This involves setting much more ambitious coding challenges, and doing away with algorithmic questions, like at
[Shopify](https://substack.com/redirect/a5370e0c-fdaf-4122-a801-25416ae53f61?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)and[Canva](https://substack.com/redirect/9444ab47-429f-4e0b-8139-4e7420980634?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).
Trial days or trial weeks. A valid criticism of 30-60 minute coding interviews in any format is that they don’t mirror the actual work of engineers. So, why not create an interview that does? Trial days and weeks are the result in both the remote and in-person format, in which candidates join a team and ship a feature to production. Linear [uses remote trial days](https://substack.com/redirect/66812e68-cdb1-4788-a311-ffa5e7a2d376?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) in their interview process, and Automattic holds [an async coding challenge](https://substack.com/redirect/5d705dc1-ec63-4c80-babf-8a202873c0a6?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) as the final “coding” interview, which can take days to complete. The downside is that trial days can add up to a week of time invested. Linear pays candidates for this, but the demand on time can make it hard for some people to commit to.
The biggest downside of in-person interviews is obviously the cost: candidates must travel to an office, and overnight accommodation may be required. Some employers like Big Tech companies usually foot such bills. For candidates interviewing on Fridays, this process might turn into a free city break, as happened when Uber flew me out from London to interview at its office in Amsterdam, across the North Sea.
With that, it’s over to Mike…
Market forces and AI-enabled cheating are changing technical interviews, by forcing a move away from verbatim LeetCode questions back to in-person interviews – or something else entirely. In this new world, knowing how to think outweighs memorizing lists of problems. That’s why we decided to write [a sequel to “Cracking the Coding Interview](https://substack.com/redirect/de2f0bdb-90a8-4df3-9743-5a1026695021?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o).” Our goal with this new book is to teach the “why” rather than the “what”, and to go deep into problem-solving approaches.
Let’s acknowledge the elephant in the room: data structure and algorithm (DS&A) questions have very little to do with software engineers’ daily lives. When was the last time you implemented a binary search tree from scratch, or used backtracking at work? For many people, the answer is “never, except in an interview.”
These interviews favor those with time to grind LeetCode. They focus on niche topics most engineers never use, which can make the process feel disconnected from reality, and frankly, a bit demoralizing.
Yet despite this, DS&A interviews remain the industry standard at most major tech companies. Why’s that?
It’s because hiring managers know something many engineers overlook: there simply aren’t better alternatives. Take-homes are easy to cheat on, and system design and behavioral interviews are harder to scale with limited questions and non-technical answers. All the while, DS&A questions remain the most scalable, cheat-resistant way to test problem-solving skills under pressure.
Amid AI-powered cheating and headlines declaring LeetCode dead, Big Tech follows the path of least resistance: rather than invent something unproven, they shift back to in-person interviews to make cheating harder. This format may evolve, but time-pressured coding isn’t going anywhere.
So, rather than fighting the system, it’s more pragmatic to embrace the “suck”, and learn to become great at these interviews.
Coding interviews are meant to challenge you. Even seasoned engineers hit roadblocks, and that’s not failure; it’s the point. Interviewers want to see how you respond when the path forward isn’t obvious. Do you freeze, flail, or push forward with a plan?
That’s where the MIKE framework comes in. Based on years of real interview experience and refined by teaching thousands of engineers, MIKE is a structured, reliable approach for navigating moments of uncertainty. Success doesn’t come from avoiding confusion, it comes from knowing exactly what to do when it hits.
The MIKE framework consists of four main, problem-solving strategies that experienced engineers employ to solve problems when they get stuck:
[M]inimally sketch the naive solution: Start by establishing a baseline approach, even if it’s inefficient. This ensures you understand the problem, and it gives you something to optimize.
[I]dentify upper and lower bounds: Use
[big O analysis](https://substack.com/redirect/d88b3a86-6987-4965-b996-02ca61281bfe?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)to narrow down the range of possible solutions. This helps you quickly discard approaches that are too slow or unrealistically fast. See a helpful[visual introduction to Big O analysis.](https://substack.com/redirect/56b3bff8-ca3f-4664-b839-52d8365e1a81?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)[K]eywords/triggers: Look for hints in the problem statement that suggest specific techniques. For example, a sorted input array might trigger thoughts of binary search, while questions involving parentheses often suggest use of a stack.
[E]mploy boosters: If the first three parts don’t get you unstuck, there’s a series of techniques designed to give you a “boost”. These include optimizing the brute force solution, hunting for useful properties, and ways to decrease difficulty.
This framework isn’t revolutionary; it simply spells out what good problem solvers do instinctively.
Let’s explore each component in detail.
When you’re stuck, the first step is to stop worrying about optimization and just find a working approach. Don’t jump into code, just sketch the simplest brute force solution that solves the problem.
Get the ball rolling. Many candidates chase optimal solutions and end up with nothing. A bad-but-working solution beats no solution at all.
Solve the right problem. If your basic approach fails on examples, you probably misunderstood something.
Set up optimization techniques. Naive solutions are often a stepping stone towards an optimal solution. With a naive solution, you can spot bottlenecks, unnecessary work, and duplicate work that can be optimized (see Booster 1).
You might ask what “sketch” means in this context. You shouldn’t code a solution, but minimally sketching it is a good use of time. For this, I recommend “indented English”, a middle ground between code and vaguely describing it out loud. It skips syntax and focuses on the code structure using indentation. Avoid full-blown pseudocode, with which it’s too easy to slip into writing real (often buggy) code. Consider the “indented English” on the left which focuses on the high-level idea, vs. the “pseudocode” on the right that has a bug.
Pitfalls to avoid:
Overthinking syntax: When writing a high-level idea out, it’s not the time to think through the syntax of conditionals or complex list comprehensions. Explain the idea succinctly, then code.
Skipping non-trivial test cases: We’ve seen candidates skip test cases that don’t follow the happy path of their algorithm. Run through non-trivial examples to make sure an idea is sound.
Handling logic for trivial test cases: Sometimes, we see candidates wasting time on trivial test cases. You don’t need to write the logic on how to handle empty arrays; just write a one-line reminder like, “TODO: handle empty array,” to show the interviewer you’re aware of the test case.
Writing actual code: We’ve seen candidates write working Python code inside of a comment string and call it “pseudocode”.
Starting with a naive solution gives clarity, confidence, and a launchpad for optimization. Once that’s locked in, then you can move on to performance.
The solution to the bug in the code: We are mixing types in the Python code – which is a common problem in Python. The line “for row in grid” gives us a list, and not an array. Because of this, the following line (“for col in len(grid[row])”) would not work.
The correct code would be this:
for row in range(len(grid)):
for col in range(len(grid[row])):
Problem: [Increasing Triplet Subsequence](https://substack.com/redirect/8116a7ff-6147-4957-b5c5-b9f46828a7ec?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
Given an integer array arr, return true if there exists a triple of indices (i, j, k) such that i < j < k and arr[i] < arr[j] < arr[k]. If no such indices exists, return false.
Example 1: arr = [8, 5, 4, 9, 7, 6, 5, 6, 4]
Output: True. There are three values in increasing order (4 < 5 < 6) and their indices are also in increasing order (2 < 6 < 7).
Example 2: arr = [9, 8, 7, 6]
Output: False. No such triplet exists.
Example 3: arr = [3, 2, 6, 1, 5, 8]
Output: True. There are five valid triplets:
• 3, 6, 8; (indices 0, 2, 5)
• 3, 5, 8; (indices 0, 4, 5)
• 2, 6, 8; (indices 1, 2, 5)
• 2, 5, 8; (indices 1, 4, 5)
• 1, 5, 8; (indices 3, 4, 5)
If your spidey senses are tingling, it may be because you’ve heard of a similar problem called [3Sum](https://substack.com/redirect/cffb64c5-584f-43b9-82c9-2126d94366e0?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). The same brute force solution with nested loops would work here and look like this:
Algo 1: Nested loops
n = len(arr)
Time: O(n^3)
Space: O(1)
valid_triplet(arr):
for i in arr
for j in arr
for k in arr
// if indices and values are in increasing order
if i < j < k and arr[i] < arr[j] < arr[k]
return True
return False
The skeleton of a solution can be sketched in just a minute or two. While our approach is not optimal, it helps convey to an interviewer that you understand the question and the naive way to tackle the problem. And it’s a starting point for optimizations.
We will continue to revisit this problem throughout as we work through the framework.
After minimally sketching a naive solution, we suggest identifying the upper and lower bounds for your algorithm’s time complexity (the next steps can be in any order). This process of identifying boundaries, which we call boundary thinking, helps narrow down the range of possible solutions and guides you toward the optimal approach.
A lower bound establishes a threshold below which no solutions can exist. If a problem has a lower bound of O(n), it means we can’t solve it in O(log n) time, or anything faster than O(n). This helps us avoid wasting time on trying to optimize beyond what’s theoretically possible.
An upper bound establishes a threshold above which solutions are not worth considering. While we can always create slower algorithms, the upper bound helps us discard approaches that are too inefficient to pass the interview.
There are two main types of lower bounds to consider:
Output-size lower bound: This one is straightforward: the output size is a lower bound for the runtime. With a sequential algorithm, we can’t output an array of size O(n) in less than O(n) time; that’s how long it takes just to write it.
For example, in the Increasing Triplet Subsequence problem, if we were asked to return all increasing triplets, the output size would be cubic (think of an already-sorted array), meaning that our brute force algorithm would already be optimal.
If the output is just a number or Boolean, the O(1) lower bound isn’t very constraining, but for problems with potentially large outputs – like finding all combinations or permutations – this bound can be quite useful.
Task-based lower bound: Sometimes, regardless of the approach, there’s a fundamental “task” that any solution must perform. The runtime of this task establishes a lower bound.
For instance, if we need to find a specific value in an unsorted array, we must check every element in the worst case, giving us a task-based lower bound of O(n). This immediately rules out any approaches that would work in O(log n) or O(1) time.
Common task-based lower bounds include:
O(n) for problems requiring the processing of each input element at least once
O(n log n) for problems that inherently require comparison-based sorting
O(2n) for problems that require all subsets of the input to be found, like generating a power set
When we have both output-size and task-based lower bounds, we take the greater of the two as our final lower bound.
Similarly, there are two main approaches to establishing upper bounds:
Naive upper bound: The time complexity of the naive solution serves as an initial upper bound. If your brute force approach runs in O(n³) time, then you know you don’t need to consider anything slower.
This bound is particularly useful because you’ve already done the work of sketching the naive solution in the first step of the MIKE framework.
Time Limit Exceeded (TLE) upper bound: This one is a bit strange. In online coding assessments, when a submitted solution is too slow, we get a “Time Limit Exceeded” message. We can anticipate whether a solution will be too slow in an online assessment or interview by understanding the problem’s constraints.
For example:
If n ≤ 10, an O(n!) approach might be acceptable
If n ≤ 20, an O(2n) approach might work
If n ≤ 500, consider O(n³) approaches or better
If n ≤ 104, consider O(n²) approaches or better
If n ≤ 106, consider O(n log n) and O(n) approaches or better
These aren’t hard rules, but they are guidance. If you aren’t given problem constraints during an in-person interview you can always ask the interviewer for them, but be mindful that not everyone will provide useful responses to such a nuanced question.
When we have both the naive and TLE upper bounds, we take the lesser of the two as our final upper bound.
We know what you’re thinking: “that’s a lot of effort. How does it help?” To find out, let’s take a practical example with a new problem.
Problem: maximum tunnel depth
You're given an nxn binary matrix, tunnel, representing a tunnel network that archeologists have excavated. The ground level is above the first row. The first row is at depth 0, and each subsequent row is deeper underground.
1’s represent excavated tunnel pathways in the network.
0’s represent earth that has not been excavated yet.
The tunnel starts at the top-left and top-right corners (the cells (0, 0) and (0, n - 1) are always 1’s) and consists of a single connected network. Since the tunnel represents a single connected component in the grid, an input like this would not be valid because there is a 1 that is unreachable:
tunnel = [ [1,0,0,1],
[1,1,1,1],
[0,0,0,0],
[0,0,0,1], <- Disconnected 1, so the input is not valid!
]
Write a function that returns the maximum tunnel depth.
Pause for a minute; really stop and think through the following questions before proceeding:
How would you go about solving this problem?
Minimally sketch the naive solution. What does a “naive” solution look like?
Identify upper and lower bounds. In particular, can you derive any insights on the best conceivable runtime for this question?
Hopefully, you tried to answer the questions above before reading this!
How would you go about solving this problem?
If you’re like most engineers with a reasonable amount of data structures and algorithms experience, your first thought might be to use a graph traversal, like a depth-first search or breadth-first search. Given that the matrix is square, our time complexity would be O(n2), and the space complexity would be similar since we have to track visited cells to avoid cycles (plus the recursive call stack in a DFS).
What does the “naive” solution look like?
The first step in our MIKE framework helps us identify this second (simpler!) approach. If we step back and ask if there are other ways to find the maximum depth, most people notice a significantly more straightforward solution: traverse the tunnel matrix with a pair of nested loops.
Looping through the tunnel directly lets us record the deepest point without the need to write a whole graph traversal. Because the tunnel input is guaranteed to always be connected, we don’t have to worry about finding stray ones in the tunnel that would throw off our depth count.
The time complexity would be identical to the graph traversal in the worst case, O(n2), but the space complexity is actually better since it is constant (O(1)).
What happens when we apply boundary thinking to the problem?
The naive approach alone is a novel solution, since it is uncommon for the straightforward approach to be better than a common algorithmic one. However, if we apply boundary thinking we can squeeze more out of this problem.
We’ve already identified a constant space solution with a quadratic time complexity, so if there are improvements to be made, they will need to be with the time complexity. Is this possible? Let’s identify the upper and lower bounds to find out.
Naive upper bound: O(n²) to iterate through the entire matrix.
Lower bound: The output is just a number, so the output-size lower bound is O(1). The task-based lower bound isn’t immediately clear: do we need to check every cell? Your gut might say “yes”, but we should default to the output-size lower bound if we’re uncertain.
With bounds of O(1) to O(n2), we should consider approaches from constant time upwards, carefully considering each option within the range:
O(1): Seems unlikely for a grid problem
O(log n): Binary search, searching in a tree?
O(n): Scanning just a fraction of the grid?
O(n log n): A sorting solution, heaps, or some combination of the above?
O(n²): Our naive solution
Mapping time complexities to possible algorithmic approaches helps narrow the choices. These mappings give clues for the options to try: linear scans, binary search, sorting, and trees.
After just a minute or two of experimentation, it is fairly obvious that sorting breaks our input and doesn’t seem to help. We can similarly eliminate tree-based solutions like heaps, as there is no clear way to use them. The binary search idea is intriguing, but how can we apply it? Consider the following input. Can we repeatedly halve something to help narrow the search range?
tunnel = [ [1,0,0,1],
[1,0,1,1],
[1,1,1,0],
[0,0,0,0],
[0,0,0,0],
[0,0,0,0],
[0,0,0,0],
]
If we check the middle row in the tunnel matrix and scan through it, we will always find one of two scenarios:
We encounter a 1 in the scanned row. Since we know this must be part of the tunnel, we eliminate the top half of the matrix from our search. We know the maximum depth is at least that middle row or lower in the matrix.
We do not encounter a 1 in the scanned row. Since the tunnel is a single connected component that starts at the top, any row without a 1 means no further rows can contain the connected tunnel.
Repeating this binary search approach will lead to an O(n log n) solution that’s better than our naive O(n²) approach. Using boundary thinking helps us identify a non-obvious optimization that significantly improves the solution’s efficiency.
Boundary thinking is a powerful tool that avoids wasting time on impossible optimizations or unnecessarily complex solutions. By establishing clear bounds, you focus your problem-solving efforts where they’re most likely to bear fruit.
Let’s see how boundary thinking applies to our [Increasing Triplet Sequence](https://substack.com/redirect/8116a7ff-6147-4957-b5c5-b9f46828a7ec?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) problem:
Upper bound: As we sketched in step ‘M’, the naive solution is three nested loops with a time complexity of O(n3), which serves as the naive upper bound. No constraints are given, so we can’t deduce a TLE upper bound.
Lower bound: The problem asks for a Boolean output (true or false). Thus, the output-size lower bound is O(1), which isn’t very restrictive. To determine if an increasing triplet exists, we must, at a minimum, inspect the elements of the input array. Therefore, the task-based lower bound is O(n). Unlike the tunnel problem, there is nothing obvious to repeatedly halve, so it’s hard to imagine finding a valid triplet without looking at most – if not all – elements in the array in some cases.
Given our upper bound of O(n3) and our lower bound of O(n), we should focus on algorithms that take O(n) or O(n log n) time, with O(n2) as a possibility (O(n2) is the optimal runtime for 3Sum).
The third step in the MIKE framework is to look for keywords that act as triggers to try a specific approach with a particular data structure or algorithm. This technique, which we call “trigger thinking”, is a powerful shortcut that experienced engineers use intuitively. Triggers might show up in the input type, output type, constraints, problem description, or even during failed attempts to solve the problem...
Become a paying subscriber of The Pragmatic Engineer to get access to this post and other subscriber-only content.
| Full articles every Tuesday and Thursday | |
| Access to resources and templates for engineering managers and engineers | |
| Access to the complete archive, see all comments and comment on articles |