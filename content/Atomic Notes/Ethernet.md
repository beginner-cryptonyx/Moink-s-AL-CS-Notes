---
subject:
  - "[[Computer Science]]"
grade:
  - "[[AS Level]]"
related: 
creation-date: 2025-03-05
up: "[[Networking]]"
tags: 
aliases: 
modified:
  - 2025-05-05
  - 2025-04-05
---

## Characteristics
- Protocol for data transmission over a standard wired network connection
- Adopted by [[Ethics and Ownership#IEEE|IEEE]] 
- Ethernet made up of
  - A node 
  - Medium (cable)
  - Frame : data transfer happens in frames which consist of source address and destination address (MAC address)
- It uses CSMA/CD
- Data is trasmitted in frames
	- Each frame has a source and destination (as either IP/MAC address)
	- Error checking is done so damaged frames can be resent

## Conflicts
- Conflicts can occur when devices without unique IP addresses join the same network
- Solved by restarting router

## Collisions
- Collisions occurs when 2 devices transmit messages at the same time
- % Occurs as the voltages of the 2 different messages interfere with each other and corrupt the message
- Solved via CSMA/CD (Carrier Sense Multiple Access with Collision Detection) 

### CSMA/CD
1. A node wanting to transmit data listens to the communication channel
2. If activity is detected (based on voltage),node waits before checking again
3. If there is no activity and the channel is free/idle, then transmission is beguin 
4. After transfer of each frame, transmission medium is check for collision
5. If no collision, then next frame is sent 
6. If a collision is detected
   - Sending device aborts transmission
   - **Jamming signal** is transmitted from the *sending device* to warn all devices
   - After a **random time**, sending device tries data transmission again
   - If more collisoons occur then waiting time is increased

- % Collisions occur in legacy ethernet systems only as modern ethernet works with a star config with a switch, meaning CSMA/CD is not required as no collisions occur

#### Advantages of CSMA/CD
1. Efficent usage of bandwidth
2. Reduces chances of collision
3. Automatic handling of collisions
4. Decentralised control
5. Cost effective for small networks

#### Disadvantages if CSMA/CD
1. Random waiting time increased each time so there can be infinite waiting
2. There could be a constant jamming signal so nothing ever sends
3. Certain nodes cannot be prioritised
4. high power consumption
5. Only suitiable for short distance networks
6. Not Scallable
