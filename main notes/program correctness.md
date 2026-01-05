---
title: program correctness
created: Wednesday 17th September 2025 15:38
last_modified: Wednesday 17th September 2025 15:38
aliases: []
tags:
  - computer-science/computation-logic/program-correctness
course:
  - CSCB36
LEC:
  - "3"
---
# Proving program correctness
## <u>notations</u>
Consider a variable $x$ and an iteration, then $x$ denotes the value before the iteration, and $x'$ denotes the value after the iteration

The same applies to an algebraic expression $e$
## <u>definition of 'correct' program</u>
We say a program is correct if:
if the proper condition holds, and program is run, and the program ends with the desired results, then the program is 'correct'
- __precondition__: 'the proper condition'
- __termination__: 'the program stops (halts)'
- __postcondition__: 'the desired result'
- __program's specification__: the pre & postcondition pair

In general:
<i>if precondition, then termination & postcondition</i>

This can be proven in two ways:
- precondition $\rightarrow$ (termination $\wedge$ postcondition)
- (precondition $\rightarrow$ termination) & (precondition $\wedge$ termination) $\rightarrow$ postcondition
In the second way, (precondition $\wedge$ termination) $\rightarrow$ postcondition is called 'partial correctness'
## <u>Principle of Well-Ordering (PWO)</u>
Every (strictly) decreasing sequence of natural numbers is finite


## <u>Loop Invariants (LI)</u>
Loop invariants (LI) are helpful for proving correctness of iterative programs
A LI is a statement that is true on entering a loop, and true after every iteration

To prove LI, we use induction:
- basis: we prove that LI holds on entering loop
- induction step: we prove if LI holds before iteration, then it holds after that iteration

## <u>steps to prove iterative is correct</u>
1. Formulate a LI
2. Prove LI holds on entering the loop, and still holds after every iteration (assuming precondition holds) using induction
3. Prove partial correctness using LI from step 1.
4. Prove termination using LI from step 1. This is done by setting a variable e:
	e is a natural number on entering the loop
	e decreases with every iteration
5. Prove the sequence of values of e after each iteration is a decreasing sequence of natural numbers. This means proving
	e is always a natural number
	e decreases with every iteration (e' < e)