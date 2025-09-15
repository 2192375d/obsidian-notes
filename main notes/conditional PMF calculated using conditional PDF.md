---
title: conditional PMF calculated using conditional PDF
created: Before 28th July, 2025
last_modified: Monday 28th July 2025 17:04
tags:
  - probability/CDF
  - probability/conditional
course:
  - STAB52
LEC: 7
---
# Calculate conditional probability using conditional PDF
$f_{X|Y}(x|y)$ can be integrated to find conditional probabilities:
$$
P(X\in A|Y=y)=\int_{A}f_{X|Y}(x|y)=P(X\leq x|Y=y)=\int_{-\infty}^xf_{X|Y}(t|y)dt
$$
