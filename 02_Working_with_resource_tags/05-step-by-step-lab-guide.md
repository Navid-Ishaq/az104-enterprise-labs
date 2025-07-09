# [2] Working with resource tags

This lab guide provides enterprise-ready, scenario-driven walkthroughs for mastering key Azure administrator tasks aligned with the AZ-104 certification.

### 🏷️ Lab 2: Working with Resource Tags in Azure

**Organization:** *BrightOps Solutions*
**User Role:** *Jordan – Junior Cloud Administrator*
**Objective:** Learn how to create a virtual machine, apply resource tags, and filter resources by tag for better organization and management.

---

## 🔹 Task 1: Create a Virtual Machine (VM)

1. **Sign in** to the [Azure Portal](https://portal.azure.com) using your provided credentials.

2. In the **left-hand menu**, select **Virtual Machines**, then click **+ Create** > **Azure Virtual Machine**.

3. In the **Basics** tab, enter the following configuration:

   * **Subscription:** Use the default subscription.
   * **Resource Group:** Create or select `rg-brightops-jordan`
   * **Virtual Machine Name:** `vm-brightops-web01`
   * **Region:** East US
   * **Availability Options:** No infrastructure redundancy required
   * **Security Type:** Standard
   * **Image:** Windows Server 2019 Datacenter - x64 Gen2
   * **Size:** Click **See all sizes**, select **B1s**, then click **Select**
   * **Username:** `JordanAdmin`
   * **Password:** `StrongPassword@123`

4. Scroll down and leave **Azure Spot Instance** unchecked.

5. Under **Inbound Ports**, leave default settings as they are (No public inbound ports selected).

6. Navigate to the **Disks** tab:

   * **OS Disk Type:** Select **Standard SSD**

7. Click **Review + Create**, verify your settings, then click **Create** to provision the virtual machine.

---

## 🔹 Task 2: Apply a Tag to the Virtual Machine

1. In the **Azure Portal**, go to **Resource Groups** from the left menu.

2. Open your resource group named `rg-brightops-jordan`.

3. Select the virtual machine you just created: `vm-brightops-web01`.

4. In the VM's left-side menu, scroll down and select **Tags** under the **Settings** section.

5. Add the following tag:

   * **Name:** `Department`
   * **Value:** `IT`

6. Click **Apply** to save the tag.

   > 💡 *Tagging helps identify, organize, and manage resources easily — especially in larger environments with multiple departments or teams.*

---

## 🔹 Task 3: Filter Resources by Tag

1. Return to the **Resource Groups** section from the Azure portal menu.

2. Select the resource group `rg-brightops-jordan`.

3. At the top, click **Add filters**.

4. In the filter window:

   * Choose **Tag Name:** `Department`
   * Choose **Tag Value:** `IT`

5. Click **Apply**.

6. You should now see only the resources within the resource group that have the tag **Department = IT**, such as your VM.

   > ✅ *This filter is useful when managing resources across multiple teams or projects—especially for budgeting, monitoring, or clean-up.*

---

## 🔹 Final Step: Clean Up Resources

To avoid unnecessary charges:

1. From your resource group `rg-brightops-jordan`, click **Delete resource group**.

2. Type the resource group name to confirm, then click **Delete**.

   > 🔐 *Always delete lab resources once testing is complete unless otherwise instructed.*

---

## 🎯 Summary

In this lab, Jordan from **BrightOps Solutions** successfully:

* Created a virtual machine named `vm-brightops-web01`
* Tagged the VM to identify its department
* Used tag filters to locate resources
* Cleaned up the environment after use

This lab reinforces key practices in **resource tagging and organization**, which are essential for efficient cloud management—especially as environments scale.

🧠 **Next Step Recommendation:**
Create a tagging policy for your team and ensure all Azure resources follow consistent naming and tagging conventions. This makes management, billing, and auditing much easier as you grow.
