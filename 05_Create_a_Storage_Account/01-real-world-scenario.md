# [5] Create a Storage Account

This lab guide provides enterprise-ready, scenario-driven walkthroughs for mastering key Azure administrator tasks aligned with the AZ-104 certification.

---
### 🔹 **Point 1 of 9: Real-World Scenario – Making Storage Count at Scale**

---

## 🌟 Main Title: “The Storage Dilemma at SkyBridgeTech – Picking the Right Fit for the Cloud”

---

### 🏢 A Normal Monday, an Unexpected Storage Need

At **SkyBridgeTech**, a mid-sized cloud consulting firm, the infrastructure team was preparing for a new client onboarding—a healthcare analytics startup called *MediTrack Insights*. The client had one requirement: their patient reports, dashboards, and backups must be stored securely and reliably in the cloud, with **minimal cost and maximum performance**.

**Ayesha**, a cloud administrator from Toronto, and **Omar**, a junior engineer from Cairo, were tasked with building a proof-of-concept in Azure. Their manager, Jordan, popped into their Teams chat:

> **“Let’s keep it simple for now. Show the client how we can store files, secure them, and access them easily. Start with Azure Storage Accounts.”**

---

### 📦 Understanding Storage Options Before Clicking “Create”

Before diving into the portal, Ayesha and Omar sat down to compare Azure storage account options. Omar read aloud, “So we have **Standard** and **Premium** performance tiers. Standard is more cost-effective. That might work for these initial dashboards, right?”

They also reviewed **redundancy options**—from LRS (local copies) to GZRS (geo + zone redundancy).

> “Since this is just a demo, let’s go with **LRS** for now,” Ayesha said. “But when we go live, GRS or GZRS could be safer for compliance.”

Then they discussed **access tiers**:

* **Hot** for frequent access
* **Cool** for less-used files
* **Cold/Archive** for long-term storage

Understanding these options gave them a clearer picture of how Azure helps control **cost** and **availability** based on how data is used.

---

### 🏗️ Building Their First Azure Storage Account

With their plan set, the duo logged into the Azure portal. They chose the resource group `rg-eastus-skybridge`, named the storage account `mystorageaccayesha`, and selected the **Standard performance** tier with **LRS** redundancy.

Everything else was left at default—just enough for a clean, test-ready setup.

> “We don’t need bells and whistles today,” said Ayesha. “Let’s get the foundation right first.”

They clicked **Review + Create**, and in under a minute, their storage account was live.

---

### 📂 Making Room for Files – Blob Container & File Share

Omar was excited to explore both blob storage and file shares.

> “I’ve heard blobs are great for unstructured data. Can we try uploading a web file?” he asked.

So they created a **blob container** named `mycontainer25`, then uploaded a small HTML file called `sample.html` that simply said:

```html
<h1>This is a sample document!</h1>
```

Next, they moved to the **File Shares** section and created `myfile123` with the **Hot tier**, which is ideal for frequent file access. Omar uploaded a test report from his local drive.

> “This would be perfect for daily report logs or shared project files,” he said.

---

### 🔄 Why This Matters for Real Clients

As they worked through the lab, it became clear: these weren’t just tasks—they were real decisions cloud teams make every day.

> “If we pick the wrong redundancy or tier, the client either overpays or risks data loss,” Ayesha explained.
> Omar added, “And using blob vs. file share depends on *how* the data is used.”

The lab gave them a safe space to test these differences before facing real-world pressure.

---

### 🔐 Cleaning Up and Thinking Ahead

Once they had tested uploads, reviewed access settings, and walked through the client presentation demo, Ayesha reminded Omar to **delete all the resources**.

> “No budget surprises for test labs,” she said with a wink.

Before signing off, they documented their process in a shared OneNote:

* Which settings they chose and why
* When to use each redundancy type
* How blob and file share work differently

---

### 🚀 What This Lab Prepared Them For

This lab wasn’t about creating a simple storage account. It was about learning to make **smart choices** about cost, access, availability, and usability—skills that **real Azure admins** use every day.

From performance tiers to upload testing, Omar and Ayesha left the lab ready to advise their next client with confidence.

> “We’re not just storing files,” said Omar, “we’re building the right foundation for the data to grow safely.”

---

**💡 Lesson:**
**Cloud storage is more than space—it's about strategy.** This lab helped our team turn decisions into knowledge, and knowledge into value.

---
## ✅ Smart Guide: Lab 5 – Storage That Works for You  
**Point 1 of 9: Real-World Scenario – Making Smart Storage Decisions at SkyBridgeTech**

---

### 🎯 The Scenario  
Ayesha and Omar at **SkyBridgeTech** were tasked with setting up a reliable, cost-effective storage solution for a healthcare client. Their goal: show how Azure Storage can meet real-world needs for performance, redundancy, and access.

---

### 🧠 What They Did  
- Explored **performance tiers** (Standard vs. Premium)  
- Compared **redundancy options** (LRS, ZRS, GRS, GZRS)  
- Understood **blob access tiers** (Hot, Cool, Cold, Archive)  
- Created a **storage account** using Standard + LRS  
- Built a **blob container** and uploaded a sample HTML file  
- Created a **file share** and uploaded a test report  

---

### 💡 Why It Mattered  
- Helped them balance **cost vs. availability**  
- Taught when to use **blobs** vs. **file shares**  
- Practiced structuring data for real client scenarios

---

### 🚀 Takeaway  
Azure Storage isn't just about uploading files—it's about **making the right choices** for data usage, durability, and efficiency.

> **“We’re not just storing files—we’re building the right foundation.”** – Omar

---

📘 Lab 5: Create a Storage Account  
🧭 Scenario driven, client-ready, and AZ-104 aligned  
👩‍💻 Created by Ayesha & Omar with cloud curiosity and clarity
