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


### 4️⃣ Reflection: Did the **Alex** accomplish the task?

Yes, **Alex**, the **Azure admin** at **CloudCore Labs**, successfully completed the assigned task with clarity and precision.

He began by provisioning a **virtual machine** (`vm-cloudcore-linux01`) in Azure and organizing it under a well-named **resource group** (`rg-cloudcore-alex`). This setup reflects strong resource management and aligns with organizational conventions — a good practice in enterprise environments.

To fulfill the goal of improving **resource governance and protection**, he applied a **Delete lock** to the VM. This lock ensures that no accidental or unauthorized deletion can occur unless the lock is explicitly removed, directly solving the issue his team previously faced.

Further strengthening the protection, Alex added a **Read-only lock** at the **resource group level**. This action prevents any unintended modifications to all resources inside the group — enforcing an extra layer of operational safety.

The tasks were implemented without errors, and all configurations were verified in the **Azure portal**. The strategy aligns with **best practices in Azure governance**, especially for environments managed by multiple users or teams.

In a production scenario, Alex might further consider using **role-based access control (RBAC)** to complement the locks and refine who can manage, read, or delete resources. But overall, the lab objective was clearly met, and the outcome reflects a proactive and practical approach to resource protection in a cloud environment.


## 5️⃣ 10+ Conceptual MCQs aligned with exam readiness

**1. Why might an Azure admin apply a Delete lock on a virtual machine in a production environment?**

(a) To improve performance of the VM  
(b) To allow only auto-scaling services  
(c) To prevent accidental deletion of the VM  
(d) To avoid resource tagging conflicts  

**Correct answer: (c)**  
A **Delete lock** ensures that even users with contributor roles cannot delete the resource unless the lock is removed. It's a best practice in production environments where resource protection is crucial.

---

**2. What happens when a Read-only lock is applied at the resource group level in Azure?**

(a) It prevents all VM operations, including starting or stopping  
(b) It allows reading but restricts create, update, or delete operations on all resources within the group  
(c) It deletes unused resources automatically  
(d) It enables high availability by default  

**Correct answer: (b)**  
A **Read-only lock** restricts users from making changes to resources within the resource group. They can still read configurations but cannot modify or delete anything until the lock is removed.

---

**3. Which Azure role is still unable to delete a resource if a Delete lock is applied?**

(a) Owner  
(b) Contributor  
(c) Reader  
(d) Global Administrator  

**Correct answer: (b)**  
Even if a user is a **Contributor**, a **Delete lock** overrides role-based permissions and blocks deletion unless the lock is removed explicitly.

---

**4. Why is it important to use resource locks in environments managed by multiple teams?**

(a) To reduce the Azure subscription cost  
(b) To restrict VM backups  
(c) To enforce policy creation  
(d) To protect resources from unintentional actions  

**Correct answer: (d)**  
In multi-user environments, applying locks helps prevent **accidental deletion or changes** to critical resources by users with broad permissions.

---

**5. In which situation would a Read-only lock create challenges for regular operations?**

(a) When monitoring metrics  
(b) When running queries using Azure Monitor  
(c) When trying to scale up a VM inside the locked resource group  
(d) When viewing the activity log  

**Correct answer: (c)**  
A **Read-only lock** blocks all write operations, including scaling, modifying settings, or updating configurations, which can affect operational agility.

---

**6. Which Azure service is used to apply and manage resource locks?**

(a) Azure Security Center  
(b) Azure Resource Manager  
(c) Azure DevOps  
(d) Azure Monitor  

**Correct answer: (b)**  
**Azure Resource Manager (ARM)** is the underlying platform responsible for managing and deploying resources, including applying **resource locks**.

---

**7. What will happen if you try to delete a resource group that has a Read-only lock applied?**

(a) The resource group will be deleted with a warning  
(b) It will delete only unlocked resources  
(c) The delete operation will fail unless the lock is removed  
(d) Azure will archive the group for recovery  

**Correct answer: (c)**  
A **Read-only lock** prevents deletion of the resource group. You must **remove the lock first** to perform delete operations.

---

