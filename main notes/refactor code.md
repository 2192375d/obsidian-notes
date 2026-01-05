---
title: refactor code
created: Sunday 7th December 2025 18:41
last_modified: Sunday 7th December 2025 18:41
aliases: []
tags:
  - software-development/clean-code
course:
  - CSCB07
LEC:
  - "10"
---

# refactoring
Refactoring is the process of changing a software system in such a way that it does not alter the external behavior of the code yet it improves its internal structure

advantages of refactoring:
- improve software design
- making software easier to understand
- finding bugs more easily
- speeding up development

## how to refactor?
Process of refactoring should follow:
- apply changes in a sequence of small steps
- do not add new functionality
- make sure that all existing tests pass and add new ones if needed

refactoring methods:
- __extract method__: used when a bunch of code can be grouped together. 
	Solved by making those code a function
- __replace method with method object__: used when extract method doesn't work due to local variable usage. 
	Solved by turning the method itself into an object with those local variables as field
- __consolidate conditional expression__: used when you have a sequence of conditional tests with the same result.
	solved by making a boolean funciton that checks all the conditional tests.
- __consolidate dupplicate condidtional fragments__: used when a bunch of code is reused in every branch in a conditional expression.
	solved by moving it outside of the conditional expression
- __remove control flag__: used when you got a bunch of stupid if statements placed together, but if one of them happens then the rest of the if statements will never be true.
	solved by return/break
- __replace nested conditional with guard clauses__: used when you have a bunch of if-else statements
	solved by using return/break
- __replace magic nmber with symbolic constant__: title
- __parameterize method__: used when you got distinct methods like `fivePercentRaise()`, `tenPercentRaise()` doing almost the exact same thing except with a different value.
	solved by passing the value directly `raise(percentage)`
- __replace parameter with explicit methods__: reverse of the previous one, used when you have a method that does different things based on an enum parameter (eg. `setValue(String name, int value)`, where the method sets height if `name == "height"` and sets width if it's width.
	solved by making it two different functions `setHeight(int value)`, `setWidth(int value)`
- __introduce explaining variable__: bullshit thing that tells you to make a super long statement to a bunch of statements each with a variable.
- __extract class__: used when one class is doing the work that should be done by two
	solved by making two classes
- __extract superclass__: used when two independent classes have similar features
	solved by making them inherit from the same base class, base class containing the same features
- __extract subclass__: used when class `A` contains all features of another class `B`
	solved by making `A` a derived class of `B`
- __pull up field/method__: used when you have classes with identical fields/methods
	solved by making moving the common features to the superclass
- __push down field/method__: used when fields/method of a superclass is relevant only for some of its subclasses
	solved by making them part of the subclasses
- __replace inheritance with delegation__: more like "replace inheritance with composition"
- __replace delegation with inheritance__: ___uno reverse___
- __replace conditional with polymorphism__: title
- __introduce null object__: used when you check null value too many times
	solved by making a subclass representing the null object, that handles things differently.