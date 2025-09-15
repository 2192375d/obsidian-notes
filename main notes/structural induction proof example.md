---
title: structural induction proof example
created: Friday 12th September 2025 14:33
last_modified: Friday 12th September 2025 14:33
aliases:
tags:
  - math/induction
  - computer-science/computation-logic
course:
  - CSCB36
LEC:
  - "2"
---
# structural induction on $\operatorname{vr}$ and $\operatorname{op}$ example
For $e\in \Sigma^*$, we define
- $\operatorname{vr}(e)$ to be the number of occurrences of variables in $e$
- $\operatorname{op}(e)$ to be the number of occurrences of operators in $e$

We define a predicate on $\Sigma^*$ 
$$
P(e):\operatorname{vr}(e)=\operatorname{op}(e)+1
$$
WTP: $\forall e\in\mathcal{E},P(e)$ by structural induction

_proof_
-  basis: Consider 3 cases: $e=x,e=y,e=z$,
	For $e=x,\operatorname{vr}(e)=1,\operatorname{op}(e)=0$
	$vr(e)=op(e)+1$, as wanted
	(same for the other two cases)

 - induction step: Let $e_{1},e_{2}\in\mathcal{E}$,
	Suppose $P(e_{1}),P(e_{2})$ \[IH\]
	(Ie $\operatorname{vr}(e_{1})=\operatorname{op}(e_{1})+1$, $\operatorname{vr}(e_{2})=\operatorname{op}(e_{2})+1$)
	WTP $P(e)$ for 4 cases: $(e_{1}+e_{2}),(e_{1}-e_{2}),(e_{1}\times e_{2}),(e_{1}\div e_{2})\in\mathcal{E}$
	
	For $e=(e_{1}+e_{2})$, 
	$$
\begin{align}
\operatorname{vr}(e)&=\operatorname{vr}(e_{1})+\operatorname{vr}(e_{2}) \\
&=\operatorname{op}(e_{1})+1+\operatorname{op}(e_{2})+1&&\text{[IH]} \\
&=\operatorname{op}(e)+1
\end{align}
$$
	As wanted
	(the 3 other cases' proof is left for the reader)

# Why "smallest"?
Let $S$ be the __smallest__ set S.T.
- basis: $0\in S$
- induction step: if $n\in S$, then $n+1\in S$
Then, $S=\mathbb{N}$

Without the word smallest, we lose the uniqueness of $S$, for example, $S$ can be $\mathbb{Z}, \mathbb{R}, \{ -1 \}\cup\mathbb{Z}$