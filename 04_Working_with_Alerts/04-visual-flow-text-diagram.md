# [4] Working with Alerts

This lab guide provides enterprise-ready, scenario-driven walkthroughs for mastering key Azure administrator tasks aligned with the AZ-104 certification.

---
**📊 Title: “Step-by-Step with Azure Alerts: A Simple Visual Guide with Storytelling Support”**
*Helping your virtual machine speak up when something happens*

---

## 🧭 TEXT-BASED FLOW DIAGRAM

```
Start
  |
  |--> [Step 1: Create a Virtual Machine]
  |        |
  |        |--> Choose region, image, size, and OS disk
  |        |--> Set username and password
  |        |--> Deploy the VM (resizeVM)
  |
  |--> [Step 2: Create an Alert Rule]
  |        |
  |        |--> Go to Monitoring > Alerts
  |        |--> + Create Alert Rule
  |        |--> Select scope: resizeVM
  |        |--> Choose signal: All Administrative Operations
  |        |
  |        |--> [Create Action Group]
  |        |        |
  |        |        |--> Set name: alertactiongrp
  |        |        |--> Notification: Email to your address
  |
  |--> [Step 3: Trigger the Alert]
  |        |
  |        |--> Restart the VM
  |        |--> Wait a few minutes
  |        |--> Check your email for alert message
  |
  |--> [Final Step: Clean up resources]
  |
  End
```

---

## 1️⃣ Starting Fresh with a Purpose

At **BrightOps Solutions**, a growing cloud services company, two team members — **Rohan**, a cloud engineer from Bangalore, and **Ayesha**, a systems analyst from Toronto — sat down to complete an important Azure lab. They wanted their cloud environments to notify them when something changes, like someone restarting a virtual machine.

“We had that one restart last week nobody knew about,” Ayesha said. “Let’s make sure that doesn’t happen again.” Their goal? Follow this lab to teach their cloud to *speak up* when something happens.

---

## 2️⃣ Building the Machine (Step 1)

First, Rohan opened the Azure portal and went to **Virtual Machines**. He clicked “+ Create” and started setting up a new VM. He named it **resizeVM**, selected **East US** as the region, and chose a small but efficient size — **B2s** — to keep things light.

He carefully added login details, selected the operating system (**Windows Server 2022**), and chose a **Standard SSD** for the disk. “It’s like building a new computer, but in the cloud,” Rohan explained. A few clicks later, the VM was ready.

---

## 3️⃣ Setting Up the Alert (Step 2 – Part 1)

Now came the part they were most interested in — **alerts**. Ayesha navigated to the **Monitoring** section in the Azure portal. Inside the VM’s settings, they clicked on **Alerts** and then “+ Create > Alert rule.”

They picked their VM (**resizeVM**) as the *scope* — basically telling Azure, “Watch this machine.” Then, they searched for the signal **All Administrative Operations**. That means Azure will watch for any major changes, like restarts or configuration edits.

“It’s like asking Azure to raise its hand if someone touches the machine,” Ayesha said with a smile.

---

## 4️⃣ Creating the Messenger: Action Group (Step 2 – Part 2)

Once the alert was set up, they had to tell Azure *who* to notify. This is where the **Action Group** comes in. Rohan clicked “+ Create action group,” filled in the name `alertactiongrp`, and added his email under notifications.

He selected **Email**, gave it the label **Email action**, and confirmed the address. “Now Azure knows where to send the message if anything happens,” he said. This step makes sure alerts don’t just sit there — they get delivered.

---

## 5️⃣ Testing It Out (Step 3)

With everything ready, Rohan restarted the virtual machine. “This should trigger the alert,” he said as he clicked **Restart** on **resizeVM**. They waited a couple of minutes, fingers crossed.

**Ping!** An email arrived:

> *“ALERT: An administrative operation has been performed on resizeVM.”*

“Boom!” Ayesha laughed. “That’s the sound of our cloud talking back!”

---

## 6️⃣ Wrapping Up: Clean, Smart, and Confident

After verifying the alert worked, Rohan went back to Azure and deleted the VM and other resources to avoid charges. “Always clean up your lab,” he reminded himself.

They felt more confident now. “This was more than just a lab,” Ayesha said. “It showed us how to build a system that *talks to us*, so we’re never in the dark again.”

---

## 7️⃣ Real-World Reflection: Why This Lab Really Matters

For teams like BrightOps — or anyone managing cloud systems — visibility is everything. Without alerts, small changes go unnoticed. This lab taught Rohan and Ayesha how to make their system more **transparent** and **responsive**.

“It’s like installing a doorbell camera on your virtual house,” Rohan said. “Now we know exactly when someone comes and goes.”

---

## 8️⃣ Final Thought: Simple Steps, Powerful Impact

This lab didn’t use advanced tools or fancy setups. It used basic, beginner-friendly features — a VM, an alert rule, and an email — to build something incredibly useful.

If you're new to Azure, this lab is a perfect way to learn not just *how* to set things up, but *why* they matter. Just like Rohan and Ayesha, you’ll walk away knowing how to build a cloud that listens, responds, and keeps you informed — every step of the way.

> ✅ **Lesson:** One alert rule can save you hours of guessing. Listen to your cloud.

---

