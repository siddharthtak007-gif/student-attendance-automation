# Student Low Attendance Alert System (n8n Automation)

This is an automated workflow that tracks student attendance and automatically sends a warning email containing a Google Form link to students whose attendance falls below the required criteria.

## 🚀 Features
- **Auto-Scheduling:** The workflow runs automatically at scheduled intervals.
- **Google Sheets Integration:** Fetches student data directly from a specific Google Sheet.
- **Smart Filtering:** Uses an 'If' condition to filter out only the students with low attendance.
- **Gmail Automation:** Sends personalized alert messages and a Google Form link for responses via Gmail.

## 🛠️ Workflow Nodes
1. **Schedule Trigger:** Defines when the automation will run (e.g., Daily or Weekly).
2. **Google Sheets (Get rows):** Reads the student's name, email, and attendance percentage from the connected sheet.
3. **If Node:** Checks the data against the attendance threshold (Example: `< 75%`).
4. **Gmail (Send message):** Dispatches the warning email to students who meet the low attendance condition.

## 📋 Prerequisites
- **n8n Instance** (Cloud or Desktop version).
- **Google Cloud Console Credentials:** Required for Google Sheets and Gmail API access.
- **Google Sheet:** A structured sheet containing `Name`, `Email`, and `Attendance` columns.
- **Google Form:** An active form link for student acknowledgment or to collect reasons for absence.

## ⚙️ Setup Instructions
1. **JSON Import:** Download the `workflow.json` file from this repository. In your n8n workspace, go to the top right menu, click 'Import from File', and upload the JSON file.
2. **Authentication:**
   - Open the **Google Sheets** node and connect/authenticate your Google account.
   - Open the **Gmail** node and set up your Gmail API credentials.
3. **Configuration:**
   - In the **Google Sheets** node, select your target Spreadsheet and define the data range.
   - In the **If Node**, adjust the percentage value to match your specific attendance criteria limit.
   - In the **Gmail** node, customize the email body and paste your Google Form link.
4. **Activate:** Toggle the workflow status to **Active** in the top right corner.

## 📂 Repository Structure
- `workflow.json`: The main n8n workflow export file for direct import.
- `README.md`: Project documentation and setup guide.

## 👤 Author
**Siddharth Tak**