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
  - 2026-01-13
  - 2025-11-12
  - 2025-11-11
  - 2025-11-08
  - 2025-10-08
  - 2025-10-04
  - 2025-10-03
  - 2025-09-28
  - 2025-09-24
  - 2025-09-20
completion: "90.91"
importance: 17
---


> [!grey]- Syllabus
> # 17 Security
> 
> ## 17.1 Encryption, Encryption Protocols and Digital Certificates
> 
> ### Encryption
> - [x] Show understanding of how encryption works  
>   - [x] Public key  
>   - [x] Private key  
>   - [x] Plain text  
>   - [x] Cipher text  
>   - [x] Encryption  
>   - [x] Symmetric key cryptography  
>   - [x] Asymmetric key cryptography  
> - [ ] How keys can be used:  
>   - [x] To send a private message from the public to an individual/organisation  
>   - [ ] To send a verified message to the public  
> - [x] How data is encrypted and decrypted using:  
>   - [x] Symmetric cryptography  
>   - [x] Asymmetric cryptography  
> - [x] Purpose, benefits, and drawbacks of quantum cryptography  
> 
> ### SSL/TLS
> - [x] Show awareness of the Secure Socket Layer (SSL)/Transport Layer Security (TLS)  
>   - [x] Purpose of SSL/TLS  
>   - [x] Use of SSL/TLS in client-server communication  
>   - [x] Situations where SSL/TLS would be appropriate  
> 
> ### Digital Certificates
> - [x] Show understanding of digital certification  
>   - [x] How a digital certificate is acquired  
>   - [x] How a digital certificate is used to produce digital signatures  
> 
> ---


# Encryption
Why do encryption?
1. To ensure message is authentic and came from a trusted source
2. To ensure that only the intended recipient is able to understand the message
3. To ensure the message has not been altered during transmission
4. Non-repudiation, neither sender nor receiver can deny that the transmission has occured
## Working of encryption
### KEY concepts of encryption 
(get it??????)

1. Private key
   - It is the unpublished, secret key, that is NEVER transmitted anywhere
   - It has a matching public key
   - It is used to decrypt data that was encrypted with its matching public key
2. Public Key
3. Plain Text
4. Cipher text
### Symmetric key cryptography
1. Uses single key to encrypt and decrypt messages
2. The symmetric key is shared (unlike asymmetric key where only the public key is shared)
3. Simple and fast process 
4. Smaller length of keys (128or 256 bits)

Disadvantages:
- It is less secure (higher risk of compromise)
- Smaller length of keys (128or 256 bits)
- Key has to be exchanged securely
- Once compromised, the key can be used to decrypt both sent and received messaged
- Non-repudiation cannot be ensured
### Asymmetric key cryptography
- More secure compared to symmetric key cryptography
- More complicated process that takes time
- Longer keys are used (2048 bits)

Purpose:
1. Provides better security
   - By using 2 different keys, a public key and a private key
2. One of the keys is used to encrypt the message
3. The matching key is used to decrypt the message

Process:
1. An algorithm is used to generate a matching pair of private and public keys
2. Public key of recipient is sent to sender
3. Message to be sent is encrypted using the public key of the recipient to create cipher text
4. Sender sends cipher text back to recipient
5. Cipher text can only be decrypted using recipients private key 

## How to send keys
## How is data encrypted and decrypted
## Quantum cryptography
Purpose:
1. To produce a virtually unbreakable encryption system
2. Which used the laws of quantum physics, and properties of photons
3. It is able to detect eavesdropping
   - Because the properties of the photons change
4. To enable use of longer keys
5. Protect the security of data sent over fibre optic cables


Benefits:
1. Security provided is based on laws of physics rather than mathematical algorithms, so it is therefore *more secure*
2. Longer keys can be used
3. Eavesdropping can be detected
4. It is used to protect the security of data transmitted over fibre optic cables 
5. Virtually unhackable, the integrity of key once transferred is guaranteed as it cannot be replicated
6. Quantum cryptography's performance is constantly being improved, making it more secure for valuable government and industrial secrets

Disadvantages:
1. Lacks many vital features such as digital signatures and certified mail
2. High cost of purchasing and mainlining the equipment required
3. Currently works over short distances only
4. It is a developing technology, and hence has higher error rates
5. Polarization of light can change during transmission
6. Allows criminals and terrorists to hide their communications

# SSL / TLS
- % SSL -> Secure Sockets Layer
- % TLS -> Transport Layer Security
## Purpose of SSL and TLS
1. Ensure security and privacy when using the internet
2. Data encryption
3. Authentication of client and server
	- So that they both can communicate with confidentiality and integrity

## Protocols used in SSL/TLS
1. Handshake protocol
   - It is used to establish a secure and reliable connection between 2 devices, systems, or networks
   - It permits the web server and the client to authenticate to each other to make use of encryption algorithms
2. Record protocol
   - Provides a secure and reliable way to send and receive data (which includes exchange of records) over a network, which is encrypted and authenticated.
   - Deals with the format for data transmission
## Use of SSL and TLS in client-server communication
When client server communication is initiated:
1. An SSL/TLS is initiated by an application
	- This application is the client
2. The application that receives the connection, becomes the server
3. Every new connection begains with a handshake as defined by SSL/TLS
4. The client requests the digital certificate from the server, which the server sends to the client
5. Client verifies the server's digital certificate
   - It obtains the servers public key
7. The encryption algorithms are agreed upon, and the symmetric session keys are generated and defined
8. A secure connection is established between the client and the server
## Use cases of SSL/TLS
1. Transmitting authentication data like passwords and session cookies 
2. When the transmission of data must be protected from modification on its way to or from a server, such as user input or server responses
3. When transmitting data classified as non-public



# Digital Certificates
- A digital certificate is an electronic document
- It is used to authenticate the online identity of a website, individual or organization
- Typically issued by a CA
- It contains information identifying website owner and a public key

## How digital certificates are acquired
1. The enquirer requests a certificate from a Certificate Authority (CA)
2. Enquirer may send their public key to CA
3. The enquirer gathers all information required by the CA in order to obtain their certificate, this includes information to prove their identity
4. The CA verifies enquirer's identity
5. CA generates the enquirer's certificate including the enquirer's public key, along with other information
6. Data sent between CA and enquirer is encrypted
	- Data sent to CA is encrypted with CA's public key
	- Data receive by CA is encrypted with CA's private key
## Digital Signatures
### Digital signatures to verify a message
1. The message and the digital signature is decrypted using the receivers private key
2. The digital signature received is decrypted with the senders public key to recover the message digest sent
3. The decrypted message received is hashed with the agreed hashing algorithm to reproduce the message digest of the message received
4. Both digests are compared
5. If they are the same then the message has not been altered

### How is digital certificate used to produce digital signatures
- Digital certificate provides the public key
- Which is used to validate the private key associated with the entity organization/website/digital

### How message is used to produce digital signature
1. The message is hashed with the agreed hashing algorithm
2. This produces a message digest
3. The digest is encrypted with the senders private key to form the digital signature


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

