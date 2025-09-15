---
title: pros & cons of binary search tree
created: Before 28th July, 2025
last_modified: Tuesday 15th July 2025 04:18
tags:
  - computer-science/structure/binary-search-tree
course:
  - CSCA48
---
Consider the following aspects of BST, linked list and sorted array

## initiate a BST
- It takes a linked list and arrays $O(N)$ time to be built
- It takes BST $O(N\log N)$ time to be built on average

	linked list > array > BST

(Note > here means better, not longer)
## sorting
- It takes an array $O(\log(N))$ to be sorted on average
- It takes a BST $O(\log(N))$ to be sorted on average
- It takes a linked list $O(N\log(N))$ to be sorted on average (with merge sort)

sorted array > BST > linked list

Note that sorted array is "almost" the same as BST, slightly faster by milli
## search complexity
- It takes sorted array $O(\log(N))$ worst case using binary search
- It takes linked list $O(N)$ both average and worst case
- It takes BST $O(\log(N))$ average, $O(N)$ worst case

sorted list > BST > linked list, unsorted array
## storage
- Array takes fixed size, bad bad for growing/shrinking collections
- Linked list: space usage is $O(N)$
- BST: space usage is $O(N)$

BST = linked list > array