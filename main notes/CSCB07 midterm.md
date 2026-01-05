# general info
- time: November 7th 19:00-21:00
- location: IC130

# content
- Java default values
- primitive/reference type and stack/heap

- static modifier
- inheritance (`super()` method)
- package private
- declare type and runtime type
- dynamic binding

- Object class (`equals()`, `hashCode()`, `toString()`)
- abstract class and interface
- generics (`Comparable` interface, `ArrayList` and `HashSet` class)

- exception (checked and unchecked)

- unit test (and testing criterion, JUnit)
- fault, error, failure
- RPIR model (reachability, infection, propagation, revealability)

- software dev process (waterfall and agile)
- scrum (scrum mechanism, roles, user stories, planning session (start of sprint), working agreement, definition of done)

- Android stuffs...

# todo
- RQ1
- remember weird stuffs (especially with regards to cha software dev and Android)
- study the example of Android program

# mock exam notes
- abstract can have a concrete constructor

# stuffs to remember
- syntax error: a missing parenthesis
  runtime error: ___too obvious___
  compilation error: type mismatch
  Note that invalid access (accessing private members) will be considered as a __syntax error__
- Fields not initiated will be by default in a form of `0`, while for __character__ it is `\u0000`, for __boolean__ is `false`, for __reference__ is `null`
- Reference itself is stored in __stack__, while the address is in __heap__

- `super()` must be invoked as the __first statement__ for overriden method
- Fields are by default __package private__
- Declare type: checked during __compilation__, runtime type: checked during __run__
  Consider `Employee extends Person;`, then `Person p = Employee(args)` will create a `Person` reference (or pointer, from C), that points to a new `Employee` in the heap.
  To access fields from `Employee` and not from `Person`, you must typecase like this `Employee e = p`, then access it from `e` (pointer `p` doesn't know what the new fields are)
  
  In this example, `p`'s declare type is `Person`, `p`'s runtime type is `Employee`
  if we attempt to call methods from `Employee` using `p`, there will be a syntax error
- Non static/private methods in Java are by default __virtual__, which means when calling a method from a subclass will go find the first method in the inheritance hierarchy from the lowest (the one that inherits all other classes) to the highest.
- In Java each class can only inherit from one class, not more, unlike C++

- `equals()` is reflexive, transitive, consistent, `equals(null)` returns false
  `hashCode()` should be unique, `x.equals(y)` returns true implies `x.hashCode() == y.hashCode()`
  `toString()` is automatically passed to `println` and string concatenation, dedicated to be a better description to print for the object
- You cannot use `new` to create a new instance from an abstract class.
  All inherited classes of an abstract must implement the abstract methods of the abstract class
- All methods from an interface must be abstract, an interface __can have no method__
- (review interface diagram [[interface diagram (UML diagram)]])

- `RuntimeException` and its subclasses are unchecked exceptions, all other exceptions are checked exceptions, where checked exceptions are checked during __compile time__, and force you to handle it, while compiler doesn't care for unchecked once.
- fault: anything wrong (eg assigning the wrong value)
  error: a state of the program is not correct
  failure: external incorrect behaviour with respect to the expectation
  bug->one of the three above occurs
- failure can be observed -> everything in RIPR occurs
  reachability: statement with fault reached
  infection: fault caused error (wrong state)
  propagation: infected state eventually cause some output or final state of program to be incorrect
  revealability: tester can observe incorrect part
  note that propagation->infection->reachability, but reachability does not imply infection

- waterfall: requirement->analysis->design->coding->testing->operations _to remember_
