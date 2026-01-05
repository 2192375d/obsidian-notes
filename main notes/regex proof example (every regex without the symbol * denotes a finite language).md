---
title: regex proof example (every regex without the symbol * denotes a finite language)
created: Friday 3rd October 2025 14:18
last_modified: Friday 3rd October 2025 14:18
aliases: []
tags:
  - computer-science/string/regex
course:
  - CSCB36
LEC:
  - "5"
---
Consider proving:
- Every regex without the symbol $*$ denotes a finite language

Define $P(R)$: if $R$ does not contain the symbol $*$, then $\mathcal{L}(R)$ is finite
WTP: $P(R)$ holds for all regexes $R\in\mathcal{RE}$

basis case: Consider $R=\emptyset,R=\epsilon,R=c$, where $c\in\Sigma$
case 1: $R=\emptyset$
Then, $R$ does not contain the symbol $*$ and $\mathcal{L}(R)=\emptyset$ which is finite
As wanted
case 2: $R=\epsilon$
Then, $R$ does not contain the symbol $*$ and $\mathcal{L}(R)=\{ \epsilon \}$ which is finite
As wanted
case 3: $R=c$, where $c\in\Sigma$
Then, $R$ does not contain the symbol $*$ and $\mathcal{L}(R)=\{ c \}$, which is finite
As wanted

induction step: Let $S,T$ be regexes,
Suppose $P(S)$ and $P(T)$ hold \[IH\]
Consider cases: $R=S+T,R=ST,R=S^*$

case 1: $R=S+T$
Then, $\mathcal{L}(R)=\mathcal{L}(S+T)=\mathcal{L}(S)\cup\mathcal{L}(T)$
Note that $\mathcal{L}(S)$ and $\mathcal{L}(T)$ are finite by IH, thus $\mathcal{L}(R)$ is finite
As wanted

case 2: $R=ST$
Then, $\mathcal{L}(R)=\mathcal{L}(ST)=\mathcal{L}(S)\mathcal{L}(T)$
Note that $\mathcal{L}(S)$ and $\mathcal{L}(T)$ are finite by IH, thus $\mathcal{L}(R)$ is finite
As wanted

case 3: $R=S^*$
Then, $R$ contains $*$, thus $P(R)$ is vaccuously true
As wanted