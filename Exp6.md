# Use Sleuth Kit to Analyze Digital Evidence

## Aim
The aim of this experiment is to analyze a forensic disk image using Sleuth Kit (TSK) to examine file systems, extract information, and recover deleted files.  
This process helps identify digital artifacts relevant to an investigation.  
The experiment demonstrates forensic acquisition and analysis workflow using CLI tools.  
It also helps understand how investigators handle evidence without altering its original contents.

---

## Description
The Sleuth Kit (TSK) is an open-source collection of command-line forensic tools used to examine disk images.  
It supports formats such as `.dd`, `.raw`, `.img`, and `.E01`, allowing investigators to view filesystem structures, metadata, deleted files, and timestamps.  
TSK is widely used across digital forensics, cybersecurity investigations, and incident response.  
With TSK, evidence integrity is preserved because all operations are read-only.  
This experiment highlights how Sleuth Kit’s utilities help analysts interpret filesystem data and extract vital digital evidence.

---

## Procedure  

---

### 1) Install Sleuth Kit
Download and install Sleuth Kit from the official website or shared link.

Visit official Sleuth Kit website or provided Google Drive link.
Install using Windows installer.


![Step 1 Screenshot]

---

### 2) Acquire / Download Disk Image
Download the sample `.E01` evidence files:  
- `4Dell Latitude CPi.E01`  
- `4Dell Latitude CPi.E02`

![Step 2 Screenshot]

---

### 3) (Optional) Mount the Disk Image
Use OSFMount to mount the image as a virtual drive to view file structure.

![Step 3 Screenshot]

---

### 4) Open Sleuth Kit in Terminal
Navigate to the Sleuth Kit installation directory from CMD.



### 5) Identify File System Type
Run fsstat to view filesystem information.


### 6) List Partitions
Use mmls to list the partitions available in the disk image.


### 7) List Files & Directories
Recursively list file system entries using fls.


### 8) Recover Deleted Files
Use icat to extract deleted files based on inode number.


### 9) View File Metadata
Use istat to inspect metadata of a specific file.


### 10) (Optional) Timeline Analysis
Generate a body file
Then generate timeline


### 11) Document & Report Findings
Gather all exported files:

filesystem_info.txt
partitions.txt
file_list.txt
metadata_info.txt
timeline.txt

Analyze the extracted data and prepare a report summarizing the evidence.


## Result
Sleuth Kit was successfully used to analyze the provided forensic disk image.
The tools enabled partition inspection, recursive file listing, metadata analysis, and recovery of deleted artifacts.
Optional timeline analysis helped in understanding event chronology.
This demonstrates Sleuth Kit’s capability in real-world forensic workflows supporting evidence acquisition and investigation.