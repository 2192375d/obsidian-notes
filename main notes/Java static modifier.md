---
title: Java static modifier
created: Monday 15th September 2025 19:53
last_modified: Monday 15th September 2025 19:53
aliases: []
tags:
  - computer-science/software-development/java
course:
  - CSCB07
LEC: 2
---
# static modifier
__static fields/methods__ can be accessed from any reference of the same class name
__non-statis (or instance) fields/methods__ can only be accessed from a reference variable

In other words, you cannot access a non-static reference from a static method.

## static modifier application
One application of static modifier is that you can keep track number of instances created from the same class by incrementing the a static variable count