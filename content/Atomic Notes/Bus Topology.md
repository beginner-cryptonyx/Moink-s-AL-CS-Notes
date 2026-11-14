---
subject:
  - "[[Computer Science]]"
grade:
  - "[[AS Level]]"
related: 
creation-date: 2025-01-09
up: "[[Network Topologies]]"
tags: 
aliases: 
modified:
  - 2025-05-04
  - 2025-05-03
  - 2025-04-05
---

> [!error] Bus Topology
> **Bus Topology** :: Contains one shared link to which all devices are connected to
---

> [!blank|float-right-large] Title
> ![[Bus Topology 2025-01-09 20.23.04.excalidraw|100%]]

### Characteristics
1. Single cable to connect all nodes
2. Terminators at ends to prevent **signal bounce**
3. Half duplex data transmission

### Data Transfer Method
1. Packet sent
   - Containing address of destination 
2. All nodes gets the packets
   - Checks to see if destination address matches node address
   - If not then sends it along the transmission line to next nodes
   - Else accepts the packet
### Benefits
1. Failure of one node does not affect the network
2. Easy to expand by adding additional nodes
3. Easy to setup
4. Cheaper
   - less cabling required compared to mesh and star

### Limitations
1. If main cable fails, whole network goes down
2. Not secure as each packet passes through every node
3. Performance deteriorates under heavy load
4. Difficult to troubleshoot a singular node
5. Lots of collisions
6. Efficiency reduces as device count increases

### Use cases
1. Low device count
2. Light traffic
3. Low budget
