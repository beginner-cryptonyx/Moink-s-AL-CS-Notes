---
subject:
  - "[[Computer Science]]"
grade:
  - "[[A Level]]"
related:
creation-date: 2025-09-20
up:
  - "[[Computer Science]]"
tags:
aliases:
modified:
  - 2025-10-08
  - 2025-09-28
  - 2025-09-23
  - 2025-09-20
completion: "74.07"
importance: 16
---


> [!grey]- Syllabus
> # 16 System Software
> 
> ## 16.1 Purposes of an Operating System (OS)
> 
> - [ ] Show understanding of how an OS can maximise the use of resources  
> - [x] Describe the ways in which the user interface hides the complexities of the hardware from the user  
> - [ ] Show understanding of process management  
>   - [x] Process states: running, ready, blocked  
>   - [x] Concept of multi-tasking and a process  
>   - [x] Scheduling
>     - [x] round robin
>     - [x] shortest job first
>     - [x] first come first served
>     - [x] shortest remaining time  
>   - [x] Kernel as interrupt handler  
>   - [ ] Interrupt handling for low-level scheduling  
> - [x] Show understanding of virtual memory, paging, and segmentation for memory management  
>   - [x] Concepts of paging, virtual memory, segmentation  
>   - [x] Difference between paging and segmentation  
>   - [x] How pages can be replaced  
>   - [x] How disk thrashing can occur  
> 
> ---
> 
> ## 16.2 Translation Software
> 
> - [ ] Show understanding of how an interpreter can execute programs without producing a translated version  
> - [ ] Show understanding of the various stages in the compilation of a program  
>   - [x] Lexical analysis  
>   - [x] Syntax analysis  
>   - [ ] Code generation  
>   - [ ] Optimisation  
> - [x] Show understanding of how the grammar of a language can be expressed using:  
>   - [x] Syntax diagrams  
>   - [x] Backus-Naur Form (BNF) notation  
> - [x] Show understanding of how Reverse Polish Notation (RPN) can be used to carry out the evaluation of expressions  

# Operating system
## Maximization of resource usage
## User Interface
- Hides complexities of the computer hardware and operating system from the user
- It provides appropriate access systems for users with different needs
- Complex commands involving memory locations, busses and computer hardware are avoided
  - Like using icons for navigation


## Process Management
### Process states
1. Running state
2. Ready state
3. Blocked state

Conditions for program to go from running state to ready state
1. When time slice of running program expires (such as in round robbin)
   - Or there is a process with higher priority in the ready queue, the running process is pre-empted
2. When interrupt arrives at CPU, the programming running gets pre-empted
### Multitasking
> [!tip] Multitasking
> **Multitasking** -> Running multiple processes concurrently, allowing the computer to carry out more than one process at a time

- Benefits process management by allowing more tasks to be completed that would be the case if they had to run tasks one after another

Implementation of multitasking
1. Processor time, common hardware, and resources are shared between tasks
2. Scheduling is used to decide on the processes to be carried out to ensure multitasking operates correctly, and efficiently, without clashes
3. One task of a higher priority can interrupt another task that is currently running

### Scheduling
- Required to ensure that all processes are executed in a timely manner
- It enables multitasking, multiprogramming, and multiprocessing
- Which minimizes CPU idle time
  - To ensure all processes are executed efficiently
- It ensures that no process is starved of resources by providing them all with fair access to resources
- It ensure that processes are completed in order of priority, meaning highest priority jobs are completed first
#### Round Robin
Function:
1. Processes are queued as they arrive
2. It is a pre-emptive scheduling routine
3. A fixed time quantum (equal time size) is given to each process, meaning all processes are given the same priority
4. When a time slice ends, the status of the process is saved, so it can continue from where it left off, in its next time slice

Benefits:
- No issues with starvation of resources
- Reduces the average response time by limiting each process to a fixed amount of time
#### Shortest job first
Function:
1. Processes are queued as they arrive
2. The process with the shortest time to complete / burst time is selected first and executed
3. The process will continue until complete or put in waiting state once execution has begun, it is non pre-emptive
4. Scheduler will continue to choose shorter processes over longer processes if they continue to be added to the queue, this causes starvation for longer jobs

Benefits:
- Shorter jobs don't have to wait for longer jobs to complete before processing
  - This reduced the average overall waiting time for processes
- Increases throughput of processes
#### First come first served
- No complex logic, each process is queued as it is received and executed one by one

