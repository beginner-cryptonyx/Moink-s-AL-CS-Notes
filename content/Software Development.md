---
subject:
  - "[[Computer Science]]"
grade:
  - "[[AS Level]]"
related:
creation-date: 2024-12-09
up:
  - "[[Computer Science]]"
tags:
  - ComputerScience/Software-Development
importance: 12
completion: "100.00"
modified:
  - 2025-04-18
  - 2025-04-16
  - 2025-04-03
---

> [!grey]- Syllabus
> ## 12.1 Program Development Life Cycle
> 
> - [x] Understand the purpose of a development life cycle
> - [x] Understand the need for different development life cycles:
>   - [x] Waterfall
>   - [x] Iterative
>   - [x] Rapid Application Development (RAD)
> - [x] Describe principles, benefits, and drawbacks of each life cycle
> - [x] Understand the stages of development:
>   - [x] Analysis
>   - [x] Design
>   - [x] Coding
>   - [x] Testing
>   - [x] Maintenance
> 
> ## 12.2 Program Design
> 
> - [x] Use structure charts to decompose a problem
> - [x] Express parameters between modules/functions
> - [x] Describe the purpose of a structure chart
> - [x] Construct a structure chart from a problem
> - [x] Derive pseudocode from a structure chart
> - [x] Understand the purpose of state-transition diagrams
> 
> ## 12.3 Program Testing and Maintenance
> 
> - [x] Understand how to expose and avoid faults in programs
> - [x] Identify and correct:
>   - [x] Syntax errors
>   - [x] Logic errors
>   - [x] Run-time errors
> - [x] Understand testing methods:
>   - [x] Dry run
>   - [x] Walkthrough
>   - [x] White-box
>   - [x] Black-box
>   - [x] Integration
>   - [x] Alpha
>   - [x] Beta
>   - [x] Acceptance
>   - [x] Stub testing
> - [x] Understand test strategy and test plan contents
> - [x] Choose appropriate test data:
>   - [x] Normal
>   - [x] Abnormal
>   - [x] Extreme/Boundary
> - [x] Understand need for system maintenance:
>   - [x] Perfective
>   - [x] Adaptive
>   - [x] Corrective
> - [x] Analyse and amend existing programs to enhance functionality

## Purpose of a development life-cycle
- Develop Successful Programs
- Makes program easier to plan and manage
## Stages of Program Development lifecycle
### Analysis
1. Problem clearly defined
2. Identify what to work on
   This is called a **Requirement Specification**
### Design
1. Requirement specification from the analysis stage will be planned properly
2. Tasks Determined
3. User interface Made
4. Identifier table produced
5. Data structures and Programming language is decided
#### Structure Charts
1. Modelling Tool
2. Decompose Problem into smaller parts (modules)
3. Models relationships of different modules
   - Shows Hierarchy
   - Shows Structure of modules
   - Connection between modules
4. Determine if module is function or procedure 

> [!important|float-right-medium] Symbols
> <div>&nbsp</div>
> 
> ![[Software Development 2024-12-10 19.13.40.excalidraw|center|350]]

##### Symbols:
1. Curved Arrows -> Iteration
2. Box -> Module
3. Diamond -> Decision
#### State Transition Diagram
#### [[Pseudocode]]
### Coding
### Testing
Reasons for testing:
1. Ensures functionality
2. Detects errors easily
3. Improves quality of program
4. Mitigates future risk
#### ![[Preventing Errors]]
#### [[Types of Errors]]
#### Types of Testing
![[Types of Testing]]

#### Test Strategy
A test strategy is a high-level document that outlines the overall approach to testing. It is usually created in the analysis phase and provides a clear plan on how testing will be performed to meet the requirements of the system.

Purpose:
1. Overview of testing -> Approaches and objectives
2. Testing methods
3. Resources Identified -> hardware/software; team members

Contents:
1. Test objectives
2. Test Types
3. Test tools
4. Test Schedule
5. Roles and Responsibilities
6. Defect Management
 
#### Test Plan
A test plan is a more detailed and specific document compared to the test strategy. It breaks down the testing process and lists the individual tests to be carried out.

Purpose:
1. Detailed framework of tests
   - How each test will be conducted
   - Which modules will be tested
   - What test data will be used

2. Tracking
   - Document test results
   - Document issues

#### [[Types of test data]]
### Maintenance
#### Purpose of maintenance
#### Types of maintenance

> [!error] Maintenance
> **Corrective** :: Changes to correct a problem in the program
> **Adaptive** :: Changes due to change in specification, legislation or technology

##### Perfective
1. Accommodates legislative changes or user requirement changes
2. necessary to adapt to changes so that the system continues to work effectively
##### Adaptive
1. Change in client Requirements
2. Availability of new technology 
3. Change in relevant legislation 
##### Corrective 
1. Bugs and errors in program


## Types of Program life cycle
### 1. [[Waterfall Model]]
### 2. [[Iterative Model]]
### 3. [[Rapid Application Development]]


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