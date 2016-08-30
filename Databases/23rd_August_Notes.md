# 23rd August - Vim and Databases

> Practical Vim, Edit Text at the Speed of Thought - Drew Neil

## Vim
### Why Vim?

* It's available everywhere you have a shell
* It's available on remote and cloud machines
* It's available in local VMs, Docker containers etc
* It's extremely powerful
* It encourages DRY in you editing/navigation

### Disadvantages

* Learning curve is huge

### How to get the most out of it ...

* Learn how to use bash
* Configure it right
* Practice, practice, practice
* Learn to touch type
* Accept you won't know it all
* http://www.typingclub.com
* **c i )** - changes all in brackets (highlighted) and allows you to type what you want - stands for Change In Brackets ()
* **c i }** - changes all in braces (highlighted) and allows you to type what you want - stands for Change In Braces {}
* **c i "** - changes all in quotes (highlighted) and allows you to type what you want - stands for Change In Quotes ""
* **d i "** - delete all in quotes (highlighted) - stands for Delete In Quotes ""
* **u** - undo
* **h** - left
* **j** - down
* **k** - up
* **l** - right
* **5 j** - 5 lines down
* **:w** - save
* **d** - delete
* **c** - change
* **>** - indent
* **v** - visually select
* **y** - copy
* **w** - forward by a word
* **b** - back by a word

## Databases

### What's a database?

* Needs to be structured
> a structured set of data held in a computer, especially one that is accessible in various ways.

### Types of Database

* Document-based database
  * MogoDB
  * Elasticsearch
* Key-value datastore
  * Redis
  * Memcached
* Relational database
  * SQLite
  * MySQL

### Basic terminology

* Column
* Row
* Field
* Table
* DBMS

### Relations

* One to one
  * Each row in table A is linked to another row in table B. The number of rows in table a must equal the number of rows in table b. Wife and Husband
* One to many
  * Each row in the table can be related to many rows in the relating table.
* Many to many

### Primary key constraints  

* Uniquely identifies each record
* Must be unique
* Cannot be empty
* Value can never change
* Two Types
  * Simple
  * Compound

### Foreign Keys

* Natural relationships exist between tables in most database structures, foreign keys are used to create

### Task

* Blogging system
* Users need to be able to log in
* Support articles - posting/creating
* Users can comment, but not create
* Authors - can write articles

### Task 2

* Create a relational database structure for a system for a timesheet system
  * Users log in regularly and complete their timesheets
  * Each week, they have to submit the week's timesheet to their manage by clicking a submit button
  * A manager can add projects and work types, and authorise their employees' timesheets. They can only authorise timesheets for people who they manage (either directly or through other managers)
  * Thus, the CEO is the only person who can authorise everyone's sheets is the CEO.

### Database tools

* PostgreSQL
* SQLite
* MySQL
* Redis
* MongoDB
