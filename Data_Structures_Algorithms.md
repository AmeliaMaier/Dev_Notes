### Purpose: 

This document is intended to allow me to organize my notes while studing Data Structures and Algorithms in Python. This is not intended as a complete thesis on the topic, only a referance guide for myself as I attempt to organize concepts.


### Books used: 
1. Problem solving with algorithms and data structures using python - Second Edition - by Bradley N. Miller and David L. Ranum


### Intended Audiance:

Myself. Other python developers who are interested in data structures and algorithms or are looking for quick referances are welcome to use my notes. 

### Definitions:

Abstract Data Type: An abstraction, usually build on primitive data types, that allows the user to preform operations on the data without knowing exactly how they work. Treating data as conceptual rather than 1s and 0s.
> An abstract data type ... is a logical description of how we view the data and the operations that are allowed without regard to how they will be implemented. This means that we are concerned only with what the data is representing and not with how it will eventually be constructed.

Abstraction: The concept of dealing with using functional pieces or solutions without needing to understand more of how they work than is required for your current role.
> Abstraction allows us to view the problem and solution in such a way as to separate the so-called logical and physical perspectives...Consider the automobile that you may have driven to school or work today. As a driver, a user of the car, you have certain interactions that take place in order to utilize the car for its intended purpose...From an abstraction point of view, we can say that you are seeing the logical perspective of the automobile. You are using the functions provided by the car designers for the purpose of transporting you from one location to another.<sup>1</sup>

Algorithm: The steps needed to resolve a single clearly defined problem.
> Given a problem, a computer scientist's goal is to develope an algorithm, a step-by-step list of instructions for solving any instance of the problem that might arise. Algorithms are finite processes that if followed will solve the problem. Algorithms are solutions.<sup>1</sup>

Computable: Solvable
> We say that a problem is computable if an algorithm exists for solving it.<sup>1</sup>

Data Types: An abstraction on top of the binary data so that programers can think about the data in terms that make sense for the current problem being solved.
>All data items in the computer are represented as strings of binary digits. In order to give these strings meaning, we need to have data types. Data types provide an interpretation for this binary data so that we can think about the data in terms that make sense with respect to the problem being solved. These low-level built-in data types (sometimes called the primitive data types) provide the building blocks for algorithm development.<sup>1</sup>

Programming: The process of encoding one or more algorithms in such a way as to be executed by a computer.
> Programming is the process of taking an algorithm and encoding it into a notation, a programming language, so that it can be executed by a computer. Although many programming languages exist, the important first step is the need to have the solution. Without an algorithm there can be no program.<sup>1</sup>


### Primative/Atomic Data Types

All primative data types in Python are objects with basic funtions available like str(), isinstance(), ect.

#### Numeric

All primitive data types in python are compatible with all basic mathmatic funtions (+, -, *, **, %, //, /). The data type returned from the function depends on the type provided and the function preformed. 

Integer: int. A whole number (doesn't have a decimal point in it).

Floating Point: float. A floating point representation of a real number (has decimal point in it somewhere).

### Boolean
True or False only. Used with logical operators (and, or, not), returned from logical statements (<, >, ==, <=, >=).

### Collections

All collections are contain 0 to n number of referances to data objects. The only limit in the size of n is the amount of memory available on the current computer.

#### Ordered 

List: [,,,] Can contain data types of different types in one list, can contain any data object(s). When created, Python assigns it a block of memory; before the data contained in the list exceeds the alloted memory location a larger memory location is alloted. Mutable. Contains referances to the data objects in it, not the actual value. This means that if an object is referanced twice and it is changed in one location in the list, the other location(s) are also updated.
```Python
>>>myList = [1,2,3,4]
>>>three_of_myList = myList*3
>>>three_of_myList
[[1,2,3,4],[1,2,3,4],[1,2,3,4]]
>>>myList[2] = 'changed'
>>>three_of_myList
[[1,2,'changed',4],[1,2,'changed',4],[1,2,'changed',4]]
```

String: ' ', ''' ''', """ """, or " " Can only contain characters (letters, numbers, and symbols). Immutable. 

Tuples: (,,,,) Basically immutable lists.

#### Unordered

Set: {,,,,} Only allows immutable data types, can contain more than one data type at a time, does not allow duplicate values within a data type. Suppored in memory by a hash table, allowing for very fast membership verification but slower addition.

Dictionary: {k:v, k:v, k:v} A collection of Key Value pairs. Keys must be immutable and unique. Values can be mutible or immutable and non-uniuqe. The keys are supported in memory by a hash table allowing for fast value lookup and membership verification but slower addition of new pairs.


### Control Structures

#### Loops

Loops allow you to repetedly run the same piece of code until a specific condition is met. You can jump out of any loop with a break, you can skip remaining code in the current iteration of the loop with continue.

For: Iterate over a compatible data object (list, string, generator) from begining to end, placing the current returned value in the variable assigned.
```Python
>>>for x in range(1,5):
>>>  print(x)
1
2
3
4
```
A specialty version of the for loop is a list comprehension. It uses simplified syntacts and returns a list of the values from the loop. It allows for simple logical statements in it. Can be nested, but that should be avoided if possible.
```Python
>>>L = [x for x in range(1,5) if x%2 == 0]
>>>L
[2,4]
```

While: Runs only if the logical condition is True, continues to run until it is no longer True.
```Python
>>>count = 0
>>>while count < 5:
>>>  count += 1
>>>  print(count)
1
2
3
4
```

#### Selection Statements

If Else: Logical statement trees that execute the code in the first statement that is evaluated to True.
```Python
>>>x=5
>>>y=4
>>>if x == y:
>>> print('Yes')
>>>elif x < y:
>>> print('Maybe')
>>>else:
>>> print('No')
No
```





