---
related: "[[03. Efforts/02. Areas/Programming|Programming]]"
creation-date: 2025-09-05
tags:
aliases:
modified:
  - 2025-09-05
type: Atomic Note
up: "[[Algorithms (A level)]]"
cssclasses:
---

- A function which **calls itself**
- This function has a base-case, which is the terminating solution, the base case does not call the function, but returns a value
  - Unwinding occurs once the base case is reached
- The function will also have a general case, this is where the recursive call will be made
  - The general case changes the functions state and moves towards the base case
## Concepts of recursion
### Features
### Benefits
## Compilers and recursive code
### Use of stack
- Stack is a **LIFO** data structure
- Each recursive call is pushed onto the stack
  - The call is popped as the function ends
- A stack enables unwinding
  - Because the required order is maintained
### Winding and Unwinding 