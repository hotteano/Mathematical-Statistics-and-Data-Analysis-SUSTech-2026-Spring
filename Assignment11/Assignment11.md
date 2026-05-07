# Assignment 11

## Page 170, Problem 49
**Question:**
Two independent measurements, $X$ and $Y$, are taken of a quantity $\mu$. $E(X) = E(Y) = \mu$, but $\sigma_X$ and $\sigma_Y$ are unequal. The two measurements are combined by means of a weighted average to give
$$Z = \alpha X + (1 - \alpha)Y$$
where $\alpha$ is a scalar and $0 \le \alpha \le 1$.
a. Show that $E(Z) = \mu$.
b. Find $\alpha$ in terms of $\sigma_X$ and $\sigma_Y$ to minimize $\operatorname{Var}(Z)$.
c. Under what circumstances is it better to use the average $(X + Y)/2$ than either $X$ or $Y$ alone?

**Solution:**
Given that $X$ and $Y$ are independent, $E(X) = E(Y) = \mu$, $\operatorname{Var}(X) = \sigma_X^2$ and $\operatorname{Var}(Y) = \sigma_Y^2$.

**a.** We have
$$E(Z) = E(\alpha X + (1 - \alpha)Y) = \alpha E(X) + (1 - \alpha)E(Y) = \alpha \mu + (1 - \alpha)\mu = \mu$$

**b.** Since $X$ and $Y$ are independent, 
$$\operatorname{Var}(Z) = \operatorname{Var}(\alpha X + (1 - \alpha)Y) = \alpha^2 \operatorname{Var}(X) + (1 - \alpha)^2 \operatorname{Var}(Y) = \alpha^2 \sigma_X^2 + (1 - \alpha)^2 \sigma_Y^2$$
To minimize $\operatorname{Var}(Z)$, we take the derivative with respect to $\alpha$ and set it to $0$:
$$\frac{\mathrm{d}}{\mathrm{d}\alpha}\operatorname{Var}(Z) = 2\alpha \sigma_X^2 - 2(1 - \alpha)\sigma_Y^2 = 0 \implies \alpha = \frac{\sigma_Y^2}{\sigma_X^2 + \sigma_Y^2}$$
The second derivative is $2\sigma_X^2 + 2\sigma_Y^2 > 0$, so this $\alpha$ indeed minimizes the variance.

**c.** For the simple average, we set $\alpha = 1/2$. The variance is $\operatorname{Var}\left(\frac{X+Y}{2}\right) = \frac{\sigma_X^2 + \sigma_Y^2}{4}$. To make it have a smaller variance than using either $X$ or $Y$ alone, we need:
$$\frac{\sigma_X^2 + \sigma_Y^2}{4} < \sigma_X^2 \quad \text{and} \quad \frac{\sigma_X^2 + \sigma_Y^2}{4} < \sigma_Y^2$$
This simplifies to $\frac{1}{3}\sigma_X^2 < \sigma_Y^2 < 3\sigma_X^2$.

---

## Page 170, Problem 50
**Question:**
Suppose that $X_i$, where $i = 1, \dots, n$, are independent random variables with $E(X_i) = \mu$ and $\operatorname{Var}(X_i) = \sigma^2$. Let $\bar{X} = \frac{1}{n} \sum_{i=1}^n X_i$. Show that $E(\bar{X}) = \mu$ and $\operatorname{Var}(\bar{X}) = \sigma^2/n$.

**Solution:**
$$E(\bar{X}) = E\left(\frac{1}{n}\sum_{i=1}^n X_i\right) = \frac{1}{n}\sum_{i=1}^n E(X_i) = \mu$$
$$\operatorname{Var}(\bar{X}) = \operatorname{Var}\left(\frac{1}{n}\sum_{i=1}^n X_i\right) = \frac{1}{n^2}\sum_{i=1}^n \operatorname{Var}(X_i) = \frac{\sigma^2}{n}$$

---

