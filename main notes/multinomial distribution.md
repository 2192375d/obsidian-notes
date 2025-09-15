---
title: multinomial distribution
created: Before 28th July, 2025
last_modified: Monday 28th July 2025 16:50
tags:
  - probability/distribution
course: STAB52
LEC: 6
---

# multinomial distribution
Consider $n$ __independent trials__, each resulting in one of $k$ categories with corresponding probabilities $p_1,\dots,p_k$
Then, the joint distribution of result categories counts $x_{1},\dots,x_{k}$
$$
p(x_{1},\dots,x_{k})=\frac{n!}{x_{1}!\dots x_{k}!}p_{1}^{x_{1}}\dots p_{k}^{x_{k}}\text{ for }\begin{cases}
x_{1},\dots,x_{k}\geq 0 \\
x_{1}+\dots+x_{k}=n
\end{cases}
$$
Denoted $(X_{1},\dots,X_{n})\sim multinomial(n,p_{1},\dots,p_{n})$
_example_
Consider 10 rounds of rock-paper-scissors. What is the marginal distribution of the # of wins?
	Let RV's $X_w,X_D,X_L$ be the # of wins/draws/loses over 10 rounds
	Note that $X_L=10-X_W-X_D$
	We have $(X_{W},X_{D},X_{L})\sim Multinomial\left( n=10,p_{W}=p_{L}=p_{D}=\frac{1}{3} \right)$
	Then, ...
	(I'm too lazy to write)

Similar example is from PS6 Q10