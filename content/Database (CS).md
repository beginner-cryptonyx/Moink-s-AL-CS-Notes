---
aliases:
tags:
  - flashcards/database
subject:
  - "[[Computer Science]]"
up:
  - "[[Computer Science]]"
importance: 8
creation-date: 2024-11-15
modified:
  - 2025-05-06
  - 2025-04-21
  - 2025-04-18
  - 2025-04-16
grade:
  - "[[AS Level]]"
completion: "100.00"
marks-lost: 44
topical: "[[Database topical paper analysis]]"
---

> [!grey]- Syllabus
> ## 8.1 Database Concepts
> 
> - [x] Understand limitations of file-based data storage
> - [x] Describe relational database features that address those limitations
> - [x] Understand and use database terminology:
>   - [x] Entity
>   - [x] Table
>   - [x] Record / Tuple
>   - [x] Field / Attribute
>   - [x] Primary Key
>   - [x] Candidate Key
>   - [x] Secondary Key
>   - [x] Foreign Key
>   - [x] Composite key
>   - [x] Relationships (One-to-One, One-to-Many, Many-to-Many)
>   - [x] Referential Integrity
>   - [x] Indexing
> - [x] Create and interpret Entity-Relationship (E-R) diagrams
> - [x] Understand and apply normalization:
>   - [x] First Normal Form (1NF)
>   - [x] Second Normal Form (2NF)
>   - [x] Third Normal Form (3NF)
> - [x] Evaluate if tables are in 3NF
> - [x] Normalize from description, data, or unnormalized tables
> 
> ## 8.2 Database Management Systems (DBMS)
> 
> - [x] Describe how DBMS addresses file-based system issues
> - [x] Understand:
>   - [x] Data management and data dictionary
>   - [x] Data modelling
>   - [x] Logical schema
>   - [x] Data integrity
>   - [x] Data security (backups, access rights)
> - [x] Understand software tools in a DBMS:
>   - [x] Developer interface
>   - [x] Query processor
> 
> ## 8.3 Data Definition Language (DDL) and Data Manipulation Language (DML)
> 
> - [x] Understand the role of DDL in structure creation/modification
> - [x] Write SQL DDL statements:
>   - [x] `CREATE DATABASE`
>   - [x] `CREATE TABLE` with data types:
>     - [x] `CHARACTER`
>     - [x] `VARCHAR(n)`
>     - [x] `BOOLEAN`
>     - [x] `INTEGER`
>     - [x] `REAL`
>     - [x] `DATE`
>     - [x] `TIME`
>   - [x] `ALTER TABLE`
>   - [x] `PRIMARY KEY`
>   - [x] `FOREIGN KEY REFERENCES`
> - [x] Understand the role of DML for queries and maintenance
> - [x] Write SQL DML statements:
>   - [x] `SELECT`
>   - [x] `FROM`
>   - [x] `WHERE`
>   - [x] `ORDER BY`
>   - [x] `GROUP BY`
>   - [x] `INNER JOIN`
>   - [x] `SUM`
>   - [x] `COUNT`
>   - [x] `AVG`
>   - [x] `INSERT INTO`
>   - [x] `DELETE FROM`
>   - [x] `UPDATE`


# Flat file database and its issues

1. More data redundancy
   - Same data stored many times
2. Program dependence with flat files
   - Change in structure of data means the programs that access said data have to be re-written
3. Worse data integrity
   - Data updated in one place is not updated everywhere
4. Cannot perform complex queries
5. Lack of data privacy
   - Cannot provide user views

# Relational Database

## Advantages over flat-file database
1. Reduced data redundancy
   - Each item stored only once (no duplicate data)
2. Improved data integrity
   - Changes in one table will automatically update in another
   - Linked data cannot be different in 2 tables
3. Program-data independence
   - Changes in data does not require program to be re-written
4. Complex queries can be easily run
5. Can provide views
   - Users can only see specific aspects of the database

## Database terminology
1. Entity :: An object about which data can be stored
2. Table 
3. Record / Tuple
4. Felid / Attribute
5. Primary Key :: An unique attribute used to identify a record
6. Candidate Key :: An attribute that could potentially be a primary key
7. Secondary Key 
   -  An attribute that is a candidate key, but not the primary key
   -  An attribute that can be indexed for faster searching
8. Foreign Key :: A field in one table that is linked to a primary key in another table
9. Composite key :: Primary key that contains 2 or more attributes that together form the primary key
   - Used when both keys individually aren't unique, but together are unique
10. Relationships 
11. Referential Integrity
    - Makes sure changes in data in one place is reflected in all related records
    - Makes sure data that does not exist cannot be referenced
    - Ensures every foreign key has a corresponding primary key
    - Ensures that data in the database is consistent
    - Prevents records from being modified incorrectly
    - Makes sure queries return accurate and complete results
12. Indexing
## ER Diagram
## Normalization

# DBMS

## Data management and Data Dictionary
## Data Modelling
## Logical Schema
A model of a database that is not specific to one DBMS
## Data Integrity
## Data Security
1. Backups
   - Periodically takes copies of DB and stores it offsite 
   - So that data can be restored if lost
2. Access Rights
   - Different users are given different permissions to different tables
   - By having different accounts
   - eg. read/write, read only, full access
3. Views
   - Different users able to see different parts of the data database
4. Record/Table Locking
   - Prevents simultaneous access to data
    - So that data is not overwritten
5. Encryption
   - Data turned into cypher text
   - Cannot be understood without decryption key
## Developer Interface
A software tool that allows the user to create items such as tables, forms and reports
## Query Processor
Software that processes and executes queries written in SQL

# Normalization

## Purpose of normalization
1. Reduce data redundancy
2. Improve data integrity
3. Organising data into well-structured tables


## 1NF
- No repeating groups of data
- No repeating attributes
- **Atomic Data**
- All tables have **primary key**

## 2NF
- All data is in 1NF
- No partial dependancies

## 3NF
- All data is in 2NF
- No transitive dependancies


# 1. [[Database Types|Types of Database]]

# 2. [[ER Diagrams]]

# 4. [[DBMS (Database Management System)|DBMS]]

# [[DDL and DML]]


Field : A column / attribute in a table
Entity : Anything that data can be stored about


```dataviewjs
const file = dv.current();
const checkboxes = file.file.tasks;
const totalCheckboxes = checkboxes.length;
const completedCheckboxes = checkboxes.filter(t => t.completed).length;


const completionPercentage = totalCheckboxes > 0 
    ? ((completedCheckboxes / totalCheckboxes) * 100).toFixed(2) 
    : "0.00";
console.log(totalCheckboxes, completedCheckboxes, completionPercentage)
try {
    await app.fileManager.processFrontMatter(dv.app.vault.getAbstractFileByPath(file.file.path), (frontmatter) => {
        frontmatter["completion"] = completionPercentage;
    });
    console.log("✅ Frontmatter updated successfully!");
} catch (error) {
    console.log(`❌ Error updating frontmatter: ${error}`);
}
```
