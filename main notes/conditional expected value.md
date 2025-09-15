---
title: conditional expected value
created: Before 28th July, 2025
last_modified: Monday 28th July 2025 16:30
tags:
  - probability/expected-value
  - probability/conditional
course:
  - STAB52
LEC: "9"
---

# definition
Let $Y$ be an RV, $A$ be an event, then the __conditional expectation__ of any function $g(Y)$ given $A$ are:
$$
\text{discrete case: }E[g(Y)|A]=\sum_{y}g(y)p(y|A)
$$
$$
\text{continuous case: }E[g(Y)|A]=\int_{-\infty}^{+\infty}g(y)f(y|A)dy
$$
, where $f(y|A)=\frac{d}{dy}f(y|A)$

_example_
Let $Y\sim Exponential(\lambda)$ and $A=\{ Y>1 \}$, find $E(Y|A)$
$$
\begin{align}
E[Y|A]&=E[Y|Y>1] \\
&=\int_{-\infty}^{+\infty}yf(y|A)\dots \\
&=\dots
\end{align}
$$

# conditional expectation with a fixed RV
The __conditional expectation__ of $g(Y)$ given $X=x$ is
$$
\text{discrete case: }E[g(Y)|X=x]=\sum_{y}g(y)p_{Y|X}(y|x)
$$
$$
\text{continuous case: }E[g(Y)|X=x]=\int_{-\infty}^{+\infty}g(y)f_{Y|X}(y|x)dy
$$
Usually, we consider the expected value of $E[g(Y)|X=x]$ as a function in terms of $x$ (e.g. $g(x)=E[g(Y)|X=x]$)


_example_
For a take-out restaurant, define:
$X=\text{wait time to order}$
$Y=\text{total wait time}$	
Then, we get a joint PDF $f_{X,Y}(x,y)=\begin{cases}e^{-y},&0<x<y<\infty \\ 0,&o/w\end{cases}$
Find $E(X|Y=1)$ and $E(Y|X=1)$
- First find $f_{X}(x),f_{Y}(y)$
(Did ___something___ to find it)
Thus,
$$
\begin{align}
E(X|Y=1)&=\int_{-\infty}^\infty xf_{X|Y}(X|1)dx \\
&=\int_{0}^1x \frac{f_{X,Y}(x,1)}{f_{Y}(1)}dx \\
&=\int_{0}^1xdx \\
&=\frac{1}{2} \\
E(Y|X=1)&=\int_{-\infty}^\infty yf_{Y|X}(y|1)dy \\
&=\int_{1}^\infty y \frac{f_{X,Y}(1,y)}{f_{X}(1)}dy \\
&=\int_{1}^\infty y \frac{e^{-y}}{e^{-1}}dy \\
&=\int_{1}^\infty ye^{-(y-1)}dy \\
&=\int_{0}^\infty e^{-z}dz && \text{(by change of variable z = y - 1)} \\
&=\int_{0}^\infty(z+1)e^{-z}dz \\
&=\int_{0}^\infty xe^{-z}dz+\int_{0}^\infty e^{-z}dz \\
&=1+1=2
\end{align}
$$
