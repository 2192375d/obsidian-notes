---
title: formula normal form
created: Friday 14th November 2025 14:16
last_modified: Friday 14th November 2025 14:16
aliases:
  - literal
  - term
  - clause
  - DNF
  - CNF
tags:
  - math/logic
course:
  - CSCB36
LEC:
  - "10"
---

# literal/term/clause
- a __literal__ is a variable or the negation of a variable
- a __term__ is a literal or the cunjunction of two or more literals
- a __clause__ is a literal or the disjunction of two or more literals

# disjunctive/conjunctive normal form (DNF/CNF)
A __disjunctive normal form (DNF)__ formula is a term or the disjunction of two or more terms
A __conjunctive normal form (CNF)__ formula is a term or the conjunction of two or more clauses

## example
- $x \wedge \neg y\wedge z$, this is both a DNF and a CNF
- $(x\wedge y)\vee(\neg x\vee \neg y)$ is a DNF but not CNF