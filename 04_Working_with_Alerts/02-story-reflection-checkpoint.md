# [4] Working with Alerts

This lab guide provides enterprise-ready, scenario-driven walkthroughs for mastering key Azure administrator tasks aligned with the AZ-104 certification.

**🔔 Lab Title: “Stay Informed, Stay in Control: Creating Alerts in Azure”**

---

### 1️⃣ What This Lab Is All About

This lab, titled **“Working with Alerts”**, teaches learners how to create a **Virtual Machine (VM)** in Microsoft Azure and set up **alerts** that notify users when specific actions—like restarting or modifying the VM—take place. It's a hands-on way to understand how cloud environments can be monitored effectively.

At **BrightOps Solutions**, a fictional cloud consultancy, team members Rohan and Ayesha are always looking for ways to make sure their systems don’t change without them knowing. In this lab, they explore how Azure helps track these changes and keeps the right people informed—before issues turn into problems.

---

### 2️⃣ Why This Lab Matters in the Real World

Imagine you’re in charge of important servers that run your company’s website or client demos. What happens if someone restarts a server by mistake? Or if a system update causes downtime right before a big presentation? Without alerts, you might not even know until someone complains.

Rohan once faced this issue when a demo environment restarted unexpectedly. That’s why learning to set up **alert rules**—notifications that tell you when something changes—is a must. These alerts give IT teams peace of mind and allow them to respond quickly to potential issues. In real life, alerts are like motion sensors in your home security system—they don’t stop problems, but they make sure you know *immediately* when something unusual happens.

---

### 3️⃣ Azure Virtual Machines: Your Digital Workhorse

The first part of the lab involves creating a **Virtual Machine (VM)**—which is like having a computer that lives in the cloud. You can install software, run programs, or simulate real-world servers without needing physical hardware.

In the lab, Rohan sets up a VM called **resizeVM**, choosing the operating system (Windows Server 2022), its location (East US), and its basic configuration. This VM becomes the “target” that he wants to monitor. Think of it as a hotel room he manages—he wants to be notified if someone opens the door, turns off the lights, or changes the settings inside.

---

### 4️⃣ Alerts: Your Cloud’s Watchdog

Once the VM is set up, the next step is creating an **alert rule**. This tells Azure, “Please let me know when someone does something specific to this VM.”

Rohan selects a signal called **All Administrative operations**, which means Azure will keep an eye out for any changes made by users—like restarting, stopping, or resizing the machine. This kind of alert is perfect for teams who want to be aware of important actions without constantly checking manually.

It’s like asking your phone to send you a message whenever someone logs into your smart home camera feed—you want to know who’s doing what and when, so you can stay in control.

---

### 5️⃣ Action Groups: The Messenger System

But alerts don’t work alone—they need a way to *tell you* when something happens. That’s where **action groups** come in. Rohan creates an action group and tells Azure, “When this alert is triggered, send me an email.”

Action groups are like the delivery people for Azure alerts. You tell them where to go (email, text, app notification) and they deliver the message when it’s time. Rohan names his group **alertactiongrp** and links it to his email so he knows the moment anything changes in the VM.

Ayesha compares it to emergency contact lists: “If something happens at school, they don’t just fix it quietly—they call your parents. That’s what action groups do in the cloud world.”

---

### 6️⃣ Azure Activity Logs: The Cloud’s Memory Book

Behind the scenes, Azure keeps a **log of every action** performed—who did what and when. These are called **Activity Logs**, and the alert condition Rohan picked is based on this log. The lab helps learners realize that Azure doesn’t just *run* things—it also *remembers* everything that happened.

It’s like keeping a journal of every visitor to your office building. You might not read it every day, but when something goes wrong, it’s your first place to look for answers.

Using “All Administrative operations” as the condition means Rohan will be notified whenever the log records a significant event—like a restart or settings change.

---

### 7️⃣ Testing the Alert: Practice Before Production

To make sure the alert system works, Rohan performs a **restart** on the VM. Within minutes, he gets an email from Azure saying the machine was restarted. Success!

This part of the lab teaches something very practical: it’s not enough to *set up* alerts—you also need to **test them**. Just like you would test a smoke alarm at home, you need to make sure your alert system actually works before relying on it in a real situation.

Seeing the email arrive builds confidence and helps Rohan and Ayesha trust the system they’ve created.

---

### 8️⃣ How It All Comes Together

By the end of the lab, several Azure tools work together smoothly:

* **Azure Virtual Machines** provide the system being monitored.
* **Azure Monitoring (Alerts)** watches for specific actions.
* **Activity Logs** track all those actions in the background.
* **Action Groups** make sure someone gets the message when something important happens.

These tools are like teammates in a relay race—each passing the baton to the next, making sure the message gets to the finish line (your inbox) in time.

Rohan closes the lab session feeling empowered.

> “I get it now,” he tells Ayesha. “It’s not just about building things in the cloud—it’s about staying informed when they change.”

This lab doesn’t just teach how to click buttons. It teaches **how to stay in control** in a dynamic cloud environment—and that’s something every IT team needs.

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
