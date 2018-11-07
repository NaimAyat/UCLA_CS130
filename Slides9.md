# Testing
* Unit testing is the execution of a complete class, routine, or small program or team of programmers
* Component testing is the execution of a class, package, small program, or other program element
* Integration testing is the combined execution of two or more classes, packages, components, or subsystems
* System testing is the execution of the software in its final configuration, including integration with other software and hardware systems
* Regression testing is the repetition of previously executed test cases for the purpose of finding defects
#### Further Testing Classification
* Black-box testing refers to tests in which the test cannot see the inner workings of the item being tested
* White-box testing refers to tests in which the tester is aware of the inner workings of the item being tested
## Test Adequacy Criteria
* Problems:
  1. Developers may not write enough tests
  2. Developers may write many redundant tests, causing quality assurance overhead
  3. During software evolution, we don’t have time to retest everything. Identifying relevant tests (relevant to code changes) is difficult
### Test Coverage
* Statement coverage: How many statements are exercised by tests? 
  * Has each statement been executed? 
* Branch coverage: How many of possible branch evaluations are exercised by tests? 
  * Has each control structure evaluated both true and false?
* Path coverage: How many of possible paths are exercised by tests? 
  * Has every possible route been executed? 
## JUNIT
* Automated unit testing framework
* Provides the required environment for the component
* Executes the individual services of the component
* Compared the observed program state with the expected program state
* Reports any deviation from the expectations
* Does all of this automatically
### JUNIT Test Cases
* Each test case is realized by its own class derived from JUNIT TestCase class
* Each test of the test case is realized by its own method whose name starts with `test...`
* `assertTrue()` method inherited from `TestCase` has the same meaning as `assert
### Validating Program States
* Assertions (JDK 1.4 and later)
#### `assert(b)`
* If `b` is true, nothing happens
* If `b` is false, a runtime error occurs
* Raise `AssertionError` exception
* C and C++ have similar `abort()`
### Executing Component Tests
* If a test fails, the subsequent test cases are no longer executed
* One should be able to run tests individually, independent of other test cases
* One should be able to group tests into test suites
* One should be able to grasp immediately whether tests have failed and if so, which ones
