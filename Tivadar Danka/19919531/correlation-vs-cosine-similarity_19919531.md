---
subject: "Correlation vs. cosine similarity"
from: "The Palindrome <thepalindrome@substack.com>"
to: ""
date: 2025-09-05 10:00:32
labels: ["CATEGORY_PERSONAL", "INBOX", "Tivadar Danka", "UNREAD"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_3571324877567057163", "UNREAD"]
---
Struggling to learn math and machine learning on your own? The Palindrome makes complex ideas click—with visual explainers, step-by-step guides, and clear learning paths. Join the premium tier to master the core ideas behind machine learning! (Supporting this work doesn’t have to come out of your pocket. If you read The Palindrome as part of your professional development, you can use
|
Hi there! It’s Tivadar from The Palindrome.
Let’s welcome [Mike X Cohen](https://open.substack.com/users/382604135-mike-x-cohen?utm_source=mentions) among our guest authors! If you regularly read educational content from the intersection of mathematics and machine learning, chances are, you have already encountered his work.
Mike is an extremely prolific author; [his textbooks](https://substack.com/redirect/d018a3b5-6e09-45a5-ac8e-5eacf4c39501?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) and [online courses](https://substack.com/redirect/75b7b9e7-0f15-48e0-a5de-a226bc957287?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) range from [time series analysis](https://substack.com/redirect/73aae258-67ff-45a9-bc14-d93893477ca5?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) through [statistics](https://substack.com/redirect/56d9331c-3fae-4df5-90ca-607e352aee8f?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) to [linear algebra](https://substack.com/redirect/3a565722-8cdf-4c79-8f56-f4c0e0e47b08?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), all with a focus on practical implementations as well.
In this post, he is going to clarify one of the most common misconceptions in data science: that cosine similarity is just correlation.
It is not! The answer lies in the normalization of variables, a key concept to understand for anyone working with data. (Especially tabular data.)
Enjoy!
Cheers,
Tivadar
Height and weight, outdoor temperature and ice cream sales, exercise and health… there are myriad examples of relationships between variables.
But how do you quantify those relationships?
There are many statistical analyses that quantify bivariate (two variables) relationships; in this post, I will describe two — correlation and cosine similarity — discuss how they relate to each other, and advise you on when to use which one. The upshot is that the measures can be identical but are often different. Which one to use depends entirely on whether the scale of the data is important.
I’ll start with some math and explanations, then some cool Python [demos](https://substack.com/redirect/8aa5a2fb-772d-4999-a1c2-ff94deea3820?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) that you can try yourself.
But before getting to the measures, let’s start with the dot product. The dot product is one of the most important foundational operations in mathematics, certainly in applied math topics like data science and deep learning.
The dot product is a single number that captures the linear relationship between two variables. Mathematically, it is defined as element-wise multiplication and sum.
Here’s a small example:
Needless to say, the two variables need to have the same number of numbers, otherwise they don’t pair off and the dot product calculation fails :(
What does the result mean? The “raw” dot product (“1” in this example) is difficult to interpret on its own because it reflects a combination of (1) the scale of the first variable, (2) the scale of the second variable, and (3) the linear relationship between the variables. We want to isolate that third component, which means we need to normalize the dot product before interpreting it.
Two small comments: (1) The dot product is linear because it involves only summing and multiplying; there are no square roots, powers, logs, trig transformations, or other nonlinearities. (2) There is a geometric interpretation of the dot product, which I’m not going to discuss here.
Mathematically, the dot product between variables x and y can be defined like this:
In English: Element-wise multiply all n pairs of data points, then sum.
📌 The Palindrome breaks down advanced math and machine learning concepts with visuals that make everything click.[Join the premium tier](https://substack.com/redirect/72cfc800-0598-42e6-a3c8-56d2349a691a?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) to get access to [the upcoming live courses](https://substack.com/redirect/cfafa9cc-e55f-4c22-8f43-371a2bc4d408?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) on Neural Networks from Scratch and Mathematics of Machine Learning.
There are several types of correlation coefficients; Pearson is the most commonly used one, and when someone says “correlation”, they’re almost certainly referring to the Pearson variety.
Here’s the equation for a Pearson correlation:
where
r is the correlation coefficient,
x and y are the two variables (e.g., vectors of height and weight values for a sample of people),
n is the sample size,
and x̅ is the average of x.
Notice that the formula is a ratio of a dot product between x and y in the numerator, and two dot products in the denominator (the squaring makes it look different from a dot product, but you can write x² as x ⋅ x). Thus, the correlation is formed from dot products.
What does this equation mean? Let me start by explaining the two normalizations:
Mean-center. The variables are shifted by their average, such that the variables in the correlation equation have a mean of zero.
Variance-normalizing (denominator). The squared terms in the denominator are the variances of the variables. (Small nuance here: variance technically needs a 1/(n-1) term, but it’s in the numerator and denominator and therefore cancels.) Dividing by the product of the variances eliminates their scaling. Basically, the variance normalization accounts for the fact that, for example, weight has a different numerical value if we measure in grams, kilograms, stones, or pounds, even though the relationship between height and weight doesn’t depend on the measurement units.
Why do we need these normalizations? If you want to know the relationship between, for example, time spent in higher education and post-education salary, you don’t want to worry about whether “time spent” is measured using hours, days, months, or years; and you don’t want to worry about whether salary is measured using dollars, thousands of dollars, or hundreds of thousands of dollars. Instead, you just want to know whether the relationship is positive and how strong the relationship really is. Without the normalizations, you’d get a different correlation coefficient depending on the measurement units.
Furthermore, imagine that the two variables are already mean-centered and unit-normalized; in that case, the equation for the Pearson correlation would literally be identical to the dot product equation I showed earlier.
And what does the (suitably normalized) coefficient value mean?
When the two variables are identical (that is, x = y), then r = 1. And when the two variables are identical-but-opposite (that is, x = -y), then r = -1. When r = 0, the variables are completely unrelated to each other (e.g., the price of Bitcoin vs. the growth rate of a bacteria deep in the Mariana Trench).
For some intuition, here’s a picture of three datasets with three correlation coefficients:
On the other hand, check out the correlation between x and y here:
This demonstrates that correlation (and also cosine similarity!) can only measure linear relationships. Nonlinear relationships can be captured using, for example, mutual information.
Now for cosine similarity. Cosine similarity (sometimes indicated S꜀ for “similarity of the cosine variety”) is Equation 1 below; I’ve repeated the correlation coefficient underneath (Equation 2) for ease of comparison.
What would happen if x and y were already mean-centered? The two formulas would be identical. (As with correlation, there is a geometric interpretation that I’m not focusing on.)
In other words, correlation and cosine similarity can be identical. But what happens when the means aren’t zero? That is an intuition that is really difficult to develop just by staring at formulas. So instead, let’s run some simulations in Python!
Note about the code below: I’m only showing the most important lines of code; you can download the entire notebook file from [my git repo](https://substack.com/redirect/8aa5a2fb-772d-4999-a1c2-ff94deea3820?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o). After reading through the rest of this post, I very strongly encourage you to play around with the code yourself.
Before we get to the direct comparisons, you need to know how to simulate correlated data. That’s useful because it allows you to explore the relationship between correlation and cosine similarity with ground-truth data.
Let’s assume that
In other words, x and q are random numbers sampled from a normal (Gaussian) distribution, and x and y are variables correlated at approximately r = R. Why is the actual correlation only approximate? That’s because R is the population correlation, while r is the sample correlation. With larger sample sizes, the sample correlation will more closely match the population correlation.
The way to think about the third equation is that y equals a copy of x that is scaled up by R, and then added to random noise scaled down by R. Notice what happens when R = 0: y is simply random numbers, unrelated to x. On the other hand, when R = 1, then y = x exactly.
How’s this look in code? Something like this:
That produces a graph like this (reminder that the code snippet above is just the essentials; the full code is [linked here](https://substack.com/redirect/8aa5a2fb-772d-4999-a1c2-ff94deea3820?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)):
The code block below shows how to calculate correlation and cosine similarity using a direct translation of the formulas shown earlier.
It’s useful to see the math translated directly into code, although in practice it’s better to use library-provided functions:
Now we’re ready for the experiment!
The goal here is to simulate correlated data, with correlation values ranging from -1 to +1. The data are created using the equation I showed earlier, but I added an offset of -10 to variable x. Of course, that doesn’t matter for the correlation because the mean is subtracted off. But that offset does get incorporated into cosine similarity.
And here’s what the results look like:
Stunning differences! The x-axis is the population correlation value (R) and the y-axis is the sample correlation (r) or cosine similarity. The correlation coefficient nearly perfectly tracks the population correlation, with minor deviations attributable to noise and limited sample sizes. The cosine similarity, on the other hand, remains quite small, regardless of the actual correlation coefficient. That discrepancy is entirely due to the mean offset in variable x.
Importantly, neither analysis is inherently “right” or “wrong”; they’re simply different. Now, these simulated data are meaningless, so it’s not possible to say which analysis is more appropriate in this example. But it is super-duper clear that you can get very different results.
If you want to continue exploring [the code](https://substack.com/redirect/8aa5a2fb-772d-4999-a1c2-ff94deea3820?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) — which I super-duper recommend — then some suggestions are to (1) change the value of the x offset, (2) include a y offset that matches the x offset, (3) include a y offset with the opposite sign as the x offset.
Briefly:
Use correlation when you want to measure the relationship without worrying about the units. That’s the case when the units are arbitrary (e.g., distance can be measured in feet or meters) or different (e.g., euros vs. calories).
Use cosine similarity when both variables have the same units — and the units are informative. Cosine similarity is often used in machine-learning applications with vector-embeddings, for example of text documents or tokens in a language model. In these cases, offsets between the variables correspond to meaningful differences, and thus really do indicate weaker relationships.
There’s so much more I could write about bivariate relationships, in data and in real life… but I’ll stop here.
If you have enjoyed this post and want to support Mike on his journey of education, check out his
or his
[github page](https://substack.com/redirect/33622458-3313-4531-b7fc-c261330c5015?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)!
Also make sure to follow him on [Substack](https://substack.com/redirect/d65166b2-687d-4c85-929f-2f72ba6ea43b?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o) and [LinkedIn](https://substack.com/redirect/93f52427-b066-41f2-a267-fa98bd4d94ce?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o), where he shares similar high-quality technical content every day!
When you're ready to go deeper, here’s how I can help:
Get instant access to step-by-step learning tracks on graph theory, foundational mathematics, and building neural networks from scratch—with visuals and explanations designed to make it all finally click.
📘 [Grab ](https://substack.com/redirect/f3a4fa57-bce3-4329-b93e-c4309265b6db?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)[The Mathematics of Machine Learning ](https://substack.com/redirect/f3a4fa57-bce3-4329-b93e-c4309265b6db?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)[book](https://substack.com/redirect/f3a4fa57-bce3-4329-b93e-c4309265b6db?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)[ ](https://substack.com/redirect/f3a4fa57-bce3-4329-b93e-c4309265b6db?j=eyJ1IjoiOG81NG4ifQ.6oeetudtJEh-zO1onUJvtadWEdbodFIw0h4xbugrh1o)
Master the math that powers modern ML—linear algebra, calculus, and probability—with Python examples and crystal-clear explanations.
Bridge the gap between textbook theory and real-world implementation.