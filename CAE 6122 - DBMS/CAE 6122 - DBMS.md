
# Part - A (2M)
#### 1. Components of DBMS:
- Hardware
- Software
- Data
- Procedures
- Database Access Language
- People
#### 2. Data Definition Language
- DDL - Data Definition Language
- consists of the SQL commands that can be used to define the database schema
-  used to create and modify the structure of database objects in the database.
- DDL cmds:
	- CREATE
	- DROP
	- ALTER
	- TRUNCATE
	- RENAME
	- COMMENT
#### 3. Various cmds used in DML:
- INSERT: It is used to insert data into a table.
- UPDATE: It is used to update existing data within a table.
- DELETE: It is used to delete records from a database table.
- LOCK: Table control concurrency.
- CALL: Call a PL/SQL or JAVA subprogram.
- EXPLAIN PLAN: It describes the access path to data.
#### 4. Why $NF is more preferable than BCNF?
- 4NF has very similar definition as BCNF. 
- A relational Schema is in 4NF, if all multivalued dependencies A to B are trivial and determinate A is super key of schema. 
- If a relational schema is in 4nf, it is already in BCNF. and 4NF decomposition preserve the all functional dependency. so 4NF is preferable than to have BCNF.
#### 5. Enlist Joined Queries:
- Joined queries in SQL are used to retrieve data from multiple tables based on a related column between them. 
- The most common types of joins are:
	- Inner Join: Retrieves records that have matching values in both tables.
	- Left Join (or Left Outer Join): Retrieves all records from the left table and the matched records from the right table.
	- Right Join (or Right Outer Join): Retrieves all records from the right table and the matched records from the left table.
	- Full Join (or Full Outer Join): Retrieves all records when there is a match in either the left or right table.

```sql
SELECT * 
FROM table1
INNER JOIN table2 ON table1.column_name = table2.column_name;
```

#### 6. State transitive dependency in dbms:
- Transitive dependency occurs when the value of one non-key attribute determines the value of another non-key attribute through a chain of dependencies.
- For example, consider a relation with attributes A, B, and C, where A is the primary key. 
- If attribute B depends on attribute A, and attribute C depends on attribute B, but not directly on attribute A, then there is a transitive dependency from A to C through B.
- Transitive dependencies violate the principles of database normalization, particularly the third normal form (3NF), which aims to eliminate such dependencies. 
- To resolve transitive dependencies, the relation is typically decomposed into smaller relations to achieve normalization.
#### 7. Diff. btw shared lock vs exclusive lock
|S.No.|Shared Lock|Exclusive Lock|
|---|---|---|
|1.|Lock mode is read only operation.|Lock mode is read as well as write operation.|
|2.|Shared lock can be placed on objects that do not have an exclusive lock already placed on them.|Exclusive lock can only be placed on objects that do not have any other kind of lock.|
|3.|Prevents others from updating the data.|Prevents others from reading or updating the data.|
|4.|Issued when transaction wants to read item that do not have an exclusive lock.|Issued when transaction wants to update unlocked item.|
|5.|Any number of transaction can hold shared lock on an item.|Exclusive lock can be hold by only one transaction.|
|6.|S-lock is requested using lock-S instruction.|X-lock is requested using lock-X instruction.|
|7.|Example: Multiple transactions reading the same data|Example: Transaction updating a table row|
#### 8. Application of B+ Tree:
- Database Indexing
- File Systems
- In-Memory Databases
- Geographic Information Systems (GIS)
- Cache Management
#### 9. Outline the steps involved in Query processing:

<img src="Pasted image 20240322233614.png" alt="Query processing - Pasted image 20240322233614.png" />

![[Pasted image 20240322233614.png]]

#### 10. Highlight the role of a recovery component in DBMS:
- Transaction Rollback
- Transaction Redo
- Write-Ahead Logging (WAL)
- Checkpointing
- Undo and Redo Logs
- Crash Recovery

# Part - B

# 1. DML, DDL, TCL cmds:
https://www.geeksforgeeks.org/sql-ddl-dql-dml-dcl-tcl-commands/

DDL – Data Definition Language
DQL – Data Query Language
DML – Data Manipulation Language
DCL – Data Control Language
TCL – Transaction Control Language

## ****DDL (Data Definition Language)****

