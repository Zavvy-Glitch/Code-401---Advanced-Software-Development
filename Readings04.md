# Data Modeling

1. Name 3 advantages to Test Driven Development
    - Code refactoring goes more smoothly
One of the greatest advantages of test-driven development is making the code much more manageable. Furthermore, TDD helps to significantly cut the total hours spent on testing and maintenance activities
    - The code is easier to maintain
Arranged code is much easier to deal with when it comes to modifications. When the TDD approach is applied, developers naturally produce a cleaner, more readable, and manageable code.
    - The software design becomes modular
When using the TDD approach, developers narrow their focus to a single feature at a time, not moving to the next one until the associated unit test is passed. Written in such iterations, the code quality is naturally enhanced, making it easier to discover bugs and reuse the code, as well 
\
 [Source: Forte Group](https://fortegrp.com/test-driven-development-benefits/)

2. In what case would you need to use `beforeEach()` or `afterEach()` in a test suite?
    - If you have some work you need to do repeatedly for many tests
    - The difference is beforeEach()/afterEach() automatically run before and after each tests, which 1. removes the explicit calls from the tests themselves, and 2. invites inexperienced users to share state between tests.
Tests should be explicit, and tests should never share state.
\
[Source: Eric Elliot](https://medium.com/@_ericelliott/the-difference-is-beforeeach-aftereach-automatically-run-before-and-after-each-tests-which-1-b53a3ba5c344)

3. What is one downside of Test Driven Development
    - The test suite itself has to be maintained; tests may not be completely deterministic
    - Initially, it slows down development; for rapidly iterative startup environments the implementation code may not be ready for some time due to spending time writing tests first.
    - You have to perform housekeeping continually. Because booking more and more tests make your build longer and longer, it’s necessary to refine those tests to make them run more quickly or to remove redundant tests.

4. What’s the primary difference between ES6 Classes and Constructor/Prototype Classes?
    - ES6 Classes can be said to be a syntax base for constructor functions and instantiate objects using a new operator.
    - While Constructer/ProtoType Classes also uses a new operator for object creation, but focuses on how the objects are being instantiated.

5. Why REST?
    - Easy Integration: The usage of ubiquitous standards is a characteristic for ease of integration that has to do with REST over HTTP (THE most popular implementation of REST).
    - Scalability: Stateless communication and a replicated repository provide a high level of scalability. With the REST APIs, scaling up an existing website is easier when it is compared with something like SOAP.
    - Uniform Interface: When creating a REST API, developers agree to follow the same standards. Hence, the output is a consistent interface across all APIs.
\

## Terminology Definitions

   - Functional Programming: a programming paradigm where programs are constructed by applying and composing functions. It is a declarative programming paradigm in which function definitions are trees of expressions that map values to other values, rather than a sequence of imperative statements which update the running state of the program
   - (OOP) Object-Oriented Programming: a computer programming model that organizes software design around data, or objects, rather than functions and logic. An object can be defined as a data field that has unique attributes and behavior
   - Class: are a template for creating objects. They encapsulate data with code to work on that data. Classes in JS are built on prototypes but also have some syntax and semantics that are not shared with ES5 class-like semantics.
   - `super`: used to access and call functions on an object's parent
   - `this`: refers to the object it belongs to
   - (TDD) Test Driven Development: refers to a style of programming in which three activities are tightly interwoven: coding, testing (in the form of writing unit tests) and design (in the form of refactoring)
   - Jest: a JavaScript test runner, that is, a JavaScript library for creating, running, and structuring tests
   - Continuous Integration: a practice which prescribes to continuously integrate new code and new features into a shared codebase
   - REST: an architectural style that handles the client-server relationship, with the purpose of aiming for speed and performance by using re-usable components
   - Data Model: abstract model that organizes elements of data and standardizes how they relate to one another and to the properties of real-world entities
    
    
 ### PREP / Preview
 1. Which 3 things had you heard about previously and now have better clarity on?
    - JEST
    - Relational vs Non-Relational DB's
    - TDD
 
 2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
    - ES6 Classes
    - Linked Lists
    - THE BIG O
 
 3. What are you most excited about trying to implement or see how it works?
    - More on POSTGRES also more with TDD/JEST especially.
