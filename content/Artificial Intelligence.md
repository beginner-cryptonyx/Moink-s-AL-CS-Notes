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
  - 2026-04-10
  - 2026-01-13
  - 2025-12-08
  - 2025-12-04
  - 2025-11-29
  - 2025-11-28
  - 2025-09-29
  - 2025-09-28
  - 2025-09-24
  - 2025-09-21
  - 2025-09-20
completion: "71.43"
importance: 18
---


> [!grey] Syllabus
> # 18 Artificial Intelligence (AI)
> 
> ## 18.1 Artificial Intelligence (AI)
> 
> ### Graphs in AI
> - [ ] Show understanding of how graphs can be used to aid AI  
>   - [x] Purpose and structure of a graph  
>   - [ ] Use of A* algorithm for graph search  
>   - [ ] Use of Dijkstra’s algorithm for graph search  
>   - [ ] Limit: Candidates do not need to write algorithms to set up, access, or perform graph searches  
> 
> ### Neural Networks
> - [x] Show understanding of how artificial neural networks have helped with machine learning  
> 
> ### Machine Learning Types
> - [x] Understand categories of machine learning:  
>   - [x] Supervised learning  
>   - [x] Unsupervised learning  
> 
> ### Deep Learning & Reinforcement Learning
> - [x] Show understanding of Deep Learning  
> - [x] Show understanding of Reinforcement Learning  
> - [x] Know reasons for using these techniques  
> 
> ### Back Propagation
> - [x] Show understanding of back propagation of errors  
> - [x] Know how back propagation is used for neural networks

# Graphs in AI

## Structure and purpose of graphs
- ! Graph is used in AI to record the relationships between entities, like destinations and people
  - Done via using vertices/nodes and edges
  - Edges connect nodes, and they represent possible paths between them
  - A path is a list of nodes connected by edges between 2 given nodes
- Nodes and edges are weighted, and the weighage can be applied and be applied and used in the context of the application
- A cycle is a list of nodes that return to the same node
- For example, to represent places on a map and distances between them, in order to find the shortest route

## A\* algorithm and Dijkstra's algorithm
- ! Used to find the optimal/shortest route
  - Between 2 nodes in a graph
  - Based on a weighage like distance, cost or time



### A\* algorithm
- Tries to find a better path between points by using a heuristic function 
- The heuristic function gives priority to then nodes that are supposed to be better than the others/less costly than others
- Can work with negative weights

![[image-24.png]]
![[image-25.png]]


### Dijkstra's algorithm
- Dijkstra's algorithm explorers all paths possible
- Cannot work with negative weights
# Neural Networks

## What is an artificial neural network
1. Component of AI meant to simulate a biological brain
2. Key component to machine learning
3. ANN's have self learning capabilities that enable them to produce better results as more data is available
4. This allows them to solve problems that humans cannot solve
5. They have interconnected layers (input output hidden)
6. Weights are assigned between nodes
7. These weights can be adjusted during training for more accurate results
8. More accurate results produced from increase in the number of hidden layers
9. Output layer provides the results
   

## Importance and role of hidden layers
1. Enables deep learning to take place
2. Allows the AI model to solve more complex problems
3. Allows the AI model to learn, and make decisions on its own
4. To improve the accuracy of the result


# Machine Learning


## ANNs and Machine Learning
1. ANN replicate the way human brains work
2. Weights are assigned for each connection between nodes
3. Data is input into the input layer and is passed down into the system
	1. It is analyses in each subsequent, hidden layer
	2. Characteristics are extracted
4. Reinforcement training occurs (learning repeats), so that optimum outputs are achieved
5. Decisions are made without being specifically programmed
6. Deep learning net would have created complex feature detectors
7. Output layers provide the results
8. Back propagation of errors will be used to correct any errors that have been made


## Supervised Learning
- Uses labeled data -> known tasks with given outcomes
- Labelled data means that known outcomes are applied to specific inputs to help the AI predict future outcomes based on past data
- Requires initial human input and training
- improves performance in accomplishing similar tasks


## Unsupervised Learning
- Makes use of unlabeled data -> Large number of tasks with unknown outcomes
- The outcomes are not known
- The AI has to search and analyze data to discover hidden patterns, structures, and clusters within the data in order to predict the outcomes
- Does not require human intervention like human input and training
- It is able to discover similarities and differences in data
- improves performance in accomplishing similar tasks

---

# Deep Learning and Reinforcement learning
![[Deep Learning and Reinforcement Learning]]

# Back propagation
## Reason to implement back propagation
1. At the beginning, neural networks make incorrect predictions
2. Back propagation allows methods to measure error
3. Using the measured error, the weights are updated

## Working of back propagation
1. Forward pass
	- Feed is input through the network
	- Output is computed
	- The output is compared to the true answer (true label) using a **loss function** such as mean square error
2. Backward pass
	- The **gradient** of the loss with respect to each weight in the network is computed (involves the chain rule crap from math)
3. Updating weights


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