**8. Why is it best to name locks with descriptive identifiers (e.g., `RGReadOnly`)?**

(a) Azure requires all lock names to be uppercase  
(b) To make them more visible in the audit logs  
(c) So automated scripts can skip them  
(d) To make lock intent clear for all admins managing resources  

**Correct answer: (d)**  
Using descriptive names like `RGReadOnly` makes it easier for team members to understand the **purpose and scope** of the lock, reducing miscommunication and errors.

---

**9. Which of the following statements about Azure locks is true?**

(a) Locks are automatically inherited from subscriptions  
(b) You can apply locks only on VMs, not resource groups  
(c) Locks can be applied at resource, resource group, or subscription level  
(d) Locks override Azure Policies  

**Correct answer: (c)**  
Locks can be applied at different scopes: **individual resources, resource groups, or the entire subscription**, depending on your governance needs.

---

**10. In the context of Azure governance, why are locks not a replacement for role-based access control (RBAC)?**

(a) Locks are more flexible than RBAC  
(b) Locks can only be used for billing  
(c) Locks provide basic protection but don’t control who can access or perform actions  
(d) RBAC is deprecated when locks are used  

**Correct answer: (c)**  
**Locks** restrict actions at the resource level, while **RBAC** manages **who can perform which actions**. They complement each other but serve different purposes in governance.

---

**11. What should an Azure admin do before deleting a locked resource?**

(a) Change the pricing tier to basic  
(b) Disable monitoring temporarily  
(c) Remove the associated lock  
(d) Enable diagnostic settings  

**Correct answer: (c)**  
To **delete a locked resource**, the admin must **first remove the lock**. Azure enforces this protection regardless of user roles or permissions.

---

**12. What is the most likely reason an admin receives an error when trying to modify a VM's settings inside a locked resource group?**

(a) The storage account is full  
(b) The VM is in a stopped state  
(c) A Read-only lock exists on the resource group  
(d) The VM size is incompatible  

**Correct answer: (c)**  
A **Read-only lock** at the resource group level blocks all changes, including updates to individual VM settings, even if the admin has full access otherwise.

---


## 6️⃣ 10+ Professional Job Scenario MCQs for Interview Practice

**1. Alex, an Azure admin at CloudCore Labs, wants to protect a production virtual machine from being accidentally deleted by junior engineers. What should he implement?**

(a) Azure Policy to block delete operations  
(b) A Read-only lock on the virtual machine  
(c) A Delete lock on the virtual machine  
(d) Disable delete permissions from the Contributor role  

**Correct answer: (c)**  
A **Delete lock** is the appropriate solution to prevent accidental deletion, even if the user has full access. It adds an additional layer of protection for critical resources.

---

**2. Taylor from SkyBridgeTech needs to allow monitoring access to a resource group but prevent changes to its configuration. What’s the most suitable action?**

(a) Assign Reader role at the subscription level  
(b) Apply a Read-only lock at the resource group level  
(c) Enable auditing in Azure Monitor  
(d) Create an alert rule to notify on changes  

**Correct answer: (b)**  
A **Read-only lock** ensures that users can view but not alter any resources in the group, which fits Taylor's monitoring-only requirement.

---

**3. Jordan accidentally deleted a virtual machine while cleaning up unused resources in the DevTest environment. What governance feature could have prevented this?**

(a) Azure Monitor  
(b) Just-in-Time VM Access  
(c) Azure Policy  
(d) Resource Lock  

**Correct answer: (d)**  
A **Resource Lock**, particularly a **Delete lock**, would have blocked deletion until explicitly removed, providing a safeguard for essential resources.

---

**4. At DevStreamCloud, Morgan needs to ensure a backup job can access a VM without making configuration changes. What is the best approach to secure this requirement?**

(a) Assign Owner role to the backup service  
(b) Apply a Delete lock to the VM  
(c) Apply a Read-only lock to the VM  
(d) Enable firewall protection  

**Correct answer: (c)**  
A **Read-only lock** allows access for reading, such as backup tasks, but restricts any write or delete operations, maintaining configuration integrity.

---

