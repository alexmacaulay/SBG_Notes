# 16th August - Software Testing

## Use case Testing

* Specify functionality as business scenarios or process flows
* Capture individual interactions between 'actors' and the system
* It is often good practice to write a test case representing each use case
* Very useful when testing process flows and business rules
* Very effective in defining acceptance tests as the sue case usually represents how the system will be used

### Actors

* Users can play many roles with respect to a system
* If we do not understand all the roles a user plays, then we cannot understand the system
* Actors paths through the system can be represented diagrammatically or as a scenario

## Experienced based technique

* Use a tester's skill intuition an experience with similar application to the one under test
* Defect and failure lists can help identify areas that are susceptible to problems
* Fault attach approach lists possible defects and failures and design tests around that list

## Exploratory testing

> An informal test design technique where the tester actively controls the design of the tests as those tests are performed and uses information gained while testing to design new and better tests

* Important testing technique executed by experienced testers with an in depth knowledge of the similar systems
* Useful when specifications are missing or inadequate and there is sever time pressure
* It is especially suited to web app development in agile methods
* You still need a well defined structure rather than having a scatter gun approach

### Advantages

* It doesn't require much preparation
* Testers report a large proportion of bugs via this method

### Disadvantages

* There is no review of test planning, an experienced user of the system may not be an experienced tested
* Testers have to remember the exact steps they took to create a defect - otherwise reproduction may be difficult

## White box testing

* Also known as clear, glass, open, transparent, structural testing
* Tests internal structures as opposed to functional testing

## Control flow graphs

* A method of representing decision points and the flow of control within codeS

## Statement testing and coverage

* The statement coverage is also known as line coverage or segment coverage.
* The statement coverage covers only the true conditions.
* Through statement coverage we can identify the statements executed and where the code is not executed because of blockage.
* In this process each and every line of code needs to be checked and executed

### Advantages

* It verifies what the written code is expected to do and not to do
* It measures the quality of code written
* It checks the flow of different paths in the program and it also ensure that whether those path are tested or not.

### Disadvantages

* It cannot test the false conditions.
* It does not report that whether the loop reaches its termination condition.
* It does not understand the logical operators.

## Decision testing and coverage

* Decision coverage is also known as Branch coverage or all-edges coverage.
* It covers both the true and false conditions unlikely the statement coverage.
* A branch is the outcome of a decision, so branch coverage simply measures which decision outcomes have been tested. This sounds great because it takes a more in-depth view of the source code than simple statement coverage
* A decision is an IF statement, a loop control statement (e.g. DO-WHILE or REPEAT-UNTIL), or a CASE statement, where there are two or more outcomes from the statement. With an IF statement, the exit can either be TRUE or FALSE, depending on the value of the logical condition that comes after IF.

### Advantages

* To validate that all the branches in the code are reached
* To ensure that no branches lead to any abnormality of the program’s operation
* It eliminate problems that occur with statement coverage testing

### Disadvantages

* This metric ignores branches within boolean expressions which occur due to short-circuit operators.

## Choosing a test technique

* Type of system
  * Is it safety critical?
  * Is it a financial system?
  * Is it web or cloud based?
* Regulatory standards
* Customer/contractual requirements

## Test management

### Risk

#### Types of Risk

* Product risk
  * Potential failure areas in software that are a risk to the quality of the software
  * The potential of a defect occurring in a live environment is a product risk
  * Failure prone software
  * Potential that the software/hardware could cause harm
  * Poor software characteristics i.e. security, reliability, usability, maintainability or performance
  * Poor data integrity and quality
  * Software that does not perform intended functions

* Project risk
  * Failure of a third party
  * Contractual issues
  * Skills, training and staff shortages
  * Personal issues
  * Political issues
  * Improper attitude
  * Defining the right requirements
  * Time and budget
  * Environment inadequacy
  * Low quality of data

#### Mitigating risks

#### Risk-based testing

* An approach to testing to reduce the level of product risks and inform stakeholders of their status
* It involved the identification of the product risks and the use of risk levels to guide the test process

### Organisation

* Project managers
* QA managers
* Developers
* Business and domain experts
* Infrastructure personnel
* IT operations

