# [3] Creating Azure Policies

This lab guide provides enterprise-ready, scenario-driven walkthroughs for mastering key Azure administrator tasks aligned with the AZ-104 certification.

```markdown
# 🧠 Azure Policy – Conceptual MCQs (AZ-104 Aligned)

Below are 10+ conceptual multiple-choice questions based on **Lab 3: Creating Azure Policies**. Each question is written to reflect **real-world scenarios**, helping learners like **Ayesha, Rohan, and Jordan** at **BrightOps Solutions** develop strong, exam-ready understanding.

---

**1. Ayesha wants to ensure that her team can only deploy Azure resources within the UK South region. What is the most efficient and scalable way to enforce this rule across a resource group?**

(a) Send out an email reminder to team members  
(b) Use Resource Locks on each resource manually  
(c) Apply a built-in Azure Policy for allowed locations to the resource group  
(d) Ask users to manually select UK South when creating resources  

✅ **Correct Answer: (c)**  
**Explanation:** Azure Policy is designed for enforcing rules like allowed regions. It applies consistently and automatically, whereas options like emails or reminders depend on human compliance and can easily be ignored.

---

**2. Why is it important for BrightOps Solutions to restrict resource creation to a specific Azure region using policies?**

(a) It helps reduce the number of users who can access the portal  
(b) It ensures users don't create duplicate resources by mistake  
(c) It helps meet data residency, compliance, and performance needs  
(d) It boosts billing efficiency by tracking costs per user  

✅ **Correct Answer: (c)**  
**Explanation:** Region restrictions are especially important for businesses dealing with data privacy laws (e.g., GDPR). Creating resources in unapproved regions could lead to legal or performance issues.

---

**3. Rohan accidentally deploys a virtual machine in East US instead of UK South. Which feature could have prevented this mistake *before* the deployment?**

(a) Azure Cost Management  
(b) Azure Policy with allowed location restriction  
(c) Azure Monitor alerts  
(d) Azure Resource Manager templates  

✅ **Correct Answer: (b)**  
**Explanation:** Azure Policy can enforce rules that prevent incorrect configurations at the deployment stage itself, unlike alerts or templates which come later or are more flexible.

---

**4. While assigning the policy, Ayesha notices an option called “Policy enforcement.” What happens if she disables this setting?**

(a) The policy will automatically delete any resources outside the rule  
(b) The policy will apply but won’t block non-compliant deployments  
(c) The policy will redirect all deployments to the correct region  
(d) The policy won’t be visible in the portal  

✅ **Correct Answer: (b)**  
**Explanation:** Disabling enforcement means the policy becomes non-blocking—it reports non-compliance but does not stop it. It's useful for testing or auditing purposes.

---

**5. Which of the following best describes what the Azure Policy “Scope” setting does during assignment?**

(a) It filters which policies are available in your account  
(b) It decides the subscription’s default billing rules  
(c) It defines which Azure resources or groups the policy will apply to  
(d) It controls user access to the Azure portal  

✅ **Correct Answer: (c)**  
**Explanation:** “Scope” determines where the policy will be enforced—whether at the subscription, resource group, or management group level.

---

**6. Jordan wants to apply the policy to a specific resource group, but not the entire subscription. Which step should he focus on?**

(a) Adding a lock to the subscription  
(b) Editing role assignments  
(c) Using the Scope selector during policy assignment  
(d) Creating a new Azure region  

✅ **Correct Answer: (c)**  
**Explanation:** The Scope selector lets you narrow down where the policy applies—like applying it only to a particular department’s resource group instead of all cloud environments.

---

**7. Ayesha finishes applying the policy and then tries to test it. She creates a virtual network in East US and sees a validation error. What does this tell her?**

(a) The Azure portal is having temporary issues  
(b) The policy was not applied correctly  
(c) The resource group is misconfigured  
(d) The policy is working as expected and blocking disallowed regions  

✅ **Correct Answer: (d)**  
**Explanation:** A validation error when trying to deploy in East US confirms the policy enforcement is working and preventing non-compliant deployments.

---

**8. What is the primary purpose of using a built-in Azure Policy like “Allowed locations” instead of creating a custom policy from scratch?**

(a) Built-in policies are cheaper than custom ones  
(b) Built-in policies cannot be changed and are permanent  
(c) Built-in policies provide ready-to-use templates that save time  
(d) Custom policies are less secure  

✅ **Correct Answer: (c)**  
**Explanation:** Built-in policies are pre-created by Microsoft and can be quickly applied for common use cases like region or SKU restrictions, saving time for administrators.

---

**9. After completing the lab, Ayesha wants to clean up the test environment. What’s the best way to remove all resources created during the lab?**

(a) Delete each resource one by one manually  
(b) Use the Azure Recycle Bin  
(c) Delete the entire resource group used in the lab  
(d) Contact Azure Support  

✅ **Correct Answer: (c)**  
**Explanation:** Deleting the resource group is the fastest and cleanest way to remove all resources created under it, especially in a lab or sandbox environment.

---

**10. Why would a company like BrightOps Solutions apply region-based policies even for internal development environments?**

(a) Developers shouldn’t have access to the Azure portal  
(b) It improves load balancing of apps  
(c) It prevents inconsistent deployments that lead to extra costs or data issues  
(d) Azure forces all companies to apply regional policies  

✅ **Correct Answer: (c)**  
**Explanation:** Applying policies early—even in dev—builds good habits, avoids configuration drift, and keeps environments consistent, saving cost and avoiding surprises later.

---

**11. Omar, a new hire at BrightOps, wonders what would happen if he tried to deploy a resource outside the allowed region under an active policy. What should Ayesha tell him?**

(a) Azure would auto-correct the region during deployment  
(b) Azure will block the deployment with a clear error  
(c) Azure will create the resource in a new subscription  
(d) The deployment will go through, but trigger an email warning  

✅ **Correct Answer: (b)**  
**Explanation:** Azure Policy enforcement checks the deployment and blocks it if the resource configuration violates the assigned policy.

---

**12. Which statement best describes how Azure Policy helps with governance at scale?**

(a) It sets up automated billing for each department  
(b) It blocks all unauthorized users from logging in  
(c) It allows organizations to apply consistent rules without manual review  
(d) It replaces all manual documentation processes  

✅ **Correct Answer: (c)**  
**Explanation:** Azure Policy enables automatic rule enforcement across many resources, making governance scalable and consistent—even across large enterprises.

---

**✨ Tip for Learners:** Always think about Azure Policy as your **invisible assistant**. It doesn’t just help once—it continuously enforces rules and guides teams without needing constant reminders. That’s why it’s a vital tool for real-world cloud management and AZ-104 readiness.

```
