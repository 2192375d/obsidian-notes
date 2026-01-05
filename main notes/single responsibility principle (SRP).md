---
title: single responsibility principle
created: Monday 3rd November 2025 20:56
last_modified: Monday 3rd November 2025 20:56
aliases: []
tags:
  - computer-science/software-development/SOLID
course:
  - CSCB07
LEC:
  - "7"
---
# SRP
A class should only have one reason to change
- if you can think of more than one motive for changing a class, then taht class has __more__ than one responsibiliity
- if a class has more than one responsibility, then the responsibilities become coupled

Here is an example that violates SRP:
![[Pasted image 20251103205958.png]]

![[Pasted image 20251103210013.png]]

In the first picture, class `Rectangle` has two reasons to modify itself:
- for GUI
- for computation
To resolve this, we can use another class/interface called `GeometricRectangle` to handle the computation part