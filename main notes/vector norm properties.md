---
title: vector norms properties
created: Monday 25th August 2025 01:37
last_modified: Monday 25th August 2025 01:37
aliases: []
tags:
  - math/linear-algebra/norm
course: CSCC37
---
# vector norm properties
For any vector $x$,
1. $||x||>0$ if $x\neq0$
2. $||\gamma x||=|\gamma|\cdot||x||,\forall \gamma\in\mathbb{R}$
3. $||x+y||\leq||x||+||y||$
4. $||x-y||\geq||x||-||y||$

# other properties regarding $p$-norm
For any vector $x\in\mathbb{R}^n$,
$$
\begin{align}
&||x||_{1}\geq||x||_{2}\geq\dots\geq||x||_{\infty} \\
&||x||_{1}\leq \sqrt{ n }||x||_{2} \\
&||x||_{2}\leq \sqrt{ n }||x||_{\infty} \\
&||x||_{1}\leq n||x||_{\infty} 
\end{align}
$$