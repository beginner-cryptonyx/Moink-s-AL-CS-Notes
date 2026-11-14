---
subject:
  - "[[Computer Science]]"
grade:
  - "[[A Level]]"
related:
creation-date: 2025-05-21
up:
  - "[[Computer Science]]"
tags:
aliases:
modified:
  - 2025-09-14
  - 2025-07-30
  - 2025-06-12
  - 2025-06-11
  - 2025-06-07
  - 2025-05-30
  - 2025-05-28
  - 2025-05-22
  - 2025-05-21
importance: 14
completion: "100.00"
---

> [!grey]- Syllabus
> ## 14.1 Protocols
> 
> - [x] Understand why protocols are essential for communication between computers
> - [x] Understand the protocol stack model
>   - [x] Each layer has its own functionality
> - [x] Understand the TCP/IP protocol suite:
>   - [x] Application layer
>   - [x] Transport layer
>   - [x] Internet layer
>   - [x] Link layer
>   - [x] Purpose and function of each layer
>   - [x] Data flow when sending a message from one host to another
> - [x] Understand the purpose of the following protocols:
>   - [x] HTTP
>   - [x] FTP
>   - [x] POP3
>   - [x] IMAP
>   - [x] SMTP
>   - [x] BitTorrent (peer-to-peer file sharing)
> 
> ## 14.2 Circuit Switching and Packet Switching
> 
> - [x] Understand circuit switching:
>   - [x] Benefits
>   - [x] Drawbacks
>   - [x] Applicability
> - [x] Understand packet switching:
>   - [x] Benefits
>   - [x] Drawbacks
>   - [x] Applicability
> - [x] Understand the function of a router in packet switching
> - [x] Explain how packet switching is used to transmit messages across a network, including the internet

# Protocols
> [!Error] Protocol
> **Protocol** :: A set of roles data transmission which are agreed by the sender and receiver

## Importance of protocols
1. Sets a standard for communication
2. Allows communication between devices operating on different platforms or from different manufacturers
3. All data is sent and received using the same rules
4. All data is sent and received using the same formats
5. Communication is independent of the software used
6. Communication is independent of the hardware used

## Protocol stack model
- TCP/IP can be seen as layers within  a stack
- Each layer can only accept input from layer below or above
- Interaction between adjacent layers is done via a defined interface
- Interaction done via installed software
- A layer may contain sub layers
- Data is added to the headers as the frames or packets pass through the layers
- ! User interaction is done at the highest layer (Application layer)
- ! Direct access to the hardware is confined to the lowest layer (Link Layer)

1. Message is passed from top layer to bottom layer
2. After it is received, another message can be sent from link layer to top layer
3. Link layer interfaces with network and send/receives messages

### [[OSI Model]]
### TCP/IP
#### TCP
- Transmission Control Protocol
- Works at transport layer
- Sets up and maintains connection between 2 nodes
- Ensures delivery of data between 2 nodes

#### IP
- Internet Protocol
- Works on the network / internet layer
- Provides the rules for exchange of packets over the internet
- Decides the path of transmission for each packet

#### Application Layer
- ! Handles access to services
- Provides access to all the programs that exchange data by directly interacting with the user
- Provides mechanisms for secure communication, such as encryption and authentication
- Enables data transfer from and to the transport layer
- Allows error detection and recovery mechanisms to handle application specific errors
- Defines protocols that any application uses to exchange data
  - HTTP
  - SMTP
  - DNS
  - FTP
  - POP3
  - IMAP
- Consists of the application, presentation, and session layer of the OSI model

#### Transport Layer
- ! Handles forwarding of packets

- Uses the following protocols
  - TCP
  - UDP
  - SCTP

- It breaks down data into manageable packets via segmentation
- Adds **Packet Header** and sequences the packets
- Receives data from the application layer
- Sends data to the Network layer
- Controls the flow of the packets
- Handles packet loss and corruption
- Consists of the transport layer of the OSI model

#### Internet Layer
- Consists of the Network layer of the OSI model
- Identifies the intended network and host
- Transmits data to the physical layer
- Packets are addressed with their source and destination IP addresses
- Routes the packets independently through the most optimum route
- Uses IP address and port number to form a socket


#### Data Link Layer
- ! Handles how data is physically sent
- Ensures correct network protocols are followed
- Enables upper layers to access the physical medium
- Responsible for transmitting data within a network
  - Done via splitting segments of data into frames
- Used ARP (Address Resolution Protocol) to map IP addresses into MAC addresses
#### TCP
- ! Transmission Control Protocol
- Transmit user data to the transport layer
- Creates sufficient packets to hold all of the data
  - Each packet holds a header along with the data
- Ensures that any and all responses are directed back into the application layer protocol

## Common Protocols Used
### TCP 
- **Host to host** protocol 
- Responsible for safe delivery of a message 
  - Creates sufficient packets for data transmission
  - 
### HTTP (Hypertext Transfer Protocol)
- Used by browsers to fetch web pages
- Used for transmission of HTML files

### FTP (File Transfer Protocol)
- ! Used to transfer files between computers over a (TCP/IP) network

- Operates on client server model 
  - Server which is the central computer that stores files that are to be downloaded 
  - Client initializes connection to upload and download files
- Supports command based operations which allows user to send instruction to be carried out on the server
- Supports anonymous access which allows users to download files without needing to identify themselves via a login
### SMTP (Simple Mail Transfer Protocol)
- ! Protocol to send emails
- Mail servers use it to forward email messages

