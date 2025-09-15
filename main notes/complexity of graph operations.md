---
title: complexity of graph operations
created: Before 28th July, 2025
last_modified: Wednesday 9th July 2025 13:49
tags:
  - computer-science/structure/graph
  - computer-science/algorithm
course:
  - CSCA48
---
Let $n=|V|,m=|E|$, then

|                | adjacency list | adjacency matrix |
| -------------- | -------------- | ---------------- |
| edge query     | $O(n)$         | $O(1)$           |
| insert a node  | $O(1)$         | $O(n^2)$         |
| remove a node  | $O(m)$         | $O(n^2)$         |
| insert an edge | $O(1)$         | $O(1)$           |
| remove an edge | $O(n)$         | $O(1)$           |
