# [4] Working with Alerts

This lab guide provides enterprise-ready, scenario-driven walkthroughs for mastering key Azure administrator tasks aligned with the AZ-104 certification.

**🔁 Reflection Title: "From Guesswork to Confidence: Rohan’s First Step into Alerting in Azure"**

---
---

## 🔔 **Simple Guide: What This Azure Lab Is About**

---

### 🧭 1. What You’ll Learn in This Lab

This lab teaches you how to:

* Create a **virtual computer** (called a virtual machine or VM) in Microsoft Azure
* Set up **alerts** so you get notified when something important happens to your VM

You’ll also learn how to test the alert and check if it works. This helps you keep track of changes in your cloud environment.

---

### 🌍 2. Why This Is Useful in Real Life

In real jobs, cloud teams like the one at **BrightOps Solutions** use Azure to manage servers, test environments, and customer demos. If something changes—like if someone restarts a server—**you want to know right away**.

Without alerts, you might not know until something goes wrong. With alerts, you’ll get an email or message that tells you what happened so you can act quickly.

---

### 💻 3. Virtual Machine (VM) – Your Cloud Computer

A **Virtual Machine** is just like a regular computer, but it lives in the cloud. You can turn it on, install programs, and use it for testing or work.

In this lab:

* You create a VM named **resizeVM**
* It uses **Windows Server** as the operating system
* It’s stored in the **East US** region

This VM is the thing you’ll be monitoring with alerts.

---

### 👀 4. Alerts – Your Cloud Watchdog

**Alerts** help you watch your VM without staring at the screen all day.

You can tell Azure:

> “If someone restarts or changes this VM, please let me know.”

That’s what this lab shows you—how to create a simple alert that tells you when an important action happens.

---

### 📩 5. Action Group – The Message Sender

After setting the alert, you need to decide **how you want to be notified**. That’s what the **Action Group** is for.

An **Action Group** is like a contact list. It knows:

* Who to send the alert to
* What method to use (email, text, app)

In this lab, you:

* Create an action group called **alertactiongrp**
* Tell it to send an **email** to your inbox when something happens

---

### 📝 6. Activity Log – Azure’s Memory Book

Azure keeps track of every change in the background. This is called the **Activity Log**.

When you create the alert, you tell Azure to watch for “All Administrative operations” in the activity log. That means:

* If someone restarts the VM
* Or changes its size
* Or stops it

Azure will notice, and the alert will go off.

---

### ✅ 7. Testing the Alert – Did It Work?

To check if your alert works, you:

1. Go to your VM
2. Click **Restart**
3. Wait a few minutes
4. Check your **email inbox**

You should get a message saying the VM was restarted. That means your alert worked!

---

### 🔄 8. How All the Tools Work Together

Let’s review what you used:

| Tool                | What it does           | Real-world example              |
| ------------------- | ---------------------- | ------------------------------- |
| **Virtual Machine** | A cloud computer       | Like a rented laptop online     |
| **Alert Rule**      | Watches for changes    | Like a home security camera     |
| **Action Group**    | Sends you the message  | Like a phone call from a friend |
| **Activity Log**    | Keeps record of events | Like a diary of who did what    |

All these tools work together to **help you stay informed** and in control of your cloud systems.

---

### 🎉 Final Thought

Rohan, from BrightOps Solutions, did this lab to make sure he wouldn’t miss important changes on his demo systems. By setting up a simple alert, he can now relax, knowing Azure will send him a message when anything changes.

> **This lab teaches a small but powerful lesson:**
> You don’t need to watch your systems 24/7—just let Azure alert you when it matters.

Now *you* know how to do that, too!
