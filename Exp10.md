# Use Ghidra to Disassemble and Analyze Malware Code

--- 

## Aim

To provide a hands-on walkthrough for disassembling and analyzing suspicious binaries using Ghidra.  
This experiment aims to teach how to perform static analysis, interpret assembly and decompiled output, and identify common malicious behaviors such as persistence, anti-analysis, and network activity.  
Participants will learn safe analysis practices in an isolated environment and how to document findings for reporting or incident response.  
By the end, users should be able to locate key functions, extract indicators of compromise (IoCs), and automate repetitive analysis tasks with scripts.

---

## Description

Ghidra is a free, open-source reverse engineering suite developed by the NSA. It provides powerful disassembly, decompilation, symbol and data type management, cross-references, and scripting capabilities (Java/Python).  
This experiment covers preparing an isolated analysis environment, importing a binary into Ghidra, running auto-analysis, performing function and string analysis, annotating disassembly/decompiler output, and using headless automation for batch processing.  
Because analyzing live malware is risky, this project recommends using benign samples or generated test binaries that simulate malware-like behaviors to practice techniques safely.  
A companion GitHub repository structure (README, tutorial steps, scripts, samples, templates, screenshots) is suggested to document and share the workflow.

---

## Procedure

> After each numbered point below, add a screenshot (insert image in your repo) showing the action or output.

1) **Prepare a Safe Analysis Environment**  
   - Set up an isolated VM (offline if possible) with snapshots enabled.  
   - Install Ghidra on the VM and ensure no host networking access for the VM unless required and controlled.  
   - Confirm Java is installed (Ghidra requires a compatible JRE/JDK).  

   ![alt text](<Screenshot From 2025-10-26 01-09-37.png>)


2) **Obtain / Prepare Sample Binary**  
   - Use only benign or purpose-built samples (do not include live malware in public repos).  
   - Option: use a hex dump or a dummy binary generator script to simulate suspicious behaviors.  
   - Place sample(s) under `samples/` in your repository.  

   ![alt text](<Screenshot From 2025-10-26 01-17-47.png>)


3) **Create Project & Import Binary into Ghidra**  
   - Open Ghidra → File → New Project → choose Non-Shared Project.  
   - Import the binary: File → Import File → follow prompts and accept suggested language/format if detected.  
   - Run the initial Auto-Analysis (accept defaults or tune options as needed).  

   ![alt text](<Screenshot From 2025-10-26 01-17-47-1.png>)

   

4) **Initial Triage: Entry Points, Sections & Strings**  
   - Inspect Program Tree and Memory Map to locate .text/.data sections and entry points.  
   - Use the **Strings** window to list readable strings (URLs, file names, commands).  
   - Note suspicious strings for IoCs (domains, IPs, file paths).  

   ![alt text](<Screenshot From 2025-10-26 01-24-19.png>)

5) **Function Discovery & Cross-Referencing**  
   - Open the Function Graph / Symbol Tree and identify major functions (main, init, network routines).  
   - Use Xrefs (cross references) to see where strings and functions are used.  
   - Rename functions and add comments/labels for clarity.  
   ![alt text](<Screenshot From 2025-10-26 01-26-32.png>)

6) **Decompile Key Functions**  
   - Use the Decompiler window to get C-like pseudocode for interesting functions.  
   - Analyze control flow, conditional logic, and API calls (file I/O, registry, sockets).  
   - Add comments explaining observed behaviors (persistence, data exfiltration, obfuscation).  

   ![alt text](<Screenshot From 2025-10-26 01-26-44.png>)
   

7) **API/Import Analysis**  
   - Inspect imported libraries and API calls (e.g., WinAPI functions such as CreateService, RegSetValue, InternetConnect, socket functions).  
   - Map imports to behaviors (persistence, privilege escalation, networking).  

![alt text](<Screenshot From 2025-10-26 01-40-45.png>)

   

8) **Identify Anti-Analysis & Obfuscation Techniques**  
   - Look for packing, heavy use of indirect calls, dynamic API resolution, or encrypted strings.  
   - Note any time-based checks, debugger detection, or virtualization checks.  
   

9) **Build a Timeline & Behavioral Summary**  
   - Document the sequence of operations (what runs first, actions performed, network or file system interactions).  
   - Extract potential indicators (file names, registry keys, domains/IPs, mutexes).  

   ![alt text](<Screenshot From 2025-10-26 01-43-13.png>)

   ![alt text](<Screenshot From 2025-10-26 01-44-00.png>)



10) **Export Findings & Reporting**  
    - Prepare a structured analysis report (use `templates/analysis_report_template.md`) containing summary, function analysis, IoCs, recommended mitigations, and suggested next steps.  
    - Include annotated screenshots and code snippets from Ghidra views.  
    

---

## Result
Ghidra successfully disassembled and analyzed the sample binary.  
Key functions, strings, and imports were identified, allowing basic understanding of the program’s behavior.  
This confirmed that Ghidra is effective for safe static malware analysis in an isolated environment.


---
