### SQL cmd:

```sql
-- CREATE a DB
create database db_name;

-- GET all databases
show databases;

-- USE the particular DB
use database_name;

-- CRETAE a table
create table akbarsha ( ID int, Name varchar(255));

-- GET all tables
show tables;

-- ADD a record in a table
insert into akbarsha (ID, Name)
    values (1, "Akbarsha");

-- GET all records from the table
select * from akbarsha

-- DESCRIBE the table structure
describe table_name;

-- UPDATE the table fields
alter table students
    add column StudentBlood varchar(6);

alter table department
    add column PRIMARY KEY(ID)
```