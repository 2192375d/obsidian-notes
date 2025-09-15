---
title: depth first search
created: Before 28th July, 2025
last_modified: Thursday 24th July 2025 16:21
tags:
  - computer-science/structure/graph
  - computer-science/recursion
course:
  - CSCA48
---
The function should take current node, target node, and the adjacency matrix/adjacency list for the graph. And return the target node's address or anything like that.

base case 1:
- found the target node, return the target node
base case 2:
- all nodes processed, can't find target node, then return NULL.

recursive step:
- create a subgraph without current node
- recursively find destination in subgraph