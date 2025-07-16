
# 🔐 Azure Security MCQs – Jamalu’s Real-World Set

> “If I’m going to hire an Azure Security Engineer, I need to evaluate them with real-world, professional-level questions. The kind of questions that separate a surface learner from a solid expert.”
> — BrightOps Client

---

## 🎯 Purpose

This file contains a carefully curated set of **10+ multiple-choice questions (MCQs)** related to real-world **Azure Security** tasks. Each MCQ is scenario-based, realistic, and intended to prepare learners not just for the **AZ-500** exam — but for real job performance.

---

## 📚 Format

Each MCQ includes:

- **1 realistic scenario-based question**
- **4 options**
- **✅ Clearly marked correct answer**
- **💡 Explanation with context and clarity**

---

### **Q1. Omar is writing an Azure Policy at CloudCore Labs to ensure that VMs are only deployed in specific regions. Which built-in policy definition should he use?**

(a) Audit VMs without tags  
(b) Allowed locations  
(c) Allowed storage SKUs  
(d) DeployIfNotExists for virtual machines  

✅ **Correct Answer:** (b)  
💡 **Explanation:** *“Allowed locations” is the built-in policy that restricts resource creation to specific regions. This helps enforce geo-compliance and data residency rules.*

---

### **Q2. Sarah, a security intern at BlueNova Systems, is monitoring suspicious traffic. Which Azure tool helps her analyze outgoing traffic from VMs?**

(a) Azure Firewall  
(b) Azure Traffic Manager  
(c) NSG Flow Logs  
(d) Application Gateway  

✅ **Correct Answer:** (c)  
💡 **Explanation:** *NSG Flow Logs track inbound and outbound traffic at the network interface level, which is useful for analyzing security incidents.*

---

### **Q3. Taylor at NextGenOps wants to automate the deployment of security baseline policies across all subscriptions. Which service best supports this goal?**

(a) Azure Blueprints  
(b) Azure Monitor  
(c) Log Analytics  
(d) Resource Graph  

✅ **Correct Answer:** (a)  
💡 **Explanation:** *Azure Blueprints help automate the assignment of role-based access, policies, and resource templates across multiple environments.*

---

### **Q4. Alex notices a VM in SkyBridgeTech has unrestricted inbound RDP access from the internet. What is the best mitigation step?**

(a) Enable JIT VM Access  
(b) Change the VM password  
(c) Increase the NSG priority  
(d) Delete the VM  

✅ **Correct Answer:** (a)  
💡 **Explanation:** *Just-In-Time (JIT) VM access limits the time and IP address ranges that can connect to a VM, reducing exposure.*

---

### **Q5. Ayesha needs to store and retrieve secrets for an application running in Azure. What service should she use?**

(a) Azure Storage Account  
(b) Azure Key Vault  
(c) Azure App Service  
(d) Azure Monitor  

✅ **Correct Answer:** (b)  
💡 **Explanation:** *Azure Key Vault is a cloud service that provides secure storage and access control for secrets, keys, and certificates.*

---

### **Q6. What does the “GRS” redundancy option offer in Azure Storage?**

(a) Redundancy within a single zone  
(b) Redundancy across three zones in a region  
(c) Geo-redundancy across two regions  
(d) Manual backup of data  

✅ **Correct Answer:** (c)  
💡 **Explanation:** *Geo-redundant storage (GRS) replicates your data to a secondary region for disaster recovery.*

---

### **Q7. What’s a common use case for Azure Private Endpoints in storage?**

(a) Encrypting blob data  
(b) Controlling access through VNet integration  
(c) Caching files on-prem  
(d) Publicly exposing file shares  

✅ **Correct Answer:** (b)  
💡 **Explanation:** *Private Endpoints connect you securely to Azure services over a private IP in your VNet, avoiding public exposure.*

---

### **Q8. Why might a policy assignment fail when deploying a VM to “East US” region?**

(a) Missing tags  
(b) Policy enforcement is disabled  
(c) Region is not listed in Allowed Locations  
(d) Lack of subscription-level permissions  

✅ **Correct Answer:** (c)  
💡 **Explanation:** *If a policy limits allowed regions and “East US” isn’t included, deployment will be blocked.*

---

### **Q9. What tool helps audit changes and events in Azure subscriptions?**

(a) Azure Monitor  
(b) Azure Activity Log  
(c) Azure Sentinel  
(d) Log Analytics  

✅ **Correct Answer:** (b)  
💡 **Explanation:** *Azure Activity Log records control-plane events across subscriptions, useful for auditing.*

---

### **Q10. Which Azure service provides SIEM and SOAR capabilities for threat detection?**

(a) Azure Defender  
(b) Azure Firewall  
(c) Microsoft Sentinel  
(d) Azure Monitor  

