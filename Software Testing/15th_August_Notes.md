# 15th August - Software Testing

## What is testing?

* Finding bugs
* Ensuring work meets criteria
* Performance testing
* Security testing
* Scalability testing
* Exploratory testing

## Risk and Quality

* What is the legal impact of this issue? Could we be sued because of this issue?
* What is the financial impact?
* What is the brand impact?

## The Seven Testing Principles

1. Testing shows the presence of bugs
2. Exhaustive testing is impossible
3. Early testing
4. Defect clustering
5. The pesticide paradox
6. Testing is context dependent
7. Absence of errors fallacy

## Key testing terms

* Defect
* Effects a defect might have on a project
* Root cause vs Effects
* Error
* Failure
* Fault
* Mistake
* Bug

## Debugging and testing

* **Debugging** - used by developers to identify the cause of bugs or defects in code and undertake corrections
* **Testing** - systematic exploration of a component or system with  the main aim of finding and reporting defects

## Testing lifecycles

* Planning and control
  * Determines what is going to be tested
  * How it is going to be tested
  * Who will do the testing
  * Defining our exit criteria
  * Monitoring and control feedback into the continual activity of planning
* Analysis and design
  * Reviewing the test basis
  * Identify test conditions, cases, and procedures
  * Design the tests
  * Detail the test environment and tooling
  * Highlight the test data
  * Create traceability between test basis and test cases
* Implementation and execution
  * Prioritising test cases, creating test data and writing test procedures
  * Creating test suites from collected test cases
  * Checking environment is set-up correctly
  * Running tests in determined order
  * Log testing activities and defects
  * Reporting incidents
* Exit criteria and reporting
  * Ensure the exit criteria has been met to satisfy the stakeholders
  * Determine if more tests need to be made
  * Checking the system is in a ready state for release
  * Writing up results for sponsors and stakeholders
* Closure activities
  * Make sure docs are up to date and archived
  * Closing down and archiving the test environment, infrastructure and testware
  * Passing over testware to maintenance team
  * Documenting the lessons learnt

## Software testing models

### The waterfall model

* system requirements  
  * software requirements  
    * Analysis  
      * program design  
        * coding  
          * testing  
            * operations   

### The V-model

* Requirement spec - Capture of users needs
  * Functional spec - Definition of functions required to meet user needs
    * Technical spec - Technical design of functionality
      * Program spec - Detailed design of each module or unit
        * Coding
      * Unit testing - Testing against the program spec
    * Integration testing - Testing against the technical spec
  * System testing - Testing against the functional spec
* Acceptance testing - Testing against the requirement spec

### Iterative and incremental models

* Requirements
* Design
* Code
* Test
* Repeat

## Test Levels

### Unit testing

* Units are also called programs, modules or components
* Code is usually written in component parts or units constructed in isolation for integration at a later stage
* Each of those units of code will relate to a certain function or area and be tested by the developer to make sure it works

### Integration testing

* Purpose is to expose defects in the interfaces and interactions between integrated components or system
* The test objects are essentially the interface code
* Three type of integration testing:
  * Big bang
    * All units are linked at once resulting in a complete system
    * Difficult to isolate errors since no attention to verifying interfaces across individual units
    * Introduces risk that problems may only be found late in the project
  * Top down
    * High level modules are created first, so a stub code is needed
    * Advantages
      * Useful in creating software intended to be generic
      * This will allow for early demonstrations of the products functionality
      * May help identify requirement changes and issues
    * Disadvantages
      * Stubs can create a lot of work
      * Stub definition can be difficult
      * Reproducing test conditions may not be possible
  * Bottom up
    * In the absence of parent modules, drivers are used
      * Advantages
        * Higher accuracy at the granular level
        * Components are added in a controlled manner
        * User and business awareness used to clarify
      * Disadvantages
        * It is difficult to estimate top-level forecasts
        * Driver development could increase work load

### System testing

* Tests functionality from an end to end perspective
* Focuses on the whole system in a representative live environment
* Usually carried out by a team independent of the development process
* Tests functional and non-functional requirements

