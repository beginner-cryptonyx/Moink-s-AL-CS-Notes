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
importance: 3
completion: "100.00"
modified:
  - 2025-04-20
  - 2025-04-15
marks-lost: 33
---
> [!grey]- Syllabus
> 
> 
> ## **3.1 Computers and Their Components**  
> **Candidates should be able to:**  
>  
> - [x] **Understand the need for:**  
>   - [x] Input devices  
>   - [x] Output devices  
>   - [x] Primary memory  
>   - [x] Secondary storage (*including removable storage*)  
>  
> - [x] **Understand embedded systems**  
>   - [x] *Benefits and drawbacks of embedded systems*  
>  
> - [x] **Describe principal operations of hardware devices:**  
>   - [x] Laser printer  
>   - [x] 3D printer  
>   - [x] Microphone  
>   - [x] Speakers  
>   - [x] Magnetic hard disk  
>   - [x] Solid-state (flash) memory  
>   - [x] Optical disc reader/writer  
>   - [x] Touchscreen  
>   - [x] Virtual reality headset  
>  
> - [x] **Understand the use of buffers**  
>  
> - [x] **Explain differences between:**  
>   - [x] **RAM vs. ROM** (*including their use in various devices and systems*)  
>   - [x] **SRAM vs. DRAM**  
>     - [x] *Usage in different devices and why one is preferred over the other*  
>   - [x] **PROM vs. EPROM vs. EEPROM**  
>  
> - [x] **Understand monitoring and control systems:**  
>   - [x] Difference between *monitoring* and *control* systems  
>   - [x] Use of **sensors** (*temperature, pressure, infrared, sound*) and **actuators**  
>   - [x] *Importance of feedback in control systems*  
>  
> ---  
>  
> ## **3.2 Logic Gates and Logic Circuits**  
> **Candidates should be able to:**  
>  
> - [x] **Recognize and use the following logic gate symbols:**  
>   - [x] NOT  
>   - [x] AND  
>   - [x] OR  
>   - [x] NAND  
>   - [x] NOR  
>   - [x] XOR  
>  
> - [x] **Understand and define the functions of:**  
>   - [x] NOT, AND, OR, NAND, NOR, and XOR (*EOR*) gates  
>   - [x] *All gates except NOT will have two inputs only*  
>  
> - [x] **Construct truth tables for each logic gate**  
>  
> - [x] **Construct a logic circuit from:**  
>   - [x] A problem statement  
>   - [x] A logic expression  
>   - [x] A truth table  
>  
> - [x] **Construct a truth table from:**  
>   - [x] A problem statement  
>   - [x] A logic circuit  
>   - [x] A logic expression  
>  
> - [x] **Construct a logic expression from:**  
>   - [x] A problem statement  
>   - [x] A logic circuit  
>   - [x] A truth table  


# Embedded systems
- Consist of micro processor, memory, and I/O capability that is **part of a larger system** which performs **one specialized task**

Advantages:
- Small in size and thus easy to implement into devices
- Relatively low cost
- Dedicated to one task
- Low power consumption
- Fast reaction to changing inputs
- Easier to achieve [[Economies of scale]] 

Disadvantages:
- Hard to upgrade
- Troubleshooting issues is now a specialist task
- Due to inability to upgrade, devices are more likely to be thrown away
- Can be subject to hackers and malware if it has connection to the internet

# Buffers
## General working
1. Computer and the device send and receive data at different speeds
2. The buffer allows for **temporary storage** of the data
3. Buffer synchronises the data transfer speed
4. Computer transfers data into buffer
	- If computer has a faster data transfer rate than the device
	- Allowing computer to carry on with other tasks
5. Device retrives data from buffers
	- Buffer checks if device is free to do the task
	- Printer buffer checks if data (document) is valid
6. When buffer is full/empty an interrupt is sent to the computer requesting for data or to stop sending data
7. This ensures that device is not overloaded
8. Helps instructions to be executed independantly of each other



