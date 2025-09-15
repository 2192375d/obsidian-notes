---
title: exponential distribution
created: Before 28th July, 2025
last_modified: Monday 28th July 2025 16:37
tags:
  - probability/distribution/continuous
course:
  - STAB52
LEC: "5"
---
# PDF 
Exponential RV $X$ takes values according to PDF 
$$
f_{X}(x)=\begin{cases}\lambda e^{-\lambda x},&x\geq 0\\0,&x<0\end{cases}, \text{ for some } \lambda > 0
$$
Denoted by $X\sim Exponential(\lambda)$

This is used to measure time until something happens

![[Pasted image 20250605115537.png]]
# CDF
From the example below, we can conclude that Exponential RV $X$ takes values according to CDF
$$
F_{X}(x)=\begin{cases}
1-e^{-\lambda x},&x\geq 0 \\
0,&otherwise
\end{cases}
$$


$$

$$

_example_
Service time $X$ of request to web server follows $Exponential(\lambda)$
-  Find CDF of the service time
	$F_X(x)=P(X\leq x)=\int_{-\infty}^xf_x(u)du=\begin{cases}\int_{-\infty}^x0du=0,&x<0\\\int_{-\infty}^00du+\int_0^x\lambda e^{-\lambda x}du,&x\geq 0\end{cases}$
	For $x\geq 0$, we have $\int_0^x\lambda e^{-\lambda x}du=-e^{-\lambda x}-(-e^{-\lambda 0})=1-e^{-\lambda x}$
	
- Show that $P(X>x+y|X>y)=P(X>x)$
$$\begin{align}P(X>x+y|X>y)
  &=\frac{P(\{X>x+y\}\cap\{X>y\})}{P(X>y)}
\\&=\frac{P(X>x+y)}{P(X>y)}
\\&=\frac{1-P(x\geq X+y)}{1-P(X\geq y)}
\\&=\dots\\&=1-(1-e^{-\lambda x})
\\&=1-P(X)
\\&=P(X>x)\end{align}$$
(Noe that the second part of the previous example is essentially proving exponential is memory less)