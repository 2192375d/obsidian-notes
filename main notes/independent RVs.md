---
title: independent RVs
created: Before 28th July, 2025
last_modified: Thursday 17th July 2025 11:33
tags:
  - probability/independence
course:
  - STAB52
LEC: 7
---
# independent RVs
RVs $X,Y$ are __independent__ (denoted $X\perp Y$) if $\forall A,B\subset\mathbb{R}$
$$
P(X\in A,Y\in B)=P(X\in A)P(Y\in B)
$$




_example_
- Roll 2 dice & define RV's $X_1$=1st roll, $X_2$ = 2nd roll; are $X_1,X_2$ independent?
$$
p_{X_{1},X_{2}}(x,y)=\begin{cases} \frac{1}{36}=\frac{1}{6}*\frac{1}{6}=p_{X_{1}}(x)*p_{X_{2}}(y),&\forall x,y\in\{1,2,3,4,5,6\} \\
0.0,&otherwise
\end{cases}
$$
Thus, they are independent

- Let $X_{min}=min(X_1,X_2),X_{max}=max(X_1,X_2)$; are $X_{min},X_{max}$ independent?
	They are not independent as:
$$
p_{X_{min},X_{max}}(4,3)=0.0\neq p_{X_{min}}(4)*p_{X_{max}}(3)>0
$$