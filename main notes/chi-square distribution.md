---
title: chi-square distribution
created: Sunday 3rd August 2025 01:14
last_modified: Sunday 3rd August 2025 01:14
aliases: 
tags:
  - probability/distribution
course:
  - STAB52
LEC: 12
---

Let $\displaystyle Z_{1},\dots,Z_{n}\sim^{iid}N(0,1)$, then $\displaystyle\begin{cases}Z_{1}^2\sim Gamma\left( \frac{1}{2}, \frac{1}{2} = \chi^2(1)\right) \\ Z_{1}^2+\dots +Z_{n}^2\sim Gamma\left( \frac{n}{2}, \frac{1}{2} \right)=\chi^2(n)\end{cases}$
# chi-square distribution
In general $Gamma\left( \frac{n}{2}, \frac{1}{2} \right)$ is called __chi-square__ distribution with parameter $n$, where $n$ is the degree of freedom is the degree of freedom.
__sample variance__ is given by
$$
\frac{(n-1)S_{n}^2}{\sigma^2}=\frac{\sum_{i=1}^n(X_{i}-\overline{X}_{n})^2}{\sigma^2}\sim \chi^2(n-1)
$$
(Result derived from $\displaystyle \sum_{i=1}^n\left(\frac{X_{i}-\mu}{\sigma}\right)^2\sim \chi^2(n)$)

## Proof of $X\sim N(0,1)\to Z^2\sim \chi^2(1)$
![[chi-square distribution 2025-08-03 01.22.37.excalidraw]]
## proof of $\displaystyle\frac{(n-1)S_{n}^2}{\sigma^2}\sim \chi^2(n-1)$