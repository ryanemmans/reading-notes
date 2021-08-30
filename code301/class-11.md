# CLASS 11 NOTES - Mongo and Mongoose

## ***SQL vs NoSQL Database Differences Explained with few Example DB***

[https://www.thegeekstuff.com/2014/01/sql-vs-nosql-db/?utm_source=tuicool](https://www.thegeekstuff.com/2014/01/sql-vs-nosql-db/?utm_source=tuicool)

- - -

#### **1. Fill in the chart below with five differences between SQL and NoSQL databases:**

| SQL                                                               | NoSQL                                                                      |
|-------------------------------------------------------------------|----------------------------------------------------------------------------|
| Relational Databases (RDBMS)                                      | Non-relational or distributed databases                                    |
| Table based                                                       | Document based (key-value pairs, graph, or wide-solumn stores              |
| Predefined scheme                                                 | Dynamic schema for unstructured data                                       |
| Vertically scalable (increase horse-power of hardware)            | Horizontally scalable (increase db servers to reduce load)                 |
| Uses structured query language for defining and manipulating data | Queries are focused on collection of documents                             |
| Ex: MySql, Oracle, Sqlite, Postgres and MS-SQL                    | Ex: MongoDB, BigTable, Redis, RavenDb, Cassandra, Hbase, Neo4j and CouchDb |

#### **2. What kind of data is a good fit for an SQL database?**

- A good fit for a SQL database would be the complex query intensive environment.

#### **3. Give a real world example.**

- MySQL Community Edition is an open-source database, generally stacked with apache and PHP.
- It can also be stacked with nginx and Node.js on the server side.

#### **4. What kind of data is a good fit a NoSQL database?**

- NoSQL is a good fit for hierarchical data storage because it uses the key-value pair way of storing data similar to JSON.

#### **5. Give a real world example.**

- MongoDB stores data in JSON like documents and is a non-relational database with dynamic schema.

#### **6. Which type of database is best for hierarchical data storage?**

- NoSQL would be best for hierarchical data storage.

#### **7. Which type of database is best for scalability?**

- SQL databases are best for scalability in most typical situations, as they are vertically scalable.

- - -

## ***SQL vs NoSQL or MySQL vs MongoDB***

[https://www.youtube.com/watch?v=ZS_kXvOeQ5Y&ab_channel=Academind](https://www.youtube.com/watch?v=ZS_kXvOeQ5Y&ab_channel=Academind)

- - -

#### **1. What does SQL stand for?**

- SQL stands for Structured Query Language

#### **2. What is a relational database?**

- A relational database works with certain assumptions and supports SQL

#### **3. What type of structure does a relational database work with?**

- A relational database works with tables, or storage containers.

#### **4. What is a ‘schema’?**

- Schema is defined by fields.
- For example: Product ID, Name, Price, Description as a table header.
- Every new row in a table will have values for these fields.

#### **5. What is a NoSQL database?**

- NoSQL is non-relational database.
- It uses collections instead of tables.
- MongoDB is the most popular and is built to efficiently store a very large amount of data.

#### **6. How does it work?**

- Inside the collections are documents, which are similar to rows in a table.
- Documents in NoSQL are not required to use the same schema.
- You could have multiple documents in one collection that have different fields.
- This structure is very flexible with handling data.

#### **7. What is inside of a Mongo database?**

- A MongoDB database contains collections and documents.

#### **8. Which is more flexible - SQL or MongoDB? and why.**

- MongoDB will be more flexible because it does not require the use of the same schema.
- MongoDB also does not rely as heavily on relations.
- MongoDB will also have very fast and efficient queries

#### **9. What is the disadvantage of a NoSQL database?**

- The disadvantage is that you could have duplicate data.
- This data would need to be updated in multiple collections.
- With vertical scaling, there will be a limit to how much power can be provided to the server.

- - -

## Things I want to know more about

- How do we program a SQL or NoSQL database?
- How are these databases integrated into our applications?

[back](../README.md)
