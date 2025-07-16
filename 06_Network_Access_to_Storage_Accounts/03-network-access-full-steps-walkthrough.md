# 🧭 Full Lab Walkthrough – Secure Network Access to Azure Storage

### Lab Title: **Network Access to Storage Accounts via Private Endpoint**

**Duration:** 1 hour
**Author Style:** ✍️ With Jamalu’s calm guidance and real-world clarity

---

## 🌟 Introduction: Why This Lab Matters

In this lab, we’re not just creating cloud resources — we’re practicing **how to keep them safe**.

Jamalu explains:

> “Anyone can store data. But storing it *wisely*, with network boundaries, private endpoints, and limited exposure — that’s cloud maturity.”

Let’s begin step by step.

---

## ✅ Step 1: Create a Virtual Network (VNet)

**Purpose:** A virtual network is like your own private neighborhood in the cloud. It keeps your resources connected securely — and isolates them from the public internet.

### 🛠️ How:

1. Go to the **Azure Portal** → Click **Create a Resource**.
2. Search for **Virtual Network** and click **Create**.
3. In the **Basics** tab:

   * **Resource Group:** `rg-learntech-naveed`
   * **Name:** `vnet-ncloudedge-west1`
   * **Region:** `West Europe`
4. In the **IP Addresses** tab:

   * Remove the default address space.
   * Add a new IPv4 address space, e.g., `10.0.0.0/16`
   * Click **+ Add Subnet**

     * **Subnet Name:** `subnet-nxt-app`
     * **Subnet Address Range:** `10.0.0.0/24`
5. Click **Review + Create** → then click **Create**.

🎯 **Why this matters:**
This VNet and subnet will later serve as the foundation for **secure communication** between your VM and your storage — away from public exposure.

---

## ✅ Step 2: Create a Storage Account with Private Endpoint

**Purpose:** A storage account is where our files and blobs will live. But here’s the catch — we’re going to make it *private*. No internet access. Only internal, VNet-based access.

### 🛠️ How:

1. Search for **Storage Accounts** → Click **Create**.
2. In **Basics**:

   * **Resource Group:** `rg-learntech-naveed`
   * **Storage Account Name:** `stgnxtnav001`
   * **Region:** `West Europe`
   * **Performance:** `Standard`
   * **Redundancy:** `GRS`
3. In the **Networking** tab:

   * Choose **Disable public access**.
   * Click **+ Add Private Endpoint**:

     * **Name:** `pe-nxtblob01`
     * **Sub-resource:** `blob`
     * **Virtual Network:** `vnet-ncloudedge-west1`
     * **Subnet:** `subnet-nxt-app`
   * Click **OK**
4. Click **Review + Create**, then **Create**.

🎯 **Why this matters:**
You just created a **locked-down storage space** that can only be accessed from within your own VNet. This is what keeps sensitive data safe from outside attackers.

---

## ✅ Step 3: Access Keys – Store Connection Details

**Purpose:** To access your storage account securely from a VM, you’ll need a **connection string** (like a password + instructions).

### 🛠️ How:

1. Go to your new storage account: `stgnxtnav001`
2. On the left panel, click **Access Keys**
3. Click **Show Keys** and **copy the connection string for Key 1**

🎯 **Why this matters:**
This connection string is what the VM will use to “talk” to the storage account over a private line — no public network involved.

---

## ✅ Step 4: Create a Virtual Machine (VM)

**Purpose:** Think of this VM as your “secure laptop in the cloud” — it will be used to connect to the storage account.

### 🛠️ How:

1. Search for **Virtual Machines** → Click **+ Create**
2. In **Basics**:

   * **Resource Group:** `rg-learntech-naveed`
   * **VM Name:** `vm-ncloudedge-access`
   * **Region:** `West Europe`
   * **Image:** `Windows Server 2019 Datacenter`
   * **Size:** `Standard_B2s`
   * **Username:** `cloudadmin`
   * **Password:** (set a secure one)
   * **Inbound Ports:** Allow RDP (3389)
3. **Disks Tab:**

   * OS Disk: `Standard SSD`
4. **Networking Tab:**

   * Select your earlier VNet: `vnet-ncloudedge-west1`
   * Subnet: `subnet-nxt-app`
5. Click **Review + Create** → then **Create**

🎯 **Why this matters:**
Only this VM — from this subnet — can now access your private storage endpoint. Think of it like a **locked vault room** with one trusted keyholder.

---

## ✅ Step 5: Access VM & Connect to Storage

**Purpose:** To connect from inside the VM and verify the private storage is working.

### 🛠️ How:

1. Go to the **VM resource** → Click **Connect > RDP**

2. Download the RDP file

3. Open it → When prompted:

   * Click **More choices** → **Use a different account**
   * Enter VM credentials
   * Accept the certificate warning

4. Once inside:

   * Open **PowerShell**
   * Run:

     ```
     nslookup stgnxtnav001.blob.core.windows.net
     ```
   * ✅ If it resolves to a private IP — **your private endpoint is working.**

5. Open **Server Manager** → Turn off IE Enhanced Security

6. Download and install **Azure Storage Explorer**

7. In Storage Explorer:

   * Click **Connect**
   * Choose **Use connection string**
   * Paste the string from earlier
   * Click **Next** → then **Connect**

8. Navigate to:

   ```
   Blob Containers → $logs
   ```

🎯 **Why this matters:**
This final step proves that your VM — inside a locked network — can securely access your storage account without touching the public internet.

---

## ✅ Final Step: Clean Up

Once done, **delete all the resources** to avoid ongoing costs and keep your environment tidy.

---

## ✨ Jamalu’s Closing Whisper

> *“You didn’t just follow steps — you built a private cloud corridor.
> You proved to yourself that security isn’t about fear — it’s about quiet, intelligent design.”*
> — Jamalu
> — **Siraat AI Academy**

---

Would you like this converted into a downloadable `.md` file or enriched with a comic-style recap?
