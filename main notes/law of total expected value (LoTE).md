---
title: law of total expected value
created: Tuesday 29th July 2025 00:03
last_modified: Tuesday 29th July 2025 00:03
tags:
  - probability/expected-value
  - probability/conditional
course:
  - STAB52
LEC: 9
---
# law of total expectation
For discrete RVs X,Y
$$
E(g(Y))=E[E(g(Y)|X)]=
\sum_{x}E(g(Y)|X=x)p_{X}(x)
$$
For continuous RVs X,Y
$$
E(g(Y))=E[E(g(Y)|X)]=
\int_{x}E(g(Y)|X=x)f_{X}(x)dx
$$