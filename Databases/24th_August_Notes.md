# 24th August - SQL

## Why do we need SQL

### As a tester...

* Getting data for testing
* Saving data, generating during testing activity
* Data verifications in databases
  * Find data
  * To ensure data integrity
  * To manipulate test data for specific tests
* Testing databases

### As a developer...

* Debugging
* Injecting data into SQL databases
* Understanding SQL query performance
* Manual backup and restore
* Data verification and testing

## MySQL Workbench

### Common Data Types

* int
* smallint
* bigint
* float
* char
* varchar
* date
* time
* datetime
* boolean
* blob
* binary

### Common symbols

* **=** - equal to
* **<>** - not equal to
* **!=** - not equal to
* **>** - greater than
* **<** - less than
* **<=** - less than or equal to
* **>=** - greater than or equal to

### Adding rows

### Updating rows

### SQL Part 2

* select count(column) from people;
* select max(column) from people;
* select min(column) from people;
* select avg(column) from people;
* select sum(column) from people;

### Values and Constraints

### Users & Permissions

#### Common permissions

* ALL PERMISSIONS - access all permissions
* CREATE - create new tables or databases
* DROP - delete tables or databases
* DELETE
* INSERT
* SELECT
* UPDATE
* GRANT OPTION

#### User and permissions task

* Give some restrictive privileges to your user
* Start a new workbench connection
  * New tab at the very top of workbench
  * Use localhost as the server and the username/password you set up
* Try running some queries that should work
* Try doing something you're not allowed
* What errors do you get?
