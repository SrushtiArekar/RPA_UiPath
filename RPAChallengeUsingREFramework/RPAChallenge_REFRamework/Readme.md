# 🤖 RPA Challenge Performer – REFramework | UiPath

This project is the **Performer** component of the **RPA Challenge** implemented using **UiPath’s REFramework**. It reads data from **Orchestrator Queues**, enters each row into the RPA Challenge web form, and handles exceptions and retry mechanisms gracefully.

---

### REFrameWork ###
**Robotic Enterprise Framework**

* Built on top of *Transactional Business Process* template
* Uses *State Machine* layout for the phases of automation project
* Offers high level logging, exception handling and recovery
* Keeps external settings in *Config.xlsx* file and Orchestrator assets
* Pulls credentials from Orchestrator assets and *Windows Credential Manager*
* Gets transaction data from Orchestrator queue and updates back status
* Takes screenshots in case of system exceptions

### How It Works ###

1. **INITIALIZE PROCESS**
 + ./Framework/*InitiAllSettings* - Load configuration data from Config.xlsx file and from assets
 + ./Framework/*GetAppCredential* - Retrieve credentials from Orchestrator assets or local Windows Credential Manager
 + ./Framework/*InitiAllApplications* - Open and login to applications used throughout the process

2. **GET TRANSACTION DATA**
 + ./Framework/*GetTransactionData* - Fetches transactions from an Orchestrator queue defined by Config("OrchestratorQueueName") or any other configured data source

3. **PROCESS TRANSACTION**
 + *Process* - Process trasaction and invoke other workflows related to the process being automated 
 + ./Framework/*SetTransactionStatus* - Updates the status of the processed transaction (Orchestrator transactions by default): Success, Business Rule Exception or System Exception

4. **END PROCESS**
 + ./Framework/*CloseAllApplications* - Logs out and closes applications used throughout the process


### For New Project ###

1. Check the Config.xlsx file and add/customize any required fields and values
2. Implement InitiAllApplications.xaml and CloseAllApplicatoins.xaml workflows, linking them in the Config.xlsx fields
3. Implement GetTransactionData.xaml and SetTransactionStatus.xaml according to the transaction type being used (Orchestrator queues by default)
4. Implement Process.xaml workflow and invoke other workflows related to the process being automated

---


> 💡 This is the Performer part of the full REFramework solution. The Dispatcher (linked below) is responsible for uploading data to the queue.

### 🔗 Related Dispatcher Project
[RPAChallengeREFrameworkDispatcher](https://github.com/SrushtiArekar/UiPath-Portfolio/tree/main/RPAChallengeUsingREFramework/RPAChallengeREFrameworkDispatcher)

---

## 📌 Project Overview

- Uses **UiPath REFramework** with minor modifications for queue-based input
- Reads `TransactionItem` of type `QueueItem`
- Extracts SpecificContent from each queue item
- Navigates to the [RPA Challenge website](https://www.rpachallenge.com/)
- Fills out the form with all the required fields
- Submits the form and proceeds with the next item

---

## 📂 Project Contents

- `Main.xaml` – REFramework entry point
- `InitAllSettings.xaml` – Initializes config
- `GetTransactionData.xaml` – Fetches next queue item
- `Process.xaml` – Main logic to fill and submit the form
- `ExceptionHandler.xaml` – Handles errors and retries
- `Config.xlsx` – Configuration file

---

## 🖼️ Screenshots



---

## ▶️ How to Run

1. Run the [Dispatcher](https://github.com/SrushtiArekar/UiPath-Portfolio/tree/main/RPAChallengeUsingREFramework/RPAChallengeREFrameworkDispatcher) project to upload queue items to `RPAChallengeREFrameworkQueue`.
2. In UiPath Orchestrator:
   - Ensure assets like URL, credentials (if needed), etc. are defined.
3. Open this Performer project in UiPath Studio.
4. Run `Main.xaml`.
5. Watch as it loops through the queue, submits the form, and logs the results.

---

## 🛠️ Built With

- UiPath Studio – Community/Enterprise Edition
- REFramework (Robotic Enterprise Framework) – Used for standardized project structure
- UiPath Orchestrator – For managing assets and queues
- Excel Activities Package – For reading tabular data
- System Activities – For dictionary and workflow control
- Orchestrator Queues – For transaction-level processing

---

## 🙋‍♀️ Author

**Srushti Arekar**  
[MyProfile](https://github.com/SrushtiArekar)

---

## 📄 License

This project is licensed under the MIT License.
