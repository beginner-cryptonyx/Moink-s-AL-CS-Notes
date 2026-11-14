---
subject:
  - "[[Computer Science]]"
grade:
  - "[[A Level]]"
related:
creation-date: 2025-09-04
up:
  - "[[Computer Science]]"
tags:
aliases:
modified:
  - 2025-09-20
  - 2025-09-06
  - 2025-09-05
  - 2025-09-04
completion: "88.00"
importance: 20
---


> [!grey]- Syllabus
> 
> # 20 Programming
> 
> ## 20.1 Programming Paradigms
> 
> ### Low-level Programming
> - [x] Write low-level code with addressing modes:  
>   - [x] Immediate  
>   - [x] Direct  
>   - [x] Indirect  
>   - [x] Indexed  
>   - [x] Relative  
> 
> ### Imperative (Procedural) Programming
> - [x] Recall structural programming constructs  
> - [x] Write code with variables, procedures, functions  
> 
> ### Object-Oriented Programming (OOP)
> - [ ] Understand OOP terminology:  
>   - [x] Objects, properties/attributes, methods, classes  
>   - [x] Inheritance, polymorphism, aggregation, encapsulation  
>   - [x] Getters, setters, instances  
> - [x] Design problem solutions with classes  
> - [x] Write code demonstrating OOP  
> 
> ### Declarative Programming
> - [x] Write rules & facts-based solutions  
> - [x] Solve problems with goal satisfaction (facts & rules)  
> 
> ---
> 
> ## 20.2 File Processing & Exception Handling
> 
> ### File Processing
> - [x] Open/close files (read, write, append modes)  
> - [x] Read from and write to a file  
> - [x] Perform operations on:  
>   - [x] Serial files  
>   - [x] Sequential files  
>   - [x] Random files  
> 
> ### Exception Handling
> - [ ] Understand exceptions & importance of handling them  
> - [ ] Know when to use exception handling  
> - [x] Write program code with exception handling  
> 




# Programming
## Programming Paradigms
> [!error] Programming paradigms
> **Declarative** : Programs that specify the desired result rather than how to get to it
> **Imperative** : Programs with an explicit sequence of commands that update the program state, with or without procedure calls
> **Low-Level** : Programs using the instruction set of a processor
> **Object oriented** : Programs using the concepts of class, inheritance, encapsulation and polymorphism
### Low level
example
```asm
Start: LDD Counter
       INC ACC
       STO Counter
```
### Imperative (Procedural)
1. Imperative programming uses variables
2. Variables are changed using assignment statements
3. Imperative programming relies on iteration
4. Statements provide a sequence of commands for the computer to perform
5. Instructions are executed in the order that it is written
6. Each line of the code changes something in the program that is run

example
```rust
// simple program that calculates the factorial of 20
x <- 1
FOR Counter <- 1 TO 20
  x = x * Counter
NEXT Counter
```
### Object Oriented Programming


Objects: 
Attributes: 
Methods: The procedures and functions in a class that implement behaviors that act on properties 
Classes: 
Properties: the data items (attributes), the data types (characteristics) that are defined in a class
Instance: An occurrence of an object based on a class
Inheritance: The capability of defining a new class of objects that has all the attributes and methods from a parent class
Polymorphism: Allows the same method to take on different behaviors depending on which class is instantiated, thus allowing derived classes to have redefined methods
Aggregation: 
Encapsulation: Putting properties (data) and methods inside a class as a single unit to ensure sensitive data is hidden from users by hiding values of a structured data object inside a class
Getter: Method that is used to return the value of a property
Setter: Method that is used to update the value of a property

example
```java
public class Vehicle{
  private speed;
  public Vehicle(){
    speed = 0
  }
}
```

#### Structure of a class
1. Attributes with their datatypes 
2. Methods, which are functions and subroutines that act upon attributes
3. Getters and setters, which are methods that get (return) or set (update) the value of attributes respectively
4. A Constructor, that is used to create instance of the class called objects

#### Difference between class and object
1. Classes are defined but objects are initialized
2. Defining a class requires no memory allocation, but an object requires memory to be allocated
3. Classes can be defined only once, while objects can be created multiple times from that class
4. A class is a blueprint from which objects are created (Object is an instance of the class)
5. A class can use inheritance, and object cannot
6. Since classes are not stored on memory, they cannot be manipulated, unlike objects
### Declarative Programming
1. Declarative programming instructs a program on what needs to be done, not how it needs to be done
   - Do do this it uses facts and rules
   - Queries are used to satisfy goals
2. It can be logical or functional
   - **Logical** : Stats a program as a set of logical relations
   - **Functional** : Constructed by applying functions to arguments which uses a mathematical style

example
```rust
male(john).
female(ethel).
parent(john, ethel).
```

## File processing 
### Opening and closing files
### Reading and writing to a file
### File Operations
1. Serial Files
2. Sequential Files
3. Random Files
- Contain a collection of data
- Think of a *file pointer* that can be moved to any location

```rust
// RANDOM file mode used
OPENFILE <file identifier> FOR RANDOM

// address needs to be an integer
// file pointer is moved to this address
SEEK <file>, <address>

// GETRECORD is used to read record that is pointed to by the pointer
// Variable to store is normally of a record data type
GETRECORD <file>, <variable to store>

// data in variable os inserted into the record at the file pointer
PUTRECORD <file>, <variable>


// CLOSE THE GOD DAMN FILE
CLOSEFILE <file>
```


## Exception handling
> [!important] Exception Handling
> ***Exception Handling*** : Process of responding to an unexpected event when the program is running so it doesn't halt unexpectedly
> 

Reasons:
1. Programming errors
2. User errors
3. Hardware failures
4. Runtime error

```dataviewjs
const file = dv.current();
const checkboxes = file.file.tasks;
const totalCheckboxes = checkboxes.length;
const completedCheckboxes = checkboxes.filter(t => t.completed).length;

const completionPercentage = totalCheckboxes > 0 
    ? ((completedCheckboxes / totalCheckboxes) * 100).toFixed(2) 
    : "0.00";

console.log(totalCheckboxes, completedCheckboxes, completionPercentage);

try {
    await app.fileManager.processFrontMatter(
        dv.app.vault.getAbstractFileByPath(file.file.path), 
        (frontmatter) => {
            frontmatter["completion"] = completionPercentage;
        }
    );
    console.log("✅ Frontmatter updated successfully!");
} catch (error) {
    console.log(`❌ Error updating frontmatter: ${error}`);
}
```

