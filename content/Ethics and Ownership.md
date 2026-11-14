---
subject:
  - "[[Computer Science]]"
grade:
  - "[[AS Level]]"
related:
creation-date: 2025-03-30
up:
  - "[[Computer Science]]"
tags:
aliases:
importance: 7
completion: "100.00"
modified:
  - 2025-04-16
  - 2025-04-14
  - 2025-04-03
marks-lost: 17
---



> [!grey]- Syllabus
>  
> ## **7.1 Ethics and Ownership**  
> **Candidates should be able to:**  
>  
> - [x] **Understand the purpose of ethics as a computing professional**  
> - [x] **Recognize the importance of joining professional ethical bodies**, including:  
>   - [x] **BCS** (*British Computer Society*)  
>   - [x] **IEEE** (*Institute of Electrical and Electronics Engineers*)  
>  
> - [x] **Understand the need to act ethically**  
> - [x] **Analyze the impact of ethical vs. Unethical behavior in a given situation**  
>  
> - [x] **Understand copyright legislation and its importance**  
>  
> - [x] **Understand different types of software licensing** and justify their use:  
>   - [x] **Free Software Foundation**  
>   - [x] **Open Source Initiative**  
>   - [x] **Shareware**  
>   - [x] **Commercial Software**  
>   - [x] **Freeware**
>
> - [x] **Understand Artificial Intelligence (AI):**  
>   - [x] **Impact of AI on society, economy, and environment**  
>   - [x] **Applications of AI**  
>

# Ethics
## Benefits of joining an ethical body
1. Preset ethical guidelines -> clients and staff know standards they have to meet
2. Clients and staff know he is reputable (professional integrity)
3. Legal help and support provided  
4. Training courses -> helps to keep skills updated

