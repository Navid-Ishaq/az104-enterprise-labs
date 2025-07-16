
# 🧪 Lab Walkthrough: Migrating Data to Azure with AzCopy

> _"Let’s go step by step — not just to complete the task, but to understand the 'why' behind each click."_  
> — Jamalu  
> — **Siraat AI Academy**

---

## Lab Overview

This lab walks you through how to use **AzCopy**, a command-line utility, to upload, sync, and schedule automated tasks to Azure Blob Storage.  
Whether you're a business owner, freelancer, or future security engineer — these steps help you migrate your data securely and smartly.

---

## ✅ Step 1: Create a Storage Account

### What You Do:
1. Go to the **Azure Portal**.
2. Search for **Storage accounts** and click **+ Create**.
3. Fill in:
   - **Subscription**: Use your default
   - **Resource Group**: `rg-learntech-naveed`
   - **Storage Account Name**: `ncloudstorage01` (must be unique globally)
   - **Region**: `East US`
   - **Performance**: `Standard`
   - **Redundancy**: `Geo-redundant storage (GRS)`
4. Go to the **Advanced tab** and enable:
   - **Hierarchical namespace**
5. Click **Review + create**, then **Create**.

### Why It Matters:
Your storage account is where all cloud data will live. GRS ensures it's protected even if one region fails.

---

## ✅ Step 2: Create a Container

### What You Do:
1. Go to your new **Storage Account**.
2. Under **Data Storage**, click **Containers** → **+ Container**.
3. Name it `democontainer-naveed` → Click **Create**.

### Why It Matters:
Containers act like folders. This is where your uploaded files go.

---

## ✅ Step 3: Download and Set Up AzCopy

### What You Do:
1. Download AzCopy:  
   [AzCopy for Windows](https://aka.ms/downloadazcopy-v10-windows)
2. Extract it to:  
   `C:\Tools\AzCopy`
3. Open **Command Prompt** and navigate there:
   ```bash
   cd C:\Tools\AzCopy
   ```

### Authenticate:
```bash
azcopy login
```
Follow the terminal instructions to sign in via browser.

### Why It Matters:
AzCopy is your fast, secure command-line transporter — like a delivery truck that never gets tired.

---

## ✅ Step 4: Upload Files

### What You Do:
1. Prepare a folder on your PC:  
   `C:\DataToUpload`  
   Add a few sample files.
2. Run this command:
   ```bash
   azcopy copy "C:\DataToUpload" "https://ncloudstorage01.blob.core.windows.net/democontainer-naveed" --recursive=true
   ```

### Why It Matters:
This sends your local files into Azure — recursively means subfolders and all.

---

## ✅ Step 5: Modify and Sync Data

### What You Do:
1. Modify a file or add new ones to `C:\DataToUpload`.
2. Run:
   ```bash
   azcopy sync "C:\DataToUpload" "https://ncloudstorage01.blob.core.windows.net/democontainer-naveed" --recursive=true
   ```

### Why It Matters:
Sync ensures Azure mirrors your local folder — only the changes get updated, saving time.

---

## ✅ Step 6: Schedule Automatic Syncs

### What You Do:
1. Open Notepad and paste:
   ```bash
   azcopy sync "C:\DataToUpload" "https://ncloudstorage01.blob.core.windows.net/democontainer-naveed" --recursive=true
   ```
2. Save as:  
   `C:\Scripts\sync-ncloudedge.bat`
3. Create a scheduled task:
   ```bash
   schtasks /CREATE /SC minute /MO 5 /TN "AzCopy-Sync-NCloudEdge" /TR C:\Scripts\sync-ncloudedge.bat
   ```

### Why It Matters:
This keeps your data in sync every 5 minutes — perfect for live updates without manual effort.

---

## ✅ Step 7: Clean Up

Delete all resources after testing:
- VM (if used)
- Storage account
- Scheduled task
- Local test folders

---

## 👨‍🏫 Jamalu’s Final Whisper

_"Technology is not just about tools — it's about timing, trust, and thoughtful effort."_  
_"Slow steps, clear minds — that’s how we move forward."_  

— Jamalu  
— **Siraat AI Academy**
