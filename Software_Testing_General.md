
### Purpose: 

This document is intended to offer a general overview of software testing from the point of view of a developer who is fully responsible for testing their own code. It is not language or industry specific.

### Intended Audiance:

Developers who is fully responsible for testing their own code and need an basic introduction into the concepts around software testing.

### Automation vs Manual:

One of the biggest splits in software testing is the method of running the test. The two main options are to automate the test with unit tests added to your code base or to test the code manually but going through and making the correct selectsions yourself.

When to use automated tests: 
⋅⋅* When the end result is testable through code
⋅⋅* When you will need to run the test a lot of times
⋅⋅* When the test has a lot of steps or complicated logic
⋅⋅* When you need to document special use cases
⋅⋅* To make sure future code changes don't break the code you are currently working on
⋅⋅* When your office has a policy that all code be given unit tests

When to test manually:
⋅⋅* When the end result is not testable through code
⋅⋅* When you are writing something that will not be reused and is not important
⋅⋅* When no time was budgeted for writing automated tests and the project is already behind schedule

### How to come up with what to test:

The most common reasons I have seen for people not testing their code are: they don't have time, they don't know where to start, or they figure it is working well enough as is.

I can't fix the first issue, and we all know the third one is just a hope and a prayer; below are a few of the options for how to come up with test cases.

#### Domain Based

In this case, a domain is a range of inputs or actions that are all equivelant as far as the system under test is concerned. (not to be confused with domain-driven design) This means you take a small piece of your code (or unit) and make sure all the sections of inputs work. 

If you need to test code that says if an input is positive, negative, or 0; what are the domains?

There are 3: everything less than 0, 0, and everything greater than zero

Domain based testing says that everything in each group is equivelant but 

#### Use Stories Based

#### Code Coverage

#### Path Coverage

#### Feature Coverage

#### Integration
