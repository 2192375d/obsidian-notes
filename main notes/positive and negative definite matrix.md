---
title: positive and negative definite matrix
created: Tuesday 12th August 2025 01:53
last_modified: Tuesday 12th August 2025 01:53
aliases: 
tags:
  - math/linear-algebra/matrix
  - theorem
course:
  - MATB41
---
# positive and negative definite matrix
Let $M\in\mathcal{M}(\mathbb{R}^n)$, $Q_{M}=h^TMh,\forall h\in\mathbb{R}^n$
Then, $M$ is __positive definite__ if
$$
Q_{M}(h)>0,\forall h\neq 0 \text{ and }Q_{M}(h)=0 \text{ if and only if } h=0
$$
 M is __negative definite__ if
 $$
Q_{M}(h)<0,\forall h\neq 0 \text{ and }Q_{M}(h)=0 \text{ if and only if } h=0
$$

## characterization of positive and negative definite matrix
Let $A\in \mathcal{M}(\mathbb{R}^n)$, with $A=[a_{i,j}]$, $A_{k}$ be a submatrix of $A$ with $i,j\leq k$, then
$$
\begin{align}
&A \text{ is positive definite if and only if } \det(A_{k})>0,\forall_{1}\leq k\leq n \\
&A \text{ is negative definite if and only if signs of $A_{k}$ alternates, e.g. $\det(A_{1})< 0, \det(A_{2})>0,\det(A_{3})<0\dots$} 
\end{align}
$$
