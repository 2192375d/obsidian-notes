---
title: principles of clean code
created: Monday 24th November 2025 15:27
last_modified: Monday 24th November 2025 15:27
aliases: []
tags:
  - software-development/clean-code
course:
  - CSCB07
LEC:
  - "10"
---
# features of clean code
- modularity
- readability
- efficiency
- error handling
- tests

## clean class
Classes should be small, by single responsibility principle
Classes should be cohesive
- small number of instace variables
- the more instance variables a method manipulates the more cohesive that method is to its class

## clean functions
Functions should be small
- blocks within if/else/while should be one line long (probably a function call)
- function should do one thing only, but it should do it correctly
- one level of abstraction per function
- name must be descriptive, even if it's long
- keep function arguments to a minimum
- function should either do something or answer something, but not both