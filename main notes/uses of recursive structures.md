---
title: uses of recursive structures
created: Before 28th July, 2025
last_modified: Tuesday 15th July 2025 05:06
tags:
  - computer-science/recursion
course:
  - CSCA48
---
# computer graphics (D18)
- Objects are composed of parts, thus often represented using graphs, or recursive structure
- The rendering (drawing) process for certain plants like ferns and trees is naturally recursive
- Animation of objects routintely requires us to recursively apply transformations to objects and their parts/sub parts (e.g. machines with lots of gears)
- The most advanced rendering methods (high quality scenes) are naturally recursive. They rely on tracing the path of light as it bounces from one object to another, then another, then another, and so on until the entire path of light from a light-emitting object to the camera has been found.

# programming languages (C24)
To become a serious software developer, you need to learn different programming paradigms. C is based on imperative programming model - a language where program statements change the value of data and the state of the program in order to achieve the program's goal.

However, there is a different programming model called __functional programming__, which is based on the concept of a program being the result of the evaluation of a set of mathematical expressions or functions. One example of it is __LISP__ with its derivatives (Scheme, Racket and Haskell), and they heavily rely on recursion.

# file system organization 
Consider the structure of the file system in the computer. The information are organized by folders, each of them will contain multiple items which are also, folders. The structure of the directories in the file system is straight up a tree (graph), and is recursive.

_example_
Consider the following algorithm for finding a particular name of a file in the computer
```
findFile(directory, file_name)
	if file is matching with file_name
		return directory
	else
		for every sub_directory in directory
			return findFile(sub_directory, file_name)
```
