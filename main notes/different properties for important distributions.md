---
title: expected value and variances for important distributions
created: Before 28th July, 2025
last_modified: Monday 28th July 2025 17:31
tags:
  - probability/expected-value
  - probability/variance
  - probability/distribution
  - probability/moment
course:
  - STAB52
LEC: 11
aliases:
  - expected value for important distributions
  - variance for important distributions
  - MGF for important distributions
---
# Bernoulli distribution:
Let $X\sim Bernoulli(p)$, then
$$
\begin{align}
&E(X)=p \\
&V(X)=p(1-p) \\
&m_{X}(t)=1-p+pe^t
\end{align}
$$
# binomial distribution
Let $X\sim binom(n,p)$, then
$$
\begin{align}
&E(X)=np \\
&V(X)=np(1-p) \\
&m_{X}(t)=[1-p+pe^t]^n
\end{align}
$$
# geometric distribution
Let $X\sim geometric(p)$, then
$$
\begin{align}
&E(X)=\frac{1}{p} \\
&V(X)=\frac{1-p}{p^2} \\
&m_{X}(t)= \frac{pe^t}{1-(1-p)e^t}
\end{align}
$$
# poisson distribution
Let $X\sim poisson(\lambda)$, then
$$
\begin{align}
&E(X)=\lambda \\
&V(X)=\lambda \\
&m_{X}(t)=\exp \{ \lambda(e^t-1) \}
\end{align}
$$
# negative binomial distribution
Let $X\sim negbinom(r,p)$, then
$$
\begin{align}
&E(X)=\frac{r}{p} \\
&V(X)=\frac{r(1-p)}{p^2} \\
&m_{X}(t)=\left( \frac{pe^t}{1-(1-p)e^t} \right)^r, t<-\ln(1-p)
\end{align}
$$
# hypergeometric distribution
Let $X\sim hypergeometric(n,M,N)$, then
$$
\begin{align}
&E(X)=? \\
&V(X)=? \\
&m_{X}(t)=?
\end{align}
$$
# uniform distribution
Let $X\sim uniform(l,u)$, then
$$
\begin{align}
&E(X)=? \\
&V(X)=? \\
&m_{X}(t)=?
\end{align}
$$
# exponential distribution
Let $X\sim exponential(\lambda)$, then
$$
\begin{align}
&E(X)=? \\
&V(X)=? \\
&m_{X}(t)=?
\end{align}
$$
# normal distribution
Let $X\sim normal(\mu,\sigma^2)$, then
$$
\begin{align}
&E(X)=? \\
&V(X)=? \\
&m_{X}(t)=?
\end{align}
$$
# gamma distribution
Let $X\sim gamma(a,\lambda)$, then
$$
\begin{align}
&E(X)=? \\
&V(X)=? \\
&m_{X}(t)=?
\end{align}
$$