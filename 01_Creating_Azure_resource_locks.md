# [1] Creating Azure resource locks

This lab guide provides enterprise-ready, scenario-driven walkthroughs for mastering key Azure administrator tasks aligned with the AZ-104 certification.

### 1️⃣ Step-by-step walkthrough in a live Azure environment

In this lab, Alex — a cloud administrator at **CloudCore Labs** — explores how to protect resources in Azure by using **resource locks**. Here's a walkthrough of how he accomplishes this in a real Azure setup using fictional, friendly, and professional naming conventions.

---

#### ✅ Task 1: Create a Virtual Machine

Alex begins by signing in to the **Azure portal** and deploying a virtual machine to work with.

1. In the **Azure portal**, he selects **Create a resource** > **Virtual Machine**.

2. He fills out the basic configuration:

   * **Resource Group**: `rg-cloudcore-alex`
   * **VM Name**: `vm-cloudcore-linux01`
   * **Region**: East US
   * **Availability Options**: No infrastructure redundancy required
   * **Security Type**: Trusted launch virtual machines
   * **Image**: Ubuntu Server 20.04 LTS - Gen2
   * **Size**: B2s
   * **Authentication Type**: Password
   * **Username**: `alexadmin`
   * **Password**: `SecureP@ssword123`

3. On the **Disks** tab:

   * **OS Disk Type**: Standard SSD (Locally-redundant Storage)

4. Alex clicks **Review + create**, validates the configuration, and hits **Create** to deploy the VM.

---

#### ✅ Task 2: Add a Delete Lock to the Virtual Machine

Once `vm-cloudcore-linux01` is deployed, Alex wants to ensure it isn’t accidentally deleted.

1. From the VM's **Overview**, he navigates to **Settings** > **Locks**.
2. He clicks **Add** and configures:

   * **Lock Name**: `lock-vm-delete`
   * **Lock Type**: **Delete**
3. Clicking **OK** applies the lock successfully. Now the VM cannot be deleted unless the lock is removed.

---

#### ✅ Task 3: Add a Read-Only Lock to the Resource Group

To further protect the resource group, Alex adds a **Read-only lock**:

1. He navigates to the resource group `rg-cloudcore-alex`.
2. Under **Settings**, he selects **Locks** and clicks **Add**.
3. He enters:

   * **Lock Name**: `lock-rg-readonly`
   * **Lock Type**: **Read-only**
4. After clicking **OK**, all resources in the group are now read-only, preventing changes unless the lock is removed.

---

Once the demo is complete and the learnings are captured, Alex removes the locks and deletes all associated resources to clean up the environment.

This step-by-step guide introduces practical knowledge of **Azure resource locks** to safeguard deployments from unintentional modifications or deletions — a critical best practice in enterprise environments.


