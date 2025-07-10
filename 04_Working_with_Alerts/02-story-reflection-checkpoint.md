# [4] Working with Alerts

This lab guide provides enterprise-ready, scenario-driven walkthroughs for mastering key Azure administrator tasks aligned with the AZ-104 certification.

**🔁 Reflection Title: "From Guesswork to Confidence: Rohan’s First Step into Alerting in Azure"**

---

### 1️⃣ Setting the Stage: A Simple Lab with Big Expectations

When Rohan first read through the instructions for Lab 4 — *Working with Alerts* — he thought, *“This should be pretty straightforward. Just a few clicks, right?”* But beneath his calm surface, there was a hint of doubt. It wasn’t about creating a virtual machine — he’d done that before. What made him hesitate was the part about setting up alerts. He’d seen alerts in action before, but never set one up himself from scratch.

He wasn’t alone. Ayesha, his colleague at **BrightOps Solutions**, had done the lab a while ago but remembered feeling the same way.

> “Don’t worry,” she told him with a laugh, “The first time I did it, I wasn’t even sure what ‘action group’ meant. But once it clicks, it’s easy.”
> Her encouragement helped. Rohan decided to treat the lab like a mini-mission — not just to follow the steps, but to really *understand* what each part was doing.

---

### 2️⃣ Getting Started: Familiar Ground

The first step — creating a virtual machine — felt familiar. Rohan had no trouble selecting the image, entering the username and password, and choosing the size. He gave the VM the name **resizeVM**, as the lab instructed, and double-checked everything on the “Review + create” screen.

“Alright,” he muttered to himself, “One down, two to go.”

He smiled as the VM started deploying. For now, it was just a temporary resource for a learning task, but in the real world, this was the same process he’d use to spin up test environments or simulate client setups.

---

### 3️⃣ Diving into Alerts: Not as Scary as Expected

The next step was where things got interesting. Under the Monitoring section of the newly created VM, Rohan clicked into “Alerts” and then began building the alert rule.

At first, he paused.

> “What does 'Scope' actually *do* here?” he wondered.
> Reading the description helped — it told Azure where to look. He selected the resizeVM, then moved on to setting the condition: **All Administrative operations**.

“Okay,” he said to himself, “this means *any* change to the VM, like restarting it, will be tracked. That makes sense.”

Once he moved into creating the action group and entering his email for notifications, everything started to feel more real. “So this is how Azure lets us *know* when something happens, without having to babysit every VM.”

---

### 4️⃣ Small Challenge, Big Clarity

There was a moment of hesitation when Rohan had to create the **action group**. He accidentally left out a required field the first time and got an error. “Oops,” he chuckled, fixing the display name and re-reviewing his settings.

Ayesha, who was on a quick break, peeked at his screen over Teams and said,

> “Looks like you're 95% there. Just hit ‘Create’ and you’re golden.”

Rohan appreciated how this step-by-step lab forced him to slow down and think about each decision. He wasn’t just copying instructions — he was *learning how these tools worked together*.

---

### 5️⃣ Moment of Truth: Did It Actually Work?

Now came the test: Rohan restarted the virtual machine.

“Alright,” he said with a small breath of anticipation, “let’s see if that email comes through.”

A few minutes later — *ping!* — his inbox lit up.

> **Subject:** Alert - Administrative Action on resizeVM
> **Message:** "A virtual machine administrative operation (Restart) was performed on your resource."

Rohan grinned. “Yes! It worked!”

He called Ayesha over and shared the screen. “Feels great to know I actually got it working on the first try.”

---

### 6️⃣ A Lesson in Visibility and Trust

What surprised Rohan most wasn’t the technical part — it was the realization of *why* alerts matter so much. Before, he thought of them as just extra settings. Now, he saw them as an essential part of good cloud hygiene.

> “Without that alert,” he told Ayesha, “we’d have no idea who touched what or when. In production, this could mean the difference between a 5-minute fix and a 5-hour panic.”

This wasn’t just about passing a lab. It was about practicing how to stay informed, responsible, and proactive — values that mattered deeply to everyone at BrightOps.

---

### 7️⃣ A Boost in Confidence (and Curiosity)

After finishing the lab and deleting the resources, Rohan felt a quiet sense of pride. He knew more than he did an hour ago — and not just in theory. He’d *done* it. From provisioning a VM to setting up the alert and verifying the email, the entire flow made sense now.

> “I used to skip over alerts in my mind,” he admitted to Ayesha. “Now I’m wondering what else we can automate this way.”

She smiled. “That’s how it starts. Welcome to the monitoring mindset.”

---

### 8️⃣ Looking Ahead: More Than Just a Lab

For Rohan, Lab 4 was more than just a technical task — it was a shift in mindset. He walked away not only with a completed lab, but with a deeper appreciation for how cloud systems should be managed.

He planned to review the different alert conditions and explore how they could use action groups to notify Slack channels next. It wasn’t about checking a box anymore — it was about building systems that told the truth when things changed.

> **“The lab was just one hour,”** Rohan reflected, **“but it showed me how to be more alert — in more ways than one.”**

---
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
