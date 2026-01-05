---
title: truncation error and rounding error
created: Friday 22nd August 2025 23:18
last_modified: Friday 22nd August 2025 23:18
aliases:
  - relative round off
tags:
  - computer-science/approximation/error
course: CSCC37
---

The computational error can be broken down as __truncation error__ and __computational error__
# truncation error
Truncation error occurs when a computation with $N$ or $\infty$ terms is done performed by only dealing with a $N_{0}<N<\infty$ terms. This often happens when dealing with infinite series, integrals, or replacing an arbitrary function by a polynomial

An example of this is that approximating $e^x$ using only the first 3 terms, we will get $\displaystyle e^x\approx1+x+\frac{x^2}{2}$, thus, the truncation error will be $\displaystyle e^x-1-x-\frac{x^2}{2}=\frac{x^3}{3!}+\frac{x^4}{4!}+\frac{x^5}{5!}+\dots$

# rounding error
The rounding error is the difference between $x\in\mathbb{R}$ and $fl(x)\in\mathbb{R}_{\beta}(t,x)$, usually referring to relative error:
$$
\delta=\frac{x-fl(x)}{x} \text{ or }fl(x)=x(1-\delta)
$$
Where $\delta$ is the __relative round off (RRO)__

# (to be proved) $\delta$ is independent of $x$
$\delta$ can be independent of $x$
$$
\begin{align}
\delta<\beta^{1-t}\text{ for chopped normalized FP\#S} \\
|\delta|\leq \frac{1}{2}\beta^{1-t}\text{ for rounded normalized FP\#S}
\end{align}
$$