---
title: PDF method for RV transformation
created: Before 28th July, 2025
last_modified: Thursday 17th July 2025 11:23
tags:
  - probability/method
  - probability/PDF
course: STAB52
LEC: 6
---

# theorem
Let $Y=h(X)$ for continuous injective function $h$, where PDF $f_X(x)$ is known but there is no closed-form CDF

PDF of $Y$ is given by $$f_Y(y)=\frac{f_X(h^{-1}(y))}{|h'(h^{-1}(y)|)}$$
Interval around $y$ maps to interval around $h^{-1}(y)$ scaled by slope at $(y,h^{-1}(y))$, and so does PDF.

_example_
Let RV $U\sim Uniform(0,1)$ verify that $X=-ln(1-U)$ follows $Exp(X=1)$ using the PDF method
$$f_U(u)=\begin{cases}1,&u\in[0,1]\\0,&otherwise\end{cases}$$
	then, $$h(u)=-ln(1-u)\to\begin{cases}h^{-1}(x)=1-e^{-x}\\h'(u)=\frac{1}{1-u}\end{cases}$$we get,$$f_X(x)=\frac{f_U(h^{-1}(x)}{|h'(h^{-1}(x))|}=\frac{1}{|\frac{1}{1-h^{-1}(x)}|}=|e^{-x}|=e^{-x}, x>0$$
	which is PDF of $Exp(X=1)$