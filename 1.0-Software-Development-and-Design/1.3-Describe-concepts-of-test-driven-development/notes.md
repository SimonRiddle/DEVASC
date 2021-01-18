<!-- cSpell:ignore  -->

# Test Driven Development (TDD)

## Overview

* If requirements are light, you can create test code *before* you write application code
* Helps people to be requirement focussed - only write what meets the objectives/requirements
* Helps clarify and constrain in the code, no bloat
* Makes people write code which is test-focussed

### Why use TDD?

* Ensure code is fit for purpose
* Catch bugs locally and early

## TDD 5-Step Plan

1. Create a new test (or add to existing test)
    * What are the requirements of the application code?
2. Run tests, is anything failing that you would expect to pass initially?
    * Correct the tests at this stage
    * Some aspects may fail here, which is acceptable - but use your brain on what should/shouldn't pass
3. Write application code to pass the new tests
    * Write only the code which is required to pass the test
4. Run test, is anything now failing?
    * Correct the test, re-run test
5. Refactor and improve application code

