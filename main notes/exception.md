---
title: exception
created: Monday 6th October 2025 20:26
last_modified: Monday 6th October 2025 20:25
aliases: []
tags:
  - computer-science/software-development
course:
  - CSCB07
LEC:
  - "5"
---
# exception
Exception handling enables a program to deal with exceptional situations and continue its normal execution

(Codes to be completed)
```java
public class B07Exception extends Exception {
	String message;
	
	public B07Exception(String message) {
		this.message = message;
	}
}


public class Fraction {
	private int numerator;
	private int denominator;
	
	public Fraction(int numerator, int denominator) {
		if (denominator == 0) {
			throw new B07Exception("The denominator cannot be zero");	
		}
		this.numerator = numerator;
		this.denominator = denominator;
	}
	
}

public class Driver {
	public void main(String args[]){
		//...

		try {
			Fraction fraction = new Fraction(num, den);
			fraction.reduce();
			System.out.println("The reduced fraction is: " + fraction);
		}
		//...
	}
}
```

Exception can be __checked__ or __unchecked__, if the exception is recoverable, then use checked exception, otherwise use unchecked one.
Where checked exception is done through overriding the `Exception` class and unchecked exception is done through overriding the `RuntimeException`