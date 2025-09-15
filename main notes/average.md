---
title: average
created: Before 28th July, 2025
last_modified: Monday 28th July 2025 17:24
tags:
  - probability/average
  - probability/variance
  - probability/expected-value
course:
  - STAB52
LEC: 11
---
Let $X_{1},\dots,X_{n}$ be a sequence of independent RVs, then their average is
$$
\overline{X}_{n}=\frac{1}{n}(X_{1}+\dots+X_{n})
$$
# mean and variance of average
__Mean__ and __variance__ of average of iid RVs are 
$$
\begin{align}

&E(\overline{X})=\mu \\
&V(\overline{X})=\frac{\sigma^2}{n}
\end{align}
$$

## proof
__Mean__ of the average can be calculated by:
$$
\begin{align}
E(\overline{X})&=E\left( \frac{1}{n}(X_{1}+\dots+X_{n}) \right) \\
&=\frac{1}{n}(E(X_{1})+\dots+E(X_{n})) \\
&=\frac{1}{n}(\mu+\dots+\mu) \\
&=\mu
\end{align}
$$
(Note that this result holds for any value of $n$, and also holds for dependent RVs $X_{1},\dots,X_{n}$, however, it doesn't hold for independent RVs $X_{1},\dots,X_{n}$)
__Variance__ of the average can be calculated by:
$$
\begin{align}
V(\overline{X})&=V\left( \frac{1}{n}(X_{1}+\dots+X_{n}) \right) \\
&=\frac{1}{n^2}(V(X_{1}+\dots+X_{n})) \\
&=\frac{1}{n^2}\left( V(X_{1})+\dots+V(X_{n})+\sum_{i\neq j}Cov(X_{i},X_{j}) \right) \\
&=\frac{1}{n^2}\left( \sigma^2+\dots+\sigma^2 \right) \\
&=\frac{\sigma^2}{n}
\end{align}
$$

_example_
![[weak law of large numbers (WLLN) 2025-07-22 14.58.11.excalidraw]]