**5. Casey is managing multiple Azure environments at InfraWise Inc. What is one advantage of applying locks over relying solely on role-based access control (RBAC)?**

(a) Locks provide billing control features  
(b) Locks are inherited by all resources by default  
(c) Locks override RBAC to block specific actions like delete or write  
(d) Locks provide IP-level access control  

**Correct answer: (c)**  
**Locks** add an extra layer of protection by overriding user permissions, even if those users have delete or write access through **RBAC**.

---

**6. A DevOps engineer wants to prevent accidental modifications to production configurations but still allow metric analysis. What solution should they apply?**

(a) Enable Azure Sentinel on the resource  
(b) Apply a Read-only lock to the resource  
(c) Configure a diagnostic setting  
(d) Assign Contributor role with conditions  

**Correct answer: (b)**  
A **Read-only lock** allows viewing data such as performance metrics, logs, and dashboards, while preventing unauthorized configuration changes.

---

**7. While deploying infrastructure at BrightOps Solutions, a cloud engineer applies a lock but still experiences unauthorized changes. What is the most likely issue?**

(a) The lock was applied at the wrong resource scope  
(b) Azure doesn’t support locks for virtual machines  
(c) Locks were overwritten by RBAC policies  
(d) Azure Resource Manager failed  

**Correct answer: (a)**  
**Locks** are scope-specific. If applied at the wrong level (e.g., on a VM instead of its resource group), they won’t protect all necessary components.

---

**8. Taylor sets a Read-only lock at the subscription level to protect a set of resources. What effect will this have on underlying resource groups and their contents?**

(a) Only new resources will inherit the lock  
(b) All resource groups and their resources will become undeletable  
(c) All actions will be blocked including reads  
(d) It will apply to all child resources, restricting write and delete operations  

**Correct answer: (d)**  
A **Read-only lock** at the **subscription level** propagates to all child resources, effectively preventing write and delete actions across the board.

---

**9. Jordan wants to automate VM cleanup after test completion, but the script fails when attempting to delete a VM. What should he check first?**

(a) VM size and SKU restrictions  
(b) Storage blob lifecycle policies  
(c) Whether a Delete lock exists on the VM  
(d) NSG rules blocking the VM  

**Correct answer: (c)**  
If the **Delete lock** is active, deletion scripts and portal operations will fail. Removing the lock is a prerequisite to automate cleanup.

---

**10. A compliance officer asks Morgan to ensure all production resources in Azure are protected from accidental changes. What is the best proactive approach?**

(a) Apply diagnostic settings for all resources  
(b) Enable alerts on resource changes  
(c) Apply locks (Read-only or Delete) at the resource group level  
(d) Implement availability sets  

**Correct answer: (c)**  
Using **resource locks at the resource group level** ensures consistent governance across all production resources, helping protect them from unintended changes.

---

**11. Alex applies a Read-only lock to a resource group. What happens if he later attempts to scale up a virtual machine in that group?**

(a) The scaling will succeed, but with a warning  
(b) The scaling will be ignored until lock expiration  
(c) The operation will fail unless the lock is removed  
(d) The VM will be automatically restarted  

**Correct answer: (c)**  
A **Read-only lock** blocks any modification, including scaling operations. To perform changes, the lock must first be removed.

---

**12. Which Azure CLI command is used to create a lock on a resource?**

(a) `az lock apply`  
(b) `az resource lock create`  
(c) `az group lock set`  
(d) `az lock group create`  

**Correct answer: (b)**  
The correct command for locking a resource using **Azure CLI** is `az resource lock create`, which allows you to define scope, name, and type.

---


## 7️⃣ Engaging comic-style summary for retention

### 🚀 Meet Alex, the Curious Cloud Explorer

Alex, an energetic Azure admin at **SkyBridgeTech**, had a mission: protect critical resources from accidental deletion or unwanted changes. His goal? Use **resource locks** to keep things safe — like putting a seatbelt on production infrastructure!

---

### 🧱 Spinning Up the Virtual Engine

