---
subject:
  - "[[Computer Science]]"
grade:
  - "[[AS Level]]"
related: 
creation-date: 2025-01-09
up:
  - "[[Types of Network Models]]"
tags: 
aliases:
  - Thin Client
  - Thick Client
modified:
  - 2025-05-04
  - 2025-04-05
---

### Basic Principal
> [!blank|float-medium-right] 
> ![[Client Server Model 2025-01-09 19.04.09.excalidraw|100%]]

- User's computer is called the **Client**
- Data (webpages and applications) are stored on server
- Clients send requests
- Web server process requests and returns a response to the client
- Client displays result (response to user)
-
- User's client can request file from any other client


### Advantages of client server
1. Allows organization to control usage and downloading files
2. More security as files only stored on one server
3. Files can be simultaneously accessed by multiple users

### Disadvantages if client-server
1. Higher initial cost 
2. Clients loose access to some resource if server is down
3. Performace may be limited to network speed

### Use cases
1. Centralized control by management
2. Complex networks
3. Scalable networks with good performance


### Types of clients
#### Thin Client
1. ! Client does no processing and server does all processing
2. Client only sends requests to server
3. Server sends back appropriate response to client, which the client displays
4. **Server does all the data storage and processing**

##### Advantages
1. Low expansion costs as low powered devices can be used
2. Simultaneous and easy update application across all devices
3. More secure as data stored in centralized server

##### Disadvantages
1. Excessive server reliance (if server down, all clients down)
2. Higher initial costs


#### Thick Client
1. Client does most of the processing, server does minimal processing
2. Most of the resources are installed locally

##### Advantages
1. More robust (less server reliance)
2. Client has more control due to more local storage

##### Disadvantages
1. Less secure as client has to keep their own data secure
2. Each client needs to update data individually
3. [[Data Integrity]] issues as multiple clients access same data, leading to inconsistencies
