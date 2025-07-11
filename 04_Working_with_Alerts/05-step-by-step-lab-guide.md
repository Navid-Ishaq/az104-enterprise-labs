# [4] Working with Alerts

This lab guide provides enterprise-ready, scenario-driven walkthroughs for mastering key Azure administrator tasks aligned with the AZ-104 certification.

### 🔹 **Point 5 of 9: Guided Hands-On Walkthrough — Setting Up Azure Alerts in a Real Cloud Scenario**

This walkthrough provides clear, beginner-friendly steps to complete **Lab 4: Working with Alerts** in Azure. We’ll simulate a real-world task where two engineers — **Ayesha** from BrightOps Solutions and **Rohan** from SkyNova Systems — collaborate to set up a virtual machine and configure alert rules to monitor administrative activity. This hands-on guide helps IT beginners understand how to track important changes in their cloud environment using Azure’s built-in tools.

---

## 🧩 Lab Summary

**Goal:**
Set up a **virtual machine** and create an **alert** that notifies the user when someone restarts or performs any admin-level operation on that VM.

**Duration:** 1 hour
**Scenario Characters:**

* **Ayesha**, Systems Engineer at *BrightOps Solutions*
* **Rohan**, CloudOps Specialist at *SkyNova Systems*

**Resource Naming Convention Example:**

* Resource Group: `rg-skynova-ayesha`
* Virtual Machine: `vm-brightops-demo01`
* Action Group: `ag-alert-ayesha`

---

## 🚀 Step 1: Create a Virtual Machine in Azure

1. **Log in to the Azure Portal** using your credentials.

2. In the **left-hand menu**, select **Virtual Machines**.

3. Click **+ Create > Azure virtual machine**.

4. On the **Basics** tab:

   * **Subscription**: Keep the default.
   * **Resource group**: Click *Create new* and name it `rg-skynova-ayesha`.
   * **Virtual machine name**: Use `vm-brightops-demo01`.
   * **Region**: Choose **East US**.
   * **Availability options**: Select *No infrastructure redundancy required*.
   * **Security type**: Select *Standard*.
   * **Image**: Choose *Windows Server 2022 Datacenter: Azure Edition – x64 Gen2*.
   * **Size**: Choose *B2s* (you can use the default filter).
   * **Administrator account**:

     * Username: `clouduser`
     * Password: `SecureP@ssw0rd!`
   * **Inbound ports**: Set to *None*.

5. Go to the **Disks** tab:

   * **OS disk type**: Select *Standard SSD*.

6. Click **Review + create**, then click **Create** to deploy the VM.

📝 *This machine will act as a demo server that we’ll monitor using alerts.*

---

## 🛎️ Step 2: Create an Alert Rule for the Virtual Machine

1. After deployment completes, go to **Virtual Machines** and select `vm-brightops-demo01`.

2. In the left menu of the VM, scroll down to **Monitoring** and click **Alerts**.

3. Click **+ Create > Alert rule**.

---

### 2.1 Define Scope

* Click **+ Select resource**, search for your VM name (`vm-brightops-demo01`), and click **Apply**.

---

### 2.2 Set the Alert Condition

1. Under the **Condition** section, click **Add condition**.

2. Select **See all signals**.

3. Use the search box to find **All Administrative operations** and select it.

4. Click **Apply**.

🧠 *This tells Azure to watch for changes like restarts, stops, or config updates.*

---

### 2.3 Add an Action Group

1. Under the **Actions** tab, click **+ Create action group**.

2. In the form:

   * **Resource group**: Choose `rg-skynova-ayesha`.
   * **Action group name**: Use `ag-alert-ayesha`.
   * **Display name**: Enter `Alert Ayesha`.

3. Under the **Notifications** tab:

   * Select **Email/SMS/Push/Voice**.
   * Set a **Name** like `EmailNotify`.
   * Choose **Email**, enter your email address, and click **Confirm**.

4. Click **Review + create**, then **Create**.

---

### 2.4 Finalize the Alert Rule

1. Under the **Details** tab:

   * **Alert rule name**: Use `admin-alert-demo-vm`.
   * **Description** (optional): “Alert for any admin actions on demo VM.”

2. Click **Review + create**, then **Create**.

🎯 *Your alert rule is now active and ready to notify you of any admin-level operations.*

---

## 🔁 Step 3: Trigger and Verify the Alert

1. Go back to **Virtual Machines** and open `vm-brightops-demo01`.

2. Click **Restart** to simulate an admin operation.

3. Wait 2–5 minutes.

4. Check your **email inbox** (used in the Action Group) for a message from Azure about the triggered alert.

📩 *If you receive an alert email, it means your setup is successful!*

---

## 🧹 Step 4: Clean Up Resources (Optional but Recommended)

To avoid unnecessary charges after testing:

1. Go to **Resource Groups** in the Azure Portal.

2. Find `rg-skynova-ayesha`.

3. Click **Delete resource group** and follow the confirmation process.

✅ *All resources, including the VM and alert, will be removed.*

---

## 🎓 Final Notes

This hands-on walkthrough helped Rohan and Ayesha understand how to:

* **Monitor critical operations** on their VM
* **Get notified instantly** when something changes
* **Use alerts for real-world visibility and control**

> “I used to check everything manually,” Ayesha said, “but now I know how to let the system talk to me — even while I sleep!”

---

