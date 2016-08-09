# 9th August - Web technologies and Version Control

## What is the internet?

* Lots of computers connected together
* 1969 was when the internet started - by universities

## What is the web?

* Interconnected series of web pages

## Intranet

* Internal version of the internet
* Used by organisations


## E-commerce

* Online shops
* Buying things online


## B2B

* Business-to-business
* JIRA
* Trello

## B2C

* Business-to-customer
* Amazon
* Ebay

## C2C

* Facebook
* Gumtree
* Ebay

## Difference between a website and a web application

* Website is a static page to get information, web application is something that the user interacts with

## Web Technologies
* Application layer - Applications - Application Layer
* Transport Layer - TCP, UDP - Transport Layer
* Network Layer - IP - Network Layer
* Data Link Layer - Ethernet, FDDI, ISDN - Data Link Layer
* Physical Layer - Cable, Fiber - Physical Layer
* Client --> Request --> Server
* Client <-- Response <-- Server


## HTTP - HyperText Transfer Protocol

* Everyone uses HTTP
* http://109.152.191.208
* http://google.com


## HTTP Verbs

* Get (Get http://www.google.com - server sends google home page)
* Post (Search on google - a results page is returned)
* Put (Replaces the whole thing)
* Patch (Replaces specific things)
* Delete

## What is a URL?

* Uniform Resource Locator
* scheme://domain:port/path?querystring#fragment

## CRUD

* Create
* Read
* Update
* Delete
* Design pattern for how to interact with data

### RESTful

* Index - GET ~/fish
* New - GET ~/fish/new
* Create - POST ~/fish
* Edit - GET ~/fish/:id/edit
* Update - PUT ~/fish/:id
* Show - GET ~/fish/:id
* Delete - DELETE ~/fish/:id

## HTTP Status codes

* 200 = OK
* 201 = Created
* 204 = No content
* 206 = Partial content
* 301 = Moved permanently
* 302 = Found
* 304 = Not modified
* 307 = Temporary redirect
* 400 = Bad request
* 401 = Unauthorised
* 403 = Forbidden
* 404 = Not found
* 405 = Method not allowed
* 408 = Request timeout
* 410 = Gone
* 429 = Too many requests
* 500 = Internal server error
* 502 = Bad gateway
* 502 = Service unavailable

## Task

* Using Postman or Insomnia look up some APIs

## Version Control

### What do we need from a Version Control Tool?

* Backup and Restore
* Synchronisation between different developers
* Short-term undo
* Tracking of who changed what, and when
* Sandboxing
* Branching and Merging

### Terminology

* Repo (repository) - the database storing the files
* Local copy - your directory of files. The version of the project on your machine
* Remote copy - the version of the project on a remote server
* Master/Trunk - the primary branch
* Commit - save a shanpshot of your repo

### Git

* git init
* git add
* git commit
* git status
* git diff
* git log
* git log --oneline
* git reset (--soft/--hard)
* git clone
* git pull
* git push 
