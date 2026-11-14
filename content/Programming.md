---
subject:
  - "[[Computer Science]]"
grade:
  - "[[AS Level]]"
related:
creation-date: 2025-04-23
up:
  - "[[Computer Science]]"
tags:
aliases:
modified:
  - 2025-04-23
completion: "100.00"
importance: 11
---

> [!grey]- Syllabus
> ## 11.1 Programming Basics
> 
> - [x] Implement and write pseudocode from:
>   - [x] Program flowchart
>   - [x] Structured English
> - [x] Write pseudocode for:
>   - [x] Declaration and initialisation of constants
>   - [x] Declaration of variables
>   - [x] Assignment of values to variables
>   - [x] Expressions with arithmetic and logical operators
>   - [x] Input from keyboard
>   - [x] Output to console
> - [x] Use built-in functions and library routines
>   - [x] Use string manipulation functions (given when needed)
> 
> ## 11.2 Constructs
> 
> - [x] Use pseudocode to write:
>   - [x] `IF` statements (including `ELSE` and nested `IF`)
>   - [x] `CASE` structures
>   - [x] Count-controlled loops
>   - [x] Post-condition loops
>   - [x] Pre-condition loops
> - [x] Justify appropriate loop structure for a given problem
> 
> ## 11.3 Structured Programming
> 
> - [x] Define and use procedures
>   - [x] Explain when to use a procedure in an algorithm
>   - [x] Use parameters in procedures
>     - [x] No parameters / one or more parameters
>     - [x] Parameters passed by reference or by value
> - [x] Define and use functions
>   - [x] Explain when to use a function in an algorithm
>   - [x] Use return values in expressions
> - [x] Use appropriate terminology:
>   - [x] Procedure/function header
>   - [x] Procedure/function interface
>   - [x] Parameter
>   - [x] Argument
>   - [x] Return value
> - [x] Write efficient pseudocode


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