
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
### Object
### Unit Test

## General Overview

[The four principles of object-oriented programming are encapsulation, abstraction, inheritance, and polymorphism.](https://medium.freecodecamp.org/object-oriented-programming-concepts-21bb035f7260)
Not all the principles of object-oriented programming are truely possible in Python, but it is important to have at least a basic understanding of them so you know what you do and don't have access to.

### Encapsulation
[Encapsulation is achieved when each object keeps its state private, inside a class. Other objects don’t have direct access to this state. Instead, they can only call a list of public functions — called methods.](https://medium.freecodecamp.org/object-oriented-programming-concepts-21bb035f7260)

#### Python Encapsulation
Python does not actually support encapsulation in the way languages like C# and Java do. Those languages enforce privacy: a private method or variable can not be accessed outside the class that owns it. In Python, private vs public is controled entirly by convention. To mark a function, method or variable as private you use 'dunder' or 'double under score' before the name.
```
def thisIsAPublicMethod:
  print("I can be accessed from anywhere and everyone knows they can use me")
 
def __thisIsAPrivateMethod:
  print("I can be accessed from anywhere but everyone agrees I shouldn't be")
```

## Sources and further reading:

https://medium.freecodecamp.org/object-oriented-programming-concepts-21bb035f7260

https://stackoverflow.com/questions/155609/whats-the-difference-between-a-method-and-a-function


