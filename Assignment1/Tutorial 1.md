# Tutorial 1 

## Question 1

> 设事件$A, B, C$，表示以下内容：
> - 事件$A,B,C$都发生或者都不发生
> - 事件$A,B,C$不多于一个发生
> - 事件$A,B,C$中至少两个发生

- $(A\cap B \cap C) \cup (\bar{A} \cap \bar{B} \cap \bar{C})$
- $(A \cap \bar{B} \cap \bar{C}) \cup (\bar{A} \cap B \cap \bar{C}) \cup (\bar{A} \cap \bar{B} \cap C) \cup (\bar{A} \cap \bar{B} \cap \bar{C})$
- $(A \cap B \cap \bar{C}) \cup (A \cap \bar{B} \cap C) \cup (\bar{A} \cap B \cap C) \cup (A \cap B \cap C)$

## Question 2 

> 证明$A\cap C = B \cap C\Leftrightarrow (\overline{A\cup B}) \cap C = (\bar{A} \cap C) \cup (\bar{B} \cap C)$

**Proof.** 右侧$(\bar{A} \cap \bar{B}) \cap C = (\bar{A} \cup C) \cap (\bar{B} \cap C) = (\bar{A} \cap C) \cup (\bar{B} \cap C)$。

**引理.** $X \cup Y = X \cap Y \Leftrightarrow X = Y$

**Proof.** 由$X \cup Y = X \cap Y$，我们有$X \subseteq Y$和$Y \subseteq X$，所以$X = Y$。反过来，由$X = Y$，我们有$X \cup Y = X \cap Y$.

因此我们令$X = (\bar{A} \cap C)$和$Y = (\bar{B} \cap C)$，则有$(\bar{A} \cap C) \cup (\bar{B} \cap C) = (\bar{A} \cap C) \cap (\bar{B} \cap C)$当且仅当$(\bar{A} \cap C) = (\bar{B} \cap C)$.

我们注意到左侧$A \cap C = B \cap C$, 则$C \setminus (A \cap C) = C \setminus (B \cap C)$，即$(\bar{A} \cap C) = (\bar{B} \cap C)$.

因此左右可以互推。

## Question 3

用集合列表示极限：

> $\{f_n(x), x\in [0,1]\}, \lim_{n\to \infty} f_n(x) \to 0$

$$
\lim_{n\to \infty} f_n(x) = 0 \Leftrightarrow \bigcap_{k=1}^\infty \bigcup_{N=1}^\infty \bigcap_{n=N}^\infty \{x\in [0,1]: f_n(x) < \frac{1}{k}\}
$$

不使用$\bigcap_{\epsilon}$是因为我们要求可数交，而$\epsilon$是不可数的。

## Question 4

> 证明 $\bigcup_{i=1}^n \bigcap_{j=1}^m A_{i,j} = \bigcap_{j=1}^m \bigcup_{i=1}^n A_{i,j}$

**Proof.** 我们要证明两个集合相等，即对任意元素$x$，有$x \in \bigcup_{i=1}^n \bigcap_{j=1}^m A_{i,j}$当且仅当$x \in \bigcap_{j=1}^m \bigcup_{i=1}^n A_{i,j}$。

左边：$x \in \bigcup_{i=1}^n \bigcap_{j=1}^m A_{i,j}$意味着存在某个$i_0$使得$x \in \bigcap_{j=1}^m A_{i_0,j}$，即对所有$j$都有$x \in A_{i_0,j}$。

右边：$x \in \bigcap_{j=1}^m \bigcup_{i=1}^n A_{i,j}$意味着对所有$j$都有$x \in \bigcup_{i=1}^n A_{i,j}$，即存在某个$i_j$使得$x \in A_{i_j,j}$。

因此我们有：
$$
\left(\exists i_0\right)\left(\forall j\right) x\in A_{i_0,j}
\Leftrightarrow
\left(\forall j\right)\left(\exists i_j\right) x\in A_{i_j,j}
$$

这说明两个集合相等。