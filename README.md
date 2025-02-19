**Folder Backup and Log to Excel - Documentation**

## **1. Project Overview**
**Project Name:** Folder Backup and Log to Excel  
**Description:** This flow automates the process of backing up a selected folder and logging the backup details (folder path and timestamp) into an Excel file.

## **2. Prerequisites**
- Install **Power Automate Desktop**.
- Ensure access to the folders for backup.
- Create an empty Excel file named `BackupLogs.xlsx` at the following location:
  ```
  C:\Users\<YourUsername>\Desktop\BackupLogs.xlsx
  ```

## **3. Step-by-Step Instructions**
### **Step 1: Select Folder**
- The flow displays a folder selection dialog where the user can choose a folder for backup.

### **Step 2: Copy Folder**
- The selected folder is copied to the backup location:
  ```
  C:\Users\<YourUsername>\Desktop\profile\Backup
  ```

### **Step 3: Open Excel Log File**
- The flow launches Excel and opens `BackupLogs.xlsx` to log the backup details.
- If the file does not exist, a new one is created.

### **Step 4: Write Headers (If Not Exists)**
- The column headers **"Backup Path"** and **"Backup Time"** are written in the first row if they are not already present.

### **Step 5: Find First Empty Row**
- The flow retrieves the first empty row in the Excel sheet to ensure new entries do not overwrite existing logs.

### **Step 6: Write Backup Data to Excel**
- The selected folder path is written to column **1**.
- The current date and time are written to column **2**.

### **Step 7: Save and Close Excel**
- The Excel file is saved to ensure all data is retained.
- The Excel instance is closed properly to avoid memory issues.

![Backup flow screenshot 1 ](https://github.com/Gaya39597/PowerAutomate-Projects/blob/main/Folder%20Backup%20Flow.png)
![Backup flow screenshot 2 ](https://github.com/Gaya39597/PowerAutomate-Projects/blob/main/Folder%20Backup%20Flow%20-2.png)

## **4. Future Enhancements**
- Automate this process to run on a schedule.
- Implement email notifications after a successful backup.
- Add error handling to ensure smooth execution.