## Buffer in optical disk
1. The computer and optical disc reader/writer send and receive data at **different speeds**
2. A buffer allows **temporary storage** of the data
3. The compuer can transfer data to the buffer at a higher speed
	- Thus the computer can carry on with other tasks
4. Buffer trasnfers data to the optical disc at a slower rate
	- This ensures that the disc reader/writer is not overloaded

# Memory Components

> [!multi-column]
>
>> [!error] Memory Components
>> **Random Access Memory (RAM)** :: Volatile memory that can be read from or written to any number of times
>> **Read Only Memory(ROM)** :: Non-volatile memory that cannot be written to but can be read any number of times
>
>> [!none]
>>```mermaid
>>graph TD
>>  PRIMARY_MEMORY[Primary Memory]
>>
>>  PRIMARY_MEMORY --> RAM[RAM]
>>  PRIMARY_MEMORY --> ROM[ROM]
>>
>>  RAM --> SRAM[SRAM]
>>  RAM --> DRAM[DRAM]
>>
>>  ROM --> PROM[PROM]
>>  ROM --> EPROM[EPROM]
>>  ROM --> EEPROM[EEPROM]
>>```


## RAM
- Random Access Memory
- Volatile
- Data stored can be changed by user or computer
- Stores data/part of application/part of OS that is currently under use
### SRAM
- Static RAM
- Constructed from arrangement of flip-flops
- No need for constant re-charging  
- Stores data indefinitely whilst computer is switched on
- Much faster *access times* compared to DRAM
- Used for cache memory 
### DRAM
- Dynamic RAM
- Constructed from capacitors which leak electricity
  - Each capacitor either holds charge or doesn't (1 or 0)
- Thus it needs recharging every few milliseconds
- Fewer components required per bit of storage
- Higher density for data storage
- Consume less power compared to SRAM
- **Cheaper**
- Used in main memory


## ROM
- Read only Memory
- Permanent memory device
- Non-volatile
- Data is read only (cannot be altered)
- Used to store **BIOS** and other **start up data**

### PROM
- Programmable Read Only Memory
- Can be altered **only once**
- PROM is made up of a matrix of fuzes
- PROM writer needed to program this memory
  - Uses electric current
  - alters specific cells by burning fuzes
- Used for mobile phones and RFID tags
### EPROM
- Erasable Programmable Read Only Memory
- Works via **floating gate transistors** and **capacitors**
- **UV light** used to program EPROM through a quartz window
- EPROM used for applications which are under development
- Requires chip to be removed from circuit
- Chip needs to entirely be wiped before rewriting
### EEPROM
- Electrically Erasable Programmable Read Only Memory
- Electrical signal used to remove data from ROM
- This can be done whilst the chip is in the circuit
- EEPROM does not need to be complexly erased before rewriting

# Storage Devices

## Magnetic Media
### Construction
1. Hard disk has one or more platters/disk
2. Each disk is made up of *ferrous oxide*, meaning it can be magnetized
3. Each disk is mounted on a central *spindle*
4. Each disk has a read/write head mounted on an arm positioned above surface of the disk
5. Each disk is divided into **concentric** circles called **Tracks**
6. These tracks are divided into **sectors**
7. Each track of a sector is the basic unit of storage, it is called a **block**
8. The entire mechanism is contained inside a sealed *aluminum* box

### Working Mechanism
1. The disks rotate at high speeds
2. Electric currents control the position of the arms, and thus the heads
3. Data is encoded in each block as a *magnetic pattern*
4. To write to the disk, an electric current in the head induces change of magnetic pattern
5. To read, the magnetic current will induce current in the head

