##Python Essential Terminologies
**1. How Python uses Indentation to control Flow:-**
Control flow in your code is to affect the order in which the code in your program is executed. Up until this point in the course, you have seen (and hopefully written) code that executes linearly.


simple code without any "control flow"
i.e. no branches in logic, loops, or # code encapsulation
```
x = 6 
y = 23
print("x + y = ", x + y)
print("x - y = ", x - y)
```

**2. Don’t repeat yourself:-**
The Don’t Repeat Yourself (DRY) principle states that duplication in logic should be eliminated via abstraction; duplication in process should be eliminated via automation.
Duplication is Waste
Adding additional, unnecessary code to a codebase increases the amount of work required to extend and maintain the software in the future.  Duplicate code adds to technical debt. 


**3. Design Patterns from Gang of Four:-**
The Gang of Four are the four authors of the book, "Design Patterns: Elements of Reusable Object-Oriented Software". In this there are twenty-three design patterns are described with links to UML diagrams, source code and real-world examples for each.  This important book describes various development techniques and pitfalls in addition to providing twenty-three object-oriented programming design patterns. The four authors were Erich Gamma, Richard Helm, Ralph Johnson and John Vlissides.
Design patterns provide solutions to common software design problems. In the case of object oriented programming, design patterns are generally aimed at solving the problems of object generation and interaction, rather than the larger scale problems of overall software architecture. 

```
a)Types of creational design patterns:-
-Abstract factory
-Builder
-Factory model
-Prototype
-Singleton

b)Types of structural design patterns:-
-Adapter
-Bridge
-Composite
-Decorator
-Facade
-Flyweight
-Proxy

c)Types of behavioural design patterns:-
-Chain of responsibilty
-Command
-Interpreter
-Iterator
-Mediator
-Memento
-Observer
-State
-Strategy
-Template Method
-Visitor
```

**4. Class:-**
Classes provide a means of bundling data and functionality together. Creating a new class creates a new type of object, allowing new instances of that type to be made. Each class instance can have attributes attached to it for maintaining its state. Class instances can also have methods (defined by its class) for modifying its state.
```
class ClassName:
    <statement-1>
    .
    .
    .
    <statement-N>
```

**5. Object:-**
Object is simply a collection of data (variables) and methods (functions) that act on those data. And, class is a blueprint for the object. The class object could be used to access different attributes.
It can also be used to create new object instances (instantiation) of that class. The procedure to create an object is similar to Function  call.

```
x = MyClass()
```

* https://docs.python.org/3/tutorial/classes.html
* http://www.blackwasp.co.uk/gofpatterns.aspx
* https://www.pythonlikeyoumeanit.com/Module2_EssentialsOfPython/Introduction.html






