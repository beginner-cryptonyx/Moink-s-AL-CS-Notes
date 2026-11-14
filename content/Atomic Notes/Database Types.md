---
tags:
  - flashcards/database
aliases:
  - Relational Database
  - Flat file database
  - referential integrity
subject:
  - "[[Computer Science]]"
---

***A structured collection of items that can be accessed by different application [[Program|programs]]***
# Types of database

## Flat file database
1. Collection of items of data
2. Can be structured as collection of records

## Relational Databases:
<div></div>
***A database where the data items are linked by internal pointers***
<div class='blank'></div>

**Advantages of relational database over flat file**
<div></div>

---

| **Aspect**                    | **File-Based Approach**                                                                        | **Relational Database**                                                                           |
| ----------------------------- | ---------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| **Data Redundancy**           | More data redundancy                                                                           | Reduced data redundancy                                                                           |
| **Data Consistency**          | More data inconsistency (worse integrity)<br><br>updates are not propagated across the system. | Maintains data consistency<br><br>changes in one table automatically reflect in others.           |
| **Query Complexity**          | Hard to perform complex queries<br><br>new programs must be written each time.                 | Complex queries are easier to run.                                                                |
| **Privacy**                   | Lack of privacy<br><br>user views/access cannot be implemented.                                | Provides different views<br><br>users see only specific parts of the database (improved privacy). |
| **Program-Data Independence** | Not independent<br><br>data changes require rewriting programs.                                | Program-data independence<br><br>data changes do not require rewriting programs.                  |

---
<div class='blank'></div>

## Database Terminology
#### Table:
<div></div>
- A **group of similar data**, in a database, with rows for each instance of an entity, and columns for each attribute.
<div class='blank'></div>
#### Entity:
<div></div>
- Referred to, as a **row** or **[[#Tuple]]** or record
- *object which data can be stored about*
<div class='blank'></div>

#### Field:
<div></div>

- Referred to as a **column** or **attribute**
<div class='blank'></div>

#### Tuple:
<div></div>

- a **single row of data** in a table
- Also called **[[#Entity]]**
<div class='blank'></div>

#### Attribute:
<div></div>

- An **individual data item** stored for an [[#Entity]]

#### Candidate Key:
<div></div>

- an **attribute that could be a [[#Primary key]]
- smallest set of [[#Attribute]]s where no other tuple has the same vale
<div class='blank'></div>
#### Primary key:
<div></div>

- **Unique Attribute**
- used to uniquely identify a record/tuple
- can be used as a [[#Foreign Key]] in another table
- forms link between the tables
<div class='blank'></div>

#### Foreign Key:
<div></div>

- a **field in one table** that **links to a primary key** in another
<!--SR:!2024-11-19,1,230-->
<div class='blank'></div>

#### Secondary Key:
<div></div>

- Alternative / additional key used along with the [[#Primary key]] to locate specific data
<!--SR:!2024-11-21,3,250-->
<div class='blank'></div>

#### Composite Key:
<div></div>

- Set of [[#Attribute]]s that form a [[#Primary key]] to provide an unique identifier for a table
<div class='blank'></div>

#### Relationship:
<div></div>

- Situation in which one table in a database has a foreign key that refers to a primary key in another table in the database
<div class='blank'></div>

### Referential integrity
<div></div>

 - The Property of a database that does not contain values of foreign key that are not matched to the corresponding primary key
 - 
<div class='blank'></div>
##### Importance of Referential integrity:
<div></div>

1. Makes sure data in the database is **consistent** and up to date
2. Ensures *every* foreign key had a corresponding primary key
3. prevents records being added/modified/deleted incorrectly 
4. Makes sure changes in one place are reflected in all related records 
5. Ensures queries made return accurate and complete results
6. makes sire non-existent data cannot be referenced
<div class='blank'></div>
---