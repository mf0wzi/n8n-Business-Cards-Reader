# 📇 n8n Business Cards Reader

An easy-to-use **n8n workflow** that extracts contact information from business card images using AI, then saves the details automatically into Google Sheets.  
This project runs fully in **Docker**, making setup simple and fast.

Created by **Mohammed Fowzi** (GitHub: [@mf0wzi](https://github.com/mf0wzi)).

---

## 🚀 Features

- Upload a business card image through a web form  
- Automatically extract:
  - Name  
  - Mobile / Phone numbers  
  - Email  
  - Business name  
  - Title  
  - Website  
  - Address  
- Sends data into Google Sheets  
- Email notifications for success or errors  
- Clean success/error page with a button to upload another card  
- Runs easily via Docker Compose

---

## 📦 Requirements

- Docker  
- Docker Compose  
- An `.env` file (you create this from `.env.example`)

---

## 🛠️ How to Run

1. **Clone the repo**

   ```bash
   git clone https://github.com/mf0wzi/n8n-Business-Cards-Reader.git
   cd n8n-Business-Cards-Reader
   ```
2. **Create your environment file**

   ```bash
   cp .env.example .env
   ```
   Fill in your API keys + n8n credentials.

3. **Start n8n using Docker**

   ```bash
   docker compose up -d
   ```
   or on Windows:

   ```bash
   n8n-run.bat
   ```
4. **Open n8n**

   ```bash
   http://localhost:5678
   ```
5. **Import the workflow**
   - Go to Workflows → Import from File
   - Select business cards extractor.json
   - Save and activate

## 📤 Using the Tool

  - Open the Form Trigger URL inside n8n
  - Upload a business card image
  - AI extracts all fields
  - Data is saved to your Google Sheet
  - Email notification is sent on success or error

## 🧩 Stopping the Tool
   ```bash
   docker compose down
   ```
   or on Windows:

   ```bash
   stop-n8n.bat
   ```

## ⚠️ Important Notes
   - Never commit your .env file
   - Google Sheets and Gmail authentication must be configured inside n8n
   - Workflow can be customized to send data to CRMs, Notion, Airtable, etc.

## 📄 License

    This project is free to use.
