---
title: regular expression
created: Wednesday 1st October 2025 19:50
last_modified: Wednesday 1st October 2025 19:50
aliases:
  - regex
tags:
  - computer-science/string/regex
course:
  - CSCB36
LEC:
  - "5"
---
# regular expression (regex)
A __regex__ is a specific type of nonempty string with the following alphabet (given another alphabet $\Sigma$)
$$
\Sigma\cup \{ \emptyset,\epsilon,+,*,(,) \}
$$

(Note that all of those (eg $\emptyset$) are just characters, not an actual set like empty set)

## definition for the set of ALL regexes (syntax of regex)
We going to define $\mathcal{RE}$ as the set of all regexes over $\Sigma$ using __structural induction__

Let $\mathcal{RE}$ be the smallest set S.T.
basis: $\emptyset,\epsilon\in\mathcal{RE},c\in\mathcal{RE}$ for every $c\in\Sigma$
induction step: if $S,T\in\mathcal{RE}$, then $(S+T),(ST),S^*\in\mathcal{RE}$

## what each regex matches to(semantics of regex)
Each regex maches with a set of strings

We use $\mathcal{L}(R)$ to represent the set of all strings $R$ maches
- $\mathcal{L}(\emptyset)=\emptyset$
- $\mathcal{L}(\epsilon)=\{ \epsilon \}$
- $\mathcal{L}(c)=\{ c \}$, for every $c\in \Sigma$
- $\mathcal{L}((S+T))=\mathcal{L}(S)\cup\mathcal{L}(T)$
- $\mathcal{L}((ST))=\mathcal{L}(S)\mathcal{L}(T)$
- $\mathcal{L}(S^*)=\mathcal{L}(S)^*$

## regex equivalence definition
2 regexes $R,S$ are equivalent iff $\mathcal{L}(R)=\mathcal{L}(S)$, denoted as $R\equiv S$
