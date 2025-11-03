# Ex.No.8 — Use StegExpose to Detect Hidden Data in Images

## Aim
To detect the presence of hidden information (steganography) inside digital images using the StegExpose tool.  
This experiment helps understand forensic techniques to analyze stego-images and interpret confidence scores.  
It also demonstrates how fast bulk detection can be done using command-line analysis without modifying image data.

---

## Description
StegExpose is a Java-based steganalysis tool that identifies hidden data in images by evaluating statistical signatures.  
It supports formats including PNG, JPG, and BMP, and assigns a “suspect” score (0–1) indicating the likelihood of hidden data.  
A higher score increases the probability that steganography is present, making it useful in cyber forensics investigations.

---

## Procedure

### **1) Install Required Tools**
1. Download **StegExpose** `.jar` file from its official GitHub repository.

2. Install **Java Runtime Environment (JRE)** on your system.
 
3. Place the `.jar` file in a working directory along with target images.
   

---

### **2) Prepare Images for Analysis**
1. Collect all suspected images (formats supported: `.png`, `.jpg`, `.bmp`, etc.)
  

---

### **3) Open Command Line**
1. Navigate to the directory containing StegExpose `.jar` file.

2. Open:
   - **Command Prompt** (Windows)  
   - **Terminal** (Linux/MacOS)
   


### **4) Run StegExpose on a Single Image**
1. Execute:
   
   java -jar StegExpose.jar 


### 5) Analyze Output
StegExpose returns a suspect score between 0 and 1.

Interpretation thresholds

< 0.2 → Clean
0.2 – 0.3 → Possibly hidden data
> 0.3 → Steganography likely


### 6) Batch Analysis (Folder)
Analyze multiple images at once:

java -jar StegExpose.jar <folder_path>


### 7) Use Advanced Options (Optional)
View available options:

java -jar StegExpose.jar --help


### 8) Review Results
Check suspect scores and flag images requiring deeper investigation.


java -jar StegExpose.jar suspect_image.png


Analyzing suspect_image.png...
Result: 0.4
Steganography likely present


--- 


## Result
StegExpose successfully analyzed the provided images and produced confidence scores indicating the likelihood of hidden data.
Images scoring above threshold (0.3) were identified as potentially containing steganographic content, supporting further forensic examination.
Thus, StegExpose proved effective for rapid stego-image detection in forensic workflows.

---
