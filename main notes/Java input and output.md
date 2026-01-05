---
title: Java input
created: Monday 15th September 2025 20:30
last_modified: Monday 15th September 2025 20:30
aliases: []
tags:
  - computer-science/software-development/java
course:
  - CSCB07
LEC:
  - "2"
---
# input
Java input sources include
- keyboard
- file
- network

# output
Java output destinations include
- console
- file
- network

# standard I/O
Use `System.in` for input
- System.in is an object of type __InputStream__
- typically refers to the keyboard
- reading data could be done using the __Scanner__ class, with methods:
	`String next()`
	`String nextLine()`
	`int nextInt()
	`double nextDouble()`

Use `System.out` for output
- object of type __PrintStream__
- typically refers to the console

## standard I/O sample code
```
import java.util.Scanner;

public class Driver {

	public static void main(String [] args) {
		Scanner scan = new Scanner(System.in);
		System.out.println("Enter a number:" );
		int n = scan.nextInt();
		System.out.println("You entered " + n);
	}
}
```
Note this gives the same result
```
import java.util.Scanner;

public class Driver {

	public static void main(String [] args) {
		Scanner scan = new Scanner(System.in);
		System.out.println("Enter a number:" );
		System.out.println("You entered " + scan.nextInt()); // difference is here!
	}
}
```