---
subject:
  - "[[Computer Science]]"
grade:
  - "[[A Level]]"
related:
creation-date: 2025-05-21
up:
  - "[[Computer Science]]"
tags:
aliases:
modified:
  - 2025-09-20
  - 2025-09-11
  - 2025-06-12
  - 2025-06-10
  - 2025-06-02
  - 2025-06-01
  - 2025-05-21
importance: 13
completion: "89.29"
topical: "[[Data Representation Topical Analysis]]"
---

> [!grey]- Syllabus
> ## 13.1 User-defined Data Types
> 
> - [x] Understand why user-defined types are necessary
> - [x] Define and use non-composite types:
>   - [x] Enumerated
>   - [x] Pointer
> - [ ] Define and use composite data types:
>   - [x] Set
>   - [x] Record
>   - [ ] Class/Object
> - [x] Choose and design appropriate user-defined data types for a given problem
> 
> ## 13.2 File Organisation and Access
> 
> - [x] Understand methods of file organisation:
>   - [x] Serial
>   - [x] Sequential (using a key field)
>   - [x] Random (using a record key)
> - [x] Understand file access methods:
>   - [x] Sequential access (for serial/sequential files)
>   - [x] Direct access (for sequential/random files)
> - [x] Describe and use hashing algorithms for:
>   - [x] Reading from files
>   - [x] Writing to files
> 
> ## 13.3 Floating-point Numbers, Representation and Manipulation
> 
> - [ ] Describe binary floating-point real number format
> - [x] Use two’s complement form
> - [x] Understand effect of changing bit allocation (mantissa vs exponent)
> - [x] Convert between binary and denary floating-point numbers
> - [x] Normalise floating-point numbers
> - [x] Understand reasons for normalisation
> - [x] Understand consequences of binary approximation of real numbers
> - [x] Understand underflow and overflow
> - [x] Understand how rounding errors occur in binary representation
>



# User defined data types
> [!error] Data types
> **Primitive Data Types** :: Data types that are directly supported by the programming language, they are built in and represent one value
>
> **User defined Data types** :: A data type that is constructed by a programmer that references atleast one other data type ( this could be primitive or user defined )
>
> **Composite Data Types** :: Data types that group multiple values
>
> **Non-composite data types** :: Data types that store a single value
> 

## Importance of user defined data types
- Create a new suitable data type that the language does not provide 
- Allows data types not available in a programming language to be constructed
  - To meet requirements of application
- Extends the flexibility of the programming language
## Non composite data types
### Pointer
- ! User defined non composite data type referencing memory locations and indicates the type of data stored in the memory location
```rust
// Declaration
TYPE <identifier> = ^<datatype> //data type that is stored in the memory address

// Example
TYPE MyIntegerPointerType = ^INTEGER
DECLARE MyIntPointer : MyIntegerPointerType
```
### Enumerator
- ! User defined non composite data type that stores a list of possible values that is ordered
```rust
// declaration
TYPE <identifier> = (value1, value2, value3, ...)

//example
TYPE Season = (Spring, Summer, Autumn, Winter)
```
## Composite data types
- Datatype constructed by a **programmer**
- References at least one other data type, which is either a primitive data type or a user defined data type 


### Set
- User defined data type which is a composite data type
- Includes a list of unordered elements
- Set theory operations like union and intersection can be applied to the elements
- To define a set, the data type it will use needs to be included
- All elements in a set have to be of the same data type

```rust
TYPE <NameOfSet> = SET OF <datatype>
DEFINE <identifier> (<item1>,<item2>,<item4>,<item4>) : <NameOfSet>

//example
//Write pseudocode statements to declare the set data type, SymbolSet, to hold the following set of mathematical operators, using the variable Operators.
// + – * / ^
TYPE SymbolSet = SET OF CHAR
DEFINE Operators ('+', '–', '*', '/', '^') : SymbolSet 
```
### Record
- User defined data type which is a composite data type
- It uses other data types in its definition to form a single new data type
- Data types that are referenced in a record could be primitive or user defined data types
- It includes and basically groups together related items
- It includes a fixed number of items

```rust
TYPE <NameOfRecord>
  DECLARE <Item1>: <Datatype of item 1>
  DECLARE <Item2>: <Datatype of item 2>
  DECLARE <Item3>: <Datatype of item 3>
  DECLARE <Item4>: <Datatype of item 4>
  DECLARE <Item5>: <Datatype of item 5>
ENDTYPE
```
### Class / Object

# File organization
## Serial file
- ! Files are stored in chronological order
- Files stored one after the other and also access one after the other
- New records are appended to the file (added in the next available space)

Advantages:
1. Easy to append each new record to the end of the file
2. Allows data to be in the same order as it has been read
3. No **key felids** (extra data) needed to put files in order (such as customer id or time)


## Sequential file
- Records are stored in a particular order, one after the other based on the key field
- New records are added into their correct positions
## Random file
- Data is stored in any available location
- Location of a record is found via using a **hashing algorithm** on the key field 

# File Access
## Sequential access
- ! Used for **sequential** and **serial** files
- Records are accessed one after the other (linearly)
- Records are found via searching from the beginning of the file till the end (record by record) until record is found or end of file reached, this is done for serial files
- Record by record file search is also done for sequential files until the required record is found or the key field value is exceeded.

## Random access / Direct access
- ! Used for **sequential** and **random** files
- Allows a record to be found in a file without other records being read
- Records are found by using the key field of the target record, using a hashing algorithm the records location is found

Advantages:
1. High access speeds
2. No need for serial or sequential processing, meaning there is no need to search through records

### Random access for Sequential files
- For **sequential files** an index of all key fields are kept
- This index is searched for the address of the file location where the target record is stores 

### Random access for random files
- A hashing algorithm is used on the key field of the record
- To calculate the address of the memory location where target record is expected to be stored
- Methods like linear probing or search overflow area is used if record is not at the expected location
### Hashing algorithm
- **Mathematical formula which is used to perform calculations on the key field of the record being searched or stored**
- These hashing algorithms allow for **direct access** to files by getting the location as a result of the calculation, of a record in random and sequential files
- However the hash calculated could be a duplicate
  - This causes a collision, as records key does not match stored record key
  - This means that the determined location is already in use for storing another record
  - Then either open hash or closed hash is used

#### Open Hash
- To store records
  - The overflow area is searched linearly 
  - The next open space is found 
- To access records
  - The overflow area is searched linearly until matching record key is found
  - If it is not found the record is not in the file

#### Close hash
- To store records:
  - The file is searched linearly
  - The next available storage space is found and used
- To access records
  - The file is searched linearly from the current position until the matching record key is found
  - If it is not found the record is not in the file

# Floating point numbers

## Bit allocation
- The number of bits in the mantissa is directly proportional to the accuracy of the floating point number
- The number of bits in the exponent is directly proportional to the range of the floating point number

## Normalization
- Stores the maximum range of numbers with the minimum number of bits
- Minimizes the number of leading 0/1's represented
- Increases accuracy when storing very small or large numbers
- Avoids possibility of many numbers having multiple representation


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