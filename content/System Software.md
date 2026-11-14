---
subject:
  - "[[Computer Science]]"
grade:
  - "[[AS Level]]"
related:
creation-date: 2024-12-30
up:
  - "[[Computer Science]]"
tags:
importance: 5
completion: "100.00"
modified:
  - 2025-04-22
  - 2025-04-21
  - 2025-04-20
  - 2025-04-18
  - 2025-04-10
  - 2025-04-12
marks-lost: 31
---

> [!grey]- Syllabus  
>  
> ## 🖥️ **5.1 Operating Systems**  
> ### 📌 General Concepts  
> - [x] Explain **why an Operating System is required**  
>  
> ### ⚙️ OS Management Tasks  
> - [x] **Memory Management**  
> - [x] **File Management**  
> - [x] **Security Management**  
> - [x] **Hardware/Peripheral Management**  
> - [x] **Process Management**  
>  
> ### 🛠️ Utility Software (built-in)  
> - [x] Disk Formatter  
> - [x] Virus Checker  
> - [x] Defragmentation Software  
> - [x] Disk Contents Analysis / Repair Tools  
> - [x] File Compression Software  
> - [x] Backup Software  
>  
> ### 📚 Program Libraries  
> - [x] Understand the **use of library code** in development  
> - [x] Benefits of using library files (e.g. **DLL files**)  
>  
> ---  
>  
> ## 🧾 **5.2 Language Translators**  
> ### 🔁 Types of Translators  
> - [x] Assembler for **assembly language**  
> - [x] Compiler for **high-level language**  
> - [x] Interpreter for **execution + translation** of high-level code  
>  
> ### 🔍 Compiler vs Interpreter  
> - [x] Know **benefits and drawbacks** of each  
> - [x] Justify the use of each in a given scenario  
>  
> ### ☕ Mixed Mode Execution  
> - [x] Awareness of **partially compiled/interpreted** languages (e.g. Java)  
>  
> ### 🧰 IDE Features  
> #### Coding  
> - [x] Context-sensitive prompts  
>  
> #### Error Detection  
> - [x] Dynamic syntax checking  
>  
> #### Code Presentation  
> - [x] Pretty-print  
> - [x] Expand/collapse code blocks  
>  
> #### Debugging Tools  
> - [x] Single Stepping  
> - [x] Breakpoints  
> - [x] Report/Output window  
>  
> ---  
>  
> **Cambridge International AS & A Level Computer Science 9618 (2024–2025)** ✅  

# Operating Systems

> [!error] OS: Operating system
> **Operating system** :: A software platform that provides facilities for programs to be run

## Need for operating system
1. **Provide User interface**
   - Allow user to interact with software and hardware
   - **GUI** :: Graphical user interface
   - **CLI** :: Command line interface 
2. **Provide a platform for software to run on**
   - Called the *program-hardware* interface
1. **Hides complexities of hardware from user**
2. **Resource Management**
   - Scheduling of processes
   - Resolution of resource conflicts

## Key management tasks carried out by OS

> [!important] Process
> **Process** :: A [[Program]] that has begun execution

### Memory management
1. Controls movement of data form processor and RAM
2. Allocates Memory to Processes
3. **Dynamic RAM allocation**
   - RAM is assigned into blocks
   - This RAM is allocated to programs
4. Reclaims unused blocks of RAM 
5. Prevents processes from accessing same area of RAM simultaneously
6. Moves data from secondary storage when needed
7. Manages **paging** and **virtual memory**
8. Stores data from all currently running program concurrently in RAM
9. Stops data from overwriting each other in RAM
10. Decides which processes need to be in the main memory
11. Makes efficient use of memory

#### Memory Optimization
1. Determines how memory is allocated and deallocated
2. Keeps track of where all the memory is stored
3. Swaps data from HDD and SSD

#### Memory Organization
- Determines how much memory is allocated to an application

1. Contiguous Allocation: All memory available for a single application (Embedded systems use this)
2. Partitioned Allocation: Memory split into contiguous partitions with varying sizes that are allocated to an application
3. Paged Memory: Memory split into contiguous partitions with constant sizes. (Used by virtual memory systems)
4. Segmented memory: Memory blocks are not contiguous, each segment will be a logical grouping of data

#### Memory Protection
1. Ensures that 2 applications cannot use the same memory location at the same time
2. prevents Data loss

### File management
1. Allocates space to files
2. Maintains **directory structure**
3. Allows **file renaming** abilities
4. Implements **access rights**
5. Allows **file sharing**
6. Provision of file manipulation tools like 
   - `copy`
   - `paste`
   - `delete`
   - `close`
7. Specifies logical method of file storage like FAT or NTFS

### Security management
1. Creates accounts/passwords  
2. Provides [[Firewall]] or [[Anti-Malware]]  
3. Validates user and process authenticity
4. Ensures [[Data Privacy]]
5. Prevention of intrusion
6. Automatic Backups
7. Implements access rights
8. System restore ability provisioned

### Hardware management 
1. Receives data from input devices
2. Sends data to output devices
3. Operates and installs device drivers
4. Allows **communication** between peripherals and computers
5. Handles **[[Buffers]]** for data transfer
   - Ensures smooth data transfer
6. Manages [[Interrupts]]

### Process management
1. Manages **scheduling of processes**
   - Decides order of processes
