# Recover Deleted or Damaged Files Using TestDisk

## Aim

To recover missing, deleted, or damaged files and partitions from a storage device using the TestDisk utility, demonstrating the detection and repair process for typical data loss scenarios.

## Description

TestDisk is a free and open-source forensic recovery tool designed to recover lost partitions and repair damaged file systems.  
It supports multiple partition table types, file system structures, and boot sectors.  
The tool allows investigators to perform partition analysis, quick and deep searches, file listing, partition recovery, and NTFS boot sector repair, making it effective for both simple and advanced recovery scenarios.

## Procedure

1. Launch TestDisk and create a recovery log.  
![alt text](<Screenshots/Ex2-ss/Screenshot 2025-09-02 213908.png>)

2. Select the correct storage device from the list (using raw device for faster data transfer if available).  
![alt text](<Screenshots/Ex2-ss/Screenshot 2025-09-02 213928.png>)

3. TestDisk automatically detects the partition table type (Intel/PC, EFI/GPT, etc.) and suggests the default option.  
![alt text](<Screenshots/Ex2-ss/Screenshot 2025-09-02 214026.png>)

4. View the current partition table and choose the "Analyse" menu to examine existing partitions.  
![alt text](<Screenshots/Ex2-ss/Screenshot 2025-09-02 214041.png>)

5. Run a Quick Search to detect lost or deleted partitions.  
   - Use `p` to list files within discovered partitions.  
   - Deleted entries are highlighted in red.  
![alt text](<Screenshots/Ex2-ss/Screenshot 2025-09-02 214126.png>)

6. If partitions are recovered, use the "Write" option to save the updated table.  
   - If not, perform a Deeper Search to locate additional partitions using backup boot sectors or superblocks.  
![alt text](<Screenshots/Ex2-ss/Screenshot 2025-09-02 214144.png>)

7. Review deeper search results to resolve overlapping or duplicated partitions.  
   - Adjust partition status (Primary, Bootable, Logical, Deleted) as required.  
![alt text](<Screenshots/Ex2-ss/Screenshot 2025-09-02 214453.png>)

8. Confirm recovery by writing the corrected partition structure to disk.  
![alt text](<Screenshots/Ex2-ss/Screenshot 2025-09-02 214521.png>)

 
9. Reboot the system to finalize recovery and access restored partitions and files.
![alt text](<Screenshots/Ex2-ss/Screenshot 2025-09-02 214548.png>)


## Result
Successfully detected and restored deleted or corrupted partitions, file systems, and boot sectors using TestDisk.  
Recovered data became accessible after system reboot, demonstrating the effectiveness of TestDisk as a free and reliable forensic recovery tool.
