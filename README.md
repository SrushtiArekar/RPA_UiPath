# Srushti Arekar - RPA UiPath Portfolio

This repository showcases some of the UiPath automation projects I have built while transitioning into RPA.

## 📁 Projects

### 🔹 [RPA Project – Dynamic Form Data Entry](https://github.com/SrushtiArekar/UiPath-Portfolio/tree/main/RPAChallenge)

A UiPath automation project that reads structured data from an Excel file and submits it into the dynamic web form at [rpachallenge.com](https://rpachallenge.com/).

**Key Highlights:**
- Reads data row by row from Excel
- Uses `Anchor Base` to dynamically identify form fields
- Handles randomly changing field order on the form
- Submits each form and loops through all Excel rows
- Built using `Type Into`, `Click`, `For Each Row`, and `Anchor Base` activities

**Technologies:** UiPath Studio, Excel Activities, UIAutomation, DataTables  
**Input:** `RPAChallenge.xlsx`  
**Output:** Successful submission of all data rows on the website 

### 🔹 [RPA Project_REFramework – Queue-based Data Entry with REFramework](https://github.com/SrushtiArekar/UiPath-Portfolio/tree/main/RPAChallengeUsingREFramework)

An advanced UiPath project implementing the RPA Challenge using **REFramework**, **Orchestrator Queues**, and **Assets**.

**Key Highlights:**
- Uses Queue-based transaction processing
- Assets-driven configuration for file path and URL
- Dynamic field mapping using `Anchor Base`
- Robust error handling with retry, logging, exception screens
- Fully aligned with enterprise UiPath best practices

**Technologies:** REFramework, Orchestrator Queues, Assets, Excel Activities, UI Automation  
**Input:** Excel data as queue items  
**Output:** Successful web form submission per transaction item

### 🔹 [REFramework Project – Accrual Journal Entry Automation in JD Edwards](https://github.com/SrushtiArekar/UiPath-Portfolio/tree/main/RPA_JDEdwards_REFramework)

An enterprise-grade automation using UiPath REFramework that **reads data from an Accrual Excel file** and **performs end-to-end Journal Entry** posting **in JD Edwards EnterpriseOne**. The automation **retrieves the generated Batch Number**, **prepares a consolidated PDF report**, and **delivers it to stakeholders via email**.

**Key Highlights:**
- Reads line-wise transactional data from Accrual Excel input
- Uses Assets to configure input file path and JD Edwards URL
- Pushes each row as a Queue Item to Orchestrator Queues
- Leverages REFramework for robust, retry-safe transaction processing
- Automates the JD Edwards menu navigation and opens the Journal Entry form
- Enters data into the grid line by line to create journal entries
- Extracts the Batch Number once the transaction is submitted
- Executes General Journal by Batch Report using the Batch Number
- Downloads the generated report in PDF format
- Converts the Accrual Excel into a PDF
- Merges Accrual PDF + JD Edwards Report to form a final consolidated document
- Sends the final report to designated stakeholders via email
- Gracefully handles System and Business Exceptions using REFramework best practices

**Technologies:** UiPath REFramework, Orchestrator Queues, Assets, Excel Activities, UI Automation, JD Edwards ERP, PDF Activities, Email Automation
**Input:** Accrual_Report Excel File
**Output:** Journal Entry Posted in JD Edwards + Final Report (PDF) emailed to stakeholders


