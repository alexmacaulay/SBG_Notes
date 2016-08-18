# 17th August - Software Testing

## Performance

### Factors affecting performance

* Sever hardware speed
* Database query speed
* Location of servers
* User connection speed
* Page weight
* Number of HTTP requests

#### Caching

#### Number of HTTP requests

#### Page weight

* Only include what's necessary
* Don't serve large images
* Compress images
* GZip assets
* Minify code

### Web performance testing toold

* pingdom
* JMeter
* YSlow

### Exploratory testing

> It's so frustrating. No matter how many tests we write, no matter how many test cases we execute, we always find the most serious bugs when we go off the scripts

#### Test strategy aims

* Does the software behave as expected under the conditions it's supposed to be able to handle?
* Are there any other risks?

> Simultaneously designing and executing tests to learn about the system, using your insights from the last experiment to inform the next

#### Essential Elements

* Designing
* Executing
* Learning
* Steering
* Timeboxing

#### Charters

* Often generated during conversations
  * Agile ceremonies
  * Requirements gathering meetings
  * Conversations with BA, stakeholders and developers
* Often generated when executing test cases
* Must include:
  * The target area
  * The resources/techniques/tools we'll use
  * The information we're looking for
* Should not be too specific
* Should not be too broad

#### Where can we get ideas?

* Stakeholder questions and comments
  * "What will happen if we add 300 more products in the future?"
  * "Could a user ever see another user's private profile?"
* The source code
  * //TODO: Don't know why this works, but it does. Don't touch it. Need to fix at some point
* Developer comments
  * "The profile image upload is a bit flaky because the Redis write queue is being weird. It works most of the time though"
* Your own findings and knowledge of the system
  * "That video behaved strangely when I put the iPad in landscape mode I wonder if that problem exists any else?"
* Existing defects and defect reports

#### Observation

* De alert to subtle clues
* Try unusual things
* Use monitoring software to look for the unusual
  * High CPU/Memory usage
  * Unusual network traffic
  * Strange HTTP requests / responses
* Look at console & server logs

### Stress testing

* What's the maximum load until a system breaks?
* How is the system breaking?
* Is the system able to recover?
* When under stress, in how many ways can the system break and where?

### Volume testing

* Does the system break when handling a large volume of data?
* Is its performance affected by large volumes of data?

### Load (or capacity) testing

* Will the system support the anticipated load?
* Will the system support the expected peak load?
* Is the system capable of handling increased load?

### Reliability & recovery testing

* Is the system able to recover from breakages?
* How often does the system break?

### Functional vs performance testing  

### Load testing tools

* HP LoadRunner
* JMeter

# Benefits

## Health & Medical

* Private medical insurance - Bupa
  * SBG pay cost of annual health insurance
  * Gives access to medical care in case you need it
  * Excess of £150

## Sky

* Fill out form
* Can get for friends and family

## Gym

* 4 gyms nearby
* SBG pay £35 towards it
* You only have to pay > £35 and tax
* gymmembership@skybettingandgaming.co.uk
* Different gym - apply on portal
