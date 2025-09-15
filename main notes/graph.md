---
title: graph
created: Before 28th July, 2025
last_modified: Monday 7th July 2025 14:58
tags:
  - computer-science/structure/graph
course:
  - CSCA48
---
A graph consists of
- A set $V$ of __nodes__ (or vertex), where the size of $V$ (number of nodes in the graph) is $N$
- A set $E$ of __edges__
Together we define the graph $G=(V,E)$

There are two types of graphs: __undirected graphs__, __directed graphs__.
which are: ___boring___

## Terminologies for graphs
<u>neighbours</u>
For undirected graphs, a node v is a __neighbour__ of u if they are connected by an edge, we also say they are __adjacent__.
For directed graphs, a node v is an __out-neighbour__ of u if there is an edge from u to v, conversely, v is an __in-neighbour__ of u if there is an edge from v to u.

<u>neighbourhood</u>
For undirected graphs, a __neighbour__ of a node u is the set of all nodes that is neighbours of u. 
For directed graphs, an __out-neighbourhood__ or __in-neighbourhood__ corresponds to neighborhoods to out-neighbour and in-neighbour. 

<u>degree</u>
For an undirected graph, the __degree__ of node u is the size of the neighbourhood of u.
Similarly, for directed graph, there are __out-degree__ and __in-degree__

<u>path</u>
A __path__ through a graph is a sequence of con