## Purpose and need to act ethically
1. Increase work quality due to more worker [[Human Resource Management#Motivation|Motivation]]
2. Make team members feel valued
3. Encourage teamwork and corporation
4. Better client product

## Acting ethically


### General
1. Being truthful
2. Performing research (upon inadequacy)
3. Asking for additional training (upon inadequacy)

### To Clients
1. Personal data should be private
2. Good communication with client (keep them up to date)
3. Provide solutions requested by client
4. Stay within budget

- % related: [[Software Development]]

### To product
1. Report errors

# Ethical Bodies
## British Computer Society (BCS)

Code of Conduct headings
1. Public interest
2. Professional Competency and Integrity
3. Duty to relevant authority
4. Duty to Profession

## IEEE
Code of Conduct headings
1. Public interest
2. Client and product interest
3. Product interest
4. Judgement - Integrity of professional Judgement
5. Management - ethical approach to software development
6. Profession - advance integrity and reputation of profession
7. Colleagues - supportive to co-workers
8. Self - lifelong learning mentality

---

# Software licensing
> [!error] Different Software licenses
> **Open Source Software** :: software provided with the source code
> **Free Software** :: Software provided with source code, which the user is free to use in any way
> **Shareware** :: Software provided free of cost for a limited period (without source code)
> **Freeware** :: Software provided free of cost with no time limit and no source code
## Commercial Software 
- Software license paid for by user
- software not owned by user (only the license to use it)
- Distribution not allowed
- User cannot edit source code
  
Applications:
1. Software available for immediate functional use 
2. Continuous maintenance/support provided


## Free software foundation
- Non profit
- Full freedom given to user to use, modify and re-distribute (according to license) software
- Different from open source due to **copyleft** principal, where modified redistribution must have the same licensing as software modified
- Still open source
- ! Redistribution allowed
- No payment needed
- User can edit source code

## Open source initiative
- Source code provided
- User can use source code any way they desire (accordance to license)
- Promotes collaboration between developers (via source control like git)
- Endless lifespan as users can modify code to match require
- ! Redistribution allowed
- No payment needed
## Shareware
- Fully functional software allowed to be used, but with a time limit (trial period)
- After time limit is done, the software will ask for a license fee
- ! Redistribution allowed
- User cannot edit source code
- No need for user to pay before hand
## Freeware
- Limited version of Commercial software
- No time limit restrictions, rather focuses on functionality limitations
- Subject to copyright laws
- User not allowed to study/modify/use source code

---

# Copyright
> [!error|float-right-large] Copyright
> **Copyright** :: A formal recognition of ownership of a created and published work

- Formal and legal rights to ownership
- Protects against unauthorized reproduction of work
- Provides for legal right of redress (take legal action upon infringement)
## Applications of copyright
1. Literature
2. Music
3. Media 
4. Software

## Arguments for copyright
1. Creation takes time, effort and needs original thinking, thus the opportunity for OC to capitalize on their creation
2. It is unfair for a separate party to monetize content without compensation to the creator
3. Prevents piracy

## Typical Copyright Laws 
1. Defined time period where copyright is active
2. Agreed method to show copyright is active (like the © sign)
3. Policies to be applied upon passing of the copyright holder
4. Requirement for registering for copyright protection (recording the creation date of the work)


### Software Specific
1. Illegal to copy or distribute (sell) software
2. Software cannot be used on multiple devices (eg: run on a network) without a multi-use license
3. Code from software cannot be copied without permission
4. The trademarked name of software cannot be used

## Enforcing Copyright
1. Checkbox asking user to accept terms and conditions
2. Dongle required to run some software
3. DRM (Digital Rights Management)
4. Product keys

---

# Artificial intelligence
## Impacts of AI
### Social
- privacy exploitation (data stored for AI models to be trained on)
- Improved life expectancy
  - Could be used for improved healthcare
  - Could be used for reducing crime rate 
  - Could allow for improved and more accessible education
- Helps people with disabilities
### Economic
- Unemployment
- Reduced cost for enterprises -> decreased cost for consumers
### Environmental
- Possible to introduce AI into energy optimization
- Climate change solutions could be aided
- % The above points can be achieved due to AI's ability to form patterns from huge data sets
- High energy consumption to run AI models -> increased carbon footprint
- Waste of water (large amounts of water wasted as it is required for cooling purposes of data centers running AI models)

## Applications of AI
1. Self driving cars
2. Prosthetics
3. NLP (natural language processing)
4. Facial recognition
5. Pattern predictions and correlations
6. Performing tasks of extreme precision and dexterity (eg: eye surgeries)

## Common AI buzzwords in the marking scheme
1. Image recognition
    - To identify features and items in an image
	- This is done by comparing image to a large database of images
	- Matches features of image and images in database to get a match probablity 
    - If done for a video, each **frame** is analysed
2. Speech recognition
    - Identifies when a user is speaking
    - Converts speech into text
    - Key phrases/words are stored in a database
    - Text is matched to phrases stored 
    - Generates most likely sentance
3. Facial Regonition
    - Identifies if there are faces in the image
    - Uses image recognition
    - Analyses pixels
    - Stores pattern for a face (in a database)
    - Looks for patters (from the analysed pixels) that match face patterns
4. NLP (Natural Language Processing)
    - Uses speech recognition
    - Takes in a sentance and work out its meaning

![[Pasted image 20250414150624-1.png]]

```dataviewjs
const file = dv.current();
const checkboxes = file.file.tasks;
const totalCheckboxes = checkboxes.length;
const completedCheckboxes = checkboxes.filter(t => t.completed).length;

const completionPercentage = totalCheckboxes > 0 
    ? ((completedCheckboxes / totalCheckboxes) * 100).toFixed(2) 
    : "0.00";

try {
    await app.fileManager.processFrontMatter(dv.app.vault.getAbstractFileByPath(file.file.path), (frontmatter) => {
        frontmatter["completion"] = completionPercentage;
    });
    console.log("✅ Frontmatter updated successfully!");
} catch (error) {
    console.log(`❌ Error updating frontmatter: ${error}`);
}
```
