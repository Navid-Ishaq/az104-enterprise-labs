**Title:**
**Today Lab: Create a Storage Account**

---

## **Point 1 of 9: Building a Resilient Cloud Storage Foundation**

### 🌍 Real-World Scenario Title:

**"SkyBridgeTech's Data Storage Dilemma: How a Simple Azure Storage Setup Helped a Fast-Growing Startup Scale Smartly"**

---

### 1️⃣ **Meet the Team: Diverse People, One Cloud Challenge**

At **SkyBridgeTech**, a mid-sized cloud consulting startup based in Austin, business was booming. They had just signed a new client — a global eco-travel platform — and needed to ramp up their Azure infrastructure fast.

**Ayesha**, the infrastructure analyst from Dubai, had just joined the team and was excited to get hands-on experience with Azure. Her colleague **Jordan**, a seasoned DevOps engineer from Toronto, had been with SkyBridgeTech for years and often mentored new hires. Together, they were assigned to set up a reliable cloud storage solution that could handle documents, media files, and backend logs — all with different usage patterns.

> “We need storage that’s cost-efficient, fast, and won’t break if something goes down in one zone,” said Jordan during their morning stand-up.

---

### 2️⃣ **Why They Needed Cloud Storage (And Fast)**

The new eco-travel client wanted **three key things**:

1. Reliable document access for their worldwide team
2. Scalable storage for customer media uploads
3. Redundancy for high availability in case of regional failures

This wasn’t just about throwing files into the cloud — SkyBridgeTech had to make sure **performance**, **redundancy**, and **access levels** were properly balanced for cost and speed.

> “If we put everything on the fastest tier, we’ll blow the budget,” Ayesha noted.
> “But if we pick the wrong one, we’ll have delays. We need to be smart about this.”

---

### 3️⃣ **Learning Before Doing: Understanding the Options**

Before diving into the Azure Portal, Ayesha and Jordan took a few minutes to break down their options.

Jordan explained:

> “Azure has *Standard* and *Premium* storage. For general files, *Standard* is good enough — unless you're working with ultra-fast databases.”

They also discussed **redundancy**:

* **LRS (Locally-Redundant)** was cheaper but riskier if the datacenter went down.
* **ZRS (Zone-Redundant)** was more resilient.
* **GRS (Geo-Redundant)** added global protection.
* **GZRS** combined the best of both.

> “Let’s start with LRS for the trial run — but we’ll document when to upgrade,” said Jordan.

---

### 4️⃣ **Action Time: Creating Their First Azure Storage Account**

Inside the Azure portal, they followed a clear checklist.
They selected:

* **Region**: East US (as their client’s backend was based there)
* **Performance**: Standard
* **Redundancy**: LRS

> “Naming it mystorageaccayesha for now — we’ll delete it after the trial,” said Ayesha as she filled in the details.

They clicked through the **Review + Create** tab and launched their first Azure storage account. Just like that, they had the foundation in place.

---

### 5️⃣ **Organizing Data: Blobs, Containers, and Structure**

Next up, they needed to organize the data.
Jordan explained:

> “Think of containers like folders, and blobs like files inside those folders. Containers keep things clean.”

Ayesha created a container named `mycontainer25` and uploaded a basic HTML file to test the structure.

> “Uploaded!” she smiled.
> “It’s like setting up a smart digital filing cabinet.”

They discussed how this structure would work for the eco-travel client's photo uploads and promotional files.

---

### 6️⃣ **Adding Flexibility: File Shares for Team Collaboration**

The eco-travel client also had remote content teams who needed access to shared files. This is where **File Shares** came in.

They created a file share named `myfile123` and chose the **Hot** access tier — ideal for frequently used team files.

> “This gives us an easy way to share docs, scripts, even spreadsheets — all through Azure,” Jordan explained.

They uploaded a few mock documents and confirmed access from different devices. It worked perfectly.

---

### 7️⃣ **Reflection: Why This Matters for Growing Teams**

By the end of the session, Ayesha and Jordan had not only created a working storage system — they had also **learned how to think strategically** about storage choices.

> “It’s not just about uploading files,” Ayesha reflected.
> “It’s about aligning storage types with how the business uses data.”

They noted which workloads would benefit from **Hot**, **Cool**, or even **Archive** tiers later — and which situations would require **ZRS** or **GRS** for redundancy.

---

### 8️⃣ **Cleanup and Confidence**

Before logging off, they deleted all their resources — a good practice for avoiding unexpected costs. But the knowledge remained.

SkyBridgeTech’s small experiment had prepared them to build **scalable, resilient, and efficient** cloud storage for real clients — starting with their eco-travel partner.

> “Next time, we try ZRS and play with blob lifecycle management,” said Jordan, already planning their next lab.

> “Bring it on,” Ayesha grinned.
> “Azure’s not so scary after all.”

---

🧠 **Key Takeaway:**
This lab isn’t just about clicking buttons. It’s about understanding how **different kinds of data** need different kinds of **cloud storage** — and how choosing the right setup can help businesses work smarter, save money, and stay resilient.

---
