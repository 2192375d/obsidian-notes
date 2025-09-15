---
title: merge sort time complexity
created: Wednesday 10th September 2025 16:42
last_modified: Wednesday 10th September 2025 16:42
aliases: []
tags:
  - computer-science/algorithm/sort
course:
  - CSCB36
LEC:
  - "2"
---
# Unwinding recurrence (lecture example)
Let $c(n)$ be thenumber of data assignments when sorting list of $n$ elements using mergesort
Then,
$$
c(n)=\begin{cases}
0,&n=1 \\
c\left( \left\lfloor  \frac{n}{2}  \right\rfloor  \right)+c\left( \left\lceil  \frac{n}{2}  \right\rceil  \right)+2n,&n>1
\end{cases}
$$

Supposed $n$ is a large power of $2$ (Ie $n=2^k$ for some large $k\in\mathbb{N}$)
Then, 
$$
\begin{align}
c(n)&=2c\left( \frac{n}{2} \right)+2n && \text{first iteration} \\
&=2\left( 2c\left( \frac{n}{4} \right)+2 \frac{n}{2} \right)+2n && \text{second iteration} \\
&=2^3\left( 2c\left( \frac{n}{8} \right) \right)+6n && \text{third iteration} \\
&\dots \\
&=2^ic\left( \frac{n}{2^i} \right)+2in && \text{i'th iteration} \\
&\dots \\
&=2^kc\left( \frac{n}{2^k} \right)+2kn && \text{last iteration} \\
&=2^kc(1)+2k\log_{2}n \\
&=2n\log_{2}n
\end{align}
$$
Thus, mergesort follow 