### Acceptance testing

* Testing to provide end users confidence that the system function according to user experience
* Often done by customers or users of the system
* Key purpose is to demonstrate system conformance to customer requirements and operational processes

#### Forms of Acceptance Testing

* Contract and Regulation Acceptance Testing
  * **Contractual** - acceptance criteria outlined in a contract
  * **Regulations** - certain industries have rigid regulations that must be abided by:
    * Governmental
    * Legal
    * Safety reasons
* Alpha and Beta Acceptance Testing
  * **Alpha** - Performed at the developing site, but not by the developing team
  * **Beta** - Performed by customers at their own location
* User Acceptance Testing
  * Tested by user representation
  * Checks the system meets business needs
* Operational Acceptance Testing
  * Checks the processes and procedures are in place to allow the system to be used and maintained. Includes checking:
    * Back up facilities
    * Procedures for disaster recovery
    * Training for end users
    * Maintenance procedures
    * Data load and migration tasks
    * Security Procedures

## Test types

### Functional testing

* Testing of the functions of system. Verifying a specific action or function of the code works
* Also called specification based testing - i.e. testing against a specification
* Uses the following models: process flows, state transition, security threat and plain language
### Non-functional testing

* Testing of the quality characteristics of system such as:
  * Installability
  * Maintainability
  * Performance
  * Load handling
  * Stress handling
  * Portability
  * Recoverability
  * Reliability
  * Usability
### Structural testing (white box)

* How the code makes the functionality work. What is happening 'under the hood'
  * Can be carried out at any test level
  * Decision coverage
  * Statement coverage
* Can be done at all levels of testing

### Regression testing

* Carried out on every other part of the system to check that a fixed defect hasn't changed other parts of the system
* Repeated testing of already tested program
* Performed when software or environment is changed
* Based on risk
* Performed at all levels (functional, non-functional, structural)

### RCRCRC

* Recent
* Core
* Risk
* Configuration
* Repaired
* Chronic

### Change related testing

* Testing in a live environment when there has been:
  * Modification
  * Migration
  * Retirement of software
* Impact analysis (Risk) and Metrics from previous projects are very important in this area
* They help estimate the amount of re-testing and regression testing
* What are the possible consequences?
* What ares will remain unchanged?

## Test Development and Test Design

### Test Design

#### You must consider the context (environment) within which the tests are taking place:

* The organisation
* The maturity of the development and testing process
* Time constraints
* Safety or regulatory requirements
* The people involved

### Test Terms

* Test base - all documents from which the requirements of a component or system can be inferred. The documentation on which the test cases are based.
* Test conditions - a characteristic of the software that can be checked with a test or set of tests. E.g. a function, feature, quality, attribute or structural element.
* Test cases - a set of input values, execution, pre-conditions, expected results and execution post-conditions developed for a particular test condition
* Test procedures - a sequence of actions for the execution of a test

### Test cases

* These consist of a set of input values
  * Execution pre-conditions
  * Expected results
  * Execution post-conditions
* They are developed to cover a certain test objective or test condition

### Expected results

* The most important part of executing tests is knowing why you are doing them in the first place
* Expected results should be produced as part of the specification of a test case

### Test case specification checklist

* Description
* Precondition
* Steps
* Input
* Expected result
* Actual result
* Status
  * **Passed** - the expected and actual results match
  * **Failed** - the actual result does not match the expected result
  * **Not tested** - the test case has not been executed for the test run
  * **Not applicable** - the test case does not apply
  * **Cannot be tested** - the precondition may not be met or defect in one of the steps
* Comments
* References
* Conclusion

### Approaches to creating test cases

* Functional - Test each function
* Domain - Test by partitioning different sets of values
* Specification based - Test against specifications
* Risk based
* User
* Scenario / Use Case
* Exploratory

## Test procedures

* Identifies all the necessary actions in sequence to execute a test
* Often called test scripts
* Execute the test case by inputting the values and checking the outcome

