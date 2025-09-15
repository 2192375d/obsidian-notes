---
title: distributions as sum of i.i.d. RVs
created: Saturday 2nd August 2025 13:50
last_modified: Saturday 2nd August 2025 13:50
aliases: 
tags:
  - probability/iid
  - probability/distribution
course:
  - STAB52
---
Let $X_{1},\dots,X_{n}$ be i.i.d. RVs, then
# Bernoulli and binomial
if $X_{i}\sim Bernoulli(p)$, then
$$
X_{1}+\dots+X_{n}\sim binomial(n,p)
$$

# geometric and negative binomial
if $X_{i}\sim geometric(p)$, then
$$
X_{1}+\dots+X_{n}\sim negbinom(n,p)
$$

# exponential and gamma
if $X_{i}\sim exponential(\lambda)$, then
$$
X_{1}+\dots+X_{n}\sim gamma(n,\lambda)
$$
