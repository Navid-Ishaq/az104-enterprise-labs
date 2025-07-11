# [4] Working with Alerts

This lab guide provides enterprise-ready, scenario-driven walkthroughs for mastering key Azure administrator tasks aligned with the AZ-104 certification.

---
### 🔹 Point 9 of 9: Comic-Style Recap — “The Cloud That Cried ‘Restart!’”

---

#### 🧨 Uh-oh, a Problem!

At **BrightOps Solutions**, things were going smoothly… until one day, a mysterious restart brought down a test server right before a client demo. *“Did you restart it?”* asked Ayesha. *“Nope!”* said Rohan. *“Then who did?!”* 😱 They realized something crucial was missing: their **cloud had no way to alert them** when stuff like this happened.

---

#### 💻 Time to Get to Work!

Armed with snacks, coffee, and ambition, our dynamic duo logged into Azure. First mission? **Create a Virtual Machine** called `vm-brightops-demo01`. Rohan named the resource group `rg-brightops-ayesha`, selected the **Windows Server 2022** image, chose **Standard SSD**, and skipped public ports because “we like things private,” he grinned. Boom 💥—VM deployed!

---

#### 🛠️ Tools in Action!

Now for the magic part. In the **Alerts** section, they built a rule to watch for sneaky restarts. Under **Signals**, they chose **All Administrative operations** (translation: “track anything an admin might do!”). Then, Ayesha set up an **Action Group** named `alertactiongrp` and added her email. *“Now if anything funny happens, I’ll hear it first,”* she smirked.

---

#### 🔁 Trigger Time!

Rohan clicked **Restart** on the VM and leaned back. *“Let’s see if our setup works…”* A few suspenseful moments later—DING! 💌 An email popped into Ayesha’s inbox: *“Administrative action detected on vm-brightops-demo01!”* They high-fived. *“Our cloud just told us something happened. It’s officially got a voice!”*

---

#### 🎉 Success and High-Fives!

With their alert working and their coffee cups empty, the team deleted all their test resources. *“No leftovers in the cloud fridge,”* Ayesha joked. They both agreed—this lab taught them more than just clicking buttons. It showed how a **simple alert can save hours of confusion**, and how every smart admin needs to let the cloud *speak up when it matters most*.

---

**💡 Moral of the Comic:**
**Let your cloud tell you when something’s wrong. Alerts = Awareness = Awesome!** 🚀

```

## ✅ Smart Guide: “The Cloud That Cried ‘Restart!’”

**Point 9 of 9: Fun Recap – Azure Alert Lab in Comic Form**

---

### 🧩 The Setup

Rohan and Ayesha at BrightOps had a mystery restart — no alerts, no clues. So they took on Lab 4 to fix that.

---

### 💻 What They Did

* Created a VM named `vm-brightops-demo01`
* Chose **Windows Server 2022**, **Standard SSD**, and no public ports
* Created an **alert rule** to monitor **All Administrative operations**
* Set up an **action group** with Ayesha’s email to receive alerts

---

### 🔁 The Test

* Restarted the VM
* ✅ Got an email alert within minutes
* 🎉 Success! Their system was finally talking back

---

### 🎯 Key Takeaway

Even one simple alert can prevent major confusion. It turns your cloud into an assistant that **notifies you before things go wrong**.

> **Alerts = Awareness = Awesome!**

---

