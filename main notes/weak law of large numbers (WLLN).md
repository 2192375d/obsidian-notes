---
title: weak law of large numbers (WLLN)
created: Before 28th July, 2025
last_modified: Tuesday 22nd July 2025 15:05
tags:
  - probability/average
  - probability/convergence
  - theorem
course:
  - STAB52
LEC: 11
---
# theorem
Average of __independent__ RVs with finite variance __converges__ to their common mean $\mu$
$$
P(|\overline{X}_{n}-\mu|\geq \epsilon)
$$
, as $n\to \infty, \forall \epsilon>0$

## proof
By Chebyshev's inequality,
$$
\begin{align}
\lim_{ n \to \infty } P(|\overline{X}_{n}-\mu|\geq \epsilon)&\leq \lim_{ n \to \infty } \frac{V(\overline{X}_{n})}{\epsilon^2} \\
&=\lim_{ n \to \infty } \frac{\frac{\sigma^2}{\epsilon}}{n} \\
&=0
\end{align}
$$

Note that there is also __strong law of large numbers (SLLN)__, that talks about converges in number instead of probability.

_example_
Let $X_{1},\dots,X_{n}\sim^{iid}N(0,1)$, show that $X_{n}\sim N\left( 0, \frac{1}{n} \right)$

Note that since $X_{1},\dots,X_{n}$ follows standard normal, we get
$E(X_{i})=0=\mu$
$V(X_{i})=1=\sigma^2$

Thus, we get $E(\overline{X}_{n})=0,V(\overline{X}_{n})=\frac{\sigma^2}{n}=\frac{1}{n}$

If we plot the distribution with different $n$, we get
![[Pasted image 20250722145411.png]]
based on the graph, we can tell as $n\to \infty$, evertyhing are more concentrated to the center.