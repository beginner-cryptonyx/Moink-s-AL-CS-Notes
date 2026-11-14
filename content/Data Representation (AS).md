---
subject:
  - "[[Computer Science]]"
grade:
  - "[[AS Level]]"
related:
creation-date: 2025-03-29
up:
  - "[[Computer Science]]"
tags:
aliases:
completion: "100.00"
importance: 1
modified:
  - 2025-06-16
  - 2025-05-05
  - 2025-05-04
  - 2025-05-03
  - 2025-05-02
  - 2025-04-20
  - 2025-04-16
  - 2025-04-15
marks-lost: 56
topical: "[[Data Representation Topical Analysis]]"
---

> [!grey]- Computer Science 9618 Syllabus
> 
> 
> ## ✅ Computer Science 9618 Checklist  
>  
> ---  
>  
> ### **1.1 Data Representation**  
> **Candidates should be able to:**  
>  
> - [x] **Understand binary magnitudes** and the difference between binary and decimal prefixes  
>   - [x] *Kibi (Ki) vs. Kilo (K)*  
>   - [x] *Mebi (Mi) vs. Mega (M)*  
>   - [x] *Gibi (Gi) vs. Giga (G)*  
>   - [x] *Tebi (Ti) vs. Tera (T)*  
>  
> - [x] **Understand different number systems:**  
>   - [x] Binary  
>   - [x] Denary  
>   - [x] Hexadecimal  
>   - [x] Binary Coded Decimal (BCD)  
>   - [x] One’s and Two’s complement representation  
>  
> - [x] Convert an integer value from one number base/representation to another  
>  
> - [x] **Perform binary arithmetic:**  
>   - [x] Binary addition  
>   - [x] Binary subtraction (positive & negative integers)  
>   - [x] Understand how *overflow* can occur  
>  
> - [x] **Describe practical applications** where BCD and hexadecimal are used  
>  
> - [x] **Understand character data representation**  
>   - [x] ASCII, Extended ASCII, and Unicode  
>   - [x] Internal binary representation of characters  
>   - *No need to memorize specific character codes*  
>  
> ---  
>  
> ### **1.2 Multimedia**  
> #### **Graphics**  
> **Candidates should be able to:**  
>  
> - [x] Understand how **bitmapped images** are encoded  
> - [x] Use and understand the following terms:  
>   - [x] *Pixel*  
>   - [x] *File header*  
>   - [x] *Image resolution & screen resolution*  
>   - [x] *Colour depth / Bit depth*  
>  
> - [x] **Perform calculations** to estimate bitmap file size  
> - [x] **Understand the effects** of modifying bitmap properties on image quality & file size  
>  
> - [x] Understand how **vector graphics** are encoded  
>   - [x] Use the terms: *Drawing object, Property, Drawing list*  
> - [x] **Justify the use** of bitmap vs. Vector graphics for different tasks  
>  
> #### **Sound**  
> **Candidates should be able to:**  
>  
> - [x] Understand how **sound is represented & encoded**  
> - [x] Use the following terms:  
>   - [x] *Sampling*  
>   - [x] *Sampling rate & Sampling resolution*  
>   - [x] *Analogue vs. Digital data*  
>  
> - [x] **Analyze the impact** of changing sampling rate & resolution  
>   - [x] Effect on *file size & accuracy*  
>  
> ---  
>  
> ### **1.3 Compression**  
> **Candidates should be able to:**  
>  
> - [x] **Understand the need for compression** and its real-world applications  
> - [x] Differentiate between **lossy vs. Lossless compression**  
>   - [x] Justify the use of either method based on the scenario  
> - [x] **Understand compression techniques for different file types:**  
>   - [x] Text files  
>   - [x] Bitmap images  
>   - [x] Vector graphics  
>   - [x] Sound files  
>   - [x] *Use of Run-Length Encoding (RLE)*  
>  
> ---  


# Data Representation
## Binary magnitudes

> [!tip]
> IEC format is more accurate as storage is measured in binary


Denary format:

| Name of Memory Size | Equivalent Denary Value (Bytes) |
|---------------------|--------------------------------|
| **1 Kilobyte (1KB)**   | **1,000**                          |
| 1 Megabyte (1MB)   | 1,000,000                      |
| 1 Gigabyte (1GB)   | 1,000,000,000                  |
| 1 Terabyte (1TB)   | 1,000,000,000,000              |
| 1 Petabyte (1PB)   | 1,000,000,000,000,000          |

Binary Format: (IEC)

| Name of Memory Size  | Number of Bytes | Equivalent Denary Value (Bytes) |
|----------------------|----------------|---------------------------------|
| **1 Kibibyte (1KiB)**   | **2¹⁰**            | 1,024                           |
| 1 Mebibyte (1MiB)   | 2²⁰            | 1,048,576                       |
| 1 Gibibyte (1GiB)   | 2³⁰            | 1,073,741,824                   |
| 1 Tebibyte (1TiB)   | 2⁴⁰            | 1,099,511,627,776               |
| 1 Pebibyte (1PiB)   | 2⁵⁰            | 1,125,899,906,842,624           |



---

> [!error|float-medium-right]
> **Bit** :: a digit in the binary system written using either 0 or 1
> **Byte** :: A group of 8  bits
> **Nibble** :: a group of 4 bits
> **Denary** :: also known as decimal numbers using numbers from 0 to 9 for each digit


## Number systems

### Binary
- Base 2 system
- Each digit is Either 0 or 1
- Each digit is referred to as a **bit**


