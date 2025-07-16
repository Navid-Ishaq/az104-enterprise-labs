# 📘 Azure Security Engineer – Professional-Level MCQs

Point 10 – Client Readiness Check: Evaluating with Precision

---

> *"If I'm going to hire an Azure Security Engineer, I need to evaluate with professional-level questions!"*  
> — A Real-World Client

---

## 🧠 10+ Scenario-Based Azure Security MCQs

Each question includes context, four options, the correct answer, and a clear explanation.

---

**Q1. Omar is deploying a virtual network in Azure for CloudCore Labs. He wants to restrict the creation of virtual networks only to the West Europe region. What Azure feature should he use to enforce this?**

(a) Azure Role-Based Access Control (RBAC)  
(b) Azure Policy  
(c) Azure Blueprint  
(d) Azure Locks  

✅ **Correct Answer:** (b)  
💡 **Explanation:** **Azure Policy** allows you to enforce location-based restrictions for resources. RBAC controls actions, not rules. Blueprints are collections of artifacts. Locks prevent deletion or changes but not creation scope rules.

---

**Q2. Rohan accidentally deployed a resource to East US instead of UK South. Azure Policy blocked the deployment. What was most likely applied?**

(a) Initiative Definition for Tagging  
(b) Policy Definition for Allowed Locations  
(c) RBAC Deny Assignment  
(d) Network Security Group (NSG) Rule  

✅ **Correct Answer:** (b)  
💡 **Explanation:** The **Allowed Locations policy** defines which regions are permissible for resource deployment. This is a classic use case for Azure Policy.

---

**Q3. Ayesha wants to ensure that sensitive files in Azure Blob Storage are accessed infrequently and stored at low cost. What tier should she choose?**

(a) Hot Tier  
(b) Cool Tier  
(c) Archive Tier  
(d) Premium Tier  

✅ **Correct Answer:** (b)  
💡 **Explanation:** **Cool Tier** is ideal for infrequently accessed data (30-day minimum). Archive is lower cost but less accessible and for long-term cold storage.

---

**Q4. Which of the following services provides threat protection for Azure resources and sends security alerts?**

(a) Azure Key Vault  
(b) Azure Monitor  
(c) Microsoft Defender for Cloud  
(d) Azure Firewall  

✅ **Correct Answer:** (c)  
💡 **Explanation:** **Microsoft Defender for Cloud** provides unified security management and threat protection across your Azure resources.

---

**Q5. Sofia created a File Share in Azure for a client using the Hot tier. What does the Hot tier signify in this context?**

(a) Files are encrypted by default  
(b) Files can be accessed only once a month  
(c) Files are expected to be accessed frequently  
(d) Files are stored on a local SSD  

✅ **Correct Answer:** (c)  
💡 **Explanation:** **Hot tier** in Azure File Share means data is accessed frequently and is optimized for performance.

---

**Q6. Which Azure tool would allow Jamalu to restrict the creation of virtual machines to only a specific size and region?**

(a) Azure Advisor  
(b) Azure Blueprints  
(c) Azure Policy  
(d) Azure Resource Locks  

✅ **Correct Answer:** (c)  
💡 **Explanation:** **Azure Policy** is the only one here that can define allowed VM SKUs and regions. Blueprints apply a group of policies and templates, not direct restriction.

---

**Q7. Which scenario best justifies the use of Zone-Redundant Storage (ZRS)?**

(a) Backing up long-term cold data  
(b) High-availability workloads needing in-region fault tolerance  
(c) Small development VMs  
(d) Reducing access latency for archived files  

✅ **Correct Answer:** (b)  
💡 **Explanation:** **ZRS** spreads data across availability zones in the same region, making it ideal for HA workloads.

---

**Q8. Why might a client prefer using Geo-Zone-Redundant Storage (GZRS) over Geo-Redundant Storage (GRS)?**

(a) GZRS is cheaper  
(b) GZRS combines zone redundancy with geo-replication  
(c) GRS provides lower latency  
(d) GZRS disables global replication  

✅ **Correct Answer:** (b)  
💡 **Explanation:** **GZRS** combines **ZRS + GRS**, offering the benefits of both zone and regional redundancy.

---

**Q9. Taylor needs to ensure an HTML file stored in Azure Blob Storage is publicly accessible via URL. What should they do?**

(a) Enable NSG rule for port 443  
(b) Set the container access level to Blob (anonymous)  
(c) Use a shared access signature only  
(d) Assign the Storage Contributor role  

✅ **Correct Answer:** (b)  
💡 **Explanation:** To make blobs publicly accessible, set the **container’s access level** to allow anonymous read access to blob data.

---

**Q10. Marcus uploaded sensitive client files to a File Share in Azure. What is one critical step he must take to ensure encryption at rest?**

(a) Enable BitLocker manually  
(b) Choose Premium tier  
(c) Use Azure Policy  
(d) Ensure Storage Service Encryption (SSE) is enabled  

✅ **Correct Answer:** (d)  
💡 **Explanation:** Azure **Storage Service Encryption (SSE)** is enabled by default and ensures all data is encrypted at rest.

---

## 🧭 Final Thought from Jamalu

> _"Security isn't just code — it's care, intention, and quiet vigilance."_  
> — Jamalu  
> — **Siraat AI Academy**

---
