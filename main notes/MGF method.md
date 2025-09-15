---
title: MGF method
created: Before 28th July, 2025
last_modified: Saturday 26th July 2025 13:11
tags:
  - probability/moment
  - probability/method
course:
  - STAB52
LEC: 10
---
MGF uniquely characterizes the distribution of a RV:

For RVs $X,Y$ with MGFs $m_{X}(t),m_{Y}(t)$
$$
m_{X}(t)=m_{Y}(t)\leftrightarrow X\sim Y
$$
($X\sim Y$ means $X$ and $Y$ are i.i.d.)

MGF can be used to find distribution of functions of RVs
- Let $Y=g(X_{1},\dots,X_{n})$ with $m_{Y}(t)=E(e^{tY})=E(e^{tg(X_{1}\dots X_{n})})$, then $m_{Y}(t)$ is MGF of some known distribution $\to$ $Y$ follows that distribution
- MGF is particularly useful for linear functions of independent RVs

# theorem
Let $Y=a_{1}X_{1}\dots a_{n}X_{n}$, where $X_{1},\dots,X_{n}$ are independent RVs
Then, 
$$
\displaystyle m_Y(t)=m_{X_{1}}(a_{1}t)\dots m_{X_{n}}(a_{n}t)=\prod_{i=1}^nm_{X_{i}}(a_{i})(t)
$$
## proof
![[MGF method 2025-07-15 15.25.40.excalidraw]]
In particular, for i.i.d. $X_{1},\dots,X_{n}$ and $Y=X_{1}+\dots+X_{n}$, we get $m_{Y}(t)=(m_{X}(t))^n$
![[MGF method 2025-07-15 15.32.22.excalidraw]]