---
subject:
  - "[[Computer Science]]"
grade:
  - "[[A Level]]"
related:
  - "[[Python]]"
  - "[[Pseudocode]]"
  - "[[03. Efforts/02. Areas/Programming|Programming]]"
  - "[[Programming (A levels)]]"
creation-date: 2025-09-04
up:
  - "[[Computer Science]]"
tags:
  - programming
  - DSA
aliases:
modified:
  - 2025-09-13
  - 2025-09-09
  - 2025-09-06
  - 2025-09-05
  - 2025-09-04
completion: "36.11"
importance: 19
---


> [!grey] Syllabus
> # 19 Algorithms
> 
> ## 19.1 Searching
> - [x] Understand linear and binary searching methods  
>   - [x] Write an algorithm for linear search  
>   - [x] Write an algorithm for binary search  
>   - [x] State conditions for binary search  
>   - [x] Explain how performance varies with dataset size  
> 
> ## 19.2 Sorting
> - [x] Understand insertion sort and bubble sort  
>   - [x] Write an algorithm for insertion sort  
>   - [x] Write an algorithm for bubble sort  
>   - [x] Explain performance based on initial data order & size  
> 
> ## 19.3 Abstract Data Types (ADTs)
> - [ ] Understand and use ADTs  
>   - [ ] Write algorithms to **find** an item in:  
>     - [ ] linked list  
>     - [ ] binary tree  
>   - [ ] Write algorithms to **insert** into:  
>     - [ ] stack  
>     - [ ] queue  
>     - [ ] linked list  
>     - [ ] binary tree  
>   - [ ] Write algorithms to **delete** from:  
>     - [ ] stack  
>     - [ ] queue  
>     - [ ] linked list  
>   - [ ] Understand graphs as ADTs  
>     - [ ] Key features of graphs  
>     - [ ] Justify their use in situations  
> 
> ## 19.4 Implementing ADTs
> - [ ] Show how ADTs can be implemented from other ADTs  
>   - [ ] Stack, queue, linked list, dictionary, binary tree  
> 
> ## 19.5 Algorithm Analysis
> - [ ] Compare different algorithms using criteria  
>   - [ ] Time complexity (Big O)  
>   - [ ] Space complexity (Big O)  
> 
> ---
> 
> # 19.2 Recursion
> 
> ## 19.2.1 Understanding recursion
> - [x] State essential features of recursion  
> - [ ] Explain recursion in a programming language  
> - [x] Write and trace recursive algorithms  
> - [x] Recognize when recursion is beneficial  
> 
> ## 19.2.2 Compiler and recursion
> - [ ] Explain what a compiler does with recursive code  
> - [x] Understand use of stacks & unwinding  
> 
> ---

# Algorithms
## Searching
### Binary Search
![[Binary Search]]
### Linear Search
![[Linear Search]]

### Performance
- Linear search has O(n) time complexity
- Binary search has O(log n) time complexity
- Time to search increases linearly in relation to the number of items in the list for linear search, and logarithmically for a binary search
- Time to search increases less rapidly for a binary search compared to linear search

## Sorting
### Bubble sort
#### Pseudocode Implementation
```rust
PROCEDURE SortArrays()
	DECLARE TempInt, i, Boundary : INTEGER
  DECLARE NoSwaps : BOOLEAN

  Boundary <- 100 // last element of array

  REPEAT
    NoSwaps <- FALSE
    FOR i <- 1 TO Boundary
      IF Array[i] > Array[i+1] THEN
        TempInt <- Array[i]
        Array[i] <- Array[i+1]
        Array[i+1] <- TempInt
        NoSwaps <- FALSE
      ENDIF
    NEXT i
    Boundary <- Boundary - 1 //because elements will be sorted at the end, no need to re iterate thru them all
  UNTIL NoSwaps = TRUE
ENDPROCEDURE
```
### Insertion sort

#### Method
1. First element is in the sorted list, this sorted list is presumed to be to the left of a pointer, which initially points to the second element of the list
2. Store the value to be sorted, pointed to by the current index (pointer) into a temporary variable
3. Compare this element to each element in the sorted list (all elements to the left of the current index)
4. The elements that are greater than the temporary variable get swapped with it one my one, moving from right to left until the value is in the correct position
5. This is done for every element after the second element until the end
#### Pseudocode Implementation
```rust
end <- 100 //index of the last element in the array
start <- 1

FOR index <- start + 1 TO end // algorithm starts from the second element only

  temp <- array[index] // during shifting array[index] is overwritten, so we need to remember this value
  counter <- index

  // this part of the code shifts elements forward so that there is place to insert the target element
  WHILE counter > 1 AND array[counter - 1] > temp 
    array[counter] <- array[counter - 1]
    counter <- counter - 1
  ENDWHILE

  array[counter] <- temp //Here we insert the target element

NEXT index
```

#### Python Implementation
```python
def insertion_sort(array:list[int]):
  for i in range(1, len(array)):
    temp = array[i]
    counter = i
    while counter > 0 and array[counter - 1] > temp:
      array[counter] = array[counter - 1]
      counter = counter - 1
    array[counter] = temp
```
### Performance
Factors affecting performance of a sorting algorithm
1. Initial Order of data
2. Number of items to be sorted
3. Efficiency of the sorting algorithm
## Abstract Data types
### Linked List
#### Find
#### Insert
#### Delete
### Binary Tree
#### Find
#### Insert
#### Delete
### Stack
1. LIFO data structure
2. Can vary in size
3. Data is popped and pushed out of and into the stack at the same end
4. Stack has only one movable pointer

Stack can be used for
1. Recursion
2. Implementation of Linked list
3. Procedure calls
4. Interrupt handling, where contents of registers are stored on stack
#### Insert
#### Delete
### Queue
1. FIFO data structure
2. Can vary in size
3. Queue has 2 movable pointers
4. Unlike stack, queue has both ends accessible so items can be enqueued and dequeued at opposite ends
#### Insert

### Graphs
Features of graphs
Use cases
## Algorithmic analysis (Big O Notation)

### O(n)
- Linear search
- Time taken increases linearly in relation to the number of items 

### O(log n)
- Time complexity that uses logarithmic time
- Time taken goes up linearly as the number or items rises exponentially
- O(log n) is the worst case scenario for a binary search algorithm


# Recursion
![[Recursion]]

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

