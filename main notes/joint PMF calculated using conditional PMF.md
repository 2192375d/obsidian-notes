---
title: joint PMF calculated using conditional PMF
created: Before 28th July, 2025
last_modified: Monday 28th July 2025 16:59
tags:
  - probability/PMF
course:
  - STAB52
LEC: 7
---
# joint PMF calculated using conditional PMF 
In general, 
$$\begin{align}
p_{X,Y}&=P(X=x,Y=y) \\
&=P(X=x)P(Y=y|X=x) \\
&=p_{X}(x)p_{Y|X}(y|x), \ \ \ \forall x,y
\end{align}
$$
_example_
Roll 2 fair dices; let $X_{min},X_{max}$ be max/min of rolls, find the conditional PMF of $X_{max}|X_{min}=3$
$$\begin{align}p_{X_{max}|X_{min}}(x|3)&=\frac{p_{X_{min},X_{max}}(3,x)}{p_{X_{min}}(3)} \\ &=\begin{cases} \frac{\frac{1}{36}}{\frac{7}{36}}=\frac{1}{7}, &x=3 \\
\frac{\frac{2}{36}}{\frac{7}{36}}=\frac{2}{7},&x=4 \\
\frac{2}{7},&x=5 \\
\frac{2}{7},&x=6 \\
0.0,&o/w
\end{cases}
\end{align}
$$