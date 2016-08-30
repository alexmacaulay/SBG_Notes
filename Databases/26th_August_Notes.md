# 25th August - Hadoop

## Hadoop

### HDFS (Hadoop Distributed FileSystem)

* Multiple nodes (servers)
* Based on x86 architecture
* Native support for chosen server's FileSystem
* Flexibility to choose what servers we want to use (cheap)
* Data lives on server
* We can send tasks to the server and have executed on that server

> Nodes are "industry standard" x86 servers that cost $2,500 to $15,000 each, depending on CPU, RAM, and disk choices. A standard DataNode server is typically a 2U rack server with a two-socket Intel Sandy Bridge or Ivy Bridge CPU with a total of 12 processors. Each CPU is typically fitted with 64GB to 128GB of RAM. DataNodes usually have a dozen 2TB or 3TB 3.5 inch hard drives in a JBOD (just a bunch of disks) configuration.

## MongoDB

### What is mongoDB?

> MongoDB is a free and open-source cross-platform document-oriented database. Classified as a NoSQL database, MongoDB avoids the traditional table-based relational database structure in favor of JSON-like documents with dynamic schemas (MongoDB calls the format BSON), making the integration of data in certain types of applications easier and faster. MongoDB is developed by MongoDB Inc. and is free and open-source, published under a combination of the GNU Affero General Public License and the Apache License. As of July 2015, MongoDB was the fourth most widely mentioned database engine on the web, and the most popular for document stores.

MongoDB stores data using a flexible document data model that is similar to JSON. Documents contain one or more fields, including arrays, binary data and sub-documents. Fields can vary from document to document. This flexibility allows development teams to evolve the data model rapidly as their application requirements change. When you need to lock down your data model, optional document validation enforces the rules you choose.

Developers access documents through rich, idiomatic drivers available in all popular programming languages. Documents map naturally to the objects in modern languages. Documents map naturally to the objects in modern languages, which allows developers to be extremely productive. Typically, there’s no need for an ORM layer.

MongoDB provides auto-sharding for horizontal scale out. Native replication and automatic leader election supports high availability across racks and data centres. And MongoDB makes extensive use of RAM, providing in-memory speed and on-disk capacity.

Unlike most NoSQL databases, MongoDB provides comprehensive secondary indexes, including geospatial and text search, as well as extensive security and aggregation capabilities. MongoDB provides the features you need to develop the majority of the new applications your organisation develops today.

* brew services start mongo
* mongo


### JSON DataTypes

* Strings
  * "This is a string"
* Numbers
  * 3.00
* Null
* Arrays
  * ["one", "two", "three"]
* Objects
  * {thing: "something", otherthing: 2}
* Boolean
  * true

### BSON Data Types

>BSON is a computer data interchange format used mainly as a data storage and network transfer format in the MongoDB database. It is a binary form for representing simple data structures, associative arrays (called objects or documents in MongoDB), and various data types of specific interest to MongoDB. The name "BSON" is based on the term JSON and stands for "Binary JSON".

* Object ID
  * objectid()
* string
* integer (32- or 64-bit)
* double (64-bit IEEE 754 floating point number)
* date (integer number of milliseconds since the Unix epoch)
* byte array (binary data)
* boolean (true and false)
* null
* BSON object
* BSON array
* Javascript Code
* MD5 Binary Data
* Regular Expression

### Update Operators

* **$set** - replaces the value
* **$inc** - increments a numeric value by a specified value (or 1)
* **$setOnInsert** - only sets the value if the document didn't contain that field in the first place. Has no effect on documents that did (used with {multi: true})
* **$rename** - renames the fields (i.e. changes the key)
* **$mul** - multiplies a numeric value by a specified value
* **$currentDate** - sets the value to the current date
* **$push** - adds a specified item to an array
* **$unset** - removes the field from the document

### Task

### MongoDB Brewdog Lab

So now you've seen how we can interact with MongoDB NoSQL databases, it's time to stretch ourselves and have a bit of a pratice.

### Setup
Run the following bash script from your command line to import the data from Brewdog's Punk API into a database called `brewdog` on your local machine:

```bash
touch punkapi.json && curl https://punkapi.com/api/v1/beers -u c4ae17fcb0f44fccb93f5c8494732b72 >> punkapi.json && mongoimport --db brewdog --collection beers --jsonArray --file ./punkapi.json && rm ./punkapi.json
```
Inside the brewdog database you'll find a collection called beers, containing loads of data about the beers brewdog provide for us.

### Tasks

Find a Mongo command that will do each of the following tasks. Google and the MongoDB docs are your friends:

1. Returns all the beers in the database
2. Returns how many beers are in the database as a number
3. Returns the names and alcohol contents of all the beers in the database
4. Adds a custom beer with your chosen values
10. Returns the 10 strongest beers
11. Returns the three weakest beers
4. Returns the beer with the highest pH value
6. Returns the beer with the highest number of hop varieties in its recipe
7. Returns the beer that pairs best with Haggis Spring Rolls
8. Finds your favourite beer and adds a "favourites" field to it with your name
9. Changes the "contributed_by" field for all the beers to your name
10.
