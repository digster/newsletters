---
subject: "[New post] Embeddings – Part 1"
from: "Seeking Wisdom <comment-reply@wordpress.com>"
to: ""
date: 2023-11-24 02:17:59
labels: ["CATEGORY_PERSONAL", "INBOX", "Jana V"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_8135152689830330561"]
---
This is the 8th post in my series on building a toy GPT. For better understanding, I recommend reading my [earlier posts](https://public-api.wordpress.com/bar/?stat=groovemails-events&bin=wpcom_email_click&redirect_to=https%3A%2F%2Fjanav.wordpress.com%2F&sr=1&signature=6d0891f71893981ab98f6d79de1795aa&user=8c75b1c84af96d984bdb9fbc54a41aa1&_e=eyJlcnJvciI6bnVsbCwiYmxvZ19pZCI6ODQ4MzczMSwiYmxvZ19sYW5nIjoiZW4iLCJzaXRlX2lkX2xhYmVsIjoid3Bjb20iLCJoYXNfZmVhdHVyZWRfaW1hZ2UiOiIwIiwic3Vic2NyaWJlcl9pZCI6IjIyNTQ2MDcyMSIsIl91aSI6IjhjNzViMWM4NGFmOTZkOTg0YmRiOWZiYzU0YTQxYWExIiwiX3V0IjoiYW5vbiIsImVtYWlsX2RvbWFpbiI6ImdtYWlsLmNvbSIsInBvc3RfaWQiOjgxMzcsInVzZXJfZW1haWwiOiJpc2hhbi5tYWlsQGdtYWlsLmNvbSIsImRhdGVfc2VudCI6IjIwMjMtMTEtMjQiLCJlbWFpbF9pZCI6Ijc2MDEyMGRmNGZkNDgyNGI3ZmUzZmMxNmE0NWRiNTFkIiwiZW1haWxfbmFtZSI6Im5ldy1wb3N0IiwidGVtcGxhdGUiOiJuZXctcG9zdCIsImxpbmtfZGVzYyI6InBvc3QtdXJsIiwiYW5jaG9yX3RleHQiOiJlYXJsaWVyIHBvc3RzIiwiX2RyIjpudWxsLCJfZGwiOiJcL3dwXC92Mlwvc2l0ZXNcLzg0ODM3MzFcL3Bvc3RzXC84MTM3P19lbnZlbG9wZT0xJmVudmlyb25tZW50LWlkPXByb2R1Y3Rpb24mX2d1dGVuYmVyZ19ub25jZT1jYzMyMzI4NDlhJl9sb2NhbGU9dXNlciIsIl9lbiI6IndwY29tX2VtYWlsX2NsaWNrIiwiX3RzIjoxNzAwNzkyMjc5NjI1LCJicm93c2VyX3R5cGUiOiJwaHAtYWdlbnQiLCJfYXVhIjoid3Bjb20tdHJhY2tzLWNsaWVudC12MC4zIiwiX3VsIjpudWxsLCJibG9nX3R6IjoiLTgiLCJ1c2VyX2xhbmciOm51bGx9&_z=z) first.
I love playing and watching cricket. The dominance India showed in the recently concluded World Cup is astounding. I have never seen anything like it in the four decades I've been following cricket. It’s disappointing to see us lose in the finals against Australia. The better team on that day won.
One of the best ways to grasp a new concept (embedding) is by connecting it with something you’re passionate about (cricket). I pulled up the batting averages (the number of runs a player scores on average per innings) and strike rates (the average number of runs scored per 100 balls faced) for everyone who played in the recent World Cup final.
| Player | Country | Average | Strike rate |
| Rohit Sharma | India | 49.1 | 92.0 |
| Shubman Gill | India | 61.4 | 103.5 |
| Virat Kohli | India | 58.7 | 93.6 |
| Shreyas Iyer | India | 49.6 | 101.0 |
| KL Rahul | India | 50.8 | 88.1 |
| Ravindra Jadeja | India | 32.4 | 85.1 |
| Suryakumar Yadav | India | 25.8 | 105.0 |
| Mohammed Shami | India | 7.8 | 83.0 |
| Jasprit Bumrah | India | 7.6 | 57.2 |
| Kuldeep Yadav | India | 10.5 | 56.8 |
| Mohammed Siraj | India | 7.7 | 46.0 |
| David Warner | Australia | 45.3 | 97.3 |
| Travis Head | Australia | 42.0 | 102.6 |
| Mitchell Marsh | Australia | 36.1 | 96.2 |
| Steve Smith | Australia | 43.5 | 87.2 |
| Marnus Labuschagne | Australia | 37.9 | 83.1 |
| Glenn Maxwell | Australia | 35.4 | 126.9 |
| Josh Inglis | Australia | 18.9 | 94.1 |
| Mitchell Starc | Australia | 12.4 | 79.4 |
| Pat Cummins | Australia | 13.7 | 75.1 |
| Adam Zampa | Australia | 9.5 | 65.7 |
| Josh Hazlewood | Australia | 17.3 | 91.0 |
If I asked you to find players similar to Virat Kohli, how would you go about it? One tedious method is to compare Virat's average and strike rate with every other player, then pick the one who's closest to him. Luckily, we've found a more straightforward solution to this problem: use a scatter plot.
We can examine the players around Virat and deduce that Shubman Gill, KL Rahul, Rohit Sharma, and Shreyas Iyer are similar to him. Even with this straightforward scatter plot, it's challenging to determine who is the most similar, who comes second, and so on. Now, imagine a scatter plot featuring hundreds of players, comparing more than just two features. How complex would that be?
An elegant method to represent each player's statistics is by modeling them as vectors. Think of a vector as a list of numbers, where each number describes a specific feature.
For instance, Virat Kohli can be represented by the vector (58.7, 93.6), where the first number represents his average and the second his strike rate. In a similar fashion, Rohit Sharma's vector is (49.1, 92.0), while Shubman Gill’s vector is (61.4, 103.5).
We can perform interesting mathematical operations on vectors that help answer similarity questions in an elegant way. More importantly, the solution scales to thousands of players, with each player having hundreds of features. The illustration below demonstrates how to calculate the distance between two vectors.
This concept can be extended to more than two dimensions, as the underlying mathematics remains the same. Read [this](https://www.mathsisfun.com/algebra/distance-2-points.html) excellent article to understand how to compute the distance between vectors in three or more dimensions.
By applying the distance formula to compare Virat Kohli with the other 21 players and then sorting their distance in ascending order, we find that KL Rahul is the most similar to Virat, followed by Rohit Sharma, Shubman Gill and Shreyas Iyer.
| Player | Country | Average | Strike rate | Distance from Kohli |
| Virat Kohli | India | 58.7 | 93.6 | 0.00 |
| KL Rahul | India | 50.8 | 88.1 | 9.63 |
| Rohit Sharma | India | 49.1 | 92.0 | 9.73 |
| Shubman Gill | India | 61.4 | 103.5 | 10.26 |
| Shreyas Iyer | India | 49.6 | 101.0 | 11.73 |
| David Warner | Australia | 45.3 | 97.3 | 13.90 |
| Steve Smith | Australia | 43.5 | 87.2 | 16.49 |
| Travis Head | Australia | 42.0 | 102.6 | 18.97 |
| Mitchell Marsh | Australia | 36.1 | 96.2 | 22.75 |
| Marnus Labuschagne | Australia | 37.9 | 83.1 | 23.30 |
| Ravindra Jadeja | India | 32.4 | 85.1 | 27.64 |
| Suryakumar Yadav | India | 25.8 | 105.0 | 34.82 |
| Josh Inglis | Australia | 18.9 | 94.1 | 39.80 |
| Glenn Maxwell | Australia | 35.4 | 126.9 | 40.64 |
| Josh Hazlewood | Australia | 17.3 | 91.0 | 41.48 |
| Mitchell Starc | Australia | 12.4 | 79.4 | 48.43 |
| Pat Cummins | Australia | 13.7 | 75.1 | 48.65 |
| Mohammed Shami | India | 7.8 | 83.0 | 51.99 |
| Adam Zampa | Australia | 9.5 | 65.7 | 56.56 |
| Kuldeep Yadav | India | 10.5 | 56.8 | 60.64 |
| Jasprit Bumrah | India | 7.6 | 57.2 | 62.74 |
| Mohammed Siraj | India | 7.7 | 46.0 | 69.76 |
You can ask cool questions like finding players who are a mix of Glenn Maxwell and KL Rahul. To do this, we'll average Maxwell's vector (35.4, 126.9) and Rahul's vector (50.8, 88.1). Then we'll look for players who are closer to the average vector (43.1, 107.5). Travis Head, Shreyas Iyer, David Warner, and Mitchell Marsh are the top four players who are closer to the average vector.
Similar to representing cricketers with vectors, we can also represent words using vectors.
The sentence “In the kingdom, the King spoke with wisdom and authority, showing he was in charge. His crown meant he had a high social status. He was a leader for everyone, both males and females” talks about the attributes and the abilities of the king.
From this sentence, we can identify five distinct features for the 'king' vector: authority, male, wisdom, social status, and leadership, similar to how cricketers are evaluated by their average and strike rate. While cricketers have vectors defined by two features, here we describe 'king' with a five-feature vector.
The word "queen" is the opposite of "king." The Queen is a woman and the King is a man. Therefore, we have four words and five feature vectors. Their values, ranging between 0 and 1, are as shown in the table below. I made up these numbers to illustrate the concept.
| King | Man | Woman | Queen | King - Man + Woman | |
| Authority | 1 | 0.2 | 0.2 | 1 | 1 |
| Male | 1 | 1 | 0 | 0 | 0 |
| Wisdom | 0.8 | 0.1 | 0.1 | 0.8 | 0.8 |
| Social Status | 1 | 0.3 | 0.3 | 1 | 1 |
| Leadership | 1 | 0.4 | 0.4 | 1 | 1 |
Word embeddings transform words into vectors, allowing us to perform mathematical operations on language itself. This is a powerful technique because it captures not just the word, but its deeper meaning and how it relates to other words. For example, if you take the vector for 'king', subtract the vector for 'man', and add the vector for 'woman', you get a vector very close to the one for 'queen'.
Neural networks process a vast collection of words, generating word embeddings as their output. This process results in embeddings where words with similar meanings have vectors that closely match. Take the following four sentences as examples. The neural network can identify that word pairs like king-queen, brave-courageous, and wise-intelligent are related.
- The king was brave.
- The queen was courageous.
- The king was wise.
- The queen was intelligent.
In contrast to the "King" example I made up where I identified five specific features, the specific meaning of each feature produced by a neural network remains unknown. What we understand is that these are fixed-length arrays of numbers. Therefore, when we compare vectors of different words, it's an apples-to-apples comparison.
The number of features or dimensions in a model produced by a neural network varies depending on the specific model. For example, [Bengio's model](https://www.jmlr.org/papers/volume3/bengio03a/bengio03a.pdf) in 2003 has 30 dimensions. Some of the [Word2vec models](https://arxiv.org/pdf/1301.3781.pdf) that came out in 2013 have 300 dimensions. OpenAI’s latest [Ada model](https://openai.com/blog/new-and-improved-embedding-model) has 1,536 dimensions.
Playing with a word embedding browser is a [magical experience](https://www.loom.com/share/160c0fe92d414357bdffdffecc78c3e2). Do check it out [here](https://projector.tensorflow.org/). [Understanding Word Vectors](https://gist.github.com/aparrish/2f562e3737544cf29aaf1af30362f469) by Allison Parrish is one of the best resources I've found for learning about word embeddings. I highly recommend reading it.
Is there a specific format for inputting words into a neural network to generate an embedding? What serves as the ground truth against which the neural network's output is compared? Must a special structure be designed for the embedding so that the neural network can populate it effectively? I will explore these questions in my next post.