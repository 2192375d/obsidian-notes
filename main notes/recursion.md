---
title: recursion
created: Before 28th July, 2025
last_modified: Tuesday 15th July 2025 05:21
tags:
  - computer-science/recursion
course:
  - CSCA48
---
We use recursion when
- The problem is complex
- It can be broken down into smaller/simpler versions of itself
- The same process applies to the original problem, and to the progressively smaller instances of it
- At some point, the solution to one of the small problems becomes easy to compute, we can stop breaking down into smaller problems and simply return the solution
- The process goes back building a solution for larger and more complicated subproblems until the original problem is solved.

# structure of a recursive solution
Recursion has the following two components

<b>base case</b>: 
The simplest form of the problem to solve, to which  the answer can be computed and returned without additional recursion

_example_
- For strings, the base case is often an empty string or a string with one character only
- For numeric arrays, the base case often is an array with 1 entry only, or empty array
- For graph problems, the base case often involves with a graph with a single node only, or a graph where nodes being processed has a specfic property (e.g. for mapping applications, it could be that node being processed represents the location we're looking for)
- For search on different data structures, the base case is often having reached an empty sub-list, sub-tree, or the substructure with the item we're looking for

<b>recursive case</b>
The general case, where we split, simplify, or otherwise make the problem smaller and closer to the base case.

_example_
- For strings, the recursive step often breaks the string into smaller chunks, some problems will require taking out a particular character (first one or last one), others split the string in chunks at a specific point. Either wa7, the resulting substrings are closer to the base case
- For numeric arrays, the recursive step often splits the array into pairs of sub-arrays, until it is the closest to the base case
- For graphs, the recursive case often perform  processing on subsets of the graph (e.g. for mapping applications, it could be asking neighbour what the path to the desired location is). Another possibility is that the recursive step may split the graph into sub-graphs and process each of them recursively (e.g. tree traversals)
- For search, recursive step often calls for recursively searching over a subset of the data structure where we expect the information we want to be. (e.g. BST search)

## How to design a recursive solution?
Carefully consider your problem, write down and illustrate an example, then, consider
- What should be the base case for the problem?
- How many different base cases are there?
- Have you found all of them?

One you know the base case(s), look at your example, and ask yourself how you could split the problem into sub-problems to get closer and closer to the base case, where the solution can be used to solve the original problem, to eventually find out the recursive case.

Once this is done, double check how the recursive case can reach the base case in every case, then start implementing the solution.