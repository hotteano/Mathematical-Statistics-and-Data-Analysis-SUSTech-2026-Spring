# Assignment 9 - Problem Set

Source: Rice, *Mathematical Statistics and Data Analysis*, 3rd Edition

---

## Page 107 Problems

### Problem 1

The joint frequency function of two discrete random variables, $X$ and $Y$, is given in the following table:

|       | $x=1$ | $x=2$ | $x=3$ | $x=4$ |
|-------|-------|-------|-------|-------|
| $y=1$ | .10   | .05   | .02   | .02   |
| $y=2$ | .05   | .20   | .05   | .02   |
| $y=3$ | .02   | .05   | .20   | .04   |
| $y=4$ | .02   | .02   | .04   | .10   |

**a.** Find the marginal frequency functions of $X$ and $Y$.

**b.** Find the conditional frequency function of $X$ given $Y = 1$ and of $Y$ given $X = 1$.

---

### Problem 9

Suppose that $(X, Y)$ is uniformly distributed over the region defined by $0 \leq y \leq 1 - x^2$ and $-1 \leq x \leq 1$.

**a.** Find the marginal densities of $X$ and $Y$.

**b.** Find the two conditional densities.

---

### Problem 14

Suppose that
$$
f(x, y) = xe^{-x(y+1)}, \quad 0 \leq x < \infty, \quad 0 \leq y < \infty
$$

**a.** Find the marginal densities of $X$ and $Y$. Are $X$ and $Y$ independent?

**b.** Find the conditional densities of $X$ and $Y$.

---

### Problem 15

Suppose that $X$ and $Y$ have the joint density function
$$
f(x, y) = c\sqrt{1 - x^2 - y^2}, \quad x^2 + y^2 \leq 1
$$

**a.** Find $c$.

**b.** Sketch the joint density.

**c.** Find $P(X^2 + Y^2) \leq \frac{1}{2}$.

**d.** Find the marginal densities of $X$ and $Y$. Are $X$ and $Y$ independent random variables?

**e.** Find the conditional densities.

---

## Page 112 Problems

### Problem 43

Let $U_1$ and $U_2$ be independent and uniform on $[0, 1]$. Find and sketch the density function of $S = U_1 + U_2$.

---

### Problem 44

Let $N_1$ and $N_2$ be independent random variables following Poisson distributions with parameters $\lambda_1$ and $\lambda_2$. Show that the distribution of $N = N_1 + N_2$ is Poisson with parameter $\lambda_1 + \lambda_2$.

---

### Problem 51

Let $X$ and $Y$ have the joint density function $f(x, y)$, and let $Z = XY$. Show that the density function of $Z$ is
$$
f_Z(z) = \int_{-\infty}^{\infty} f\left(y, \frac{z}{y}\right) \frac{1}{|y|} \, dy
$$

---

### Problem 52

Find the density of the quotient of two independent uniform random variables.

---

### Problem 57

Suppose that $Y_1$ and $Y_2$ follow a bivariate normal distribution with parameters $\mu_{Y_1} = \mu_{Y_2} = 0$, $\sigma_{Y_1}^2 = 1$, $\sigma_{Y_2}^2 = 2$, and $\rho = 1/\sqrt{2}$. Find a linear transformation $x_1 = a_{11}y_1 + a_{12}y_2$, $x_2 = a_{21}y_1 + a_{22}y_2$ such that $x_1$ and $x_2$ are independent standard normal random variables.

---

## Page 114 Problem

### Problem 72

Let $X_1, X_2, \ldots, X_n$ be independent continuous random variables each with cumulative distribution function $F$. Show that the joint cdf of $X_{(1)}$ and $X_{(n)}$ is
$$
F(x, y) = F^n(y) - [F(y) - F(x)]^n, \quad x \leq y
$$

---

## Extra Questions (Conditional Distribution)

### Problem 1

Suppose $X$ follows $U[0,1]$. Given $X = x$ $(0 < x < 1)$, $Y$ is uniformly distributed on $(0, x)$.

**a.** Compute the joint density function of $(X, Y)$.

**b.** Compute the marginal density function of $Y$.

**c.** Compute $P(X + Y > 1)$.

---

### Problem 3

Suppose that the joint density function of $(X, Y)$ is
$$
f(x, y) = \begin{cases} e^{-y}, & 0 < x < y, \\ 0, & \text{otherwise} \end{cases}
$$

**a.** Find the marginal density functions and check if they are independent.

**b.** Find the conditional density functions $f_{X|Y}(x|y)$ and $f_{Y|X}(y|x)$.

---

## Extra Questions (Transformation)

### Problem 1

Suppose that $X$ and $Y$ are independent random variables, and both follow normal distribution $N(0, 1)$. Let $U = X + Y$, $V = X - Y$.

**a.** Compute the joint density function of $(U, V)$ and the marginal density functions.

**b.** Check if $U$ and $V$ are independent or not.

---

### Problem 2

Suppose that the joint density function of $(X, Y)$ is
$$
f(x, y) = \begin{cases} 1, & 0 < x < 1, \, 0 < y < 2x, \\ 0, & \text{otherwise} \end{cases}
$$

**a.** Find the marginal density functions.

**b.** Find the density function of $Z = 2X - Y$.

**c.** Compute $P(Y < 1/2 \mid X < 1/2)$.

---

## Supplementary Questions

### Problem 1

Choose two numbers from $\{1, 2, 3\}$. Let $X$ denote the first number chosen and $Y$ the second number. Let $Z = \max(X, Y)$, find the joint frequency functions for $(X, Y)$ and $(X, Z)$, and compute all corresponding marginal frequency functions.

---

### Problem 2

Suppose that $X$ and $Y$ are two independent r.v.s and follow the Normal Distribution $N(0, 1)$. Let $Z = \min(X, Y)$, find the density function of $Z$.