### Test leader

* Test programme manager
* Test managers
* Test team leader
* Test co-ordinator

#### Typical tasks include

* Co-ordinate and possibly write and review test strategy (for the project) or policy (for the organisation)
* Plan and negotiate with project managers and other stakeholders

### Tester

* Review and contribute to the test plans
* Review requirements
* Test specification and test cases based on the techniques given in the test plan
* Prepare test data
* Additional resources for testing
  * Developers
  * Business analysts
  * Users
  * SMEs
  * Specialists

### Independence

#### Benefits of independent testing

* See defects that others who are closer to the project may not
* The tester is unbiased
* Can verify assumptions made during the specification and implementation phases

#### Drawbacks of independent testing

## Test planning activities

* Scope and risk
* What to test
* Who will test what
* Scheduling

### Entry criteria

* Test environment is available for use
* Test tools are installed in the environment for use
* Testable code is available

### Exit criteria

* All planned tests have been run
* Defined requirement coverage has been achieved
* No high priority or severe defects are outstanding
* High risk areas have been fully tested
* Schedule and budget has been met

### Estimation

* Metric based
  * relies on data collected from previous or similar projects. This is a fairly accurate approach when comparing similar sized projects
* Expert based
  * the estimations are based on experience. This could be from developers, analysts, SMEs, test consultants, etc. It can be similar to the Wideband Delphi approach, but not always done in that exact way.
* Functional point analysis
* Use case/story point analysis
* Delphi technique
* Expert judgment

### Test progress monitoring and control

* Based on the activities an timescales within the test plan
* We need to constantly review actual against planned. This rocied important visibility of the project progress.
* The information is also important to measure test coverage and determine if we have reacher the exit criteria goal.

#### Common metrics

* Percentage of work done
* Number of test cases executed
* Defect totals and details
* Subjective confidence of release
* Milestones achieved

#### Test reporting

* Reporting test status is about effectively communicating our findings to other project stakeholders
* Reporting should include:
  * Test summary report identifier
  * Summary
  * Variances
  * Comprehensive assessment
  * Summary of results
  * Evaluation
  * Summary of activities
  * Approvals

#### Configuration management

* Configuration identification
  * Identification of documents, labelling of hardware, grouping of related items
* Control
  * Ensures that all changes to a complex system are performed with the knowledge and consent of management
* Status accounting
  * Status accounting provides the means by which the current state of the development can be judged and the history of the development life cycle can be traced
* Auditing

#### If configuration management is not handled correctly then you may find:

* Multiple people working on the same element at the same time without any knowledge of the others work
* Not able to match program source to object code

## Incident management

* Logging incidents
* Classifying them
* Identifying the impact
* Tracking
  * for recognition to correction, retest and closure

### Incident/defect reports

* Can be raised by anyone at any time
* Provide as much information on the problem as possible

### Incident reports normally contain...

## How do we test a web app?

* Visual testing
* Cross-browser/device testing
* Functional testing
* Accessibility review
* Security testing
* Performance testing
* Stress/load testing
* Usability testing

### Visual testing

#### Things to look out for

* Form fields
* Character limits and checks
* Broken links
* Broken buttons
* Error messages & notices
* Date integrity

## Accessibility review

* WAI-ARIA
* BS 8878:2010
* WCAG WG
* Company/industry standard
* Colour blindness

### Code Validity

* HTML and CSS Validators
* Link checkers
* Apply common sense
* http://www.validator.w3.org
* http://www.jigsaw.w3.org

### Security testing

## UX

### Good UIs are hard to design

* You are not the user
* You are not your Grandma
* Users are hard to predict

### Usabilty: how well users can use the system's functionality

* **Learnability** - is it easy to learn?
* **Efficiency** - once learned, is it fast to use?
* **Memorability** - is it easy to recall what you learned?
* **Errors** - are there few, and are they useful?
* **Satisfaction** - is it enjoyable to use?

### How do we design for usability?

* Put yourself in the user's shoes
* Test with representative users
* Learn about common design patterns
* Think critically

## Homework

Find some bad UX examples.
