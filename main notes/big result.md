---
title: Big Result
created: Friday 10th October 2025 14:28
last_modified: Friday 10th October 2025 14:28
aliases: []
tags:
  - computer-science/computation-logic
course:
  - CSCB36
LEC:
  - "6"
---
# big result
Let $L$ be a language, then the followings are equivalent
- $L=\mathcal{L}(R)$ for some regex $R$
- $L=\mathcal{L}(M)$ for some DFSA $M$
- $L=\mathcal{L}(M)$ for some NFSA $M$

## NFSA to DFSA (not proof, sample example)
Consider this NFSA:
![[big result 2025-10-10 14.35.33.excalidraw|70%]]

Note that the states of DFSA are all subsets of NFSA
![[big result 2025-10-10 14.37.06.excalidraw|100%]]

# big result+
Let $L$ be a language, then the followings are equivalent
- $L=\mathcal{L}(R)$ for some regex $R$
- $L=\mathcal{L}(M)$ for some DFSA $M$
- $L=\mathcal{L}(M)$ for some NFSA $M$
- $L=\mathcal{L}(G)$ for some right linear CFG $G$
- $L=\mathcal{L}(G)$ for some strictly right linear CFG $G$

# big result 2
Let $L$ be a language, then the followings are equivalent
- $L=\mathcal{L}(G)$ for some CFG $G$
- $L=\mathcal{L}(M)$ for some PDA $M$