[DDL](https://www.geeksforgeeks.org/features-of-structured-query-language-sql/) or Data Definition Language actually consists of the SQL commands that can be used to define the database schema. 
DDL is a set of SQL commands used to create, modify, and delete database structures but not data. These commands are normally not used by a general user, who should be accessing the database via an application.

List of DDL commands: 

- [****CREATE****](https://www.geeksforgeeks.org/sql-create/): This command is used to create the database or its objects (like table, index, function, views, store procedure, and triggers).
- [****DROP****](https://www.geeksforgeeks.org/sql-drop-truncate/): This command is used to delete objects from the database.
- [****ALTER****](https://www.geeksforgeeks.org/sql-alter-add-drop-modify/)****:**** This is used to alter the structure of the database.
- [****TRUNCATE****](https://www.geeksforgeeks.org/sql-drop-truncate/)****:**** This is used to remove all records from a table, including all spaces allocated for the records are removed.
- [****COMMENT****](https://www.geeksforgeeks.org/sql-comments/): This is used to add comments to the data dictionary.
- [****RENAME****](https://www.geeksforgeeks.org/sql-alter-rename/)****:**** This is used to rename an object existing in the database.

## ****DQL (Data Query Language)****

****DQL**** statements are used for performing queries on the data within schema objects. 
	The purpose of the DQL Command is to get some schema relation based on the query passed to it.

List of DQL: 

- [****SELECT****](https://www.geeksforgeeks.org/sql-select-clause/)****:**** It is used to retrieve data from the database.

## ****DML(Data Manipulation Language)****

The SQL commands that deal with the manipulation of data present in the database belong to DML or Data Manipulation Language and this includes most of the SQL statements. 
It is the component of the SQL statement that controls access to data and to the database. Basically, DCL statements are grouped with DML statements.

List of DML commands: 

- [****INSERT****](https://www.geeksforgeeks.org/sql-insert-statement/): It is used to insert data into a table.
- [****UPDATE****](https://www.geeksforgeeks.org/sql-update-statement/)****:**** It is used to update existing data within a table.
- [****DELETE****](https://www.geeksforgeeks.org/sql-delete-statement/): It is used to delete records from a database table.
- [****LOCK:****](https://www.geeksforgeeks.org/sql-lock-table/) Table control concurrency.
- ****CALL:**** Call a PL/SQL or JAVA subprogram.
- ****EXPLAIN PLAN:**** It describes the access path to data.

## ****TCL (Transaction Control Language)****

Transactions group a set of tasks into a single execution unit. 
Each transaction begins with a specific task and ends when all the tasks in the group are successfully completed. 
If any of the tasks fail, the transaction fails. 
Therefore, a transaction has only two results: success or failure. 
You can explore more about transactions [_****here****_](https://www.geeksforgeeks.org/sql-transactions/). Hence, the following TCL commands are used to control the execution of a transaction: 

****BEGIN:**** Opens a Transaction.

[****COMMIT****](https://www.geeksforgeeks.org/sql-transactions/)****:**** Commits a Transaction.

## ****DCL (Data Control Language)****

DCL includes commands such as GRANT and REVOKE which mainly deal with the rights, permissions, and other controls of the database system. 

List of  DCL commands: 

[****GRANT:****](https://www.geeksforgeeks.org/mysql-grant-revoke-privileges/) This command gives users access privileges to the database.

# 2. Characteristics feature of NoSQL dbs. and their types:

- NoSQL is a type of database management system (DBMS) that is designed to handle and store large volumes of unstructured and semi-structured data.
- The term NoSQL originally referred to “non-SQL” or “non-relational” databases

****Key Features of NoSQL:****

1. ****Dynamic schema:*** 
	1. NoSQL databases do not have a fixed schema and can accommodate changing data structures without the need for migrations or schema alterations.
2. ****Horizontal scalability:**** 
	1. NoSQL databases are designed to scale out by adding more nodes to a database cluster, making them well-suited for handling large amounts of data and high levels of traffic.
3. ****Document-based:**** 
	1. Some NoSQL databases, such as MongoDB, use a document-based data model, where data is stored in a ****scales****semi-structured format, such as JSON or BSON.
4. ****Key-value-based:**** 
	1. Other NoSQL databases, such as Redis, use a key-value data model, where data is stored as a collection of key-value pairs.
5. ****Column-based:**** 
	1. Some NoSQL databases, such as Cassandra, use a column-based data model, where data is organized into columns instead of rows.
6. ****Distributed and high availability:**** 
	1. NoSQL databases are often designed to be highly available and to automatically handle node failures and data replication across multiple nodes in a database cluster.
7. ****Flexibility:**** 
	1. NoSQL databases allow developers to store and retrieve data in a flexible and dynamic manner, with support for multiple data types and changing data structures.
8. ****Performance:**** 
	1. NoSQL databases are optimized for high performance and can handle a high volume of reads and writes, making them suitable for big data and real-time applications.

****Types of NoSQL database:**** 
	Types of NoSQL databases and the name of the database system that falls in that category are:

1. ****Graph Databases****: 
	1. Examples – Amazon Neptune, Neo4j
2. ****Key value store:**** 
	1. Examples – Memcached, Redis, Coherence
3. ****Column:**** 
	1. Examples – Hbase, Big Table, Accumulo
4. ****Document-based:**** 
	1. Examples – MongoDB, CouchDB, Cloudant