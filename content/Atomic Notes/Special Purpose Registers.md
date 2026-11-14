---
subject:
  - "[[Computer Science]]"
grade:
  - "[[AS Level]]"
related: 
creation-date: 2025-05-05
up: 
tags: 
aliases: 
modified:
  - 2025-05-05
---
- Special purpose registers hold status of program
- Specialized for specific use
- Can be used by certain instructions

1. **Program Counter (PC) ** :: Store the memory address of the next instruction to be fetched
2. **Memory Data Register (MDR)** :: (also known as memory buffer register) Stores data which has just been read from memory
3. **Memory Address Register (MAR)** :: Stores the memory address currently being read from or written to (Direct addressing)
4. **Accumulator (ACC)** :: temporary register used to store value from result of ALU's arithmetic and logical calculations
5. **Index Register (IX)** :: Stores a value that is added to an address to give another address (When performing index addressing)
6. **Current Instruction Register (CIR)** :: Stores current instruction being decoded and executed
7. **Status Register (SR)** :: contains bits that are either set or cleared which can be referenced individually, these bits are used as flags derived from results of logical/arithmetic operations