2. Manages the resource needed by the processes
3. Enables processes to **share data**
4. **Prevents interference** between processes
5. Handles **process queues**
6. Allows **multitasking**
   - Allows one process to be paused while handling another process
   - Decides which process is to be run next
   - Ensures fair access
   - Switches between process to allow them to share the processor 
1. Handling priorities and [[Interrupts]]



## Utility Software provided with an OS
### Need for utility Software
1. Help **set-up/maintain/optimize** the computer
2. Makes memory and storage allocation more efficient
3. Checks system for faults

### Disk Formatter
Prepares disk for storing files:
1. Prepares disk for initial use
2. Delete all data from disc that has been used before 
3. Partitions Disk into logical drives
4. Generates a new file system
5. Sets up file allocation table
6. Checks disk for errors

### Virus Checker 
1. Scans for viruses [[Virus]]
2. Scans for malicious program code

### Defragmentation Software
#### Fragmentation of files
- Over time with usage of disk, files are created, modified and deleted
- This data is stored in non-contiguous (fragmented) sectors of the disk
- This occurs as OS uses the first free space available, even if it is not contiguous and rearranging every time is computationally expensive

- This slows down computer and reduces lifespan of [[HDD]]

#### Defragmentation
1. Moves and arranges blocks of files so each individual file is contiguous
2. Moves free space together


#### Impacts of defragmentation
1. Less file access times
   - Less time as less movement of disk head is required
2. Increased lifespan
   - Less mechanical wear and tear due to less movement


### Disk Repair Software
1. Check for errors on disk
   - Physical damage
2. Marks these bad sectors
3. Prevents files for occupying them
4. Tries to correct the bad sectors


### File Compression
1. Reduces file size
2. Saves storage and memory space
3. Reduces transmission time

### Backup Software
1. Establishes backup schedule
2. Creates copies of data
3. Allows retrieval of data in the case it is lost

## Program Libraries

> [!important] Program Library
> **Program Library** :: Pre-written, pre-tested, functions and subroutines, which are referenced/imported to be used in a [[Program]]  

### Using Program Libraries
1. Pre-written functions stored in program libraries in functions and routines
2. Program library should be imported
3. Functions and sub routines from library can be called  
### Benefits:
1. Pretested so more likely to work
2. Saves time as code does not need to be written in scratch
3. Can perform actions beyond the programmer's knowledge / experience, like more complex calculation
4. Improvements in library routine, program updates automatically 
### DLL

> [!important] DLL
> **DLL** :: A **DLL (Dynamic Link Library)** is a type of file used in Windows-based operating systems to provide shared functionality for multiple programs. It contains reusable code, data, and resources that applications can access dynamically at runtime.


#### Benefits of DLL
1. More memory efficient as DLL loaded only once when required
2. Smaller file size as [[Program]] doesn't contain all library routines
3. No maintenance of DLL is required by programmer as DLL is separate from [[Program]]
4. No need for recompilation when changes are made to DLL as it done independently of program

# Language Translators

## Translators
### Assembler Software
Translates [[Assembly Language]] into machine code
### Compiler
- Translates high level language into machine code
- Attempts to translate the whole source code
- Creates a separate error report at the end
- If translation successful, executable is created

#### Use cases
- Used after [[Software Development|development]] of [[Program]] is done
- Creates executable file 
- Used to repeatedly test same section of completed code

#### Working of compiler
1. Compiler starts execution
2. Line is read
3. Line is analyses
4. If error is found it is recorded
5. Else it is converted into intermediate code
6. Moves on to next line 
7. Steps 2 to 6 repeated
8. Once this is done for every line of code
   - If no errors found, intermediate code is converted into source code
   - If errors are there, they are listed and no object code is formed

#### Advantages
1. Multiple Errors can be [[Debugging|debugged]] simultaneously
2. Produces executable file 
3. Testing can be done multiple times without re-translation

##### Advantages of executable files
1. Program can be distributed without source code
2. Source code cannot be stolen
3. Users do not require the translator to run the program

#### Disadvantages
1. No changes can occur after completion
2. Program will not run whatsoever if there are errors present
3. Errors cannot be corrected in real time
4. One error may result in false errors being reported
5. Cannot test code if [[Program]] is unfinished
6. Cannot test individual sections of code

### Interpreter
- Translate high level language line by line
- Reads each line and then executes it
- Stops execution when error is encountered

#### Use cases
- Used while writing the program 
- Helps test/debug a **partially** complete program
- Errors can be corrected in realtime

#### Advantages
1. Easier to debug program
2. Because line-by-line translation is done so it stops when an error occurs
3. Errors reported one at a time
4. Thus error can be corrected in real time
5. Changed made by programmer can be seen in realtime
6. Partially complete program can be tested

### Mixed execution
- Partially compiled programs can be used on different platforms as they are interpreted when run
- Code is optimized for CPU as machine code is generated at runtime
- Source code does not need re-compiling, so more efficient to run

## Features of IDE
### Coding
1. Context Sensitive Prompts :: Displays prediction of code being entered; saves time
2. Dynamic Syntax Check :: Underlines and highlights statements that do not match rules of language
   

### Initial Error Detection
#### Dynamic Syntax Checks

### Presentation
#### Pretty Print
#### Collapsible Code Blocks

### Debugging
1. Single Stepping :: Executes one line of a program and then stops
2. Breakpoints :: Stops code execution at a set line
3. Report Window :: Outputs the contents of variables and data structures


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