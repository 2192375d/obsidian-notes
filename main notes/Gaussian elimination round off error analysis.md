---
title: Gaussian elimination round off error
created: Monday 20th October 2025 15:37
last_modified: Monday 20th October 2025 15:37
aliases: []
tags:
  - math/linear-algebra/matrix
  - math/application
course:
  - CSCC37
LEC:
  - "6"
---
In this analysis, we assume we are doing pivoting

The most crucial results of this page are in the $(*)$
# Gaussian elimination round off error analysis
Factorizaation: $PA=LU$
Because of rounding errors (both initial and propagated), we get $\hat{L},\hat{U},\hat{P}$ S.T. 
$$
\hat{P}(A+E)=\hat{L}\hat{U}
$$
By $\hat{P}$, we don't mean $P$ with small errors, instead the wrong permutation matrix due to round off error

Hopefully, $\lvert \lvert E \rvert \rvert$ is small compared to $\lvert \lvert A \rvert \rvert$ (if we pivot during the factorization)
Actually, solve (forward and backward) can introduce more roundoff error, but this can still be represented as:
$$
(A+\tilde{E})\hat{x}=b
$$
Where $\tilde{E}$ is slightly different than $E$

Note that for statement $(A+E)\hat{x}=b$, we have $E$ that captures ALL the roundoff error from ALL sources
Equivalently, let $E\hat{x}=r$, then
$$
(A+\overline{r})\hat{x}=b\text{ iff }r=b-A\hat{x}
$$
Where $r$ is the residual

Given what is above, what we care about is: "Is $||E||$ small compared to $||A||$?"

If we use row partial pivoting during the factorizaiton, we can show that:
$$
(*) \ ||E||\lesssim k\epsilon_{mach}||A||
$$
Where $k$ satisfies:
- is not too large
- grows with $n$
- depends on pivoting

Similarly, for the computed solution $\hat{x}$ and the residual $r=b-Ax$
$$
(*) \ ||r||\lesssim k\epsilon||b||\text{ iff } \frac{||I||}{||b||}\lesssim k\epsilon
$$
Note that $\displaystyle\frac{||I||}{||b||}$ is the relative residual

