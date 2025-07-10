# [4] Working with Alerts

This lab guide provides enterprise-ready, scenario-driven walkthroughs for mastering key Azure administrator tasks aligned with the AZ-104 certification.


---

## ✅ Smart Summary: Azure Lab 4 – **Working with Alerts**

**⏱ Duration:** 1 Hour
**🎯 Goal:** Create a Virtual Machine and set up an Alert that notifies you when someone restarts it.

---

### 🧠 What’s the Lab About?

You’ll create a virtual machine (VM) and set a rule to get an email when someone performs an admin action (like a restart). It’s about **awareness and control** in the cloud.

---

### 💼 Why It Matters in Real Life

In real IT work, things change fast. If a server restarts and no one knows — it can hurt business. This lab shows how to **catch problems early** using simple alerting tools.

> 🗣️ *“If something changes, I want to hear about it — not guess.”* — Ayesha, Infra Analyst at BrightOps

---

### 🔧 Azure Tools Used (With Simple Meanings)

| **Tool**             | **What It Is**                                                 | **Real-Life Example**                       |
| -------------------- | -------------------------------------------------------------- | ------------------------------------------- |
| **Virtual Machine**  | A cloud-based computer you can use for testing or apps.        | Like renting a PC that you can turn on/off. |
| **Azure Alert Rule** | A watcher that looks for specific activities (e.g., restarts). | Like a motion sensor in your house.         |
| **Action Group**     | Who gets notified and how (email, SMS, etc).                   | Like adding your family to a group chat.    |

---

### 🔁 How They Work Together

1. **VM** = The machine you're watching.
2. **Alert Rule** = The eyes that watch for changes (like a restart).
3. **Action Group** = The messenger that sends you the alert.

> 🔔 Example: VM restarts → Alert gets triggered → You get an email.

---

### 🛠️ Key Steps (In Brief)

1. **Create a VM**
2. **Go to Monitoring > Alerts**
3. **Create Alert Rule** → Choose “All Administrative Operations”
4. **Create Action Group** → Add your email
5. **Restart VM to test it**
6. **Check your inbox** ✉️

---

### 📚 What You Learn

* How to **set up a simple alert**
* Why alerts help you **catch problems faster**
* That **automation = peace of mind** in cloud work

---

### ✅ Final Takeaway

> 🧠 “Even one alert can save hours of guessing. It’s your cloud’s way of telling you: *Hey, something just happened!*”
> — *Rohan, CloudOps at BrightOps*

---

