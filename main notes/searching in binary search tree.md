---
title: searching in binary search tree
created: Before 28th July, 2025
last_modified: Tuesday 15th July 2025 03:36
tags:
  - computer-science/algorithm/search
  - computer-science/structure/binary-search-tree
course:
  - CSCA48
---
The general algorithm is

```
if the queryKey is equal to the key at the root node of the subtree  
	Found the key! Return a reference to the root node of the subtree  
else  
	if the queryKey is less than or equal to the key in the root node of the subtree  
		searchForKey ← left subtree, queryKey  
	otherwise  
		searchForKey ←right subtree, queryKey
```

With a complexity of $O(log(N))$