### POP3 (Post Office Protocol 3)
- ! Used to receive and download emails
- Mail is held by a remote server until it is downloaded

### IMAP
- It is a pull protocol
- Used by email clients to retrieve email messages
- Emails are pulled from an email server over a TCP/IP connection
- Keeps the server and client in sync, by not deleting the original email


# Transmission Modes
## Circuit switching

- ! Implemented in the physical layer
- Circuit switching uses a dedicated channel to make communication
- Dedicated path must be established before the transfer of data
- Circuit is persistent during the whole duration of data transmission
- Same path followed for all packets
- Message received in the same order as it is sent
- Message will remain intact (unlike packet switching)
- Uses the whole bandwidth
- Bi-Directional transmission
- Uses TCP (connection-oriented transmission method)

### Uses
1. Used where dedicated path of transmission must be maintained, like calls
2. Used for real time communication where full bandwidth is required
3. eg: Voice communication, video streaming

### Benefits
1. Whole bandwidth is available
2. Dedicated communication channel increases the quality of transmission
3. Data transmitted at a fixed rate
4. Simple method of data transfer
5. No waiting time at switches (as packets do not need to be reassembled)
6. Suitable for long continuous communication
7. Fast method of data transfer
8. Data cannot get lost
9. Data follows the same route
10. Better for realtime communication

### Drawbacks
1. Dedicated communication channel makes it impossible to transmit data from other nodes even when the transmission line is idle
2. Not flexible 
3. No alternative route incase of failure, error will end the communication
4. Time taken to establish the physical link between both nodes may be too much
5. Dedicated path for communication can be very expensive
6. Dedicated channels need the whole bandwidth, thus the bandwidth cannot be shared




## Packet switching
- Data transmitted over a digital network
- Data is split into packets
- Packets can all take different routes
- No need of pre-established transmission path 
- Packets that are received can be out of order
- Packets are assembled back into order at destination
- Packet switching implemented in the network layer
- Sharing of bandwidth is allowed
- Allows faulty packets to be resent unlike circut switching


### Uses:
1. Used on data networks like the internet
   - Send large files
   - Live streaming of files/content not needed 
2. Neseccery to be able to overcome faulty lines via **re-routing**
3. Security is a requirement
4. High volume data transmission
5. Using all the bandwidth is not required

- Email and text messaging

### Benefits
1. Packets are rerouted if problems arise
2. More secure as it is harder to intercept messages
3. A dedicated path does not need to be assembled
4. Whole bandwidth is not used

### Drawbacks
1. Time taken to reassemble packets at the destination
2. More complex protocols for delivery
3. Unsuitable for realtime transmission scenarios
4. Lots of RAM required to handle large amounts of data

### Router role in Packet switching
1. Router examines the packets header and gets the IP address of the destination
2. Router will have access to a **routing table** which contains
  - Information about the netmask and gateway used 
  - Available hops and status of the routes along the route
3. Router then decides the best route and the next best hop 
4. Router sends the packet on its next hop


### Use of packet switching to transfer messages across the internet
1. A large message (such as a webpage) is divided into smaller chunks *of the same size* called **packet**
2. The packet will have a header and a payload
   - This header contains a source IP address, destination IP address and the sequence number
3. Each packet is dispatched independently
   - As a result some may travel in different routes 
4. Packets will arrive out of order
   - Therefore they need to be reassembled into the original message
   - This reassembly is normally done by a **switch**, using the sequence number in the packet header
5. If packets are missing or are corrupted then re-transmission request is sent

# Bittorrent
- ! Uses the peer-to-peer network model
- ! Used for sharing of files between thousands of computers connected together over the internet
- Allowing more users to share files with each other than in a normal peer to peer network
- Users share files directly with each other
- All users/computers are of equal status
## BitTorrent client types
1. Tracker :: Central server that stores details on the computers which have all or part of the file to be downloaded, such as the IP addresses and how much of the file they have
2. Seed :: A peer computer that is uploading downloaded content
3. Swarm :: All the connected peer computers that have all, or part of the file to be downloaded
## Working of bittorrent
1. BitTorrent client software is made available to computers
2. A computer joins the swarm by using the bitTorrent software to load a torrent descriptor file 
3. The file to be shared, called torrent is split into multiple small pieces
   - For this to happen one computer in the swarm must have a complete copy of the torrent
4. A server called a tracker keeps record of all of the computers in a swarm, and the parts of the file they have
5. Tracker shares the IP addresses of computers to a computer that requests them, allowing them to connect to each other
6. Pieces of the torrent can be both downloaded and uploaded
7. Once a computer has a piece or all of the torrent,it can become a seed and upload
8. Or the computer can become a leech by downloading more than what is uploaded


```dataviewjs
const file = dv.current();
const checkboxes = file.file.tasks;
const totalCheckboxes = checkboxes.length;
const completedCheckboxes = checkboxes.filter(t => t.completed).length;


const completionPercentage = totalCheckboxes > 0 
    ? ((completedCheckboxes / totalCheckboxes) * 100).toFixed(2) 
    : "0.00";
console.log(totalCheckboxes, completedCheckboxes, completionPercentage)
try {
    await app.fileManager.processFrontMatter(dv.app.vault.getAbstractFileByPath(file.file.path), (frontmatter) => {
        frontmatter["completion"] = completionPercentage;
    });
    console.log("✅ Frontmatter updated successfully!");
} catch (error) {
    console.log(`❌ Error updating frontmatter: ${error}`);
}
```