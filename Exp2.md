# Recover Deleted or Damaged Files Using TestDisk

## Aim
To recover missing, deleted, or damaged files and partitions from a storage device using the TestDisk utility, demonstrating the detection and repair process for typical data loss scenarios.

## Description
TestDisk is a free and open-source forensic recovery tool designed to recover lost partitions and repair damaged file systems.  
It supports multiple partition table types, file system structures, and boot sectors.  
The tool allows investigators to perform partition analysis, quick and deep searches, file listing, partition recovery, and NTFS boot sector repair, making it effective for both simple and advanced recovery scenarios.

## Procedure
1. Launch TestDisk and create a recovery log.  
2. Select the correct storage device from the list (using raw device for faster data transfer if available).  
3. TestDisk automatically detects the partition table type (Intel/PC, EFI/GPT, etc.) and suggests the default option.  
4. View the current partition table and choose the "Analyse" menu to examine existing partitions.  
5. Run a Quick Search to detect lost or deleted partitions.  
   - Use `p` to list files within discovered partitions.  
   - Deleted entries are highlighted in red.  
6. If partitions are recovered, use the "Write" option to save the updated table.  
   - If not, perform a Deeper Search to locate additional partitions using backup boot sectors or superblocks.  
7. Review deeper search results to resolve overlapping or duplicated partitions.  
   - Adjust partition status (Primary, Bootable, Logical, Deleted) as required.  
8. Confirm recovery by writing the corrected partition structure to disk.  
9. For NTFS partitions, use the "Backup BS" option to repair corrupted boot sectors with a valid backup.  
10. Reboot the system to finalize recovery and access restored partitions and files.

## Result
Successfully detected and restored deleted or corrupted partitions, file systems, and boot sectors using TestDisk.  
Recovered data became accessible after system reboot, demonstrating the effectiveness of TestDisk as a free and reliable forensic recovery tool.
