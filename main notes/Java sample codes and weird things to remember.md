---
title: Java sample codes
created: Monday 8th September 2025 20:24
last_modified: Monday 8th September 2025 20:24
aliases: []
tags:
  - computer-science/software-development/java
course:
  - CSCB07
LEC:
  - "1"
---
# Main notes
```
class Point{
  private double x;
  private double y;

  public Point(){
    x = 1;
    y = 2;
  }

  public Point(double a, double b){
    x = a;
    y = b;
  }
}

class Driver{
  // `java file_name abc def ghi` will pass a array of strings args, where args[0] = "abc", args[1] = "def", args[2] = "ghi"
  public static void main(String [] args){
    Point p1; //This doesn't create the object
    p1 = new Point(10, 20); //This calls the constructor
  }
}
```

The line `p1 = new Point(10, 20);` creates a new point in the __heap__ with some address, let's it's $5000$ for now
Then, the device assigns the value of p1 as $5000$ in the __stack__ (in other words, p1 points to the object in the heap)

# Weird stuffs to remember
- invalid access (accessing private members) will be considered as a __syntax error__
- fields not initiated will be by default 0
