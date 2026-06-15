# n8n-feedback-form-automation
An automated workflow built with n8n to handle feedback form submissions, send instant email notifications via Gmail, and log data into Google Sheets.

A backend automation workflow built with n8n to seamlessly bridge Gmail communication and data logging in Google Sheets. This project automates the process of capturing incoming email data and structuring it into a spreadsheet in real-time, eliminating manual data entry.

---

##  Features

* **Automated Triggering:** Monitors specified Gmail messages/labels instantly.
* **Data Extraction:** Parses relevant details from incoming emails (Sender, Subject, Body, Date).
* **Structured Logging:** Appends data into dedicated rows within Google Sheets dynamically.
* **Error Handling:** Designed with basic error routing to ensure reliable execution.

---

##  Tech Stack & Tools

* **n8n:** Workflow automation platform.
* **Gmail API:** For email retrieval and trigger events.
* **Google Sheets API:** For data persistence and structured logging.
* **JSON:** Workflow configuration format.

---

##  Installation & Setup

To get this workflow running on your local n8n instance or cloud dashboard, follow these steps:

### 1. Prerequisites
* A running instance of **n8n** (Self-hosted via Docker, npm, or n8n Cloud).
* A Google Cloud Console account with **Gmail API** and **Google Sheets API** enabled to obtain credentials.

### 2. Import the Workflow
1. Download the `workflow.json` file from this repository.
2. Open your n8n dashboard.
3. Click on the top-right menu (`...`) and select **Import from File**.
4. Upload the downloaded `workflow.json` file.

### 3. Credentials Configuration
* **Gmail Node:** Click on the Gmail node, select "Create New Credential", and connect your Google account via OAuth2.
* **Google Sheets Node:** Click on the Google Sheets node, link your credentials, and paste your specific **Spreadsheet ID** into the designated field.

---

##  Workflow Architecture

As shown in the project setup, the data flows as follows:
```text
[Gmail Trigger] ──> [Data Parsing / ai agent] ──> [Google Sheets: Append Row]
