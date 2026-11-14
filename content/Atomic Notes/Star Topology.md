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
  - 2025-05-03
  - 2025-04-05
---


> [!error] Star Topology
> **Star Topology** :: Network topology in which all nodes are linked to a centralized sytem


> [!blank|float-medium-right]
> ![[Star Topology 2025-01-09 20.46.40.excalidraw|100%]]

### Characteristics
1. Devices connected to only one central device (can be a [[Switch]], [[Hub]] or a Server)
2. Each node has its own connection
3. Duplex transmission

### Data Transfer Method
1. Data packets sent to central [[Switch]] or [[Hub]] or [[Router]] 
2. Central device determines which device the packet should be sent to (usually based on a routing table)
3. Only recipient gets data

### Benefits
1. Easy to scale, devices just need to be added to the central device
2. Low data collisions
3. More secure as unwanted nodes don't get data
4. If any one node is broken, network will still be up
5. Connection may use different protocols
6. Helps in monitoring of network
7. Easy to troubleshoot

### Limitations
1. High installation cost
2. If central device fails, whole network fails
3. Network can be bottlenecked by bad central device

### Use Cases
1. Dynamic network where devices are added and removed constantly
2. Home networks and office networks
