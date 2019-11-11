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
**6. Static:-**
All variables defined on the class level in Python are 
considered static.See this example:

```
class Example:
    staticVariable = 5 # Access through class

print Example.staticVariable # prints 5

# Access through an instance
instance = Example()
print instance.staticVariable # still 5

# Change within an instance
instance.staticVariable = 6
print instance.staticVariable # 6
print Example.staticVariable # 5

# Change through
class Example.staticVariable = 7
print instance.staticVariable # still 6
print Example.staticVariable # now 7

```
Static Method

Method decorated with this decorator shares with the class only the 
namespace. Note that, no arguments are mandatory in the method definition. 
Static method can access classes static variables.

```
class Example:
    name = "Example"

    @staticmethod
    def static():
        print "%s static() called" % Example.name

class Offspring1(Example):
    name = "Offspring1"

class Offspring2(Example):
    name = "Offspring2"

    @staticmethod
    def static():
        print "%s static() called" % Offspring2.name

Example.static() # prints Example
Offspring1.static() # prints Example
Offspring2.static() # prints Offspring2

```
**7. Property:-**

Python has a great concept called property which makes the life
of an object oriented programmer much simpler.
Everything in Python is an object, and almost everything has attributes and methods. In python, functions too are objects.
So they have attributes like other objects. 
All functions have a built-in attribute __doc__, which returns the doc string defined in the function source code. 
We can also assign new attributes to them, as well as retrieve the values of those attributes.

For handling attributes, Python provides us with “getattr” and “setattr”, a function that takes three arguments. 
There is no difference between “setattr” and using the dot-notation on the left side of the = assignment operator:

The given code can be written as follows to assign and retrieve attributes.

```
def foo():
    pass
setattr(foo, 'age', 23 )
setattr(foo, 'name', 'John Doe' )
print(getattr(foo, 'age'))
foo.gender ='male'
print(foo.gender)
print(foo.name)
print(foo.age)

output

C:/Users/TutorialsPoint1/~.py
23
male
John Doe
23

```
**8. Method:-**
Python method is a label that you can call on an object;
it is a piece of code to execute on that object. But before
we begin getting any deeper,
let’s take a quick look at classes and objects and wherever
we encounter any doubt in the Python Method
A Python Class is an Abstract Data Type (ADT). Think of it like a blueprint. A rocket made from referring to its blueprint is according to plan. It has all the properties mentioned in the plan, and behaves accordingly. Likewise, a class is a blueprint for an object. To take an example, we would suggest thinking of a car. The class ‘Car’ contains properties like brand, model, color, fuel, and so. It also holds behavior like start(), halt(), drift(), speedup(), and turn(). An object Hyundai Verna has the following properties then.

brand: ‘Hyundai’

model: ‘Verna’

color: ‘Black’

fuel: ‘Diesel’

```
class Car:
          def __init__(self,brand,model,color,fuel):
                  self.brand=brand
                  self.model=model
                  self.color=color
                  self.fuel=fuel
           def start(self):
                  pass
           def halt(self):
                  pass
           def drift(self):
                  pass
           def speedup(self):
                  pass
           def turn(self):
                  pass
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

**14. Extend Class**

Extend class is a class that has extended function from another class.

Inheritance is a concept in object-oriented programming in which a class derives (or inherits) attributes and behaviors
from another class without needing to implement them again.

```
    
    def __init__(self, name):
        self.name = name
        
    def say_hello(self):
        print("Hi, I am " + self.name)
        
class PersonalRobot(Robot):
    pass
x = Robot("Jake")
y = PersonalRobot("Keith")
print(x, type(x))
print(y, type(y))
y.say_hello()

```

**15. CSV Files**

A CSV file (Comma Separated Values file) is a type of plain text file that uses specific structuring to arrange tabular data.
Because it’s a plain text file, it can contain only actual text data—in other words, printable ASCII or Unicode characters.

The structure of a CSV file is given away by its name. Normally, CSV files use a comma to separate each specific data value. 
Here’s what that structure looks like:

```
column 1 name,column 2 name, column 3 name
first row data 1,first row data 2,first row data 3
second row data 1,second row data 2,second row data 3
...
```

In general, the separator character is called a delimiter, and the comma is not the only one used. Other popular delimiters 
include the tab (\t), colon (:) and semi-colon (;) characters. Properly parsing a CSV file requires us to know which delimiter is being used.


**16. Reading CSV Files**

Reading from a CSV file is done using the reader object. The CSV file is opened as a text file with Python’s built-in open() function,
which returns a file object. This is then passed to the reader, which does the heavy lifting.

```
Here’s the employee_birthday.txt file:
name,department,birthday month
John Smith,Accounting,November
Erica Meyers,IT,March
```

Here’s code to read it:

```
import csv

with open('employee_birthday.txt') as csv_file:
    csv_reader = csv.reader(csv_file, delimiter=',')
    line_count = 0
    for row in csv_reader:
        if line_count == 0:
            print(f'Column names are {", ".join(row)}')
            line_count += 1
        else:
            print(f'\t{row[0]} works in the {row[1]} department, and was born in {row[2]}.')
            line_count += 1
    print(f'Processed {line_count} lines.')
```

## Source
* https://docs.python.org/3/tutorial/classes.html
* http://www.blackwasp.co.uk/gofpatterns.aspx
* https://www.pythonlikeyoumeanit.com/Module2_EssentialsOfPython/Introduction.html
* https://beginnersbook.com/2018/03/python-constructors-default-and-parameterized/
* https://realpython.com/python-csv/#:~:targetText=Reading%20CSV%20Files%20With%20csv,which%20does%20the%20heavy%20lifting.





