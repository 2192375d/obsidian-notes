---
title: regular language closure proof example (Ins0(L))
created: Friday 3rd October 2025 14:25
last_modified: Friday 3rd October 2025 14:25
aliases: []
tags:
  - computer-science/string/regex
course:
  - CSCB36
LEC:
  - "5"
---
# regular language closure proof example (Ins0(L))
Let $\Sigma=\{ 0,1 \}$, consider the following language operation
$$
\mathrm{Ins0}(L)=\{ y: \text{for some }u,v\in\Sigma^*,uv\in L,y=u0v \}
$$
For example $\mathrm{Ins 0}(\{ 101 \})=\{ 1010,0101,1001 \}$

Define predicate $P(R)$ for any regex $R$
- $P(R):$ There is a regex $R'$ S.T. $\mathcal{L}(R')=\mathrm{Ins0}(\mathcal{L}(R))$

WTP $P(R)$ holds for every regex $R$

basis case: Consider 3 cases $R=\emptyset,R=\epsilon,R=b$, where $b\in\Sigma$
case 1: $R=\emptyset$
- Let $R'=\emptyset$, then $\mathrm{Ins 0}(\mathcal{L}(R))=\emptyset=\mathcal{L}(R')$
	as wanted
case 2: $R=\epsilon$
- Let $R'=0$, then $\mathrm{Ins 0}(\mathcal{L}(R))=\{ 0 \}=\mathcal{L}(R')$
	as wanted
case 3: $R=b$, where $b\in\Sigma$
- Let $R'=(0b+b0)$, then $In$
	as wanted

induction step: Let $S,T$ be regexes
Suppose $P(S)$ and $P(T)$ hold \[IH\]
I.e. there are regexes $S',T'$ S.T. $\mathcal{L}(S')=\mathrm{Ins 0}(\mathcal{L}(S))$ and $\mathcal{L}(T')=\mathrm{Ins 0}(\mathcal{L}(T))$

Consider cases: $R=(S+T),R=(ST),R=(S^*)$
case 1: $R=(S+T)$
- 

case 2: $R=(ST)$

case 3: $$