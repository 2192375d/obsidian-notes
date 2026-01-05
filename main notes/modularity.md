---
title: modularity
created: Sunday 7th December 2025 13:46
last_modified: Sunday 7th December 2025 13:46
aliases: []
tags:
  - software-development/clean-code
course:
  - CSCB07
LEC:
  - "10"
---
## coupling
Coupling refers to the degree of interdependence between different modules

consequences of high coupling:
- reduced understandability
- higher error rate
- testing gets more challenging
- changes to one module requires modifications in another module
- limited reusability

strategies to reduce coupling:
- conform to the dependency inversion principle
- use composition instead of inheritance when reasonable
- proper usage of encapsulation
- following law of demeter

## cohesion
Cohesion refers to the degree of interconnectedness among elements within a module

consequences of low cohesion
- reduced understandability
- higher error rates
- changes to one part of the system may have unexpected side effects
- limited reusability

The most effective strategy to increase cohesion is to conform to the Single Responsibility Principle (SRP)
