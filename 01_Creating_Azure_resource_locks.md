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


### 2️⃣ Clear definition of the lab’s purpose and Azure tools used

#### 🎯 **Lab Purpose**

This lab teaches how to use **Azure resource locks** to prevent accidental deletion or modification of critical resources in a cloud environment. The goal is for learners to understand how to apply **Delete** and **Read-only** locks at both the **resource** and **resource group** levels. These locks are essential in production environments to safeguard virtual machines, databases, and other infrastructure components from unintended changes or removal — especially in environments managed by multiple team members.

In this lab, Alex, a cloud engineer at **CloudCore Labs**, creates a virtual machine and applies both types of locks. Through this hands-on activity, learners gain practical knowledge in **resource governance and control**, which are key areas in enterprise-grade Azure deployments and part of the **AZ-104** administrator certification skill set.

---

#### 🧰 **Azure Tools and Services Used**

1. **Azure Resource Groups**
   A **resource group** is a logical container that holds related Azure resources. In this lab, the group `rg-cloudcore-alex` is created to organize and manage all resources related to the virtual machine and locks. It also becomes the target for applying a **Read-only lock** at the group level.

2. **Azure Virtual Machines (VMs)**
   The **virtual machine** `vm-cloudcore-linux01` serves as the primary resource in this lab. It simulates a workload that might be running in a production environment. Creating and locking this VM helps reinforce the importance of protecting compute infrastructure.

3. **Azure Locks**
   **Locks** prevent accidental operations on Azure resources. There are two types:

   * **Delete Lock**: Prevents the resource from being deleted.
   * **Read-only Lock**: Prevents any modification to the resource or its configuration.
     In this lab, a **Delete lock** is applied to the VM, and a **Read-only lock** is applied to the resource group to simulate governance controls in action.

4. **Azure Portal**
   The **Azure portal** is the main user interface used to carry out all steps — from creating the virtual machine to adding locks. It provides a graphical, browser-based experience for managing cloud resources.

---

#### 💼 **Why This Matters in the Real World**

In large organizations or teams, it's easy to mistakenly delete or alter resources — which can lead to downtime or data loss. Implementing **resource locks** is a simple yet powerful strategy to prevent such incidents. This lab ensures that future Azure admins understand not just *how* to use locks, but *why* they are a critical part of enterprise-grade cloud governance and compliance practices.


### 3️⃣ Professional real-world scenario for practical context

At **CloudCore Labs**, a mid-sized software company specializing in enterprise SaaS solutions, the cloud operations team has been tasked with hardening their Azure environment to meet new internal compliance standards. Recently, a junior team member accidentally deleted a test virtual machine that was being used for an urgent performance benchmarking project — causing downtime and delays.

To avoid such mishaps in the future, **Alex**, the **Azure admin**, is assigned to implement preventive governance controls. His manager asks him to protect key infrastructure assets from accidental deletion or misconfiguration, starting with the company’s development and testing environments.

Alex logs into the **Azure portal** and begins by creating a new **virtual machine** named `vm-cloudcore-linux01` in the `rg-cloudcore-alex` resource group. This VM represents a simulation server frequently used by the R\&D team. Knowing how easy it is to click "Delete" by mistake, Alex applies a **Delete lock** to the virtual machine. This ensures no one — not even privileged users — can remove the VM unless the lock is intentionally removed first.

To further protect the group of resources, he adds a **Read-only lock** at the **resource group** level. This move restricts changes to any resource within the group unless explicitly authorized, adding a layer of control especially helpful in environments managed by cross-functional teams.

By completing this setup, the Azure admin not only fulfills the compliance requirement but also implements a **best practice** in cloud governance using **Azure resource locks**. His actions demonstrate how simple configurations can safeguard resources and improve operational resilience — a valuable skill for any IT professional managing enterprise workloads in Azure.


### 4️⃣ Reflection: Did the **character** accomplish the task?

Yes, **Alex**, the **Azure admin** at **CloudCore Labs**, successfully completed the assigned task with clarity and precision.

He began by provisioning a **virtual machine** (`vm-cloudcore-linux01`) in Azure and organizing it under a well-named **resource group** (`rg-cloudcore-alex`). This setup reflects strong resource management and aligns with organizational conventions — a good practice in enterprise environments.

To fulfill the goal of improving **resource governance and protection**, he applied a **Delete lock** to the VM. This lock ensures that no accidental or unauthorized deletion can occur unless the lock is explicitly removed, directly solving the issue his team previously faced.

Further strengthening the protection, Alex added a **Read-only lock** at the **resource group level**. This action prevents any unintended modifications to all resources inside the group — enforcing an extra layer of operational safety.

The tasks were implemented without errors, and all configurations were verified in the **Azure portal**. The strategy aligns with **best practices in Azure governance**, especially for environments managed by multiple users or teams.

In a production scenario, Alex might further consider using **role-based access control (RBAC)** to complement the locks and refine who can manage, read, or delete resources. But overall, the lab objective was clearly met, and the outcome reflects a proactive and practical approach to resource protection in a cloud environment.


