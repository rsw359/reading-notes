# Class 03 *Reading Notes*

## Mongo and Mongoose

Differences between Sql and NoSql

1. SQL databases are primarily called as Relational Databases (RDBMS); whereas NoSQL database are primarily called as non-relational or distributed database.

2. SQL databases are table based databases whereas NoSQL databases are document based, key-value pairs, graph databases or wide-column stores.

3. SQL databases have predefined schema whereas NoSQL databases have dynamic schema for unstructured data.

4. SQL databases are vertically scalable whereas the NoSQL databases are horizontally scalable. SQL databases are scaled by increasing the horse-power of the hardware. NoSQL databases are scaled by increasing the databases servers in the pool of resources to reduce the load.

5. SQL databases uses SQL ( structured query language ) for defining and manipulating the data, which is very powerful. In NoSQL database, queries are focused on collection of documents. Sometimes it is also called as UnQL (Unstructured Query Language). The syntax of using UnQL varies from database to database.

What kind of data is a good fit for an SQL database?

- SQL databases are good fit for the complex query intensive environment

Give a real world example.

- Oracle Express Edition

What kind of data is a good fit a NoSQL database?

- NoSQL database fits better for the hierarchical data storage as it follows the key-value pair way of storing data similar to JSON data.

Give a real world example.

- MongoDB

Which type of database is best for hierarchical data storage?

- SQL databases

Which type of database is best for scalability?

- Seems like NoSQL databases are best for scalability

What does SQL stand for?

- Structured query language

What is a relational database?

- A relational database is a database which supports SQL and stores data in related tables. The tables conform to a specific schema that contains tagged fields

What type of structure does a relational database work with?k

- A relational database works with tables with fields that are related

What is a ‘schema’?

- The requirements for querying data

What is a NoSQL database?

- A NoSQL database that stores data in a more efficient way than an SQL database

How does it work?

- It works using collections instead of tables. The collections dont use a schema

What is inside of a Mongo database?

- A nontabular collection of documents that can contain different fields

Which is more flexible - SQL or MongoDB? and why.

- NoSQL is more flexible. You can store data of different types in the same collection due to their being no implied schema

What is the disadvantage of a NoSQL database?

- One downside is that you can have duplicate data that needs to be updated in multiple places when changes are made.
- Another downside is that the data formats can be unpredictable
