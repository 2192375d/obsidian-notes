---
title: Gaussian elimination complexity
created: Monday 20th October 2025 14:39
last_modified: Monday 20th October 2025 14:39
aliases:
  - flop
tags:
  - math/linear-algebra/matrix
  - math/application
course:
  - CSCC37
LEC:
  - "6"
---

# flop (what counts as an unit of complexity)
We will count multiplication or addition pairs, for example, for 
$$
mx+b
$$
$mx$ is multiplication and $+b$ is addition

Such pair is called a __flop__ (floating point operation)

The Flop is the most expensive operation (much more expensive than a comparison), so we count flops only

# Gaussian elimination complexity
## Computing the LU factorization
1st stage: Eliminate first column of $A$

![[Gaussian elimination complexity 2025-10-20 14.52.30.excalidraw]]
Adding multiples of row 1 to row 2,...,n costs $(n-1)^2$ flops
Similarly:
2nd stage: $(n-2)^2$ flops
3rd stage: $(n-3)^2$ flops
...
(n-1)th stage: $1$ flop
Total: $\displaystyle(n-1)^2+(n-2)^2+\dots+1^2=\frac{n(n-1)(2n-1)}{6}$ flops

Thus, the complexity is $\displaystyle\frac{n^3}{3}+O(n^2)$ (Big-O assymptote complexity)
Or simply $O(n^3)$

Note that we use the different notation because they are different __aymptotely__, and for very large $n$, there will be a difference between $\displaystyle\frac{n^3}{3}+O(n^2)$ and $\displaystyle\frac{n^3}{2}+O(n^2)$

## compute forward solve $Ld=b$
![[Gaussian elimination complexity 2025-10-20 15.04.59.excalidraw|100%]]
Thus, we end up with a total of $\displaystyle0+1+2+\dots+(n-1)=\frac{n(n-1)}{2}$ flops
Which is, $\displaystyle \frac{n^2}{2}+O(n)$ flops


## compute backsolve $Ux=d$
Pretty much the same as above, we end up with $\displaystyle \frac{n(n-1)}{2}$ flops that is $\displaystyle \frac{n^2}{2}+O(n)$ flops

# total complexity
Total forward/backward solve complexity: $n^2+O(n)$ flops
Total LU factorization complexity $\displaystyle\frac{n^3}{3}+O(n^2)$ flops (i.e. facorization costs $\displaystyle\frac{n}{3}$ times as much as solving)

If you have several systems to solve with the same coefficient matrix $A$ but different $b$ (right hand side)
ie: $Ax=b$, $Ax=c$, $Ax=l$, $Ax=F$, ...
(Any of the above)
It's MUCH CHEAPER to just factor $A$ only ones and do the solving individually, by much cheaper, solving individual ones are $\displaystyle\frac{n}{3}$ cheaper (except for the first one)