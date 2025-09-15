---
title: binary search tree traversal
created: Before 28th July, 2025
last_modified: Tuesday 15th July 2025 03:50
tags:
  - computer-science/structure/binary-search-tree
course:
  - CSCA48
---
The process of visiting each node in a BST is known as a __tree traversal__, there are three types of tree traversals

All three types do the following three actions
- A: Recursive call on the left subtree
- B: Recursive call on the right subtree
- C: visit root

_example_
```
void post_order(BST_Node *root){
	if(root == NULL){
		return;
	}
	
	post_order(root->left);
	post_order(root->right);
	printf("%d\n", root->value);
}
```
__In-order traversal__ does the following order: A->C->B, used for sorting a tree 
__Pre-order traversal__ does the following order: C->A->B, used for duplicating a tree
__Post-order traversal__ does the following order: A->B->C, used for deleting a tree

Note that in-order-traversal traverses based on the order from smallest to greatest