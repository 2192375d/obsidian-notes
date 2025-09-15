---
title: expected value for discrete RV
created: Before 28th July, 2025
last_modified: Monday 28th July 2025 17:12
tags:
  - probability/expected-value
course:
  - STAB52
LEC: 8
---
__Expected value__ of RV $X$ is value we observe on average, over many repetitions of the random experiment

Note that the RV's __expected value__ is __undefined__ if the RV has infinite values (e.g. RV is nonzero for all natural numbers), this is to deal with situations from [St. Petersburg paradox](https://en.wikipedia.org/wiki/St._Petersburg_paradox).
In human language, we don't want it because expected value with a converging sum makes intuitively very little sense.

#### intuition
Consider discrete RV $X$, and assume you repeat experiment $n$ times, getting values ($c_{1},\dots,c_{n}$), then average of $n$ values is
$$
\frac{1}{n}\sum_{i}c_{i}=\sum_{x}x\left( \frac{\text{number of times }c_{i}=x}{n} \right)\approx \sum_{x}xp_{X}(x)
$$
#### definition (for discrete RV)
Let $X$ be a discrete RV, then the __expected value__ of $X$, written as $E(X)$ or $\mu_{X}$, is defined by
$$
E(X)=\sum_{x\in R^1}xP(X=x)=\sum_{x\in R^1}xp_{X}(x)
$$
Note that $E(constant)=constant$

[[different properties for important distributions]]

_example_
For sequence of independent $Bernoulli(p)$ trials, find the expected number of trials until the first success.
- Let $X\sim Geometric(p)$, then $p_{X}(x)=p(1-p)^{x-1},\forall x\in\mathbb{N}$
Thus,
$$
\begin{align}
E(X)&=\sum_{x=0}^\infty xp(1-p)^{x-1} \\
&=\sum_{y=0}^\infty(y+1)p(1-p)^y && \text{(set y = x - 1)} \\
&=\sum_{y=0}^\infty yp(1-p)^y+\sum_{y=0}^\infty p(1-p)^y \\
&=q\sum_{y=0}^\infty ypq^{y-1}+p\sum_{y=0}^\infty q^y \\
&=qE(X)+\frac{p}{1-q} \\
&=qE(X)+1 \\ \\
\end{align}
$$
We get
$$
\begin{align}
&1=E(X)-qE(X) \\
\to &1=E(X)(1-q) \\
\to &E(X)=\frac{1}{1-q}=\frac{1}{p}
\end{align}
$$
