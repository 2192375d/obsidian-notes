---
title: extended transition function
created: Wednesday 3rd September 2025 10:44
last_modified: Wednesday 3rd September 2025 10:44
aliases: []
tags:
  - computer-science/computation-logic/automata
course:
  - CSCB36
LEC: []
---
# extended transition function
Let $\delta:Q\times \Sigma\to Q$ be the transition function of a DFSA. Then, the __extended transition function__ of the DFSA is the function
$$
\delta^*:Q\times \Sigma^*\to Q
$$
defined by the structural induction on $x$:
- basis: $x=\epsilon$, then $\delta^*(q,x)=q$
- inductive step: $x=ya$, for some $y\in \Sigma^*$ and $a\in \Sigma$, where we assume, by induction, that $\delta^*(q,y)$ has been defined (in this case, that is $\delta^*(q,x)=\delta(\delta^*(q,y),a_{1}1)$)

In other words
$$
\delta^*(q,x)=\begin{cases}
q,&x=\epsilon \\
\delta(\delta^*(q,y),a) ,&x=ya,\text{ where }y\in\Sigma^*,a\in\Sigma
\end{cases}
$$