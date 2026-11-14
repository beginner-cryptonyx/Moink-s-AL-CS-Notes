---
aliases:
  - DBMS
tags:
  - flashcards/database/DBMS
---
**DBMS** :: **Database Management System**, which is a systems software for the definition, creation, and manipulation of a database


# Features of DBMS
## Data Dictionary: 
<div></div>

Contains **Meta-data** about database:
1. Table definition
2. Table names
3. Attributes
4. Data Types
5. Validation rules
6. Primary and Foreign Keys
7. Relationship between tables
8. Data about **Physical** storage of data
<div class='blank'></div>

**Improves the [[Data Integrity|Integrity]] of data**: ensuring it is accurate, complete and **consistent**

## Logical Schema:
**Logical Schema**::Shows structure of database and its relations <!--SR:!2024-11-21,3,250-->

1. Overview of database structure
2. models the problem, via methods like [[#Entity Relationship (ER) Diagrams|ER Diagrams]]
3. Independent of any particular DBMS
4. Describes the relationship between data and its structure 


# Security in DBMS
1. Authentication
2. **Back up and recovery procedures**
3. Access Rights:: Different permissions  to different tables per user (like read only) <!--SR:!2024-11-21,3,250-->
4. Views:: Different users able to see different (required) part of database <!--SR:!2024-11-21,3,250-->
5. [[Encryption]]
6. Record and Table locking::Prevents simultaneous access to data, so that data is not overwritten <!--SR:!2024-11-21,3,250-->

# Software tools in DBMS
## Developer Interface
<div></div>

1. Allows developer to write queries in SQL
2. Allows user to create items like tables, forms and reports
3. Creates input output ability via menus/buttons etc.
<div class='blank'></div>

## Query Processer
<div></div>

1. Takes in query written is SQL and processes it
2. Allows user to enter criteria
3. Searches for data that meets criteria
4. Organizes results to be displaced to the user
5. Software that processes and executes queries written in SQL
6. Contains <!--SR:!2024-11-21,3,250--> 
<div class='blank'></div>
