Once we run LDA generative process presented by the graphical model, we end up with the probabilistic model in the form of two tables shown below. If we sample topic x1, we will get word w2 with 90% certainty. If we sample document d2, then the probability that it contains topic x1 is 0.6, the probability that it contains topic x2 is 0.3 and the probability that it contains topic x3 is 0.1.

Φ =

|Topicx1|Topicx2|Topicx3|
|---| --- | --- |
| Word w1 | 0.00 | 0.1 | 0.7 |
| Word w2 | 0.9 | 0.0 | 0.1 |
| Word w3 | 0.1 | 0.8 | 0.2 |
| Word w4 | 0.0 | 0.1 | 0.0 |

Word-topic matrix

Θ = 

| Topicx1 | Topicx2 | Topicx3 |
| --- | --- | --- |
| Document, d1 | 0.03 | 0.03 | 0.94 |
| Document, d2 | 0.6 | 0.3 | 0.1 |
| Document, d3 | 0.9 | 0.05 | 0.05 |
| Document, d4 | 0.8 | 0.15 | 0.05 |

Document-topic matrix

Question 1: Using mathematical notation introduced in previous slides, write the definitions of cells (1,1) and (3,3) of the word-topic matrix.

*Answer:*
Cell (1,1) in the word-topic matrix represents the probability of selecting word w1 given topic x1, i.e., Φ(w1 | x1).
Cell (3,3) in the word-topic matrix represents the probability of selecting word w3 given topic x3, i.e., Φ(w3 | x3).

Question 2: What does the document vector (row) in document-topic matrix represent? What is the constraint that cell values in each document vector have to satisfy?

*Answer:*
The document vector (row) in the document-topic matrix represents the probabilities of each topic appearing in a given document. Each cell value in the document vector has to satisfy the constraint that it is a probability value between 0 and 1, and the sum of all cell values in the document vector has to be 1.

Question 3: Calculate the probability of selecting a word w1 in document d1 using a formula 

$P(w_i) = \sum^{T}_{j=1} P(w_i|x_i=j)P(x_i=j)$, where T=3.


*Answer:*
To calculate the probability of selecting word w1 in document d1, we need to sum over the probability of selecting topic x1 and then selecting word w1 given topic x1. Thus, using the formula given in the question, we get:

$P(w_1) = \sum_{j=1}^{3} P(w_1 | x_1=j) \times P(x_1=j) $
$= P(w_1 | x_1=1) \times P(x_1=1) + P(w_1 | x_1=2) \times P(x_1=2) + P(w_1 | x_1=3) \times P(x_1=3) $
$= 0.00 \times 0.03 + 0.1 \times 0.03 + 0.7 \times 0.94 $
$= 0.658$

Therefore, the probability of selecting word w1 in document d1 is 0.658.
