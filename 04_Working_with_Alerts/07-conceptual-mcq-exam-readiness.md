# [4] Working with Alerts

This lab guide provides enterprise-ready, scenario-driven walkthroughs for mastering key Azure administrator tasks aligned with the AZ-104 certification.

---

### 🔹 Point 7 of 9: Exam Readiness Check — 10+ Conceptual MCQs on Azure Alerts & Monitoring

Below are 10 carefully crafted multiple-choice questions (MCQs) designed to deepen understanding of core Azure monitoring concepts, especially those practiced in **Lab 4: Working with Alerts**. These questions are written in simple language but reflect **real-world scenarios** you might see in the **AZ-104** exam or while working in the field. Characters like **Ayesha**, **Rohan**, and others are included to give context and life to the situations.

---

**1. Ayesha at BrightOps Solutions wants to be notified if someone restarts her test virtual machine. What type of Azure service should she use to set up this kind of alert?**  
(a) Azure Backup  
(b) Azure Security Center  
(c) Azure Monitor Alert  
(d) Azure Resource Manager  

**✅ Correct Answer: (c)**  
**Explanation:** Azure Monitor Alert is the right tool for this job. It allows you to monitor Azure resources and notify users when a specified condition occurs. Restarting a VM falls under administrative operations, which can be tracked via alert rules.

---

**2. Rohan creates an alert rule but forgets to add an action group. What is the likely outcome?**  
(a) The VM will automatically shut down.  
(b) The alert will still be triggered, but no one will be notified.  
(c) The alert rule will not be created.  
(d) Azure will send a notification to all admins by default.  

**✅ Correct Answer: (b)**  
**Explanation:** Alerts can trigger without an action group, but no notification will be sent unless you define where and how to send it. Action groups connect the alert to actual people or systems.

---

**3. Which of the following best describes the role of an action group in Azure Alerts?**  
(a) It creates backup schedules.  
(b) It filters out unwanted alerts.  
(c) It defines who gets notified and how.  
(d) It increases VM performance.  

**✅ Correct Answer: (c)**  
**Explanation:** Action groups define how alert notifications are delivered—via email, SMS, push notification, or webhook—and to whom. It's like creating a contact list for emergencies.

---

**4. Alex set up an alert for his virtual machine, but no emails are being received. What should he check first?**  
(a) If the VM has a static IP address  
(b) If the VM was stopped  
(c) If his email is added and confirmed in the action group  
(d) If the disk type is set to SSD  

**✅ Correct Answer: (c)**  
**Explanation:** If emails aren't being received, the most common reason is that the email was not added correctly or wasn’t confirmed in the action group during setup.

---

**5. In the lab, Rohan selected the signal "All Administrative operations." What type of activities does this signal monitor?**  
(a) System memory and CPU usage  
(b) File uploads to storage  
(c) Changes like VM restarts, stops, or configuration edits  
(d) Network traffic to the VM  

**✅ Correct Answer: (c)**  
**Explanation:** The "All Administrative operations" signal helps track critical changes made through Azure Resource Manager, like VM restarts or size changes—perfect for accountability and auditing.

---

**6. Sofia works at CloudCore Labs and needs to test if her alert is working. What’s a simple action she can take to trigger it?**  
(a) Change the subscription tier  
(b) Restart the virtual machine  
(c) Open a web browser on the VM  
(d) Install antivirus software on the VM  

**✅ Correct Answer: (b)**  
**Explanation:** Restarting the VM is a common admin-level operation that triggers the alert linked to "All Administrative operations."

---

**7. Why is it important to delete the resource group after completing a test lab like this?**  
(a) To upgrade Azure services  
(b) To switch regions  
(c) To avoid ongoing charges and clean up unused resources  
(d) To reset the operating system  

**✅ Correct Answer: (c)**  
**Explanation:** Deleting the resource group cleans up all the associated resources and helps avoid unexpected billing, especially in test environments.

---

**8. Ayesha wants to monitor a production VM 24/7. What can she do to ensure alerts are not missed, even outside office hours?**  
(a) Add multiple users to the action group  
(b) Use Azure Bastion to access the VM  
(c) Change the VM size to Premium tier  
(d) Stop the VM during off-hours  

**✅ Correct Answer: (a)**  
**Explanation:** By adding multiple recipients to the action group (such as team leads, ops staff, etc.), Ayesha ensures that someone will receive and respond to the alert, even during non-working hours.

---

**9. Omar is unsure whether he should choose "All Administrative operations" or "CPU usage" for his alert condition. Which of the following would help him decide?**  
(a) He wants to track if the VM gets restarted →  
(b) He wants to detect if a file is downloaded →  
(c) He wants to know if disk space runs low →  
(d) He wants to track network latency  

**✅ Correct Answer: (a)**  
**Explanation:** “All Administrative operations” will help Omar track changes like restarts or resizing — administrative-level events, not performance-based ones like CPU.

---

**10. If Jordan restarts a VM but receives no alert, which issue is least likely to be the cause?**  
(a) The action group wasn't created  
(b) The alert rule was never saved  
(c) The alert condition wasn't specific enough  
(d) The VM was in a different subscription  

**✅ Correct Answer: (c)**  
**Explanation:** "All Administrative operations" is already broad. The other options are more likely culprits for the alert failure — especially missing action groups or mismatched scopes.

---

**11. Why might Rohan want to create alert rules for all his non-production VMs too, not just critical ones?**  
(a) Because alerts improve virtual machine boot time  
(b) Because test environments can also impact business if misconfigured  
(c) Because alerts stop the VM from restarting  
(d) Because alerts are only available for test VMs  

**✅ Correct Answer: (b)**  
**Explanation:** Even non-production environments can cause problems if misused—alerting helps catch mistakes early, even in test/demo VMs.

---

**12. Which of the following best summarizes the goal of this Azure lab?**  
(a) To reduce costs by shrinking VM size  
(b) To learn how to install security software  
(c) To set up alerts and understand how Azure communicates critical events  
(d) To build a new cloud network  

**✅ Correct Answer: (c)**  
**Explanation:** This lab focuses on building awareness through alerts—knowing when things happen inside your Azure environment and staying informed.

---

> ✍️ These MCQs reinforce **real-world thinking**, not just lab steps. They help learners get exam-ready while also preparing them to manage cloud resources responsibly and proactively.
