---
subject:
  - "[[Computer Science]]"
grade:
  - "[[A Level]]"
related: 
creation-date: 2025-05-28
up: 
tags: 
aliases: 
modified:
  - 2025-06-01
  - 2025-05-28
---

### OSI Model
> [!none|float-small-right]
>```mermaid
> graph TD
> A[Application]
> B[Presentation]
> C[Session]
> D[Transport]
> E[Network]
> F[Data Link]
> G[Physical]
> 
> A --> B
> B --> C
> C --> D
> D --> E
> E --> F
> F --> G
>
>```


#### Physical Layer
- Lowest layer
- Responsible for the actual physical connection between devices
- Information stored in the form of bits
- When receiving data (analogue) the Physical layer will convert it into binary
- Controls the bit rate
- Responsible for bit synchronization
- Uses devices like hubs, cables, modems and repeaters

#### Data Link Layer
- Responsible for node to node message delivery in the same network
- Defines the **line discipline**, the maximum time nodes can communicate
- Does flow control (Limit of data to be transmitted)
- Does error detection
- Uses frames as the data unit

Has 2 Different sub-layers:
1. MAC (Media Access Control) -> Hardware identification via MAC address that lives in the NIC
2. Logical Link Control -> Handles flow control

#### Network Layer
- Network to network communication 
- Network layer is built on routers
- Deals with packet routing
- Data unit in transmission layer is packets

Functions:
1. Routing: determine the most efficient path for data transmission
2. Logical Addressing: Senders and receivers IP address placed in the packet header

#### Transmission Layer
- Data in transmission layer is **segments**
- When receiving data it assembles packets into segments
- ! Responsible for end-to-end delivery of the complete message
- Implements flow control and error checking
- Uses protocols like:
  - TCP
  - UDP
  - PPTP
  - NetBIOS
- When sending it adds a port number to the header
- When receiving port number is read and segment is forwarded to correct application

#### Session Layer
- Allows processes to establish, manage, maintain, and terminate a connection
- Ensures that communication is open for long enough for all data to be transmitted

#### Presentation Layer
- When sending data, data from the application layer is manipulated to ensure that it is in the correct format to transmit over a network
- Uses TLS or SSL

Functions:
1. Translation
2. Encryption/Decryption
3. Compression

#### Application Layer
- Top most layer
- Uses protocols such as:
  - HTTPS
  - SMTP
  - DNS
  - FTP
- Acts as an interface to allow applications to interact weth networks

