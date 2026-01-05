## CSCB07 other stuffs
[[CSCB07 course information]]
[[CSCB07 midterm]]
[[CSCB07 final exam]]
[[CSCB07 project]]

# Java basics
## CSCB07 LEC1
[[Java]]
[[Java IDEs]]
[[Java datatypes]]
[[Java sample codes]]
[[instance and class]]
[[Java default values]]

## CSCB07 LEC2
[[Java primative and reference type]]
[[Java stack and heap]]
[[Java static modifier]]
[[Java array]]
[[Java input and output]]
[[Java file class]] (most likely not on exams)

# OOP
## CSCB07 LEC3 (important, review every subtopic)
[[OOP (object oriented programming)]]
[[Java inheritence]] (__watch out super() case__)
[[package private]] (__important__)
[[Java declare type and runtime type]] (__important as well for cause it handles lots of edge case__)

(Note in Java you can only inherit from one class, unlike in C++)

## CSCB07 LEC4
[[Java object class]]
[[polymorphism]]
[[Java dynamic binding]]

# testing
## CSCB07 LEC5
[[encapsulation]]
[[abstract class]]
[[interface]]
[[interface diagram (UML diagram)]]
[[generics]]
[[Java ArrayList class]]
[[Hashset]]
[[exception]]
[[software testing]]
[[unit testing]]
[[JUnit]]

# software development lifecycle
# Android
## CSCB07 LEC6
[[testing criterion]]
[[fault, error and failure in code]]
[[RIPR model]] [[software development process]] [[scrum (agile software development technique)]] [[Android]] [[Android app basics]]

## CSCB07 LEC7
[[Android view]]
[[Android project folder structure]]
[[Android project data storage options]]
[[JSON]]
[[testing an Android application]]
[[Android commonly used tools]]
[[Mockito]]
[[model view presenter]]

[[non functional requirements]]
[[SOLID]]
[[single responsibility principle (SRP)]]: Every class should only have one responsibility, if it has more, make it a component

## CSCB07 LEC8
[[open and closed principle (OCP)]]: Every class should be extendable but not modifiable, the modifiable part should be a component
[[Liskov substitution principle (LSP)]]: Consider base class `b` and inherited class `a`, then everything satisfied by `b` must also be satisfied by `a` (usually broken from overriding methods in `a`)
[[interface segragation principle (ISP)]]: A class should only implement an interface with methods the class needs, so getting sub interfaces can help
[[dependency inversion principle (DIP)]]: High level code should rely on interfaces, while low level code should implement interfaces


## CSCB07 LEC9
[[creational design pattern]]
- singleton: one instance only
- factory: one class for creating objects
[[structural design pattern]]
- facade: hide complex stuffs behind
- adapter: solves the problem with incompatible interfaces
[[behavioral design pattern]]
- observer: notify everytime making changes
- strategy: 

## CSCB07 LEC10
[[principles of clean code]]
[[modularity]]
[[readablity]]
[[test code]]
[[refactor code]]
