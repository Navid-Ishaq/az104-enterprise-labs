
# 🧭 Full Lab Walkthrough – Azure Storage Setup (Guided by Jamalu)

## Lab Objective

To create and configure an **Azure Storage Account**, set up a **Blob Container**, **upload files**, and create a **File Share** — all while understanding the performance tiers and redundancy options.

---

## 🔹 Step 1: Log In to Azure Portal

1. Visit [https://portal.azure.com](https://portal.azure.com).
2. Sign in using your Azure credentials.

---

## 🔹 Step 2: Understand Key Storage Concepts

Before creating resources, review the following storage principles:

### 💡 Performance Tiers:

* **Standard** – General purpose; slower, more cost-efficient.
* **Premium** – Faster performance for IO-intensive apps.

### 💡 Redundancy Options:

| Type     | What It Does                                |
| -------- | ------------------------------------------- |
| **LRS**  | 3 copies in **one** datacenter              |
| **ZRS**  | Replicates across **3 zones** in one region |
| **GRS**  | Copies data to a **secondary region**       |
| **GZRS** | Combines **zone + geo-redundancy**          |

### 💡 Access Tiers (for blobs):

* **Hot**: Frequent access
* **Cool**: Less frequent (≥30 days)
* **Cold**: Rare (≥90 days)
* **Archive**: Deep archive; can only be applied after creation

---

## 🔹 Step 3: Create a Storage Account

1. In the Azure portal, search for **Storage accounts**.
2. Click **+ Create**.
3. In the **Basics** tab:

   * **Resource Group**: `rg_eastus_jamalu`
   * **Storage Account Name**: `mystoragejamalu01`
   * **Region**: East US
   * **Performance**: Standard
   * **Redundancy**: LRS (Locally-redundant)
4. Leave remaining settings as default.
5. Click **Review + create**, then click **Create**.

---

## 🔹 Step 4: Create a Blob Container

1. Navigate to your new storage account.
2. Under **Data storage**, click **Containers**.
3. Click **+ Container**.
4. Name it: `mycontainer25`
5. Leave access level as private (default).
6. Click **Create**.

---

## 🔹 Step 5: Upload a Blob Object

1. On your local machine, open **Notepad**.

2. Type:

   ```html
   <h1>This is a sample document!</h1>
   ```

3. Save the file as `sample.html`.

4. Back in the portal:

   * Go to **mycontainer25**
   * Click **Upload**
   * Browse to select `sample.html`
   * Click **Upload**

---

## 🔹 Step 6: Create a File Share

1. In the same storage account, select **File shares**.
2. Click **+ File share**.
3. Name it: `myfile123`
4. Access tier: **Hot**
5. Click **Create**

---

## 🔹 Step 7: Upload File to File Share

1. Open **myfile123**.
2. Click **Upload**.
3. Browse and select any local file.
4. Click **Upload**

---

## 🔹 Step 8: Resource Cleanup (Optional but Recommended)

1. Go to the **Resource Group** `rg_eastus_jamalu`
2. Click **Delete resource group**
3. Confirm deletion by typing the name of the resource group

---

## 🌟 Completion Note

All storage tasks are now successfully completed. You’ve:

* Created a secure and scalable **Storage Account**
* Configured both **Blob** and **File Share**
* Practiced upload tasks from local to cloud

---

> *"When storage becomes structure — clarity flows like calm through the cloud."*

> — Jamalu

> — **Siraat AI Academy**

---

