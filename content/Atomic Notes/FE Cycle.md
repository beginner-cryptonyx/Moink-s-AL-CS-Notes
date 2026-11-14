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

>[!none|float-right-medium]
>```mermaid
>Flowchart TB
>  START ((START))
>  START --> a {{instructions to execute}}
>  a -->|yes| b[Fetch Next Instruction]
>  b --> c[Decode Instruction]
>  c --> d[Decode Instruction]
>  d --> e{Interrupts?}
>  e -->|yes| f[Control given to interrupt-handling program]
>  e -->|no| a
>  f --> a
>```

```js
MAR <- [PC] //contents of pc copied to MAR
PC <- [PC] + 1 // PC is incremented by 1
MDR <- [[MAR]] // data stored at the address shown in MAR is copied into MDR
CIR <- [MDR] // contents of MDR copied to CIR
```

### Roles of registers in FE cycle
1. PC holds address of next instruction to be executed, its contents are incremented at the end of each FE cycle
2. MAR holds the address to fetch the data from, it is provided by the PC
3. MDR holds the data at the address in the MAR
4. Instruction from the MDR is sent to CIR to decode and execute

 
### Fetch stage:
1. The address of program counter is transferred to MAR
2. Simultaneous clock cycle
   - Instruction held inside the address pointed to by the MAR is fetched into MDR
3. MDR content shifted to the CIR
4. PC will be incremented by one
   - % unless current instruction is a `jump` instruction, meaning PC address will be updated according to the jump