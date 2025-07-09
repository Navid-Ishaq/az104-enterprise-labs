# [2] Working with resource tags

This lab guide provides enterprise-ready, scenario-driven walkthroughs for mastering key Azure administrator tasks aligned with the AZ-104 certification.

# 🔹 Interview-Focused Azure MCQs: Real-World Admin Scenarios from Lab 2

The following multiple-choice questions are crafted for job interview preparation and professional readiness. Each one presents a **practical scenario** that a cloud administrator might face in a real company environment. Characters and companies are fictional but grounded in realistic enterprise practices.

---

### **1. Jordan, an Azure administrator at CloudCore Labs, wants to ensure that all newly deployed virtual machines include a tag for the department they belong to. What is the best way to enforce this consistently across the company?**

**(a)** Add the tag manually each time a resource is created  
**(b)** Create an Azure Policy that requires the Department tag on resources  
**(c)** Include the tag in the VM name  
**(d)** Use a spreadsheet to track resources and their departments manually  

✅ **Correct Answer: (b)**  
**Explanation:** Azure Policy allows organizations to enforce resource standards, such as requiring specific tags. Manual entry is prone to human error, and naming conventions are not substitutes for proper metadata.

---

### **2. Emily at InfraWise Inc. needs to identify all virtual machines that belong to the HR department for an upcoming cost audit. What is the most efficient method to retrieve these resources?**

**(a)** Use Azure Cost Management to search by resource type  
**(b)** Browse each VM individually for usage metrics  
**(c)** Use a tag filter where Department = HR in the Azure Portal  
**(d)** Sort resources by creation date  

✅ **Correct Answer: (c)**  
**Explanation:** Filtering by tag is the fastest and most accurate way to find department-specific resources when tags are applied consistently.

---

### **3. Naveed is cleaning up unused resources in the development subscription at BrightOps Solutions. One VM is not tagged, and its purpose is unclear. What is the best action to take?**

**(a)** Delete it immediately to save costs  
**(b)** Assign a default tag and rename it  
**(c)** Contact the resource owner or log source to confirm before deleting  
**(d)** Move it to another resource group for isolation  

✅ **Correct Answer: (c)**  
**Explanation:** Deleting untagged resources without verification could disrupt services. Identifying the owner or checking usage logs is a safer approach in an enterprise setting.

---

### **4. Maya at NovaBridge IT wants to ensure that only IT team members can view and manage VMs tagged as Department = IT. What should she implement?**

**(a)** RBAC permissions scoped to the VM resource group and filtered by tags  
**(b)** Rename the VMs so others won’t find them  
**(c)** Change the Azure region to restrict access  
**(d)** Use the Azure CLI to hide the VM  

✅ **Correct Answer: (a)**  
**Explanation:** Role-Based Access Control (RBAC) can be scoped to resource groups or specific resources. Combined with tag-based management, this supports secure, role-specific visibility and control.

---

### **5. Olivia from EdgeScale Technologies is managing hundreds of VMs across projects. She wants to know which VMs were used in a recent marketing campaign. What should she have done in advance?**

**(a)** Use different regions for each department  
**(b)** Assign custom tags like Campaign = Summer2024  
**(c)** Limit VM creation to only senior engineers  
**(d)** Manually write a log of VM creation dates  

✅ **Correct Answer: (b)**  
**Explanation:** Tags provide essential metadata for organizing and filtering resources. A campaign-specific tag would have made retrieval easy and reliable.

---

### **6. At BlueNova Systems, Marcus applied the tag Department = Sales to several VMs. Later, he filters the resource group but nothing shows up. What might be the issue?**

**(a)** Tags don’t work on virtual machines  
**(b)** Tags can only be applied at the resource group level  
**(c)** He applied the tags after filtering, or used a case-sensitive mismatch  
**(d)** He selected the wrong image when creating the VMs  

✅ **Correct Answer: (c)**  
**Explanation:** Tag filtering is case-insensitive but depends on accurate values. If the tag wasn’t applied before filtering or had a typo, results will not appear.

---

### **7. Fiona at DevStreamCloud wants to automate the tagging of virtual machines during deployment. What is the best way to achieve this at scale?**

**(a)** Create a script using Azure CLI or ARM templates with predefined tags  
**(b)** Apply tags manually after every VM is deployed  
**(c)** Add a note in the company wiki to remind users  
**(d)** Email her team weekly with the list of expected tags  

✅ **Correct Answer: (a)**  
**Explanation:** Automation via templates or scripting ensures consistency and efficiency. Manual tagging is unreliable at scale.

---

### **8. Lucas notices that many Azure resources in SkyBridgeTech are missing tags, leading to cost tracking issues. As an Azure Admin, what should he do first to fix this moving forward?**

**(a)** Delete all untagged resources  
**(b)** Implement a tagging policy using Azure Policy  
**(c)** Rename the resources to include team names  
**(d)** Restrict new VM creation to only one user  

✅ **Correct Answer: (b)**  
**Explanation:** Azure Policy is used to enforce resource compliance such as mandatory tagging. This helps prevent untagged resource creation in the future.

---

### **9. Nina works at NextGenOps and wants to see how many VMs the IT department is running across multiple regions. What’s the most scalable approach?**

**(a)** Create an Excel report by exporting all VMs manually  
**(b)** Use Azure Resource Graph to query resources based on tags  
**(c)** Open each resource group individually and count  
**(d)** Use Azure Monitor alerts  

✅ **Correct Answer: (b)**  
**Explanation:** Azure Resource Graph allows querying across the entire subscription using tags. This is the most scalable and accurate method for cross-region visibility.

---

### **10. A senior admin at InfraWise Inc. wants to prepare for chargeback billing. How can tagging help support that model?**

**(a)** Tags have no impact on cost analysis  
**(b)** Tags allow for tracking resource costs by project or department  
**(c)** Tags automatically apply discounts  
**(d)** Tags prevent budget overruns  

✅ **Correct Answer: (b)**  
**Explanation:** Tags enable detailed cost breakdowns in Azure Cost Management. This supports internal billing or chargeback models by tracking usage by team or project.

---

### **11. Jacob creates a VM with a tag but later moves it to another resource group. Will the tag still apply?**

**(a)** No, tags are deleted when resources are moved  
**(b)** Yes, resource-level tags stay attached to the resource  
**(c)** Only if the VM was shut down first  
**(d)** Only if the resource group has the same tag  

✅ **Correct Answer: (b)**  
**Explanation:** Tags applied at the resource level remain attached even if the resource is moved to another group.

---

### 📘 Final Note for Interview Prep:
These MCQs reflect **real-life decisions** Azure admins make daily—around cost tracking, access control, automation, and governance. Mastering resource tagging is **not just a best practice**—it’s foundational to running a scalable, secure, and well-managed Azure environment.

