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
[Sourece: Eric Elliot](https://medium.com/@_ericelliott/the-difference-is-beforeeach-aftereach-automatically-run-before-and-after-each-tests-which-1-b53a3ba5c344)

3. What is one downside of Test Driven Development
    - The test suite itself has to be maintained; tests may not be completely deterministic
    - Initially, it slows down development; for rapidly iterative startup environments the implementation code may not be ready for some time due to spending time writing tests first.
    - You have to perform housekeeping continually. Because booking more and more tests make your build longer and longer, it’s necessary to refine those tests to make them run more quickly or to remove redundant tests.

4. What’s the primary difference between ES6 Classes and Constructor/Prototype Classes?

5. Why REST?
