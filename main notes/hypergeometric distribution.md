---
title: hypergeometric distribution
created: Before 28th July, 2025
last_modified: Sunday 20th July 2025 17:53
tags: [probability/distribution/discrete]
course: [STAB52]
LEC: 5
---
# definition
Let $X\sim hypergeomtric(N,M,n)$, then
$$
p_{X}(x)=\frac{\binom{M}{x}\binom{N-M}{n-x}}{\binom{N}{n}}
$$
# intuition
Consider drawing $n$ balls from a box, where $M$ balls are white and $N-M$ balls are black. 
Let RV $X$ be number of white balls drawn out of $n$ draws, then, $X$ follows a PMF of $hypergeometric(N,M,n)$.

In simple term:
- $N$ is the total number of balls
- $M$ is the number of balls you want
- $n$ is the number of draws you perform
Hypergeometric distribution is same as binomial distribution, except the balls drawn are not placed back after drawing 