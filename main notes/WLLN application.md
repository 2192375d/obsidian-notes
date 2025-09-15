---
title: WLLN application
created: Before 28th July, 2025
last_modified: Monday 28th July 2025 17:27
tags:
  - probability/average
  - probability/convergence
course:
  - STAB52
LEC: 11
---
WLLN has applications in 
- Statistics: Estimate mean $\mu = E(X)$ of unknown distribution by averaging random values $X_{1},X_{2},\dots$ (a.k.a. samples)
$$
\overline{X}_{n}=lim\frac{1}{n}\sum_{i=1}^nX_{i}\to \mu
$$
, for $n\to \infty$
- simulation: Approximate probability of event $A$ by repeating experiment and counting average number of times an event occurs
$$
\overline{P}_{n}=\frac{1}{n}\sum_{i=1}^nI_{i}(A)\to P(A)
$$
, as $n\to \infty$
Note that $I_{i}(A)$ is the indicator variable of $A$ occuring, so we get $E(I_{i})=P(A)$

_example_
Consider flipping a fair coin 1000 times.
![[Pasted image 20250722152229.png]]
Chance of getting head approaches to $\frac{1}{2}$ as number of flips approaches to $\infty$
Note that as $n\to \infty$, the shape "converges" to a __normal distribution__