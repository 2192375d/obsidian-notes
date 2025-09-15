---
title: convolution (sum of RVs)
created: Before 28th July, 2025
last_modified: Wednesday 16th July 2025 09:39
tags:
  - probability/method
course:
  - STAB52
LEC: 7
---
# sum of RVs
__Sum of RVs__ $X_{1}+X_{2}+\dots$ is tranformation of particular importance.
	Can be used to model aggregate behavior, e.g. total/average performance

# CDF found using joint PMF
Consider we are given RVs $X,Y$ with joint PMF, and $(X,Y)\in R$ and let $Z=X+Y$, then CDF of $Z$ is
$$
F_{Z}(z)=P(Z\leq z)=P(X+Y\leq z)=P(Y\leq z-X)=\sum \sum_{R}p_{X,Y}(x,y)
$$
# CDF found using joint PDF
Consider we are given RVs $X,Y$ with joint PDF, and $(X,Y)\in R$ and let $Z=X+Y$, then CDF of $Z$ is
$$
F_{Z}(z)=P(Z\leq z)=P(X+Y\leq z)=P(Y\leq z-X)=\iint_{R}f_{X,Y}(x,y)dxdy
$$

# PDF of sum of RVs
__convolution method__ finds PDF of $Z=X+Y$ directly, where PDF is given by
$$
f_{Z}(z)=\int_{-\infty}^{+\infty}f_{X,Y}(x,z-x)dx=\int_{-\infty}^{+\infty}f_{X,Y}(z-y,y)dy
$$
As for discrete RVs $X,Y$
$$
p_{Z}(z)=\sum_{x}p_{X,Y}(x,z-x)=\sum_{y}p_{X,Y}(z-y,y)
$$
_example_
- Let $Z=X+Y$ be the sum of two i.i.d. $Exponential(\lambda)$ RVs $X,Y$. Find PDF of $Z$
<br>
Note that $f_{X}(x)=\lambda e^{-\lambda x},f_{Y}(y)=\lambda e^{-\lambda y}$
As $X,Y$ are independent, $f_{X,Y}(x,y)=f_{X}(x)f_{Y}(y)=\lambda^2e^{-\lambda(x+y)}$
(Note that $x+y=z$ implies $x<z$)
By convolution method,
$$
\begin{align}
f_{Z}(z)&=\int_{0}^zf_{X,Y}(x,z-x)dx \\
&=\int_{0}^z\lambda^2e^{-\lambda(x+z-x)}dx \\
&=\int_{0}^z\lambda^2e^{-\lambda z}dx \\
&=\lambda^2ze^{-\lambda z}
\end{align}
$$
Note that this is the PDF of $Gamma(\alpha=2,\lambda)$