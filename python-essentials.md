# Getting Started with Python
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







**11. Constructor**

A constructor is a special kind of method that Python calls when it instantiates an object using the definitions found in the class.

There two types of constructors in Python.
1. Default constructor – This constructor doesn’t accept any arguments.
2. Parameterized constructor – constructor with parameters is known as parameterized constructor.

```
class HelloWorld:
    # constructor
    def __init__(self):
        # initializing instance variable
        self.num=100

    # a method
    def read_number(self):
        print(self.num)


# creating object of the class. This invokes constructor
obj = HelloWorld()

# calling the instance method using the object obj
obj.read_number()
```

**12. Factory**

The factory pattern comes under the creational patterns list category. It provides one of the best ways to create an object. In factory pattern, objects are created without exposing the logic to client and referring to the newly created object using a common interface.

Factory patterns are implemented in Python using factory method. When a user calls a method such that we pass in a string and the return value as a new object is implemented through factory method. The type of object used in factory method is determined by string which is passed through method.

In the example below, every method includes object as a parameter, which is implemented through factory method.

```
class Button(object):
   html = ""
   def get_html(self):
      return self.html

class Image(Button):
   html = "<img></img>"

class Input(Button):
   html = "<input></input>"

class Flash(Button):
   html = "<obj></obj>"

class ButtonFactory():
   def create_button(self, typ):
      targetclass = typ.capitalize()
      return globals()[targetclass]()

button_obj = ButtonFactory()
button = ['image', 'input', 'flash']
for b in button:
   print button_obj.create_button(b).get_html()
```


**13. Decorator**


Decorator pattern allows a user to add new functionality to an existing object without altering its structure. This type of design pattern comes under structural pattern as this pattern acts as a wrapper to existing class.

This pattern creates a decorator class, which wraps the original class and provides additional functionality keeping the class methods signature intact.

The motive of a decorator pattern is to attach additional responsibilities of an object dynamically.

There are two different ways one can use decorators on classes for example one can decorate the methods of a class. 


```

class TimeWaster:
    @debug
    def __init__(self, max_num):
        self.max_num = max_num

    @timer
    def waste_time(self, num_times):
        for _ in range(num_times):
            sum([i**2 for i in range(self.max_num)])



```





## Source
* https://docs.python.org/3/tutorial/classes.html
* http://www.blackwasp.co.uk/gofpatterns.aspx
* https://www.pythonlikeyoumeanit.com/Module2_EssentialsOfPython/Introduction.html
* https://beginnersbook.com/2018/03/python-constructors-default-and-parameterized/






