---
subject:
  - "[[Computer Science]]"
grade:
  - "[[A Level]]"
related: 
creation-date: 2025-06-10
up: 
tags: 
aliases: 
modified:
  - 2025-06-11
  - 2025-06-10
---

| Question Number | Marks Gained | Marks Lost | Total Marks |
| --------------- | ------------ | ---------- | ----------- |
| 1               | 14           | 1          | 15          |
| 2               | 8            | 6          | 14          |
| 3               | 2            | 5          | 7           |
| 4               | 6            | 0          | 6           |
| 5               | 3            | 5          | 8           |
| 6               | 6            | 3          | 9           |
| 7               | 5            | 1          | 6           |
| 8               | 6            | 0          | 6           |
| 9               | 2            | 2          | 4           |
| 10              | 5            | 0          | 5           |
| 11              | 5            | 0          | 5           |
| 12              | 3            | 1          | 4           |



# Postmortem Report
## Careless Mistakes
1. Sign bit was not considered when normalizing (3)
2. Number of bits not counted properly (2)
3. Could not identify upper bound for the array like field in the array (1)
## Keywords / Phrasing Mistakes
1. For range of number changing, candidate wrote about how exponent could store a larger value instead of taking about the **number of bits** that could be stored (1)
2. Talk about the precision changes when talking about why number cannot be stored (1)
## Knowledge Gaps
1. Could not answer why certain number could not be stored in the given number of bits (3)
   - Talk about the number's binary val
   - Talk about the normalised form of that value
   - Talk about how number in binary normalised form is too large to store in the given number of bits for mantissa (or range) 
   - Talk about **overflow**
2. Creation of the enumerator data type has `TYPE` as a prefix
3. Reasons for normalising numbers (notes made and flashcards made) (3)
4. Did not know how to set range for record type declaration (1)
5. Did not know about composite data types (3)
6. Classes and object oriented programming not known (3)