## Page 170, Problem 55
**Question:**
Let $T = \sum_{k=1}^n kX_k$, where the $X_k$ are independent random variables with means $\mu$ and variances $\sigma^2$. Find $E(T)$ and $\operatorname{Var}(T)$.

**Solution:**
$$E(T) = E\left(\sum_{k=1}^n kX_k\right) = \sum_{k=1}^n kE(X_k) = \mu \sum_{k=1}^n k = \frac{n(n+1)}{2}\mu$$
$$\operatorname{Var}(T) = \operatorname{Var}\left(\sum_{k=1}^n kX_k\right) = \sum_{k=1}^n k^2 \operatorname{Var}(X_k) = \sigma^2 \sum_{k=1}^n k^2 = \sigma^2 \frac{n(n+1)(2n+1)}{6}$$

---

## Page 171, Problem 54
**Question:**
Let $X, Y$, and $Z$ be uncorrelated random variables with variances $\sigma_X^2, \sigma_Y^2$, and $\sigma_Z^2$, respectively. Let $U = Z + X$ and $V = Z + Y$. Find $\operatorname{Cov}(U, V)$ and $\rho_{UV}$.

**Solution:**
Given that $X, Y, Z$ are uncorrelated, we have
$$\operatorname{Cov}(U, V) = \operatorname{Cov}(Z + X, Z + Y) = \operatorname{Cov}(Z, Z) + \operatorname{Cov}(Z, Y) + \operatorname{Cov}(X, Z) + \operatorname{Cov}(X, Y) = \sigma_Z^2$$
$$\rho_{UV} = \frac{\operatorname{Cov}(U, V)}{\sqrt{\operatorname{Var}(U)\operatorname{Var}(V)}} = \frac{\sigma_Z^2}{\sqrt{(\sigma_X^2 + \sigma_Z^2)(\sigma_Y^2 + \sigma_Z^2)}}$$

---

## Page 171, Problem 60
**Question:**
Let $Y$ have a density that is symmetric about zero, and let $X = SY$, where $S$ is an independent random variable taking on the values $+1$ and $-1$ with probability $1/2$ each. Show that $\operatorname{Cov}(X, Y) = 0$, but that $X$ and $Y$ are not independent.

**Solution:**
Given the symmetry, $E(Y) = 0$. We have
$$\operatorname{Cov}(X, Y) = E(XY) - E(X)E(Y) = E(SY^2) - E(S)E(Y)E(Y) = E(S)E(Y^2) - 0 = 0 \times E(Y^2) = 0$$
Since $X=SY$, $P(X=Y) = P(S=1) + P(S=-1, Y=0) = \frac{1}{2} + 0 = \frac{1}{2}$. 
If $X$ and $Y$ were independent and continuous (since $Y$ has a density), then $P(X=Y)$ should be $0$. This is a contradiction. Hence $X$ and $Y$ are not independent.

---

## Extra Question
**Question:**
Assume that the density function for $X$ is $f(x) = \frac{1}{2} e^{-|x|}, -\infty < x < \infty$. 
(1) Compute $E(X)$ and $D(X)$.
(2) Are $X$ and $|X|$ independent or not? State your reason.
(3) Are $X$ and $|X|$ correlated or not? State your reason.

**Solution:**
**(1)** 
$$E(X) = \int_{-\infty}^{\infty} \frac{x}{2} e^{-|x|} \mathrm{d}x = 0 \text{ (since the integrand is an odd function)}$$
$$\operatorname{Var}(X) = \int_{-\infty}^{\infty} \frac{x^2}{2} e^{-|x|} \mathrm{d}x = \int_{0}^{\infty} x^2 e^{-x} \mathrm{d}x = \Gamma(3) = 2$$

**(2)** No, they are not independent. If $|X|$ is given, $X$ is restricted to $\pm |X|$. For example, $P(X \ge 1 \mid |X| < 1) = 0 \neq P(X \ge 1) > 0$.

