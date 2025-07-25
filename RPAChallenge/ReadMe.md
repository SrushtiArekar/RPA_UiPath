# 🤖 RPA Project – Dynamic Form Data Entry
A UiPath automation project that reads structured data from an Excel file and submits it into the dynamic web form at rpachallenge.com.

This is a UiPath automation project that completes the [RPA Challenge](https://rpachallenge.com/) by:

✅ Reading data from an Excel file  
✅ Opening the RPA Challenge form  
✅ Typing data row by row dynamically (fields change order)  
✅ Submitting each entry after filling all fields  
✅ Looping until all Excel rows are submitted  

---

## 📂 Project Structure

- `Main.xaml` — Main automation logic
- `RPAChallenge1.xlsx` — Input data file
- `project.json` — UiPath project metadata

---

## 🧰 Prerequisites

- UiPath Studio installed
- Excel installed
- Chrome/Edge with UiPath extension enabled

---

## 📌 How It Works

1. Opens the Excel file `RPAChallenge1.xlsx`
2. Reads each row into a DataTable
3. Navigates to `https://rpachallenge.com/`
4. Clicks "Start"
5. Enters the data row into dynamically ordered form fields using `Anchor Base`
6. Clicks "Submit"
7. Loops until all rows are submitted

---

## 📸 Screenshots
Input File
![Form Screenshot](Images/RPAChallengeInputExcel.png)

Form
![Form Screenshot](Images/RPAChallengeForm.png)

Steps:
1. Open the Excel File
![Form Screenshot](Images/Step1.png)

2. Read from Excel
![Form Screenshot](Images/Step2.png)

3. For each Excel row - Read cell value one by one
![Form Screenshot](Images/Step3.png)
![Form Screenshot](Images/Step4.png)
![Form Screenshot](Images/Step5.png)
![Form Screenshot](Images/Step6.png)

4. Open Form on Browser - "https://rpachallenge.com/"
![Form Screenshot](Images/Step7.png)

5. Type into Fields (use Anchors as Fields are changing its positions)
![Form Screenshot](Images/Step8.png)
![Form Screenshot](Images/Step9.png)
![Form Screenshot](Images/Step10.png)

6. Click Submit Button on the Form
![Form Screenshot](Images/Step11.png)
  
---

## ▶️ How to Run

1. Clone this repository
2. Open `RPAChallenge1` folder in UiPath Studio
3. Open `Main.xaml`
4. Make sure Excel file is in the same folder
5. Run the process

---

## 🛠️ Built With

- [UiPath Studio](https://www.uipath.com/)
- Excel Application Scope
- DataTable Looping
- Anchor Base Activities
- Chrome Browser Automation

---

## 🙋‍♀️ Author

**Srushti Arekar**  
[MyProfile](https://github.com/SrushtiArekar)

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
