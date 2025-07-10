# [4] Working with Alerts

This lab guide provides enterprise-ready, scenario-driven walkthroughs for mastering key Azure administrator tasks aligned with the AZ-104 certification.

**🌐 Scenario Title: “Keeping the Lights On: A Wake-Up Call for CloudOps Team at BrightOps Solutions”**

---
---

## 🌐 Simple Story: “The Wake-Up Call at BrightOps Solutions”

---

### 1️⃣ A Sudden Problem in the Morning

It was 9 a.m. on a rainy day in Atlanta. The CloudOps team at **BrightOps Solutions** was starting their morning meeting.

**Rohan**, a cloud engineer from Bangalore, joined from home. **Ayesha**, who works in infrastructure and lives in the U.S. now, was checking system dashboards with her coffee.

Suddenly, a message popped up from their manager, **Jordan**:

> “Hey team, one of our client demo systems restarted last night. Anyone know why?”

Everyone was surprised. This system was needed for an important meeting with a healthcare startup. If it wasn’t working, the client might not trust them.

---

### 2️⃣ Trying to Figure It Out

Rohan opened the Azure portal and checked the virtual machine (VM) that had restarted.

The VM looked fine now—but he couldn’t tell *why* or *when* it restarted.

“I wish we had alerts on this VM,” Ayesha said. “Then we would know exactly what happened.”

Rohan agreed. “We talked about doing this before… but we didn’t set it up.”

Jordan replied, “Let’s fix this today. We can’t risk this happening again.”

---

### 3️⃣ Why Alerts Are So Important

BrightOps runs many VMs across different regions. Some are for clients, some are for testing.

They have alerts on their main systems, but they forgot to add alerts to demo environments. That’s why no one noticed the restart.

Ayesha suggested a simple solution:

> “Let’s set an alert that tells us if someone restarts or changes the VM. We just need a message that says, ‘Something happened.’”

---

### 4️⃣ Rohan Builds the Alert

Rohan created a new test VM called **resizeVM**. He used Windows Server, kept it small to save money, and set it up just like the original.

Then, he went to the **Monitoring > Alerts** section in Azure and:

* Chose the VM as the target
* Picked **All Administrative operations** as the alert condition
* Made an **action group** to send email notifications
* Added both his and Ayesha’s email addresses

“Okay,” Ayesha said. “Restart it and let’s see if the alert works!”

---

### 5️⃣ The Alert Works!

Rohan clicked **Restart** on the VM.

One minute later, both he and Ayesha got an email:

> 📧 "ALERT: The resizeVM was restarted."

Rohan smiled. “Finally! Now we know when something happens.”

Jordan liked it too. “This is great,” he said. “Now I don’t have to guess or ask around when something changes.”

---

### 6️⃣ A Small Step, A Big Result

The next morning, in the team meeting, Jordan said:

> “Great job, Rohan and Ayesha. This alert setup is exactly what we need.”

Everyone agreed. It was a small lab task, but it taught a big lesson: **Always know when changes happen.**

Ayesha said it best:

> “Even one simple alert gives us more control and confidence.”

---

### 7️⃣ Sharing the Lesson with the Team

After this, BrightOps made a new rule: every demo VM must have alerts.

They also decided to train new engineers using this same lab.

> “Let’s make it part of onboarding,” Jordan said.

That 1-hour lab now became a tool for better teamwork and fewer surprises.

---

### 8️⃣ A Must for All IT Teams

In cloud systems, things change fast. Without alerts, you might not notice a mistake until it’s too late.

With alerts, teams like Rohan’s stay updated, ready, and calm—even when things go wrong.

This lab helped them get prepared, not just for today’s issue, but for all future ones too.

> 💡 **Simple Reminder:**
> One small alert can save hours of stress. That’s why alerts are a smart move for every IT team.

