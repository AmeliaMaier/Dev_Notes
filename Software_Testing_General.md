
### Purpose: 

This document is intended to offer a general overview of software testing from the point of view of a developer who is fully responsible for testing their own code. It is not language or industry specific. 

### Note:
As you go through, you will notice that many topics overlap, this is part of what leads to confusion when people are just starting out. A test case might be automated and count as a unit test and an integration test while it was designed in a domain based way. This is fine and normal. 

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

Domain based testing says that everything in each group is equivelant but that edge cases are as likely or more to cause errors. For this reason, you would test with -1, 0, and 1 if it only allowed ints or something like -.000000001, 0, .000000001 if it allows decimals.

#### User Stories Based

A lot of professionally developed software has user stories. These are simple sets of 'if I do this, I expect it to do that'. Using theses stories to plan your unit test not only makes sure you have met all the stated requirements, it also makes it easier to notice where a requirement wasn't clear or specified. 

If you have a user storie that says: "When I provide the correct login information, I expect to be taken to my personalized landing page"

You know know you need a test for the login page that provides the correct login information for a user with a personalized landinng page. You should also notice that, if no other user stories cover other login scenarios, that no requirement has been provided for exactly what should happen if an incorrect login is provided. In this case, you know the login shouldn't be allowed but may need to check back with the users for exactly what behavior they expect.

#### Code Coverage

A lot of unit tests are written to insure complete code coverage. What this means is that every line of code is tested with one or more unit tests. If you have logical splits in your code, both sides of the split should have unit tests.

If you have something similar to this sudo code:

```
if input > 10
  return True
else 
  return False
```

you should have a unit test where input is over 10 and a unit test where input is equal to or less than 10 in order to get full code coverage for that section.


#### Path Coverage

Path coverage is similar to code coverage, but often means writing a lot more unit tests. A path is any list of steps a user can take. Usually, you start all paths are opening the program (or logging in) and end all of them when the program is closed (or you log out). If there are any areas where looping is possible, full path coverage will be impossible. In most enterprise level programs, full path coverage is impracticle even if it is possible. 

If you are looking at a very simple program that only does the following sudo code:

```
iif input > 10
  return True
else 
  return False
```
Your paths would be the same as your code coverage: you should have a unit test where input is over 10 and a unit test where input is equal to or less than 10 in order to get full path coverage.

If you have a more complicated program that includes the menu below:

```
1. Sudokua
2. Connect 4
3. Hangman
4. Exit
```
This implies that you can go from game to game in any order until you choose to exit. That means you will want to pick the paths users are most likely to follow and the ones you think are most likely to cause problems, but you will be unable to reach full path coverage.

#### Feature Coverage

Feature coverage is very similar to designing unit tests around user stories. You create a full list of all the features the user asked for and make sure you have tested all of them.

#### Integration

Integration testing is any time you ensure two or more pieces of code work together. This can be as small as making sure all the code needed to log in and out work end to end or as large as ensureing your entire program can be run with different selections for a given length of time without crashing or causing an error (monkey testing). Integration testing and unit testing are often mentioned as two seperate things. Depending on how you define unit testing, this may be true. 

Some people define unit testing as any testing done by a developer (usually the definition used if a testing team is available and participating in the project). If that is the definition you are using and no testing team is working with you, you have to remember to include integration tests in your unit testing.

Some people define unit testing as the tests that ensure each tiny piece of code (in methods or functions) works the way you expect them to. If this is the definition you are using, you will want to seperately run integration tests.
