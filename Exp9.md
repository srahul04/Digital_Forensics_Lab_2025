# Ex.No.9 — Use Process Explorer to Identify Suspicious Processes

## Aim
To analyze active processes using Process Explorer and identify suspicious or potentially malicious activity.  
This experiment demonstrates the ability to assess process legitimacy through signature verification, resource usage, and network behavior.  
It also enhances investigative skills necessary for malware detection and system forensics.

---

## Description
Process Explorer is an advanced Sysinternals tool for Windows that displays detailed information about active processes.  
It helps investigators detect harmful or unknown processes by examining their execution path, digital signatures, resource consumption, and network communication.  
The hierarchical view and color-coded structure make it a powerful utility for system monitoring, malware hunting, and forensic analysis.

---

## Procedure

### 1) Download and Set Up Process Explorer
1. Download Process Explorer from the official Microsoft Sysinternals website.  

2. Extract the downloaded ZIP file.  

3. Run `procexp64.exe` (64-bit) or `procexp.exe` (32-bit) as Administrator.  
  



### 2) Familiarize Yourself with the Interface
1. Review the hierarchical process tree.  
   - Color indicators:  
     - Pink → Suspended  
     - Light Blue → Same user  
     - Dark Blue → System service  
     - Green → Newly launched  
     - Red → Recently exited  
   >

2. Observe columns such as PID, CPU, Memory usage, etc.  




### 3) Identify Suspicious Processes
1. Look for unknown or strange process names.  

2. Verify digital signatures:  
   Right-click → **Properties → Image tab → Signature**  

3. Check execution path; ensure it’s in a trusted directory like `C:\Windows\System32`.  

4. Examine CPU, memory, and disk usage for unusual spikes.  

5. Review process description and company name.  

6. Check network activity:  
   Right-click → **Properties → TCP/IP**  



### 4) Research Suspicious Processes
1. Search online using the process name (e.g., via Google).  

2. Check malware databases such as VirusTotal / ProcessLibrary.  




### 5) Kill or Suspend Suspicious Processes
1. Right-click → **Kill Process** to terminate.  

2. Right-click → **Suspend** to temporarily stop execution.  

3. Navigate to its path and delete the executable if confirmed malicious.  



### 6) Example — Detecting a Malicious Process
1. A process named `randomname123.exe` shows high CPU usage.  
2. Executable path is not a system directory.  
3. TCP/IP tab reveals suspicious outbound connections.  
4. Online research identifies it as malware.  
5. Process terminated and file removed.  
   > ![Screenshot](path/to/image19)

---

## Result
Suspicious processes were identified based on signature validation, execution path verification, resource usage, and network behavior.  
Process Explorer proved effective for detecting and investigating malicious or abnormal processes, strengthening forensic analysis skills and enhancing system security.

---
