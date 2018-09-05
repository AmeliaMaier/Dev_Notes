
# Object Oriented Programming (OOP)

## Why

Understanding OOP is important. It helps with code organization, reusability, testability, and legibility. It also shows up on a lot of job interviews. 

## Basic Terminology:
### Method vs Function: 
>A function is a piece of code that is called by name. It can be passed data to operate on (i.e. the parameters) and can optionally return data (the return value). All data that is passed to a function is explicitly passed.
>A method is a piece of code that is called by a name that is associated with an object. In most respects it is identical to a function except for two key differences:
>>A method is implicitly passed the object on which it was called.

>>A method is able to operate on data that is contained within the class (remembering that an object is an instance of a class - the class is the definition, the object is an instance of that data).
[more](https://stackoverflow.com/questions/155609/whats-the-difference-between-a-method-and-a-function)

### Class
[Classes provide a means of bundling data and functionality together. Creating a new class creates a new type of object, allowing new instances of that type to be made. Each class instance can have attributes attached to it for maintaining its state. Class instances can also have methods (defined by its class) for modifying its state.](https://docs.python.org/3/tutorial/classes.html)

This means that classes allow us to combine variables (which track values) with methods (which allow us to do things).

### Object
[The standard meaning is that an object is an instance of a class.](https://stackoverflow.com/questions/7483947/what-is-the-difference-between-objects-and-classes-in-python)

In Python, all variables are objects. 

### Unit Test
While not precisly an OOP term, unit testing is not possible without proper object oriented design practices. Unit testing is when you design a test (usually automated) to go over one small piece of functonality in your code. The larger your code blocks, the harder it is to test just one thing at a time (and the harder it is to troubleshoot errors).


## General Overview

[The four principles of object-oriented programming are encapsulation, abstraction, inheritance, and polymorphism.](https://medium.freecodecamp.org/object-oriented-programming-concepts-21bb035f7260)
Not all the principles of object-oriented programming are truely possible in Python, but it is important to have at least a basic understanding of them so you know what you do and don't have access to.

### Inheritance
[It means that you create a (child) class by deriving from another (parent) class. This way, we form a hierarchy. The child class reuses all fields and methods of the parent class (common part) and can implement its own (unique part).](https://medium.freecodecamp.org/object-oriented-programming-concepts-21bb035f7260)

#### Python Inheritance
Python is all about inheritance. You can create a class that inherits from multiple classes, you can have classes inherit as deeply as you want (grandchildren, greatgrandchildren, ect). In older versions of Python, all classes had to inherit from the Object class. In Python3, this is assumed and does not need to be called out.

### Polymorphism
[Simply put, polymorphism gives a way to use a class exactly like its parent so there’s no confusion with mixing types. But each child class keeps its own methods as they are. This typically happens by defining a (parent) interface to be reused. It outlines a bunch of common methods. Then, each child class implements its own version of these methods. Any time a collection (such as a list) or a method expects an instance of the parent (where common methods are outlined), the language takes care of evaluating the right implementation of the common method — regardless of which child is passed.](https://medium.freecodecamp.org/object-oriented-programming-concepts-21bb035f7260)


#### Python Polymorphism


### Encapsulation
[Encapsulation is achieved when each object keeps its state private, inside a class. Other objects don’t have direct access to this state. Instead, they can only call a list of public functions — called methods.](https://medium.freecodecamp.org/object-oriented-programming-concepts-21bb035f7260)

#### Python Encapsulation
Python does not actually support encapsulation in the way languages like C# and Java do. Those languages enforce privacy: a private method or variable can not be accessed outside the class that owns it. In Python, private vs public is controled entirly by convention. To mark a function, method or variable as private you use 'dunder' or 'double under score' before the name. [more](https://pythonspot.com/encapsulation/)
```
def thisIsAPublicMethod:
  print("I can be accessed from anywhere and everyone knows they can use me")
 
def __thisIsAPrivateMethod:
  print("I can be accessed from anywhere but everyone agrees I shouldn't be")
```

### Abstraction
[Applying abstraction means that each object should only expose a high-level mechanism for using it. This mechanism should hide internal implementation details. It should only reveal operations relevant for the other objects.](https://medium.freecodecamp.org/object-oriented-programming-concepts-21bb035f7260)

Abstraction and Encapsulation can be easily confused. In general: Abstraction is implemented using interface and abstract classes while Encapsulation is implemented using private and protected access modifier. [more](https://www.quora.com/What-is-the-difference-between-abstraction-and-encapsulation-in-Python)

#### Python Abstraction
[Abstract classes are classes that contain one or more abstract methods. An abstract method is a method that is declared, but contains no implementation. Abstract classes may not be instantiated, and require subclasses to provide implementations for the abstract methods. Subclasses of an abstract class in Python are not required to implement abstract methods of the parent class.](https://www.python-course.eu/python3_abstract_classes.php)


## Sources and further reading:

https://medium.freecodecamp.org/object-oriented-programming-concepts-21bb035f7260

https://stackoverflow.com/questions/155609/whats-the-difference-between-a-method-and-a-function

https://pythonspot.com/encapsulation/

https://docs.python.org/3/tutorial/classes.html

https://stackoverflow.com/questions/7483947/what-is-the-difference-between-objects-and-classes-in-python

https://www.quora.com/What-is-the-difference-between-abstraction-and-encapsulation-in-Python


