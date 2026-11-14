---
subject:
  - "[[Computer Science]]"
grade:
  - "[[AS Level]]"
related: 
creation-date: 2024-12-13
up:
  - "[[Software Development]]"
aliases:
  - Alpha Testing
  - Beta Testing
  - Dry Run
  - White Box Testing
  - Black Box Testing
---

#### Dry run/Walkthrough
##### Information Required:
1. The program code
2. Test data and expected results - so all paths can be tested

##### Identifying Errors
1. Trace table made
2. Going through one line at a time
3. Trace table records variables as they change
4. If unexpected value occurs, error found
5. If there is a fault in the logic [[Logical Error]] found

#### White box
1. Tests logic of all possible paths through the module
2. Each procedure tested thoroughly 
3. Tester can view the code
4. Tests every path 
5. Test Each line of code

#### Black Box
1. Code is unknown to tester
2. Testing done by **non programmers**
3. Testers look into program specification to create test data 
   - Can be [[Types of test data|Normal Test Data]], [[Types of test data|Abnormal Test Data]], or [[Types of test data|Extreme/Boundary Test data]]
1. Tester runs program and compares expected output with actual output
2. If errors / unexpected behaviour occur, it is reported back to the developers
3. Done to check of program meets the requirements
#### Integration
- Modules have been already tested individually
- All individual modules are then combined to test whole program
#### Alpha Testing
- Testing done by **development team**
- Check if program is working as intended
- Done at the end

#### Beta Testing
- Testing carried out by small group of chosen individuals
- Check if program is working as intended
- These users will provide feedback/suggestions to developer team
- Done before release 

#### Acceptance
- Before release to client
- Client will check if product meets specification
- Check if everything is working as expected

#### Stub
1. Used when program either contains modules **with errors** or **incomplete modules**
2. Dysfunctional modules are replaced by **dummy modules**
3. Dummy modules **contain output statement** to acknowledge that a call to the module was made