## Traceability

* Ability to trace test conditions to specs and requirements
* Allows impact analysis when the requirements change
* Ensures requirements test coverage can be determined for a set of tests
* Horizontal traceability
  > The tracing of requirements for a test level through the layers of test documentation (e.g. test plan, test design specification, test case specification and test procedure specification or test script)
* Vertical traceability
  > The tracing of requirements through the layers of development documentation to components

## Scheduling

* Once the procedures are complete the test cases can be formed into a test execution schedule
* This defines the order in which the various test procedures are executed
* The test execution schedule will take into account such factors as regression tests, prioritisation, and technical and logical dependencies

## Test execution schedule

* Most important test must be executed at the earliest to make sure that even if time is shortened, we have still tested the top priority functionality
* Take into consideration the logical order of execution and technical dependencies
* Highest priority is always run first (possibly taking the opportunity to test any dependencies or relative areas at the same time).
* Test plans must be highly dynamic due to :
  * Changing priorities
  * Defects
  * Resources

## Test coverage

* Quantitative measures are extremely important to help stakeholders to understand how much of the system has been tested
* Compare these two statements
  * We have tested for two weeks
  * 80% of the system has been tested
* Coverage mights make up part of the completion criteria defined in the test plan. It can also be used to tell us when to stop testing

## Familiarity with the software

* Get as much information about the application as possible
* Obtain available documentation (requirement specs, user guides)
* Listen to tutorials and exercise the software itself
* Determine a list of features and different user roles
* Try to become 'in tune' with the way end users interact with the system

## Standardisation

* Write in keeping with already existing documentation which the whole team / company understands
* Build your tool kit of documentation templates now - adjust and improve the specifications, test cases and test procedures in the practical sessions
* If a feature has a lot of input combinations, consider separating the testing into subtests. e.g. to verify how the registration feature works with invalid input, write sub tests for different values.

## Testing and reporting

* Make sure pre-conditions are met before performing the tests
* Perform all steps listed in the test case
* Fail status
  * If the status for a particular step is FAIL, verify if this bug has already been reported and, if not, report it straight away
  * After you have reported the bug, continue completing the subsequent steps in the test case. If subsequent steps have dependencies on a failed step and there are no workarounds, then mark them as N/A and move to next step
* Observation are very important in the test case
  * You do not have to include any insight you gathered while completing a particular step, but it can be useful. The information can help troubleshoot issues or understand if.

## Testing techniques

### Specification based (black box)

* Examines the functionality of an application without knowledge of its internal structures
* It is based entirely on the software requirements and specifications
* Specifications can include non-functional elements as well as functions (reliability, usability and performance)
* Sanity/Smoke check
* Equivalence partitioning
* Boundary value analysis
* Decision table testing
* State transition testing
* Use case testing

#### Sanity check/Smoke testing

* **Smoke test** - the aim is not to find defects but to check system health
* **Sanity check** - makes sure the bugs reported in previous builds are fixed for this release before doing a full regression test
* Acceptable in the integration / system / acceptance testing levels

#### Decision table testing

* Lists all the input conditions that can occur and all the actions that can arise from them
* Structured into tables as rows, with conditions at the top of the table and possible actions at the bottom
* Business rules involving combinations of conditions to produce combinations of actions are arranged across the top of the table
* Each column is representative of a single business rule and show how input conditions combine to produce actions
* Each column therefore is a possible test cases since it identifies inputs and expected outputs

### Infeasibility

* Certain combinations of conditions that are logically impossible
* Don't forget - sometimes, we may want to test an infeasible test condition to make sure it can't happen

### State transition testing

* When a system is represented as being in one state and transitions from that state to another
* The transformations are determined by the rules of the system

### What is the goal?

* Finding situations where the wrong action or the wrong new state occurs in response to a particular event
* As testers we reports these problems all the time as defects

### Terminology

* **States** - how something exists at that time
* **Transitions** - the change from one state to another
* **Inputs or events**
* **Actions** - the actions that can result from a transition