Benefits
- No complex logic
- Starvation doesn't occur, because all processes will eventually get a chance to run
#### Shortest remaining time
Function:
1. The processes are queued as they arrive
2. Processes with the shortest burst time are executed first
3. It is a pre-emptive scheduling process -> which means when a process with a shorter burst time arrives, the existing process is replaced by the shorter process
4. The scheduler will continue to choose shorter processes over longer processes if they continue to be added to the queue, this can cause starvation for longer jobs

Benefits:
- Processes with a short burst time are processes very quickly
- Waiting time is minimized

### Kernel interrupt handling
1. The kernel receives a signal when an interrupt is generated
2. The kernel checks the priority and reviews the status and priority of current interrupts
3. System enters kernel mode if the type of interrupt is of higher priority than the current process 
4. The kernel consults the interrupt dispatch table
   - And it saves the state of the interrupted processes via storing the contents of the registers on the kernel stack
5. The kernel restores the process state, like the contents of the registers once the interrupt is serviced

### Low level interrupt handling

## Memory

### Virtual memory
1. Virtual memory is used when RAM is running low, the secondary storage is used to extend the memory
   - Like when computer is running multiple processes at once
2. Virtual memory may be used for efficient use of RAM
   - Like when data and programs are not needed immediately
   - The data can be swapped between RAM and virtual memory as necessary
3. Virtual memory is created temporarily


### Paging memory
- Paging allows Memory to be divided into fixed sized blocks
- Operating system divides the memory into variable sized blocks
- The compiler is responsible for calculating the segment size
- Access times for paging is faster than for segmentation

### Segmentation for memory management
1. In segmented memory, the virtual address space is broken down into *varying sized blocks* called segments
2. Each segment has a name and a size
3. During execution segments from virtual memory are loaded into physical memory
4. The address is specified by the user
   - It contains segment name and offset value
5. Segments are numbered
   - This number is used as an index in the segment map
6. The offset value determines the size of the segment
7. A segment map table maps virtual addresses to physical addresses

### Disk thrashing
- It is a problem that may occur when virtual memory is being used and frequent transfers between main memory and secondary take place
- As the main memory fills up, more and more pages need to be swapped in and out of virtual memory
- This swapping leads to a very high rate of hard disk access, which leads to excessive disk head movements
- Moving hard disk head takes a relatively long time
- Eventually, more time is spent swapping pages than processing data thrash point, which can cause the program to freeze or not run
### Replacing pages
# Translation Software
## Interpreter
Execution of programs
1. Interpreter translates the source code one line at a time
2. If the line is syntax error free, it is executed
3. It is not stored as executable format
4. If an error is found, the program halts with an error message
5. Each line must be translated every time it is run, including lines running multiple times, like a loop
6. Interpretation is repeated everytime the program is ran
## Stages of compilation
### Lexical analysis
1. First stage of compilation
2. White space and comments are removed
3. It takes modified source code and breaks it's sequence of characters' down into a series of tokens
4. Each token is categorized and assigned types
5. Identifiers are stored in a symbol table
6. If the lexical analysis finds invalid tokens, it generates an error
7. Acceptable data from the lexical analyser passes to the syntax analyser
### Syntax analysis
- ! Basically uses parsing algorithms to interpret meaning of sequence of tokens that it got from lexical analysis

1. Second stage of compilation, after lexical analysis
2. It takes input from the lexical analyser in the form of token streams
3. Checks if tokens conform with rules of language by parsing the source code against the rules of the language to detect any errors in the code
4. The output from this phase is a parse tree
5. Syntax errors are reported


### Code generation
- Converts intermediate representation of source code into an executable form
### Optimization
- Minimizes programs execution time and memory requirement
## Syntax Diagrams
## BNF notation
# RPN notation
## Importance of RPN
- Reverse Polish Notation provides and unambigious method of representing an expression
- It reads from left to right
- Without the use of brackets
- There is no need for rules of precedence (BODMAS)

## Data Structures to implement RPN
### Stack
- The most appropriate structure for using RPN is stack because the operands are popped in the reverse order to how they were pushed
![[image-22.png]]
#### Evaluation of RPN statements using a stack
1. RPN expression is evaluated from left to right
2. Push each element of the RPN expression onto the stack in order until an operator is reached
3. After operator is reached, last two elements are popped, from the stack and the operator is applied
4. Push the result into the stack
5. This process is repeated until there is only one element left which means the RPN expression is evaluated
### Binary Tree
- Binary tree allows both infix and post fix to be evaluated


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

