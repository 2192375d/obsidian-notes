---
title: Hashset
created: Monday 6th October 2025 20:23
last_modified: Monday 6th October 2025 20:23
aliases: []
tags:
  - computer-science/software-development/generics
  - computer-science/software-development/java
course:
  - CSCB07
LEC:
  - "5"
---
# Hashset
A hashset is a generic class that can be used to store elements without duplicates
- no two elements `e1` and `e2` can be in the same set S.T. `e1.equals(e2)` returns true
Imported using `import java.util.HashSet;`
Any objects added to the hash set should override `equals` and `hashCode` properly

Commonly used methods:
- `boolean add(E e)`
- `int size()`
- `boolean contains(Object o)`
Also can be traversed using a for-each loop

Note that order doesn't have to be preserved inside a hashset, but __LinkedHashSet__ (a subclass of HashSet) will preserve the order