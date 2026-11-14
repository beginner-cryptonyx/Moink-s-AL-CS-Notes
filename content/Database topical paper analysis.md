---
subject:
  - "[[Computer Science]]"
grade:
  - "[[AS Level]]"
related: 
creation-date: 2025-05-05
up: "[[Database (CS)]]"
tags: 
aliases: 
modified:
  - 2025-05-07
  - 2025-05-06
  - 2025-05-05
---

# Report

| Question | Marks Gained | Marks Lost | Total Marks |
| -------- | ------------ | ---------- | ----------- |
| 1        | 13           | 2          | 15          |
| 2        | 11           | 0          | 11          |
| 3        | 14           | 2          | 16          |
| 4        | 9            | 1          | 10          |
| 5        | 14           | 1          | 15          |
| 6        | 18           | 1          | 19          |
| 7        | 16           | 1          | 17          |
| 8        | 12           | 1          | 13          |
| 9        | 13           | 2          | 15          |
| 10       | 10           | 1          | 11          |
| 11       | 12           | 2          | 14          |
| 12       | 16           | 0          | 16          |
| 13       | 16           | 1          | 17          |
| 14       | 14           | 3          | 17          |

# Postmortem report

## Careless Mistakes
1. Data type `REAL/CURRNCY` misrepresented as `REAL` (1)
2. Relationship misidentified (1)
3. Forgot to add foreign keys :sob: (1)
4. Forgot to mention to add primary key to normalize table (1)

## Phrasing / Keyword Mistakes
- Even though no marks are lost, it would be better to be more verbose in answers pertaining to flat file vs relational
1. Foreign key missing keyword **linked** (1)
2. Needed to be more verbose with access rights question (1)
	- Done via **different accounts/logins** 
	- Talk about views when talking about access rights
3. Mis wrote row as record (1)
4. Incorrect word used to represent type check criteria, `string` used instead of `alphanumeric
5. Horrible phrasing used for question pertaining to why relational database is better than flat file database (2) `

## Knowledge Gaps
1. Incorrect assignment of primary key (used a composite key when not needed) (1)
2. Incorrect answer given for why a given database is normalized in 3NF (1)
	- No many-to-many relationships
	- All fields in each table are fully dependent on PK's for each table
3. Missed one reason for why a composite key exists (1)
	- None (neither) of the keys can uniquely identify the tuple by itself
4. Incorrectly added more than one column (1)
	 ```
	 ALTER TABLE <name>
	 ADD <col> <dt>, <col> <dt>
	 ```

5. Purpose of a query processor (2)
	- Allows the user to enter criteria
	- Searches for the data that meets the entered criteria
	- Organizes the result to be displayed to the user
6. Secondary key definition (1)
	- An alternative key used as wel as tghe primary key to locate specific data