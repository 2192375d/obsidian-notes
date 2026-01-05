---
title: Big Omega notation
created: Monday 29th September 2025 13:29
last_modified: Monday 29th September 2025 13:29
aliases: []
tags:
  - computer-science/algorithm
course:
  - CSCC37
LEC: []
---
# big Omega notation
The idea to say $f(n)\in \Omega(g(n))$, we want to find a (perferably simple) function $g(n)$ S.T. for big $n$:
$$
f(n)\geq d \cdot g(n)
$$

# formal definition (CSCC37 TUT4)
Let $g\in F$, $\Omega(g(n))$ is the set of functions $F\in \mathcal{F}$ S.T.
$$
\exists d\in \mathbb{R}^+,\exists t\in\mathbb{N},\forall n\in\mathbb{N},n\geq t\to f(n)\geq d \cdot g(n)
$$

_example_
Let $F(n)=n^3-n^2+5$
Q: What should $g(n)$ be S.T. $F(n)\in \Omega(g(n))$?

(We wanna find the $d, t$ values somehow)
For $n\geq t$:
$$
\begin{align}
n^3-n^2+5&>n^3-n^2 \\
&\geq d \cdot n^3 \\
&\to n-1\geq dn \\
&\to n-dn\geq 1 \\
&\to n(1-d)\geq 1 \\
&\to n\geq \frac{1}{1-d}
\end{align}
$$
For this to happen, we want $d\leq 1$

if $\displaystyle d=\frac{1}{2}$, then $t=2$
Thus smallest value for $t$ is $2$?????? (don't think the TA knows what he's saying lol)

Therefore, $f(n)\in \Omega(n^3-n^2)$
