
# 📘 **Lab Walkthrough: Secure Network Access to Azure Storage via Private Endpoint**

## 🧭 Overview

This lab demonstrates how to securely access an **Azure Storage Account** using a **Private Endpoint** from within a **Virtual Network**.
You'll create a **VNet**, set up **storage with private access**, deploy a **VM**, and test access — all through secure internal routing.

---

## ✅ Step 1: Create a Virtual Network & Subnet

1. Go to **Create a Resource** → Search for **Virtual Network**.
2. Click **Create** and fill out:

   * **Resource Group**: `rg-learntech-naveed`
   * **Virtual Network Name**: `vnet-ncloudedge-west1`
   * **Region**: `West Europe`
3. In the **IP Addresses** tab:

   * Delete the default address space.
   * Add new IPv4 Address Space: `10.0.0.0/16`
4. Click **+ Add Subnet**:

   * Name: `subnet-nxt-app`
   * Range: `10.0.0.0/24`
5. Click **Review + Create** → **Create**

---

## ✅ Step 2: Create a Storage Account with a Private Endpoint

1. Go to **Storage Accounts** → Click **+ Create**.
2. Under **Basics**:

   * **Resource Group**: `rg-learntech-naveed`
   * **Storage Account Name**: `stgnxtnav001`
   * **Region**: `West Europe`
   * **Performance**: Standard
   * **Redundancy**: GRS
3. Under the **Networking** tab:

   * Choose: **Disable public access**
   * Add **Private Endpoint**:

     * **Name**: `pe-nxtblob01`
     * **Sub-resource**: `blob`
     * **Virtual Network**: `vnet-ncloudedge-west1`
     * **Subnet**: `subnet-nxt-app`
4. Click **Review + Create** → **Create**
5. Once deployed:

   * Go to the **Access keys** section
   * Reveal and copy **Key 1 Connection String** for later

---

## ✅ Step 3: Create a Virtual Machine Inside the Subnet

1. Go to **Virtual Machines** → Click **+ Create**.
2. Under **Basics**:

   * **Resource Group**: `rg-learntech-naveed`
   * **VM Name**: `vm-ncloudedge-access`
   * **Region**: `West Europe`
   * **Image**: Windows Server 2019 Gen2
   * **Size**: `Standard_B2s`
   * **Username**: `cloudadmin`
   * **Password**: (your password)
   * **Inbound Ports**: Allow **RDP (3389)**
3. Under **Disks**:

   * OS disk type: **Standard SSD**
4. Under **Networking**:

   * **VNet**: `vnet-ncloudedge-west1`
   * **Subnet**: `subnet-nxt-app`
5. Click **Review + Create** → **Create**

---

## ✅ Step 4: Connect to the VM and Configure Access

1. Go to **Virtual Machines** → Select `vm-ncloudedge-access`
2. Click **Connect** > **RDP** → Download RDP file
3. Open file, click **More Choices → Use a different account**
4. Enter credentials you created
5. Accept any certificate warning

---

## ✅ Step 5: Test Private Access to the Storage

### Inside the VM:

1. Open **PowerShell**

2. Run:

   ```powershell
   nslookup stgnxtnav001.blob.core.windows.net
   ```

   You should receive a **private IP** response (not public).

3. Open **Server Manager** → Local Server

   * Turn off **IE Enhanced Security Configuration**

4. Download and install **Azure Storage Explorer**

5. Open Storage Explorer → Connect:

   * Choose: **Storage account or service**
   * Method: **Connection string**
   * Paste the copied key from Step 2
   * Complete the wizard and connect

6. Verify you can browse:

   * Blob Containers → `$logs` or other blobs

---

## ✅ Step 6: Clean Up Resources

1. Return to **Resource Groups**
2. Select `rg-learntech-naveed`
3. Click **Delete Resource Group**

   * Type the group name to confirm

---

> *“Security isn’t just isolation — it’s intention. And intention needs design.”*
> — **Jamalu**
> — Siraat AI Academy

---

