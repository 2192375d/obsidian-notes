---
title: divide and conquer method complexity
created: Wednesday 10th September 2025 16:17
last_modified: Wednesday 10th September 2025 16:17
aliases: []
tags:
  - computer-science/algorithm
---
# A general divide and conquer recurrence
The __divide and conquer__ method's time complexity can "usually" be expressed as
$$
T(n)=\begin{cases}
c,&1\leq n<b \\
a_{1}T\left( \left\lceil \frac{n}{b} \right\rceil \right)+a_{2}T\left( \left\lfloor  \frac{n}{b}  \right\rfloor  \right)+dn^l,&n\geq b
\end{cases}
$$
Where $c,d$ are values depending on what's considered as a step

# divide and conquer method time complexity
There is a constant $\kappa\geq0$ so that for any integer $n\geq b$, $n$ is a power of $b$, the time complexity of the divide and conquer method satisfies
$$
T(n)\leq
\begin{cases}
\kappa n^l,&a<b^l \\
\kappa n^l\log_{b}n,&a=b^l \\
\kappa n^{\log_{b}a},&a>b^l
\end{cases}
$$