### Denary
- Base 10
- Uses symbols *0* -> *9* for each digit


### Hexadecimal
- Base 16 system
- Uses symbols *A* -> *F* (representing numbers 10 -> 15) and *0* -> *9*
- One digit on hexadecimal represents one *nibble* of binary data

Applications:
1. MAC addresses
2. HTML color codes
3. Memory addresses in assembly

### BCD

Benefits:
1. More straightforward to convert from and to denary
2. Less complicated for developers to encode and decode
3. Easier for digital equipment to use BCD to display information

Applications:
1. Electronic displays like calculators
2. Date and time storage in BIOS of PC

### Overflow
### Internal coding of numbers
> [!error]
> **One's complement** :: Binary number obtained by subtracting each digit in a binary number from 1
> **Two's complement** :: One's complement of a number, plus 1 
#### One's complement 

- To convert binary to one's compliment, flip all the bits

#### Two's complement
- Convert number to one's compliment
- Add one


## Character data representation
- A Character set is a list of **ALL** symbols a computer can represent
- Each character has an unique binary number associated with it

![[ASCII]]
![[Extended ASCII]]
![[Unicode]]


### Binary representation

# Multimedia

> [!error] Types of data
> **analogue** :: Data that varies **continuously** and can take **any value within a range**
> **digital** :: Data that is **discrete** and represented using **binary values (0s and 1s)**

## Graphics


### Bitmap
> [!error]
> **Pixel** :: Single square of one color which is the smallest addressable element in an image
> **File Header** :: Contains data about the bitmap image like file size, dimensions and color depth
> **Image Resolution** :: Number of pixels wide by the number of pixels high
> **Bit Depth** :: The number of bits used to represent each color

- Made up of pixels, each having a single color
- Stored as a sequence of binary numbers

#### File header
- Dimensions
- File size
- Bit Depth
- Compression type
- Filetype
- Image resolution
- Color palette


### Vector

#### Vector Image components
1. Drawing object :: An individual shape defined using mathematics/geometry
2. Property :: Contains data about each shape
   - Line color
   - Line width
   - Fill color
   - Shape
   - Outline style
   - Size
   - Position
3. Drawing List :: A list that stores all the commands required to draw each object 

#### Benefits:
1. Can be enlarged without pixelation (loss of quality)
2. Individual components of the image can be edited
3. Generally smaller file size

### Vector vs Bitmap

|             | Vector                                                 | Bitmap                                         |
| ----------- | ------------------------------------------------------ | ---------------------------------------------- |
| Storage     | Set of instructions on how to draw the shape           | Pixels, each one having a color                |
| Pixelation  | No pixelation, as it recalculates upon resizing        | Pixelation, as each pixel gets bigger          |
| Size        | Smaller, only instructions to create shape             | Larger, data for each pixel needs to be stored |
| Compression | Less compression as very little redundant data present | Significant compression power                  |


## Sounds

### Sound encoding
> [!error] Definition
> Sampling :: Measuring the amplitude of the sound wave at regular intervals
> Sampling rate :: Number of samples taken per unit time
> Sampling resolution :: The number of bits used to represent each sample

- Amplitude is recorded a set number of times a second
- Each instance of an amplitude is given a corresponding binary number
- The binary number of each amplitude is saved in sequence

#### Impacts of changing sound sampling rate and resolution
Increasing sampling rate:
  - Smaller gaps in the sound wave as sound is recorded more often
  - Digital waveform is closer to the analogue waveform
  - Smaller quantisation errors
  - More accurate
  - File size increases
  - Increases amount of detail stored

Increasing sampling resolution:
  - More bits per sample -> more range of amplitudes can be stored
  - Each digital amplitude is closer to the analogue amplitude
  - Digital waveform is closer to the analogue waveform
  - The quantisation errors are smaller
  - More accurate
  - File size increases
  - Increases amount of detail stored


# Compression

## Reasons for compression
1. Reduces file size
2. Faster to upload/download
3. Original file too large to be used as attachment
4. Reduced bandwidth when transmitted
5. Reduced transmission time


> [!error] Compression
> **Lossless** :: a method of data compression where no data is lost during the process, allowing the exact original file to be reconstructed from the compressed file
> **Lossy** :: a method of data compression where some data is permanently removed, resulting in a reduced file size but making it impossible to fully restore the original data


## Compression of different file types
### Text
Lossy:
- Lossless compression not possible as none of the data can be lost
- If lossless compression done, then text file would be corrupted

Lossless:
- RLE used
- Identifies group of repeating characters
- Replaces them with one copy of the character's ASCII value and the amount of times it occurs

### Images
Lossy:
1. Reduce bit depth
   - Reduce number of bits per pixel
2. Reduce color palette
   - Reduce number of bits per color
3. Reduce image resolution
   - Fewer pixels per unit measurement -> less binary

Lossless:


Why lossless may not work:
- RLE stores color and the number of times it occurs consecutively 
- A Image may not have many sequences of the same color
- It would need to store number of times it repeats, which adds data


### Sounds
Lossy:
- Amplitude can be reduced
- Limited amplitude means fewer samples

Justification:
1. Human ear will not be able to notice (human ear can only hear from 20Hz to 20KHz) that some parts of audio have been removed
2. File size reduction is greater in lossy compression
3. File does not have to be high precision

Lossless:
- RLE
  - Binary of consecutive sounds along with number of times it has been repeated
- Record changes instead of sounds

Justification:
1. File needs high accuracy
2. None of the original data is lost


### RLE
- Replaces repeating sequence of same data with the data and number of repetitions
---

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