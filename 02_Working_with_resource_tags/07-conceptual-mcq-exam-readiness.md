# [2] Working with resource tags

This lab guide provides enterprise-ready, scenario-driven walkthroughs for mastering key Azure administrator tasks aligned with the AZ-104 certification.

### 📝 **Azure Conceptual MCQs: Understanding Resource Tags, VMs, and Filtering**

Below are **10+ exam-style multiple-choice questions (MCQs)** designed to test your **conceptual understanding** of Azure resource tagging, virtual machine setup, and filtering practices—as explored in Lab 2. These questions use beginner-friendly language while still aligning with the **AZ-104 certification** mindset.

Each question includes a **real-world scenario**, four answer choices, and a detailed explanation for the correct choice.

---

### **1. Why might Sarah from BrightTech Solutions want to add a 'Department' tag to every virtual machine her team creates?**

**(a)** To reduce the size of the VM storage
**(b)** To make the VM run faster in Azure
**(c)** To help identify who owns or uses the resource
**(d)** To allow the VM to connect to external networks

✅ **Correct Answer: (c)**
**Explanation:** Tags like “Department” help track ownership and purpose of cloud resources. This makes it easier to manage costs, locate resources by team, and avoid confusion. The other options (a, b, d) have nothing to do with tagging.

---

### **2. Mike from NovaMedica wants to view only the virtual machines used by the Finance department. What’s the best way to do this in the Azure Portal?**

**(a)** Open each VM manually and read the notes
**(b)** Use the tag filter feature and search by Department = Finance
**(c)** Sort by region and find the ones from East US
**(d)** Delete all VMs and start from scratch

✅ **Correct Answer: (b)**
**Explanation:** Azure allows filtering by tags, which is much faster than checking each VM manually. This lets users instantly see only the resources related to a certain tag value, like “Finance.”

---

### **3. Alex created a VM in Azure and forgot to tag it. Later, during cleanup, he isn’t sure if it's still in use. What risk is he facing?**

**(a)** The VM will automatically turn off if it’s not tagged
**(b)** The VM will be locked permanently
**(c)** He might delete a critical resource by mistake
**(d)** Azure won’t allow him to use the VM

✅ **Correct Answer: (c)**
**Explanation:** Untagged resources make it difficult to know their purpose or owner. In large environments, this could lead to accidental deletion or billing issues.

---

### **4. In the lab, Taylor selects the VM size “B1s” when creating `vm-skynova-web01`. Why might this size be appropriate for a lab environment?**

**(a)** It’s a high-performance size for production workloads
**(b)** It’s a cost-effective size for light or test use
**(c)** It comes with extra tagging options
**(d)** It’s required for adding a Department tag

✅ **Correct Answer: (b)**
**Explanation:** The B1s size is often used for testing or lightweight use because it is small and affordable. It’s perfect for lab tasks that don’t require high performance.

---

### **5. John is applying a tag to a VM. He adds Name = "Finance" and Value = "Department". Why might this be confusing later?**

**(a)** Azure will block the tag
**(b)** The value "Department" is not valid
**(c)** He reversed the intended tag structure
**(d)** Tags can only be used on storage accounts

✅ **Correct Answer: (c)**
**Explanation:** The correct convention is **Name = Department, Value = Finance**. Reversing it could lead to confusion or filtering issues.

---

### **6. Sarah creates a resource group called `rg-labresources`, but forgets to assign it to a specific region. What could be the result?**

**(a)** The VM won’t be deployed
**(b)** The resource group will default to a region based on the first resource
**(c)** Tags won’t work
**(d)** Azure charges double the cost

✅ **Correct Answer: (b)**
**Explanation:** Resource groups themselves don’t lock into a region, but the region is tied to the **resources inside** it. Azure applies the region setting based on the VM or first deployed item.

---

### **7. Grace is auditing her Azure environment. She wants to identify all IT-related resources quickly. What should she do?**

**(a)** Check billing details one by one
**(b)** Ask every team to email her a list
**(c)** Use tag filters with Department = IT
**(d)** Rename every resource manually

✅ **Correct Answer: (c)**
**Explanation:** Tag filters allow you to instantly view all resources tagged with specific values like “IT,” making audits faster and more accurate.

---

### **8. Liam deletes a resource group and loses a virtual machine that wasn’t tagged. What lesson can be learned here?**

**(a)** Deleting resource groups is not allowed
**(b)** Tags automatically prevent deletion
**(c)** Untagged resources are harder to track and protect
**(d)** Azure restores deleted VMs by default

✅ **Correct Answer: (c)**
**Explanation:** Tags provide context and ownership information. Without them, it’s easy to accidentally delete something that might still be important.

---

### **9. Why is it useful to apply the tag directly on the virtual machine instead of just at the resource group level?**

**(a)** Because Azure doesn’t allow tagging at the resource group level
**(b)** Because individual tags help filter specific resources within a group
**(c)** Because only virtual machines can be billed
**(d)** Because tagging at the VM level increases its speed

✅ **Correct Answer: (b)**
**Explanation:** Tagging at the individual VM level provides **granular tracking**, especially when a resource group contains mixed resources used by different teams or projects.

---

### **10. Morgan wants to make sure all future Azure resources are tagged automatically. What’s the best long-term strategy?**

**(a)** Use Azure Policy to enforce tag rules
**(b)** Manually remind the team every day
**(c)** Disable tag settings so nothing is missed
**(d)** Use only one resource group forever

✅ **Correct Answer: (a)**
**Explanation:** Azure Policy can enforce rules such as requiring tags on all new resources. This reduces the chance of human error and ensures consistency.

---

### **11. If Sarah wants to remove all test VMs after a project ends, which practice would help her the most?**

**(a)** Naming each VM after the current day
**(b)** Adding a tag like Environment = Test to all temporary VMs
**(c)** Deleting every VM just to be sure
**(d)** Using different images for test and production VMs

✅ **Correct Answer: (b)**
**Explanation:** Adding a tag like `Environment = Test` helps Sarah filter out all temporary or non-production resources for easy cleanup later.

---

### 📘 **Final Note for Learners:**

These MCQs aren’t just for memory—they help you think like a cloud admin. By understanding how tags, VMs, and filters work together, you’ll be better prepared for real-world Azure tasks and the **AZ-104 certification exam**.

> Keep asking: *Who owns this? Why is it here? What happens if we lose it?*
> That’s where tagging becomes a superpower.
