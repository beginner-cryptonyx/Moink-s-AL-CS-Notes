---
subject:
  - "[[Computer Science]]"
grade:
  - "[[AS Level]]"
related:
creation-date: 2024-12-15
up:
  - "[[Computer Science]]"
importance: 9
completion: "100.00"
---

> [!grey] Syllabus
> ## 9.1 Computational Thinking Skills
> 
> - [x] Understand the concept of abstraction
>   - [x] Explain the need for abstraction
>   - [x] Describe the benefits of abstraction
>   - [x] Describe the purpose of abstraction
>   - [x] Create an abstract model with only essential details
> - [x] Describe and use decomposition
>   - [x] Break down problems into sub-problems
>   - [x] Understand decomposition leads to program modules (procedures/functions)
> 
> ## 9.2 Algorithms
> 
> - [x] Understand that an algorithm is a solution expressed in defined steps
> - [x] Use suitable identifier names
> - [x] Create an identifier table to represent problem data
> - [x] Write pseudocode for:
>   - [x] Input
>   - [x] Process
>   - [x] Output
> - [x] Use three basic constructs in pseudocode:
>   - [x] Sequence
>   - [x] Selection
>   - [x] Iteration (repetition)
> - [x] Document an algorithm using:
>   - [x] Structured English
>   - [x] Flowchart
>   - [x] Pseudocode
> - [x] Write pseudocode from:
>   - [x] Structured English
>   - [x] Flowchart
> - [x] Draw a flowchart from:
>   - [x] Structured English
>   - [x] Pseudocode
> - [x] Use stepwise refinement to express an algorithm at a programmable level
> - [x] Use logic statements within an algorithm



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