# [3] Creating Azure Policies

This lab guide provides enterprise-ready, scenario-driven walkthroughs for mastering key Azure administrator tasks aligned with the AZ-104 certification.

---

# 💼 Azure Policy – Real-World Job Scenario MCQs (Interview Style)

These 10+ scenario-based MCQs are designed to help Azure admins and job seekers prepare for **real-world challenges** in enterprise cloud environments. Each question is structured like a situation you might face on the job or in a technical interview. Characters like **Ayesha**, **Rohan**, and **Omar** at **BrightOps Solutions** provide relatable context to mirror actual workplace decision-making.

---

**1. Ayesha is working on a project for BrightOps Solutions where the client must ensure all resources stay within UK data centers for legal compliance. What’s the best Azure-native way to enforce this requirement across all development environments?**

(a) Share a document outlining best practices with developers  
(b) Create an Azure Blueprint  
(c) Apply a built-in Azure Policy for allowed locations to each resource group  
(d) Tag all resources with "Region: UK South"  

✅ **Correct Answer: (c)**  
**Explanation:** Azure Policy is the most reliable way to enforce region-based restrictions consistently. Tags and documents can guide behavior, but only policy blocks non-compliant actions.

---

**2. During a review, Omar notices resources are being created in non-approved regions, despite an existing “Allowed Locations” policy. What is the first thing he should check in the policy configuration?**

(a) Whether the policy scope is set at the subscription level  
(b) If enforcement is enabled on the policy assignment  
(c) If the resource group has an access lock  
(d) Whether Azure Monitor is enabled  

✅ **Correct Answer: (b)**  
**Explanation:** A policy that isn’t enforced will only audit behavior and won’t block deployments. Always ensure enforcement is enabled for compliance-driven use cases.

---

**3. Rohan wants to apply a new policy only to a specific project team at BrightOps without affecting other departments. How should he scope the Azure Policy?**

(a) Apply it at the subscription level  
(b) Use a management group  
(c) Assign it directly to the specific resource group used by that team  
(d) Apply it to each individual resource manually  

✅ **Correct Answer: (c)**  
**Explanation:** Scoping at the resource group level provides precision and avoids unintended impact on other parts of the environment.

---

**4. Ayesha is preparing a policy to restrict location but is unsure which policy definition to use. What’s the most efficient method to identify suitable built-in policy templates in Azure?**

(a) Export policies from Azure Advisor  
(b) Manually write JSON policy from scratch  
(c) Use the “Definitions” section in the Policy service and search “Allowed locations”  
(d) Create a new resource and then reverse-engineer a policy  

✅ **Correct Answer: (c)**  
**Explanation:** Azure provides many built-in policies accessible through the “Definitions” area. Searching by keyword is fast and beginner-friendly.

---

**5. A new intern at BrightOps accidentally tried to deploy a database in East US, but the deployment failed. What message likely appeared during validation?**

(a) “Service unavailable in this region”  
(b) “Policy violation: deployment region not allowed”  
(c) “Admin approval required”  
(d) “Quota exceeded”  

✅ **Correct Answer: (b)**  
**Explanation:** If a policy restricting allowed locations is in place, Azure blocks the deployment and shows a clear error about the policy violation.

---

**6. Sofia, a senior admin, wants to validate compliance without blocking deployments. What setting should she disable in the policy assignment?**

(a) Scope  
(b) Parameters  
(c) Enforcement  
(d) Definitions  

✅ **Correct Answer: (c)**  
**Explanation:** Turning off enforcement allows Azure to log policy violations without preventing deployment—ideal for initial audits or monitoring-only scenarios.

---

**7. Jordan is building a new environment for the marketing team. To simplify policy application, he decides to use tags. How do tags differ from policies in this case?**

(a) Tags allow enforcement of deployment rules  
(b) Tags only label resources and do not enforce compliance  
(c) Tags work better than policies for region restrictions  
(d) Tags automatically delete non-compliant resources  

✅ **Correct Answer: (b)**  
**Explanation:** Tags help with organization and tracking but do not enforce behavior. Only policies can restrict or block deployments.

---

**8. Rohan is assigning a policy and sees the “Review + create” step. What happens if he skips reviewing and immediately hits Create without checking?**

(a) The policy is created, but it’s not active  
(b) Azure will ask for more admin approvals  
(c) The policy will be enforced immediately with the selected settings  
(d) The policy will apply after 24 hours  

✅ **Correct Answer: (c)**  
**Explanation:** Once deployed, a policy with enforcement enabled takes immediate effect for all resources within its scope.

---

**9. Alex at CloudCore Labs wants to prevent deployment of expensive VMs in non-production environments. Which approach aligns best with Azure governance practices?**

(a) Create custom alert rules  
(b) Block high-cost SKUs with Azure Policy  
(c) Use network security groups to isolate costly VMs  
(d) Manually check each VM size after deployment  

✅ **Correct Answer: (b)**  
**Explanation:** Azure Policy can block specific VM SKUs (e.g., high-cost series) from being deployed in non-production subscriptions or resource groups.

---

**10. Ayesha wants to reuse her “Allowed Locations” policy setup in another project. What’s the best way to duplicate this setup efficiently?**

(a) Write a PowerShell script from scratch  
(b) Use the same JSON and assign the policy to a new resource group  
(c) Ask each team to recreate it manually  
(d) Use Azure DevTest Labs templates  

✅ **Correct Answer: (b)**  
**Explanation:** Once defined, a policy can be reassigned to other scopes (resource groups or subscriptions) with minimal effort by reusing the definition.

---

**11. Morgan is helping audit BrightOps' Azure environment. She wants to know *which* resources are not following region restrictions. What tool should she use?**

(a) Azure Monitor Alerts  
(b) Azure CLI  
(c) Compliance view in the Policy service  
(d) Microsoft Defender for Cloud  

✅ **Correct Answer: (c)**  
**Explanation:** The Compliance tab in Azure Policy provides a visual report on which resources comply with the assigned policies.

---

**12. Omar deleted a policy by mistake, and now deployments are occurring in incorrect regions. What should his first recovery step be?**

(a) Re-enable Role-Based Access Control  
(b) Create a new policy definition from scratch  
(c) Reassign the existing built-in policy to the same scope  
(d) Wait for Azure to auto-restore policies  

✅ **Correct Answer: (c)**  
**Explanation:** If the policy was removed, simply reassigning the built-in version can restore compliance. There is no auto-restore feature.

---

**💡 Pro Tip for Interviews:** In real-world Azure environments, **governance through policies is key to scale**, especially when you manage many users or teams. Demonstrating policy understanding shows employers you're not just technical—you’re also strategic.