## Optical Media
- Surface of a disk coated with light sensitive layer
- Disk tracks have pits and lands
- Motor used to spin disk
- Laser focused by a lens 
- Reflected light is encoded as a bit pattern
## Solid State Media
- No moving parts
- Non volatile
- Uses arrays of transistors
- SSD controller manages the components
- Made up of NAND and NOR gates
- Uses a grid of columns and rows that have 2 transistors at each intersection 
  - Each intersection called a memory cell
  - One transistor is called a floating gate transistor, retains electrons without power
  - The second one is called a control gate, allows or stops current from passing through
- Memory cells store voltages which represent either 1 or 0
- Movement of electrons is controlled to read or write
- Not possible to overwrite data (must be erased first)
# Output Devices
## Laser Printer
- Use powdered dry ink rather than liquid ink 
- Works on the principal of static electricity
- Unlike ink-jet, whole page is printed out at one go

Working:
1. Data from document sent to printer driver
2. Printer driver ensures format of data is correct
3. Printer driver ensures printer is able to print
4. Data sent to printer buffer
5. Printer drum is given a positive charge, laser scans across it to remove charge from some areas. Negative charge is given to areas where ink is to be applied
6. Drum is coated with positively charged toner, which sticks to negatively charged areas
7. Negatively charged paper is rolled over the drum
8. Toner sticks to paper
9. Charge is removed from paper
10. Paper goes through a set of heated rollers, which melt the ink onto paper
11. Discharge lamp removes all the charge form drum

## 3D Printer
- Uses *Additive* manufacturing where object is built layer by layer
- Printer head can move left to right and up to down
- Uses powdered material or resin or liquid polymers
- UV light and lasers used to harden polymers

Working:
1. 3D design made using CAD software
2. Design split into layers
3. Nozzle squirts material onto printer bed 
4. Process repeated for each layer
5. After completion the object has to be cured (eg: UV light)

## VR Headset
- Headset can have either 1 or 2 LCD screens 
- Headset has speakers that output surround sound for a realistic experience
- Head movements detected by gyroscope or accelerometer
- Data from headset sent to microprocessor
- Microprocessor calculates the direction and speed of head movements
- Digital cameras used to record and analyze users eye movements
## Speakers
![[Pasted image 20250411182123-1.png|float-right-small]]
1. Digital data converted to analogue data using DAC, outputs electric current
2. Current passed through an amplifier, as current by DAC is small
3. Current is fed to a speaker
4. Current flows through a coil of wire that is wrapped around an iron core, this becomes an electromagnet 
5. As the current varies, the attraction towards a permanent magnet, essentially causing a vibration
6. Core is attached to a cone, which produces the sound
   
---

# Input Devices
## Microphone
- Has a diaphragm
- Incoming sound waves cause vibrations of the diaphragm
- This causes a coil to move a magnet
- Inducing electrical current in a coil


## Touch Screen
### Resistive
- Has 2 layers
- When user touches the screen a circuit is completed
- Point of contact is registered
- Horizontal and vertical position is calculated

### Capacitive
- Made from materials thats electric charge
- When touched by finger, charge is transferred
- Sensors detect the change
- Point of contact is registered
- Coordinates used to calculate position

# Monitoring and Control Systems

> [!error] Definition
> **Sensor** :: a hardware device that measures a property and transmits a value to a computer
> **Actuator** :: A hardware device that receives a signal from a computer and adjusts the setting of a controlling device


## Monitoring Systems
 - Used to create a log or record of the conditions to be measured

## Control Systems
- Has capability of monitoring systems
- Also has capability of controlling the system (ie. output affects the next input/producing an action)
- Done via an actuator that is hooked up to a controlling device

1. Sensor sends data to microprocessor or computer
2. Signals converted from analogue to digital via ADC if needed

### Importance of feedback in control systems
- The output of the control system effects the subsequent input
- Thus conditions are automatically adjusted
- This allows the system to operate within a given criteria

## Sensors
1. Temperature
2. Pressure
3. Infra-red :: detects motion
4. Sound
5. pH
6. Moisture
7. Humidity
8. Precipitation :: measures amount of rainfall


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
