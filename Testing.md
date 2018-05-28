# Testing

In this chapter we will discuss about testing, its importance, type, testing strategy, and how we can write a good testing.

## Why (Automate) Testing ?

* To verify our code automatically : because manual testing is expensive and slow.
* To avoid regression : like parachute this is our safety net so that we don't break existing code.
* To design our code (Test Driven Development) : test help us to design our code because good code is always easy to test.

## Type of Test

* Unit Test : test unitary on one unit (class, but can be classes)
* Integration Test : testing the integration of classes, also integration with the third party.
* Acceptance Test : testing the application.

Those tests are mocked and run to validate the application

* Smoke Test : to validate with the real environment.
* Performance Test : To validate the performance.

## Test Pyramid

         AT
      IT IT IT
    UT UT UT UT UT
  
Not

    AT AT AT AT
      IT IT IT
        UT
       
## Unit Test

Test the feature not the implementation.
  
## F.I.R.S.T Principles of Unit Test

* Fast : how many time we should run the test ? (1 min, 2 min, 1 Hour)
* Isolated and Independent : Test should be independent of environment. (Study case with time dependent). The Given, When, Then.
* Repeatable : Test should be deterministic result.
* Self - Validating : No manual inspection, only Red and Green.
* Timely : Test first.

## Tools

* Junit
* AssertJ
* Mockito

## Excercice 

* Testing existing code (see excercice)
* Junit
 * @Before, @BeforeClass, @Test
 * Testing Exception
* AssertJ
 * Assert Equal
 * Assert Collections, Map
* Mockito
 * Create Mock using Mockito : using annotation, using factory
 * Mockito to throw exception
* TDD with FizzBuzz
 * RED : Create a failing test
 * GREEN : Fix the test
 * Refactor

## Integration Test

### Test third party 

* Test the use of third party API (Library, Url, database, BOM, etc.)
* The objective is to make sure that the evolution of the API doesn't break the code.
* Can be limited to the happy path and some edge case.

### Test Spring Configuration

* Testing that all configuration, and classes are colaborated correctly.
* Can be limited to the happy path and some edge case.

## Excercice

* Test third party API call using WireMock and Spring Runner

## Tools

* Junit
* Spring Runner
* Wiremock

## Acceptance test

* Highest confidence
* But expensive and hard to maintain
* To validate the critical path
* Use Mock mvc if need to test directly in controller
* Use Application Server if we want to test also the code before controller such as Filter

## Excercice

* Test integral application with SpringBoot + MockMvc
* Test integral application with SpringBoot + Application Server 

## Another type of test

### BDD

* Behavior Driven Development
* Write a test in a language understandable by non DEV person
* Colaboration between product, Dev and Tester
* Use Cucumber for JVM

### Smoke Test

* Test if the application doesn't break in the production environment (doesn't use any mock)
* Limited to the critical path


