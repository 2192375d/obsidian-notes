---
title: ordered statistics' distribution of maximum and minimum
created: Before 28th July, 2025
last_modified: Monday 28th July 2025 17:07
tags:
  - probability
course:
  - STAB52
LEC: 7
---
# distribution of maximum
For i.i.d. RVs $X_{1},\dots,X_{n}$ with CDF $F(x)$ and PDF $f(x)$, the distribution of the maximum $X_{(n)}$ is
$$
F_{(n)}(x)=[F(x)]^n\&f_{(n)}(x)=n[F(x)]^{n-1}f(x)
$$
proof:
	CDF of $X_{(n)}=max\{x_{1},\dots,x_{n}\}$
	Thus,
$$\begin{align}F_{(n)}(x)&=P(X_{(n)}\leq x) \\
&=P(max\{X_{1},\dots,X_{n}\}) \\
&\dots
\end{align}$$
# distribution of minimum
...

_example_
Machine has $n$ components with i.i.d. $Exponential(\lambda)$ lifetimes.
- if it breaks down when any component dies, find the CDF of its lifetime

Denote $X_{1},\dots,X_{n}$ be the component lifetimes (e.g. $X_{i}\sim Exponential(\lambda)$)
Machine lifetime: $X_{(1)}=min(X_{1},\dots,X_{n})$
Thus, 
$$\begin{align}
F_{(1)}(x)&=1-[1-F(x)]^n \\
&=1-[1-(1-e^{-\lambda x})]^n \\
&=1-e^{-n\lambda},x>0\end{align}$$
