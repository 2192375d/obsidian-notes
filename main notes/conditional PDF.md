---
title: conditional PDF
created: Before 28th July, 2025
last_modified: Monday 28th July 2025 17:03
tags:
  - probability/PDF
  - probability/conditional
course: STAB52
LEC: 7
---

# conditional PDF
Let continuous RVs $X,Y$ have a joint PDF $f_{X,Y}(x,y)$, then __conditional PDF__ of $X$ given $Y=y$ is defined as 
$$
f_{X|Y}(x|y)=\frac{f_{X,Y}(x,y)}{f_{Y}(y)},\text{{ for }}f_{Y}(y)>0
$$
# intuition
Note that $f_{X|Y}(x,y)$ cuts slice of $f_{X,Y}(x,y)$ at $Y=y$ and scales it by $\frac{1}{f_{Y}(y)}$, where $f_{Y}(y)=\text{slice area}$, so that it integrates to $1$, thus,
- $f_{X|Y}(x,y)\geq 0$
- $\int_{\mathbb{R}}f_{X|Y}(x|Y)dx=1.0$

_example_
Let $X,Y$ have joint pdf $f(x,y)=\begin{cases}3x,&0\geq y\geq x\geq 0\\0,&otherwise\end{cases}$
- find the conditional PDF of $Y$ given $X=0.5$
	First note that $$f_{X}(x)=\int_{-\infty}^{+\infty}f_{X,Y}(x,y)dy=\int_{-\infty}^00dy+\int_{0}^x(3x)dy+\int_{x}^{+\infty}0dy=3x^2$$
	Thus, 
	$$\begin{align}
f_{Y|X}(y,0.5)&=\frac{f_{X,Y}\left( \frac{1}{2},y \right)}{f_{X}\left( \frac{1}{2} \right)} \\
&=\frac{3*\left( \frac{1}{2} \right)}{3*\left( \frac{1}{2} \right)^2} \\ \\
&=2
\end{align}$$
