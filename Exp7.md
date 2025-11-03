# Use AFLogical OSE to Extract Data from an Android Device

## Aim
To perform logical data extraction from an Android device using AFLogical OSE and analyze the retrieved information such as contacts, call logs, SMS, and MMS.  
The goal is to understand Android forensic acquisition techniques and learn to retrieve data without rooting the device.  
This helps investigators preserve device integrity and perform evidence collection securely.

---

## Description
AFLogical OSE (Open Source Edition) is an Android forensic tool used to perform logical extraction, retrieving user-level data such as contacts, call logs, SMS, and MMS.  
It operates using Android Debug Bridge (ADB) to communicate with the device and stores results in CSV format for further analysis.  
It is widely used in forensic workflows due to its portability, ease of use, and minimal interference with device file systems.

---

## Procedure

### 1 — Prepare Your Environment**
1. Download AFLogical OSE from the GitHub repository or clone source files.
   > ![Screenshot](path/to/image1)
2. Install Java (required to run the tool).
   > ![Screenshot](path/to/image2)
3. Install ADB tools on your workstation.
   > ![Screenshot](path/to/image3)
4. Add ADB to system PATH for easy use.
   > ![Screenshot](path/to/image4)
5. Enable USB Debugging on the Android phone:  
   `Settings → About Phone → Tap Build Number (7 times) → Developer Options → Enable USB Debugging`
   > ![Screenshot](path/to/image5)

---

### 2 — Connect the Android Device**
1. Connect the Android phone to your computer via USB.
   > ![Screenshot](path/to/image6)
2. Verify connection:
   ```bash
   adb devices

### 3 — Extract Data Using AFLogical OSE
Navigate to AFLogical OSE location.


Install AFLogical OSE APK

Open AFLogical app → Select data types (contacts / SMS / MMS / call logs).

Begin extraction → Tool saves CSV data to /sdcard/aflogical


### 4 — Transfer Extracted Data to PC
Pull data using ADB:
Verify .csv files in saved folder.


### 5 — Analyze Extracted Data
Review data and document useful artifacts.


### 6 — Clean-up
Uninstall AFLogical OSE using:
Disconnect Android device safely.


## Result
Data from the Android device was successfully extracted using AFLogical OSE.
CSV files containing contacts, SMS, MMS, and call logs were obtained and analyzed for relevant forensic information.
This validated the effectiveness of AFLogical OSE for logical acquisition without accessing protected system partitions or requiring root access.