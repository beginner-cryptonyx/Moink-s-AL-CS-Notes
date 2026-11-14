---
subject:
  - "[[Computer Science]]"
grade:
  - "[[AS Level]]"
related:
creation-date: 2025-04-22
up:
  - "[[Computer Science]]"
tags:
aliases:
modified:
  - 2025-04-23
  - 2025-04-22
completion: "100.00"
importance: 10
---

> [!grey]- Syllabus
> ## 10.1 Data Types and Records
> 
> - [x] Select and use appropriate data types:
>   - [x] INTEGER
>   - [x] REAL
>   - [x] CHAR
>   - [x] STRING
>   - [x] BOOLEAN
>   - [x] DATE
>   - [x] ARRAY
>   - [x] FILE
> - [x] Understand the purpose of a record structure
> - [x] Write pseudocode to:
>   - [x] Define a record structure
>   - [x] Read data from a record
>   - [x] Save data to a record
> 
> ## 10.2 Arrays
> 
> - [x] Understand technical terms: index, upper bound, lower bound
> - [x] Select suitable data structure: 1D or 2D array
> - [x] Write pseudocode for:
>   - [x] Declaring and using 1D arrays
>   - [x] Declaring and using 2D arrays
> - [x] Write pseudocode to process array data:
>   - [x] Bubble sort
>   - [x] Linear search
> 
> ## 10.3 Files
> 
> - [x] Understand why files are needed
> - [x] Write pseudocode to:
>   - [x] Handle text files with one or more lines
> 
> ## 10.4 Introduction to Abstract Data Types (ADT)
> 
> - [x] Understand that an ADT is a collection of data + operations
> - [x] Recognise stacks, queues, and linked lists as ADTs
> - [x] Describe key features of:
>   - [x] Stack
>   - [x] Queue
>   - [x] Linked list
> - [x] Justify use of stack, queue, or linked list for a given scenario
> - [x] Perform operations (add, edit, delete) on:
>   - [x] Stack
>   - [x] Queue
>   - [x] Linked list
> - [x] Describe array-based implementations of:
>   - [x] Stack
>   - [x] Queue
>   - [x] Linked list


# Abstract data types
## Linked List
### Properties
1. Consists of nodes
2. Has a `Start pointer` which is a pointer that points to the start of the list
3. Last node in the linked list has a null pointer
4. Data is added by manipulating pointers
5. Nodes are traversed in sequence
6. Unused nodes are stored on the free list

### Insertion of new node
1. Check for a empty node 
2. Assign data item to first empty node in the free list
3. The same node's pointer will be set to the node that will come after insertion
4. Node that was pointing to node that comes after insertion will now point to this new node
5. The free list pointer is set to point to the next free node

### Advantages
1. It is easier to add/delete data
2. Only the pointers need to be changed if data is to be rearranged
### Disadvantages
1. Pointers need to be stored as well
2. More complex to implement
### Implementation
Array Implementation
1. Two one dimensional arrays will be declared, one for data and one for pointers
2. Same index represents one node
3. Declare variable for start pointer
4. Define variable for null pointer (-1)
5. Add routines to add and delete data

Record based Implementation
1. Define record type with felid for data and pointer
2. Declare a 1D array of the defined record type
## Stack
### Implementation
1. Declare 1D array 
2. Number of elements in the array correspond to the size of the required stack
3. Declare a variable for a stack pointer
4. Declare variable for max size of stack
5. Stack pointer is used as an index to the array
6. Initialize variables to indicate empty stack
7. Store each item on stack as one array element
8. implement push and pop routines

## Queue

```dataviewjs
const file = dv.current();
const checkboxes = file.file.tasks;
const totalCheckboxes = checkboxes.length;
const completedCheckboxes = checkboxes.filter(t => t.completed).length;
const completionPercentage = totalCheckboxes > 0 
    ? ((completedCheckboxes / totalCheckboxes) * 100).toFixed(2) 
    : "0.00";

try {
    await app.fileManager.processFrontMatter(dv.app.vault.getAbstractFileByPath(file.file.path), (frontmatter) => {
        frontmatter["completion"] = completionPercentage;
    });
    console.log("✅ Frontmatter updated successfully!");
} catch (error) {
    console.log(`❌ Error updating frontmatter: ${error}`);
}
```