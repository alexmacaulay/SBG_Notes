# Kanban, Agile Tooling & The Spotify Model

## Kanban

* Introduced by Taichi Ono at Toyota in the 1940s to:
	* Remove waste
	* Improve flow of production process
	* Utilise people's efforts efficiently
* Adopted for production of software to promote Just in Time (JIT) delivery

> "Kanban is not a software development lifecycle methodology ... It requires that some process is already in place so that Kanban can be applied to incrementally change the underlying process." - David Anderson

![kanban board](http://kanbanblog.com/explained/image/kanban-board-1.png)

### Principles of Kanban

* Start with the existing software development processes
* Agreement to pursue incremental and evolutionary change
* A respect and evolution of the current processes, roles and responsibilities
* Encouragement of leadership at all levels in development process

### Kanban Process

* Visualises data flow to identify bottleneck
* Sets Work-In-Progress (WIP) limits to focus on the current task
* Concentrate effort on a single task at any given time to enhance efficiency


### Good Flow

* Workflow should be monitored regularly and blockages solved
* Measurements of flow are used to identify core improvements in the process
* Promotes a shared understanding of the system
* Introduces the ability to monitor whether changes to the process have produced 

### Limit WIP

* Apply limits to the work in progress at each stage of the development process
* Work is pulled into the next phase of development once it is ready
* Increase in quality of task completion due to a focus on singular tasks
* Can reduce lead time by easing competing concerns for tasks beyond developer's role
* Focuses on the important tasks first one by one — ticks off the singular most important tasks

## Agile Tooling

### Agile tools

* Preference for 'all inclusive' tools — application lifecycle management (ALM) or task management solution
* To enhance team collaboration and information sharing
* Key features include agile task boards, user stories and burn-down charts
* Configuration management — to accommodate greater automation

### Task Management Tools

* ALM and task management tools
* Visual representation (via metrics, charts and dashboards) of the current state of each user story, the iteration and the release
* Integrate with configurations management tools
* Aggregate developer and tester updates to the task status as they complete their work
* Associate development tasks and test tasks with the same story, to provide a complete picture
* Record stories and their relevant development and test tasks

### Wikis

* Product feature diagrams, feature discussions, prototype diagrams, photos of whiteboard discussions
* Tools and/or techniques for developing and testing found to be useful by other members of the team
* Metrics, charts, and dashboards on product status
* Conversations between team members, similar to instant messaging and email, but shared with all team members

### Instant messaging and video

* Allow real time direct communication between, team members, especially distributed teams
* Involve distributed teams in standup meetings
* Reduce telephone bills by use of VOIP technology, removing cost constraints in distributed settings

### Desktop Sharing

* In distributed teams, product demonstrations, code reviews, and even pairing can occur
* Capturing product demonstrations at the end of each iteration, which could be posted to the team's wiki

### Other tools

#### Test Design and Implementation Tools

* Test design tools
* Test case management tools
* Test data preparation and generation tools
* Test data load tools
* Automated test execution tools
* Exploratory test tools

#### Configuration Management and DevOps Tools

* Configuration Management
	* Stores source code, automated tests, manual tests and other test work products in the same repository as the product source code. 
	* Provides traceability between which versions of the software were tested with which particular versions of the tests
* Cloud computing and virtualisation


## The Spotify Model

![The Spotify Model Part 1](https://spotifylabscom.files.wordpress.com/2014/03/spotify-engineering-culture-part1.jpeg)
![The Spotify Model Part 2](https://spotifylabscom.files.wordpress.com/2014/09/spotify-engineering-culture-part2.jpeg)

### Squads

* Co-located & self-organising
* One long-term mission
* End-to-end development ability
	* All skills/tools to design, develop, test and release to production
* Experts on their product area
* Product Owner prioritises work
* A **mini-startup**
	* Lean Startup Thinking
	* MVP and Validated Learning

#### Build-Measure-Learn Loop

![Build-Measure-Learn loop](http://www.400minutes.com/wp-content/uploads/2013/02/f0405.jpg)



### Tribes

* Usually co-located
* An "incubator" for mini-startups
* Always < 100 people
	* Dunbar Number: "Most people cannot maintain a social relationship with more than 100 people"
* Shared lounges promote inter-squad contact & sharing
* Regular informal meet ups, demos, hack-days and socials
* A tribe leader
	* Responsible for providing the right habitat for the tribe
* Has access to Agile Coaches and DevOps experts

> A business incubator in business speak is a company that helps new and startup companies to develop by providing services such as management training or office space. Business incubators differ from research and technology parks in their dedication to startup and early-stage companies.

#### Dependencies

* Remove inter-tribe dependencies
* Minimise inter-squad dependencies
	* Regular surveys to identify blocker and dependencies
	* Product owners work together (within a tribe)
	* "Scrum of Scrums" on an ad-hoc basis

### DevOps Squad

* No handoff from dev team to DevOps team
* Informal F2F collaboration with Squads
* DevOps **enable**	squads to deploy their own code:
	* Configuring environments for squads

### Chapters

* People who do similar work
* Usually local to a tribe (not company-wide)
* Meet regularly to discuss best practice/ideas
* Has a **Chapter Lead**:
	* Is always part of a squad, and does real work
	* Is the **line manager** for chapter members
	* Develops chapter members

### Guilds

* Communities of interest
* Organisation-wide
* No restrictions on membership
* Communicate regularly
	* To share tools, code, examples, practices, etc.
	* Meet regularly and organise events
	* Talk regularly in #channels and mailing lists
* Has a **Guild Coordinator**