First things first, our CloudOps pro opened the **Azure portal** and created a brand-new **Virtual Machine** named `vm-skybridge-ubuntu01` under the resource group `rg-cloudcore-alex`. He chose **Ubuntu Server 20.04**, added credentials, picked a **Standard SSD**, and hit **Create**. Boom! His VM was up and running like a charm.

---

### 🔒 Armor Up with Delete Lock

Now that the VM was cruising, the Curious Cloud Explorer added a **Delete Lock** to the VM. This lock acted like a superhero shield, blocking any accidental delete clicks from even the most distracted engineer. Safe and sound!

---

### 🛡️ Fortifying the Whole Castle

But Alex didn’t stop there. To protect everything inside the resource group, he applied a **Read-only Lock** at the **resource group** level. That meant no sneaky config changes or resource deletions—just view access only. It was like putting the whole castle behind a magic "look-but-don’t-touch" barrier.

---

### 💥 Mission Accomplished, Cleanup Time

Once the demo was over, Alex removed the locks and cleaned up the entire environment with one click. No hiccups. Just a clean, safe, and smart Azure experience.

---

### 🎉 Lesson Learned

By using **resource locks**, our Azure admin ensured that production resources stayed protected and untouched — unless someone intentionally removed those locks. It’s a simple yet powerful trick every Azure pro should keep in their toolbox!

## 8️⃣ Text-based diagrams to visualize steps clearly

+-------------------------------------------------------------+
| Azure Resource Lock Lab |
| Guided by Alex from CloudCore Labs |
+-------------------------------------------------------------+

Start
↓
Login to Azure Portal as Alex
↓
+-----------------------------------------------+
| Create Resource Group |
| Name: rg-cloudcore-alex |
+-----------------------------------------------+
↓
+-----------------------------------------------+
| Create Virtual Machine |
| Name: vm-cloudcore-ubuntu01 |
| OS: Ubuntu Server 20.04 LTS |
| Size: Standard B2s |
| Disk: Standard SSD |
| Username: alex_admin |
+-----------------------------------------------+
↓
Deploy VM → Wait for provisioning to complete
↓
+-----------------------------------------------+
| Add Delete Lock to the Virtual Machine |
| Lock Name: VMDeleteLock |
| Lock Type: Delete |
+-----------------------------------------------+
↓
+------------------------------------------------+
| Add Read-only Lock to the Resource Group |
| Lock Name: RGReadOnly |
| Lock Type: Read-only |
+------------------------------------------------+
↓
(Optional) Test lock behavior:
→ Try to delete VM (should be blocked ❌)
→ Try to edit RG resources (should be blocked ❌)
↓
Remove Locks → Cleanup Resources
↓
End

### 🔍 What This Diagram Shows:

This diagram outlines the full process of using **resource locks** in Azure to protect both a **Virtual Machine** and its **Resource Group** from deletion or modification. Guided by Alex at **CloudCore Labs**, this lab emphasizes how to set up locks, validate their behavior, and manage cleanup effectively. Key Azure tools used include the **Azure Portal**, **Virtual Machine**, and the **Locks** feature under **Azure Resource Manager**.


## 9️⃣ Final reflection on the real-world efficiency of the lab

This lab provided Alex, the Azure admin at **CloudCore Labs**, with hands-on experience using **Azure Resource Locks** — a vital tool for maintaining governance and operational integrity in a cloud environment. By applying a **Delete lock** on a **Virtual Machine** and a **Read-only lock** on a **Resource Group**, Alex ensured that critical resources are protected against accidental or unauthorized changes — a common risk in shared or fast-moving cloud environments.

From a business perspective, implementing **resource locks** aligns directly with goals like **cost control**, **security**, and **compliance**. In real-world enterprise environments, such safeguards can prevent costly disruptions caused by mistaken deletions during maintenance or misconfigurations by new team members. This lab not only reinforces best practices in **Azure governance**, but also sharpens the learner’s skillset in **access control**, **infrastructure protection**, and **policy enforcement** — all key responsibilities for anyone in an **Azure Administrator** or **CloudOps** role.

Completing this exercise boosts confidence in managing production environments and empowers learners to design resilient, well-governed Azure architectures.


