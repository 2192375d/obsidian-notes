---
title: matrix norms properties
created: Wednesday 27th August 2025 13:30
last_modified: Wednesday 27th August 2025 13:30
aliases: []
tags:
  - math/linear-algebra/matrix
  - math/linear-algebra/norm
course: CSCC37
---
# matrix norm properties
For matrices $A$ and $B$,
1. $||A||>0$ if $A\neq 0$
2. $||\gamma A||=|\gamma|\cdot||A||$ for any scalar $\gamma$
3. $||A+B||<||A||+||B||$
4. $||AB||\leq||A||\cdot||B||$
5. $||Ax||\leq||A||\cdot||x||$ for any vector $x$

# other matrix norm properties
For any matrix $A$
$$
\begin{align}
||A||_{1}=\max_{j}\sum_{i=1}^n|a_{ij}| \\
||A||_{\infty}=\max_{i}\sum_{j=1}^n|a_{ij}|
\end{align}
$$