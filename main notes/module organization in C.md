---
title: module organization in C
created: Before 28th July, 2025
last_modified: Monday 28th July 2025 00:48
tags:
  - computer-science/software-development
course:
  - CSCA48
---
In C, we use __include__ to import all the code into a single program which is compiled into our application's executable.

We can think about individual head files as __modules__ that will be implemented as part of the application's functionality.

In C, we do module organization by
- __header file__: the __.h files__, contain only the function declarations, with no code
- __program files__: the __.c files__, contain the actual code needed to implement the functions declared in the header file.

We do this so that we can:
- Compile each seperate module into executable code with placeholders or functions from other modules
- Linking all the moduels together, bringing together the code that implements the functionality from each of the modules, and updating the place-holders with the actual function calls to implement function code.