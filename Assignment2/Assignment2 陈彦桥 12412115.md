# Assignment 2 

**Author: 陈彦桥 12412115**

## Page 27, Problem 7

**Proof**

From the formula $P(A\cup B) = P(A) + P(B) - P(AB)$ and $P(A \cup B) \leq 1$, we have:
$$
P(A) + P(B) - P(AB) \leq 1
$$
Rearranging the inequality, we get:
$$
P(AB) \geq P(A) + P(B) - 1
$$
This complete the whole proof. $\square$

## Page 27, Problem 8

**Proof**

We prove this by mathematical induction. 

When $n=2$, we have:
$$
P(A_1 \cup A_2) = P(A_1) + P(A_2) - P(A_1 A_2) \leq P(A_1) + P(A_2)
$$

Assume that the inequality holds for $n=k$, that is:
$$
P\left(\bigcup_{i=1}^k A_i\right) \leq \sum_{i=1}^k P(A_i)
$$

Then for $n=k+1$, we have:

$$
\begin{align*}
P\left(\bigcup_{i=1}^{k+1} A_i\right) &= P\left(\bigcup_{i=1}^k A_i \cup A_{k+1}\right) \\
&= P\left(\bigcup_{i=1}^k A_i\right) + P(A_{k+1}) - P\left(\bigcup_{i=1}^k A_i A_{k+1}\right) \\
& \leq \sum_{i=1}^k P(A_i) + P(A_{k+1}) = \sum_{i=1}^{k+1} P(A_i)
\end{align*}
$$

From the principle of mathematical induction, for all $n$, the inequality holds.

This complete the whole proof.$\square$

## Supplementary Question 1

The event "At least one of the events A,B,C happens" correspond to the set $A \cup B \cup C$.

$$
P(A \cup B \cup C) = P(A) + P(B) + P(C) - P(AB) - P(AC) - P(BC) + P(ABC)
$$

And from $P(AB) = 0$ we derives $P(ABC) = P(AB \cap C) = 0$.

Thus, we obtain:
$$
P(A \cup B \cup C) = \frac{3}{4} - 0 - 0 - \frac{1}{8} + 0 = \frac{5}{8}
$$

## Supplementary Question 2

From the given information, we know that 
$$
P(AB) = P(\bar{A} \cap B) = P(\overline{A \cup B}) = 1 - P(A \cup B)
$$

From the formula $P(A \cup B) = P(A) + P(B) - P(AB)$, we have:
$$
P(A \cup B) + P(AB) = P(A) + P(B) = p + P(B)
$$

Thus we conclude that 
$$
P(B) = 1 - p
$$