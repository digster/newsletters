---
subject: "[New post] Hello LLMs!"
from: "Seeking Wisdom <comment-reply@wordpress.com>"
to: ""
date: 2023-10-04 04:01:29
labels: ["CATEGORY_PERSONAL", "INBOX", "Jana V", "UNREAD"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_8135152689830330561", "UNREAD"]
---
When you are having trouble getting your thinking straight, consider an extreme or simple case. This will often give you the insight needed to move forward.
I nodded in agreement when I read the above lines from the book [Maxims for Thinking Analytically](https://www.amazon.com/Maxims-Thinking-Analytically-Legendary-Zeckhauser/dp/B09GD9375L).
ChatGPT took the world by storm when it was launched last November. It reached 1 million users in just 5 days after launch. It's a chatbot that's orders of magnitude more advanced than anything I had previously interacted with. Behind the scenes, it uses Large Language Models to create the magic.
A language model is a statistical model that predicts the next word given a sequence of words. Google search has been using a language model years before ChatGPT came out. This shouldn’t be surprising as the [architecture](https://arxiv.org/abs/1706.03762) that powers language models (LLM) came out of Google.
The reason why it’s not just a language model but a large language model is because it’s trained on a large corpus of data from the internet. The data comes from various sources like Wikipedia, GitHub, Books, ArXiv, StackExchange, etc.
The key ingredient behind the LLM revolution is that these models can be trained on unstructured and messy real world data, without the need for carefully curated and human-labeled data sets. This is why these models are self-supervised.
For example, we can train the model to generate the next word by showing it “The cat sat on the …“. If it generates “floor, carpet, or mat” the model will be rewarded. Otherwise, the model will be penalized. This way the model learns, like how a child learns to walk. Fall several times, learn from failures, and walk right.
As a result almost all textual data on the web becomes useful to train these LLMs. These models are trained on trillions of words. [The Coming Wave](https://www.amazon.com/Coming-Wave-Technology-Twenty-First-Centurys/dp/B0BVSW143K/) highlighted the staggering difference between the volume of data these models are trained on and the amount an average American reads.
An average American reads for 15 minutes a day. Assuming a reading speed of 200 wpm, this translates to 1 million words per year. In contrast, an LLM is trained on trillions of words in just a single month-long training run. After grasping this comparison, I felt a jolt of electricity shooting from the tail of my spine to my brain.
Consider the LLM as a black-box where you can pose any question in natural language. It replies in the same natural language. These models can craft stories, essays, answer queries, translate between languages, converse with humans, and even ace AP tests. The technical term for what you instruct an LLM to do is called a "Prompt."
How do these LLMs achieve such a wondrous feat? What's happening inside them? I'm eager to delve into the nuts and bolts of everything that happens within an LLM. Where's the best place to begin? I think it's essential to reiterate Richard Zeckhauser's maxim with which I began this post.
When you are having trouble getting your thinking straight, consider an extreme or simple case. This will often give you the insight needed to move forward.
Instead of trying to understand how to predict the next word, how about we try to predict the next character? Instead of using a neural network, how about we use a simple logic of frequency counting to predict the next character?
This is what [Andrej Karpathy](https://www.youtube.com/watch?v=PaCmpygFfXo&feature=youtu.be&ab_channel=AndrejKarpathy) did by starting with a simple Character Level Language Model in his [Neural Networks lecture](https://karpathy.ai/zero-to-hero.html). The idea is to predict the next character based on the previous character. Karpathy used 26 English alphabets.
I’m going to simplify it by using only four letters A, T, C, G. Yes, these are the alphabets that the book of life is written on.
I created 100 DNA sequences of varying lengths from 1-100 using [this](https://users-birc.au.dk/palle/php/fabox/random_sequence_generator.php#formtools.results) tool. I constructed a 5x5 table and filled in the frequency counts as shown below.
The grid captures three pieces of information for each sequence:
- The first row tracks how often a sequence begins with one of the four characters, each indicated by a prefix (e.g., .a, .t, .c, .g). For instance, 18 sequences start with "a", 56 with "t", 17 with "c", and 9 with "g".
- The first column tracks how often a sequence ends with one of the four characters, each indicated by a suffix (e.g., a., t., c., g.). For example, 15 sequences end with "a", 50 with "t", 23 with "c", and 12 with "g".
- The remaining cells track the frequency of one character following another. For instance, the cell at the intersection of the second row and second column indicates that "a" followed by another "a" appears 19 times. Similarly, the cell at the third row and fourth column shows that "t" followed by "c" occurs 51 times.
The count of 0 in the cell at the first row and first column (..) signifies that there were no empty sequences.
Verify for yourself by mentally populating an empty grid using the sequence 'ctatgt' and then compare it to the grid provided below.
We're now ready to use the grid, which traces the frequency of 100 sequences, to create new DNA sequences!
- Begin with the first row.
- Perform a multinomial sample and select one item. “a” will appear 18% (18/100) of the time, “t” 56%, “c” 17%, and “g” 9%. Suppose you select “g”.
- Move to row 5 and perform another multinomial sample to determine the character following “g”. Let's say you select “t”. This has a 31% probability because “t” appears 22 times out of the 72 possible sequences after “g”.
- Proceed to row 3 and conduct a multinomial sample to identify the character following “t”. Suppose the sequence concludes here. There's a 22% chance of this happening, as the sequence can end in 50 out of the 232 possible sequences after “t”.
- Your resulting sequence is “gt”.
I generated 100 DNA sequences using the above algorithm and drew the grid below.
Congratulations! We came up with a DNA sequence generator by predicting the next character using the previous character.
Our generator can be enhanced by considering more than one previous character. However, the lookup table required to monitor frequency counts expands exponentially. The English language comprises over 170,000 words, and the relationships between words in a sentence are much more complex.
Consider the following 2 sentences.
The children played joyfully on the bank of the river, watching the water flow by.
I need to visit the bank today to deposit my paycheck.
The meaning of the word bank depends on the context. It refers to the river bank in the first example. The second example is a reference to a financial institution. Such complex relationships can’t be modeled with a simple frequency counting.
How does the machine learn this relationship?
To understand that we need to open our high school textbook and start reading the chapter on Derivatives. I’ll cover this topic in my next post.