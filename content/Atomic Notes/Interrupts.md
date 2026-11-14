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
> [!error] Interrupt
> **Interrupt** :: Signal sent from a device for from software to the processor, seeking attention from the processor, causing it to temporarily stop what it is doing, and service the interrupt

### Causes of interrupts
Software Interrupts:
1. Runtime error like division by 0
2. Attempt to access invalid memory location
3. Array index out of bounds
4. Stack overflow


### Handling interrupts

1. Priority of interrupt is checked
2. If priority is lower than current process , FE cycle is continues
3. If priority is higher:
   4. State of registers stored on stack
   5. Type of interrupt is identified
   6. Appropriate Interrupt Service Routine (ISR) is called to handle interrupt
   7. After ISR is done, check for any other high priority interrupt and handle them
   8. After all high priority interrupts are handled data from stack is restored