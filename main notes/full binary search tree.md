---
title: full binary search tree
created: Before 28th July, 2025
last_modified: Tuesday 15th July 2025 03:42
tags:
  - computer-science/structure/binary-search-tree
course:
  - CSCA48
---
In a __full BST__, every level except for the last one is full (fully occupied)

![[Pasted image 20250715033941.png]]

In a full BST, every level contains as many nodes as all the levels above +1.
Thus, a BST with $k$ levels can store up to $N=2^k$ keys. Thus, a collection with $N$ keys, we need a BST with at least $\log_{2}(N)$ levels.