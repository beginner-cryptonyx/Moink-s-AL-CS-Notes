---
subject:
  - "[[Computer Science]]"
grade:
  - "[[AS Level]]"
related:
creation-date: 2025-04-11
up:
  - "[[Computer Science]]"
tags:
aliases:
modified:
  - 2025-05-04
  - 2025-04-18
  - 2025-04-13
  - 2025-04-12
completion: "100.00"
importance: 6
marks-lost: 31
---

> [!grey]- Syllabus 
>  
> ## 🔐 **6.1 Data Security**
> ### 🧠 Key Concepts
> - [x] Understand the **difference between**:  
>   - [x] **Security** (protection from unauthorized access)  
>   - [x] **Privacy** (control over who sees personal data)  
>   - [x] **Integrity** (accuracy and consistency of data)
> 
> ### 🛡️ Importance of Security
> - [x] Appreciate need for
> 	- [x] **data security**
> 	- [x] **system security**
> 
> ### 🔧 Security Measures
> - [x] User accounts & passwords  
> - [x] Authentication techniques:
>   - [x] Digital signatures  
>   - [x] Biometrics  
> - [x] Firewalls  
> - [x] Anti-virus software  
> - [x] Anti-spyware  
> - [x] Encryption
> 
> ### ⚠️ Threats from Networks/Internet
> - [x] Malware 
> 	- [x] virus
> 	- [x] spyware
> 	- [x] Trojan horse
> 	- [x] Bots
> 	- [x] Worms
> 	- [x] Logic Bomb 
> 	- [x] Spyware
> - [x] Hackers  
> - [x] Phishing  
> - [x] Pharming
> 
> ### 🚫 Risk Mitigation Methods
> - [x] Describe **preventive measures** against each threat  
> - [x] Use of **access rights** and **encryption** to protect data
> 
> ---  
>  
> ## 🧮 **6.2 Data Integrity**
> ### ✅ Data Validation
> - [x] Understand how **validation** maintains data accuracy  
> - [x] Use and describe types of validation:
>   - [x] Range check  
>   - [x] Format check  
>   - [x] Length check  
>   - [x] Presence check  
>   - [x] Existence check  
>   - [x] Limit check  
>   - [x] Check digit
> 
> ### 🔁 Data Verification
> - [x] Understand role of **verification** in detecting entry errors  
> #### 🔤 During Data Entry:
> - [x] Visual check  
> - [x] Double entry  
>  
> #### 📤 During Data Transfer:
> - [x] Parity check (byte and block level)  
> - [x] Checksum  

---

# Data Security
> [!error] Data Security and Privacy
> **Data Security** :: A requirement for data to be available for use when needed, ensures that only authorized users have access to the system and data can be recovered when lost or corrupted
> **Data Privacy** :: A requirement for data to be available only to authorized user

## Need for Data privacy
- Prevents unauthorized access
## Need for data security
- Stop data being lost or corrupted or deleted or amended
- Making sure data is recoverable
## Need for system security
- Prevent damaging the system
- Ensures that system continues to carry out tasks users need
- Ensure thats only authorized users have access to the system
- Ensures data security
## Security measures
### User accounts and passwords
### Authentication Techniques
> [!error] Authentication
> **Authentication** ::verification of a user’s identity
#### Digital Signatures
1. The sender uses a hashing algorithm on the data to make a digest
2. Using the **private** key the sender encrypts this data to make a digital signature
3. This signature is sent along with the original data
4. Once receiver gets the data and the digital signature
5. It uses the **same hashing** algorithm to hash the data, to create another digest
6. It then decrypts the digital signature using the senders **public key** to get the original digest
7. If both digests are the same, then data will be authentic and unchanged

#### Biometrics
- Relies on characteristics of human beings such as
  - Fingerprint Scans :: Compares pattern of ridges and valleys, which are unique
  - Retina Scans :: unique pattern of blood vessels in the retina
### Firewalls
> [!tip] Firewall
> **Firewall** :: Hardware or software that monitors and controls network traffic

Tasks carried out by firewall:
1. Examines traffic between users computer or internal network and a public network
2. Checks whether incoming or outgoing data meets the criteria, only then are requests and packets allowed
3. Contains **Blacklist** of undesirable sites and IP addresses, which are blocked from being accessed
4. Helps prevent viruses or hackers entering computer or network
5. Logs all network requests to allow user to later interrogate 


### Anti-virus software
1. Constantly runs in the background to check for viruses
2. Check software or files before they are loaded/run
3. Compares possible viruses against database of known viruses
4. Carries out heuristic checking, meaning it scans software for behaviour that indicates it is a virus
5. Quarantines files or programs which are possibly infected
### Anti-Spyware
1. Spyware database contains list of known spyware, needs to be constantly updated
2. Compares files and programs to the database, quarantines and deletes the spyware
### Encryption
- Data is encoded into cipher text based on a key
- This data cannot be comprehended without this decryption key

## Network threats
### Malware
> [!tip] Malware
> **Malware** :: Malicious software that has the intention of causing harm to a system or its contents

#### Malware Software
- Installed without users knowledge
- All run in background
- pretend to be legit software

##### Types of malware
1. Virus :: Replicates itself inside other executable code
2. Worm :: Runs independently and transfers itself to other network hosts
3. Logic bomb :: stays inactive until some condition is met
4. Trojan horse :: Replaces all or part of a previously useful program
5. Spyware :: Installed on the user's system without their knowledge; logs activity and sends to a third party
6. Bot :: Takes control of another computer and tries to launch attacks

#### Malware Activities
1. Phishing :: Sending an email or electronic message from an apparently legitimate source requesting confidential information
  - Anti-phishing toolbars on web browsers 
  - Check for SSL certificate
  - Change passwords
  - Update browser
  - Run good firewall
  - Be wary of popups
2. Pharming :: Setting up a bogus website which appears to be a legitimate site
   - Use anti-virus
   - Use modern web browser
   - Check spelling of websites
   - Check for SSL certificate
3. Keylogger :: Recording keyboard usage by legitimate user of the system


### Hackers
- People who gain illegal access to data inode to destroy or damage it
- Run firewall and have strong passwords to prevent risk


## Mitigation of risk
### Access rights
### Encryption


# Data Integrity
> [!error] Definitions
> **Data integrity** :: Making sure data is consistent, accurate, and up to date
> **Data Validation** :: A check that data entered is of the correct type and format

## Data validation
### Maintaining data Accuracy
### Types of data validation
#### Range Check
#### Format check
#### Length Check
#### Presence Check
#### Existence Check
#### Limit check
#### Check Digit

## Data Verification
### Role of verification
### Types of data verification
Visual Check :: After data is entered, it is manually compared 
Double Data entry :: Data is entered twice, the computer/system compares the data
#### Parity check
- All computers involved in data transfer decide whether odd or even parity should be used
- An additional bit is added to make the number of 1's in the byte either odd or even
- If a byte with odd number of 1 bits are received when even parity is used, there is an error

##### Parity block
- Parity is calculated horizontally and vertically 
- A parity bit is created from the bits produced by the vertical parity check 
- This is sent with the data
- The parity is rechecked when received
- The position of an incorrect bit can be determined

#### Checksum
- A calculation is made from the data 
- Result transferred along with the data
- Receiver repeats the calculation
- Compares the result with the value received 
- If they both are different, there is an error


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