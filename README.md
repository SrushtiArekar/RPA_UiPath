# UiPath Portfolio – Srushti Arekar

This repository showcases some of the UiPath automation projects I have built while transitioning into RPA.

## 📁 Projects

### 🔹 [RPAChallenge1 – Dynamic Form Data Entry](https://github.com/SrushtiArekar/UiPath-Portfolio/tree/main/RPAChallenge)

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

### 🔹 [RPAChallenge_REFramework – Queue-based Data Entry with REFramework](https://github.com/SrushtiArekar/UiPath-Portfolio/tree/main/RPAChallengeUsingREFramework)

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
