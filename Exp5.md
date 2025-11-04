# Use Autopsy to Create a Case and Import Evidence

## Aim
To learn how to use Autopsy, an open-source digital forensics platform, to create a case, import digital evidence, and perform basic forensic analysis.

---

## Description
Autopsy is an open-source digital forensics platform used for analyzing and extracting data from digital devices. This lab provides a step-by-step process to perform a basic forensic investigation using Autopsy, including case creation, data source import, analysis, and reporting.


---

## Procedure

### 1. Installation
- Download Autopsy from the [official website](https://www.autopsy.com/) and install it according to your operating system (Windows, Linux, or macOS).

![alt text](<Screenshots/Ex5-ss/Screenshot 2025-11-04 210613.png>)


### 2. Starting a New Case
- Open Autopsy after installation.
- Click on **New Case**.
- Enter the case name, location, case number, and examiner’s name.
- Click **Next**.

![New Case Setup]




### 3. Adding a Data Source
- Select the type of data source (e.g., disk image, directory, logical files).
- Browse and select the evidence file (e.g., `4Dell Latitude CPi.E01`).
- Configure ingest modules (e.g., File Type Identification, Keyword Search, Hash Lookup).
- Click **Next** to begin analysis.

![Add Data Source]



### 4. Initial Analysis and Overview
- Monitor the ingest progress in the lower-left corner.
- Explore automatically categorized artifacts like web history, file system metadata, and emails using the Tree Viewer.

![Ingest Progress]



### 5. Detailed Analysis
- Use the **Keyword Search** module to search for specific terms.
- Navigate through files and folders in the **File System** section.
- Use the **Timeline** module to view events chronologically.
- Perform **Hash Analysis** to identify known files.

![Keyword Search]


### 6. Reporting
- Click **Generate Report** from the toolbar.
- Choose the report format (HTML, CSV, Excel, etc.).
- Select the content to include and export the report.

![Generate Report]


### 7. Case Closure
- Close the case once the investigation is complete.
- Archive all data and reports as per organizational policies.


### 8. Advanced Features (Optional)
- Add custom ingest modules for specialized analysis.
- Configure multi-user access for team collaboration.


## Result

Successfully created a case in Autopsy, imported and analyzed digital evidence, and generated a forensic report. Gained hands-on experience with key digital forensics workflows including data ingestion, keyword search, timeline analysis, and reporting.

---