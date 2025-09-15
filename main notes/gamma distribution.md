---
title: gamma distribution
created: Before 28th July, 2025
last_modified: Friday 18th July 2025 23:52
tags:
  - probability/distribution/continuous
course:
  - STAB52
LEC: "5"
---
# defintion
Parameters are: $a,\lambda>0$, where $a,\lambda\in\mathbb{R}$
Denoted $X\sim Gamma(a,\lambda)$

sequence of a independent exponential$(\lambda)$ values
![[>>>>>>>>>>>>>>>>>>>>>>>>>>>>>.png]]

Sum of independent exponentials follow gamma distribution.
This is used to model positive quantities e.g. system lifetime, total insurance claims...

PDF of Gamma distribution is $$f(x)=\begin{cases}\frac{\lambda^a}{\Gamma(a)}x^{a-1}e^{-\lambda x},&x>0\\0,&x\leq 0\end{cases}$$

You cannot integrate gamma PDF, thus no closed form CDF. However, there is a special case:
	special case $a=1\leftrightarrow Exponential(\lambda)$

# gamma function

This is defined based on gamma function, which is a continuous version of the factorial function: $$\Gamma(a)=\int_0^{\infty}x^{a-1}e^{-x}dx$$
Where $a\in\mathbb{Z^+}\cup\{0\},\Gamma(a + 1)=a!$
Note that $\Gamma(\frac{1}{2})=\sqrt{\pi}$ and $\Gamma(a+1)=a\Gamma(a)$

