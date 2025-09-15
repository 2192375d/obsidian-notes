---
title: represent graphs
created: Before 28th July, 2025
last_modified: Tuesday 22nd July 2025 22:38
tags:
  - computer-science/structure/graph
course:
  - CSCA48
---
We use __adjacency list__ or __adjacency matrix__ to store a linked list

# represent graph using adjacency list
The __adjacency list__ is an array with one entry per node. Each entry in the array contains a pointer to a linked list that stores the indexes of nodes to which this entry is connected.

_example_
```
typedef struct node{
	int val;
	struct node *next;
}Node;

typedef struct{
	Node *lists[NUM_VERTICES]
}Graph;

int main(){
	Graph g;
	//stuffs to initialize g
	
	Node *p = (*g).lists[3];
	
	//Print all nodes connected to p
	while(p != NULL){
		printf("%d\n", p->val);
		p = p->next;
	}
}
```
# represent graph using adjacency matrix
The __adjacency matrix__ is a 2D float array of size $N\times N$, where if there is an edge from $i$ to $j$, then $A[i][j]=\text{the weight from i to j}$, if there is no edge from $i$ to $j$, then $A[i][j]=0$
For undirected graph, the matrix is symmetric.

_exercise_
![[represent graph using linked list 2025-07-15 04.42.40.excalidraw]]