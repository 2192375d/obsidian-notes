---
title: language operation
created: Wednesday 1st October 2025 17:56
last_modified: Wednesday 1st October 2025 17:56
aliases:
  - Kleene star
tags:
  - computer-science/string
course:
  - CSCB36
LEC:
  - "5"
---
# language operation
Let $L$ be a language, then
- complement: $\overline{L}=\{ x\in \Sigma^*:x\notin L \}$
- union: $L_{1}\cup L_{2}=\{ x:x\in L_{1} \text{ or }x\in L_{2}\}$
- intersection: $L_{1}\cap L_{2}=\{ x:x\in L_{1}\text{ and }x\in L_{2} \}$
- concatenation: $L_1\cdot L_2=\{xy:x\in L_1\text{ and }y\in L_2\}$
- Kleene star: $L^*=\{ x:x=\epsilon \text{ or }x=y_{1}y_{2}\dots y_{k},\text{ where }k>0 \text{ and each }y_{i}\in L \}$
- exponentiation ($k\in\mathbb{N}$): $L^k=\begin{cases} \{ \epsilon \},&k=0 \\ L^{k-1}L, &k>0\end{cases}$
- reversal: $\operatorname{Rev}(L)=\{ x^R:x\in L \}$, where $x^R$ is the reversal of $x$