✅ **Correct Answer:** (c)  
💡 **Explanation:** *Microsoft Sentinel is Azure’s cloud-native SIEM/SOAR platform for threat detection and automated response.*

---

> _“These questions won’t just prepare you to pass — they’ll prepare you to perform.”_  
> — Jamalu  
> — **Siraat AI Academy**

---



# 🔐 Azure Security MCQs – Lab 6: Network Access to Storage Accounts

> High-quality, scenario-based MCQs for AZ-500 interview readiness and certification preparation.

---

## 📘 Topic Overview:
This MCQ set is based on **Lab 6: Network Access to Storage Accounts**, focusing on secure access to Azure **Storage Accounts** via **Private Endpoints**, **Virtual Networks**, and **Storage Explorer** within a **Windows VM**.

---

### ✅ Questions

**Q1. Why was a private endpoint used for the storage account in this lab?**

(a) To improve performance during uploads  
(b) To enable encryption of storage data  
(c) To restrict access to the storage account via a private IP  
(d) To configure DNS forwarding  

✅ **Correct Answer:** (c)  
💡 **Explanation:** A **private endpoint** provides secure access to an Azure resource over a private IP address from within a virtual network, removing the need for public access.

---

**Q2. What was the purpose of disabling public access during storage account creation?**

(a) It enables geo-replication  
(b) It allows NSG rules to apply directly  
(c) It forces access to happen only over private endpoint  
(d) It is required for Standard_LRS performance tier  

✅ **Correct Answer:** (c)  
💡 **Explanation:** Disabling public access ensures that only **private endpoint traffic** can reach the storage account, increasing security.

---

**Q3. In the virtual network setup, why was a custom subnet address (10.0.0.0/24) used?**

(a) To ensure compatibility with the VM image  
(b) To define IP range for private endpoint and VM  
(c) To enforce encryption at subnet level  
(d) Required for GRS redundancy  

✅ **Correct Answer:** (b)  
💡 **Explanation:** Defining a subnet IP range ensures that **VMs and endpoints** deployed in the same subnet can communicate securely.

---

**Q4. What command helps validate private DNS resolution inside the VM?**

(a) ping stgnxtnav001.blob.core.windows.net  
(b) curl stgnxtnav001  
(c) nslookup stgnxtnav001.blob.core.windows.net  
(d) az login  

✅ **Correct Answer:** (c)  
💡 **Explanation:** `nslookup` checks if the **blob endpoint** resolves correctly using **private DNS** when connected through a **private endpoint**.

---

**Q5. Why was Azure Storage Explorer installed inside the VM?**

(a) To download operating system logs  
(b) To manage VM snapshots  
(c) To upload and explore storage account blobs  
(d) Required to connect via RDP  

✅ **Correct Answer:** (c)  
💡 **Explanation:** **Azure Storage Explorer** enables you to manage blob containers, file shares, and other storage elements from within the VM environment.

---

**Q6. What happens if the VM is deployed in a different virtual network than the private endpoint?**

(a) It will automatically create a peering  
(b) Access to the storage account might fail  
(c) The VM will still access the blob using public DNS  
(d) GRS will automatically replicate data  

✅ **Correct Answer:** (b)  
💡 **Explanation:** The VM must be in the **same VNet or properly peered** network to access the resource via private endpoint.

---

**Q7. Which access method was used in Storage Explorer to connect to the storage account?**

(a) Azure AD sign-in  
(b) SAS Token  
(c) Connection String  
(d) Shared File Mount  

✅ **Correct Answer:** (c)  
💡 **Explanation:** The lab used a **connection string** obtained from the **Access Keys** section of the storage account to authenticate.

---

**Q8. What type of redundancy was selected during storage account setup?**

(a) LRS  
(b) ZRS  
(c) GRS  
(d) GZRS  

✅ **Correct Answer:** (c)  
💡 **Explanation:** **GRS (Geo-redundant storage)** replicates your data to a secondary region for higher availability.

---

**Q9. Why was the VM deployed into the same subnet as the private endpoint?**

(a) For easier NSG control  
(b) To support boot diagnostics  
(c) To enable private IP communication  
(d) For better performance of SSD  

✅ **Correct Answer:** (c)  
💡 **Explanation:** Being in the same **subnet** allows the VM to access the storage account using the **private endpoint IP**.

---

**Q10. What initial setting had to be turned off in Server Manager to allow browser downloads?**

(a) RDP Access  
(b) IE Enhanced Security Configuration  
(c) Windows Firewall  
(d) PowerShell Execution Policy  

✅ **Correct Answer:** (b)  
💡 **Explanation:** **IE Enhanced Security Configuration** limits downloads and browsing; turning it off allows downloading tools like Storage Explorer.

---

> _"Real security isn't just about locks and firewalls — it's about understanding the path and respecting the limits."_  
> — Jamalu  
> — **Siraat AI Academy**

"""

