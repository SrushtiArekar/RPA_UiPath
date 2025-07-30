# 🤖 RPA Project_REFramework – Journal Entry Processing in JD Edwards using RPA REFramework

This project automation project uses the **Robotic Enterprise Framework (REFramework)** to automate the process of **creating Journal Entries** in **JD Edwards EnterpriseOne (ERP System)**.


---

## 🚀 What It Does

This process will read the data from Accrual excel file and create Journal entry in JD Edwards system. The Journal entry is created, and the batch number is extracted from JD Edwards. The batch number is populated in Accrual excel file along with the information such as Prepared By and the date of preparation. The Accrual excel file is converted to PDF format. The Batch report is then downloaded from JD Edwards system in PDF format. The PDF format of Accrual file and the batch report are merged to prepare a final report. The final report is then sent to stakeholders through email.

 - Reads data from a **Accrual excel file**.
 - Uses Assets for **input file path** and **URL**
 - Pushes each row as a transaction item to an **Orchestrator Queue**
 - Uses **REFramework** to process each line dynamically
 - Traverses through the **JD Edwards EnterpriseOne Menu** to open the **desired application for entering the Journal Entries**
 - Adds the data into the grid **line by line**, followed by the required steps for the Journal Entry
 - Once all the data is added into the grid, **submits the data** and then **extracts the Batch Number generated**
 - Runs a report named **General Journal by Batch Report** using the **generated Batch Number**
 - Downloads the executed report in **PDF format**
 - Sends the **final report to stakeholders via email**
 - Gracefully **handles system/business exceptions**
![Form Screenshot](Images/ProcessFlow.png)

---

## 🏗️ Project Architecture

- **Framework:** REFramework (Transactional Business Process)
- **Queues:** `RPAChallengeREFrameworkQueue`  
- **Assets:**  
  - `RPAChallengeREFrameworkPath` - `C:\Users\srush\Downloads\RPAChallengeNew.xlsx`
- **Transaction Item Type:** `QueueItem` with fields like FirstName, LastName, etc.

---

## 🛠️ Technologies Used

- UiPath Studio (REFramework)
- Orchestrator Queues & Assets
- Excel Activities
- Anchor Base Activities
- Error Handling with Try-Catch & Logging

---

## 📁 Folder Structure

RPAChallengeREFrameworkDispatcher/
- Main.xaml
- project.json
- README.md

RPAChallenge_REFRamework/
- Main.xaml
- project.json
- README.md


---

## 📸 Screenshots
1. Input
![Form Screenshot](Images/InputExcel.png)

2. Asset
![Form Screenshot](Images/Asset.png)

3. Queue
![Form Screenshot](Images/Queue.png)

4. BotExecution
![Form Screenshot](Images/BotExecution.png)

---

## ▶️ How to Run

1. Upload the Excel data to Orchestrator Queue in RPAChallengeREFrameworkDispatcher 
2. Configure Assets: `RPAChallengeREFrameworkPath`
3. Publish to Orchestrator or run locally
4. Monitor transactions in Orchestrator

---

## 🙋‍♀️ Author

**Srushti Arekar**  
[MyProfile](https://github.com/SrushtiArekar)

---

## 📄 License

This project is licensed under the MIT License.

