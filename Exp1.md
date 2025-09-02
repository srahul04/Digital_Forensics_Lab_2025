# Evidence Acquisition Using AccessData FTK Imager

## Aim

To acquire and verify digital forensic evidence using AccessData FTK Imager, including both volatile (RAM) and non-volatile (disk) memory, and to understand various image formats and integrity verification techniques.

## Description

Forensic Toolkit (FTK) Imager is a Windows-based tool developed by AccessData for acquiring and analyzing computer forensic evidence. It supports both live (volatile memory) and offline (disk image) evidence acquisition. The collected data can be stored in multiple formats for subsequent analysis, ensuring integrity and reliability of forensic processes.

## Procedure

### Acquiring Volatile Memory (RAM)

1. Open FTK Imager on the target system.

![alt text](<Screenshots/Ex1-ss/Screenshot 2025-09-02 152712.png>) 


2. Navigate to the volatile memory icon and select Capture Memory.
![alt text](<Screenshots/Ex1-ss/Screenshot 2025-09-02 152836.png>)

3. Optionally include:  
   - Pagefile.sys: Captures additional RAM spillage from system partition.  
   - AD1 file: Proprietary AccessData image format for later use.
   ![alt text](<Screenshots/Ex1-ss/Screenshot 2025-09-02 211355.png>)

4. Click the Capture Memory button. 
![alt text](<Screenshots/Ex1-ss/Screenshot 2025-09-02 153219.png>)

5. Upon completion, note the `.mem` extension of the output file in the destination folder.  
![text](<Screenshots/Ex1-ss/Screenshot 2025-09-02 153503.png>)


## Result

- Successfully acquired RAM using FTK Imager in multiple formats.   
- Generated evidence files can be used for further forensic analysis.  