**(3)** They are uncorrelated. 
$$\operatorname{Cov}(X, |X|) = E(X|X|) - E(X)E(|X|)$$
Since $x|x|$ is an odd function and $f(x)$ is even, $E(X|X|) = 0$. Since $E(X) = 0$, the covariance is $0$. Therefore, they are not correlated.

---

## Supplementary Questions

### Question 1.1
**Question:** Suppose that $X$ and $Y$ are independent random variables. $E(X)=3, E(Y)=1, D(X)=4, D(Y)=9$. If $Z=5X-2Y+15$, compute $E(Z), D(Z)$.
**Solution:**
$$E(Z) = 5E(X) - 2E(Y) + 15 = 5(3) - 2(1) + 15 = 28$$
$$D(Z) = 25D(X) + 4D(Y) = 25(4) + 4(9) = 136$$

### Question 1.2
**Question:** Suppose that $X_i (i=1,2,3,4)$ are mutually independent. $E(X_i)=2i, D(X_i)=5-i$. If $Z=2X_1-X_2+3X_3-0.5X_4$, compute $E(Z)$ and $D(Z)$.
**Solution:**
$$E(Z) = 2E(X_1) - E(X_2) + 3E(X_3) - 0.5E(X_4) = 2(2) - 4 + 3(6) - 0.5(8) = 14$$
$$D(Z) = 4D(X_1) + D(X_2) + 9D(X_3) + 0.25D(X_4) = 4(4) + 3 + 9(2) + 0.25(1) = 37.25$$

### Question 2.1
**Question:** Suppose the joint density of $(X,Y)$ is $f(x,y) = \frac{x+y}{8}$ for $0 \le x,y \le 2$. Compute $E(X), E(Y), \operatorname{Cov}(X,Y), \rho_{XY}, D(X+Y)$.
**Solution:**
$$f_X(x) = \int_0^2 \frac{x+y}{8}\mathrm{d}y = \frac{x}{4} + \frac{1}{4}, \quad f_Y(y) = \frac{y}{4} + \frac{1}{4}$$
$$E(X) = E(Y) = \int_0^2 x(\frac{x}{4}+\frac{1}{4})\mathrm{d}x = \frac{7}{6}$$
$$E(XY) = \int_0^2\int_0^2 xy\frac{x+y}{8}\mathrm{d}x\mathrm{d}y = \frac{4}{3}$$
$$\operatorname{Cov}(X,Y) = E(XY) - E(X)E(Y) = \frac{4}{3} - \frac{49}{36} = -\frac{1}{36}$$
$$D(X) = D(Y) = \int_0^2 x^2(\frac{x}{4}+\frac{1}{4})\mathrm{d}x - (\frac{7}{6})^2 = \frac{5}{3} - \frac{49}{36} = \frac{11}{36}, \quad \rho_{XY} = \frac{-1/36}{11/36} = -\frac{1}{11}$$
$$D(X+Y) = D(X) + D(Y) + 2\operatorname{Cov}(X,Y) = \frac{11}{36} + \frac{11}{36} - \frac{2}{36} = \frac{5}{9}$$

### Question 2.2
**Question:** $X, Y$ are independent and $N(\mu,\sigma^2)$. If $Z=\alpha X + \beta Y, W=\alpha X - \beta Y$, compute $\operatorname{Cov}(Z,W)$ and $\rho_{ZW}$.
**Solution:**
$$\operatorname{Cov}(Z,W) = E((\alpha X+\beta Y)(\alpha X-\beta Y)) - E(\alpha X+\beta Y)E(\alpha X-\beta Y) = \dots = (\alpha^2-\beta^2)\sigma^2$$
$$\operatorname{Var}(Z) = \operatorname{Var}(W) = (\alpha^2+\beta^2)\sigma^2$$
$$\rho_{ZW} = \frac{\operatorname{Cov}(Z,W)}{\sqrt{\operatorname{Var}(Z)\operatorname{Var}(W)}} = \frac{\alpha^2-\beta^2}{\alpha^2+\beta^2}$$