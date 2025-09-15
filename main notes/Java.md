---
title: Java
created: Monday 8th September 2025 19:47
last_modified: Monday 8th September 2025 19:47
aliases: []
tags:
  - computer-science/software-development
  - computer-science/software-development/java
course:
  - CSCB07
LEC:
  - "1"
---
# what is Java?
- An OOP language invented by James Gosling in 1994 at Sun Microsystems
- Write ones, run anywhere (WORA)
- Used to develop software running on desktop computers, servers, mobile devices

# how does Java run
Java runs in 3 main steps
1. Writing the source code using a text editor
2. Translate the source code into Java bytecode using a compiler (Bytecode is similar to machine instructions but __runs on any platform that has Java Virtual Machine (JVM)__ and is __architecture neutral__)
3. execute the bytecode (The JVM  translates the bytecode into the target machine language code)

## command to run java
`javac Welcome.java`
If there is no syntax error, it will generate bytecode
`java Welcome`
This line will run the output of the previous command
![[Pasted image 20250908195646.png]]
