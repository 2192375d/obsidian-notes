---
title: change of variables
created: Monday 11th August 2025 21:31
last_modified: Monday 11th August 2025 21:31
aliases: 
tags:
  - calculus/multivariable
  - calculus/integral
course:
  - MATB41
---
# u-sub in multivariable integral
Let $D$ and $D^*$ be elementary regions in a plane, $T:D^*\to D$ be $C^1$ and injective on $D^*$
Then for any integrable function $f:D\to\mathbb{R}$, we have
$$
\iint_{D}f(x,y)dxdy=\iint_{D^*}f(x(u,v),y(u,v))\left| \frac{\partial(x,y)}{\partial(u,v)} \right|dudv
$$
