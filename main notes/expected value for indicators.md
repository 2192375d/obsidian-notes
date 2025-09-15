---
title: expected value for indicators
created: Before 28th July, 2025
last_modified: Monday 28th July 2025 17:13
tags:
  - probability/expected-value
course:
  - STAB52
LEC: 8
---
# theorem
Consider indicator RV $I_{A}(s)=\begin{cases}1,&s\in A \\ 0,&s\not\in A\end{cases}$ , for some $A\subset S$
Then, expected value of indicator RV is equal to probability of its defining event:
$$
E(I_{A})=P(A)
$$
# proof
$$
E(I_{A})=\sum_{x=0}^1xp_{I_{A}}(x)=0+1*p_{I_{A}}(0)=P(I_{A}=1)=P(A)
$$