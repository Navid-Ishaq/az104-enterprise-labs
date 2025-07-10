# [4] Working with Alerts

This lab guide provides enterprise-ready, scenario-driven walkthroughs for mastering key Azure administrator tasks aligned with the AZ-104 certification.

**🌐 Scenario Title: “Keeping the Lights On: A Wake-Up Call for CloudOps Team at BrightOps Solutions”**

---

### 1️⃣ A Morning Surprise at BrightOps HQ

It was just after 9 a.m. on a rainy Tuesday in Atlanta. At *BrightOps Solutions*, a fast-growing cloud consultancy that supports small businesses across the U.S., the CloudOps team was already deep in their daily standup.

Rohan, a cloud operations engineer originally from Bangalore, joined the meeting from his apartment. Across the city, Ayesha, an infrastructure analyst from Toronto now working remotely in the U.S., sipped her coffee and scanned the status dashboards on her second monitor. All systems looked calm — until a ping came through Slack.

> **"Hey team, one of our client demo environments restarted unexpectedly last night. Any idea what happened?"**
> — *Jordan, Project Manager*

The message stirred concern. That demo environment was built for an important meeting with a healthcare startup, and any unplanned downtime could hurt their chances of landing the contract.

---

### 2️⃣ The Root Cause Mystery

Rohan pulled up the Azure dashboard and navigated to the affected virtual machine — a Windows Server setup used for simulating client environments. But nothing obvious stood out. It was online now, but when had it restarted? Why?

“I wish we had alerting in place for this VM,” Ayesha said. “We’d have known exactly *when* and *why* this happened — and maybe even *who* triggered it.”

Rohan nodded. “Yeah, this is on us. We’ve talked about setting up alerts for admin actions but never actually implemented them for these test VMs.”

Jordan chimed in again.

> **"Let's fix this now before it becomes a pattern. We can't afford surprises in front of clients."**

---

### 3️⃣ Why Alerts Matter in the Real World

BrightOps prides itself on reliability and proactive operations. They manage dozens of virtual machines across multiple regions — some used for internal testing, others as staging environments for client presentations. While production systems had strict monitoring rules in place, demo and dev environments were often overlooked.

That oversight came with a cost: a restart no one had expected, and no way to prove whether it was caused by a scheduled maintenance event, user error, or something else.

Ayesha suggested a simple but impactful solution: set up an Azure alert on administrative actions, especially restarts. "We don’t need anything fancy," she said. "Just a basic notification that says, ‘Hey, something changed.’ That alone gives us a head start."

---

### 4️⃣ Getting Hands-On: Rohan Sets Up an Alert

Rohan spun up a new test VM called **resizeVM**, mimicking the same configuration as the affected one. He carefully followed the steps:

* Created a resource group and selected East US for the region.
* Set up the VM with Windows Server 2022 and standard security.
* Named it clearly and chose a small VM size to save costs.

Next, he jumped into the Monitoring section. This is where the real value kicks in. Under Alerts, he built a new rule:

* Targeted the VM (resizeVM) as the scope.
* Selected the signal: **All Administrative Operations** from the activity log — ensuring anything like restarts, stops, or size changes would trigger a flag.
* Set up an **action group** with an email notification to both his and Ayesha’s inboxes.

“Let’s test it now,” Ayesha said, smiling. “Go ahead, restart the VM.”

---

### 5️⃣ An Alert Arrives: Proof It Works

Rohan clicked “Restart” on the VM. The operation began.

Within a minute, both Rohan and Ayesha received email notifications:

> 📧 *“ALERT: An administrative action was performed on resizeVM – Action Type: Restart Virtual Machine.”*

Rohan grinned. “This is what we needed all along — visibility.”

Even Jordan, who wasn't deeply technical, appreciated the simplicity. “I didn’t need to chase anyone down or guess what happened. That email alert gives me peace of mind.”

---

### 6️⃣ Team Reflection: Small Change, Big Impact

Back in the next day’s standup, Jordan opened with a shout-out:

> “Rohan and Ayesha, awesome job on the alert setup. This is exactly the kind of proactive thinking that makes BrightOps a trusted name.”

The team agreed. What started as a small lab task — creating a VM and attaching a simple alert — turned into a powerful lesson in operational discipline.

Ayesha summarized it perfectly: “When you manage cloud environments, information is your first line of defense. Even if it’s just a restart, knowing *when* it happened gives us control.”

---

### 7️⃣ Taking the Lesson Company-Wide

After the success, BrightOps leadership decided to roll out a new internal policy: every demo or client-facing VM must have at least one alert tied to administrative operations.

They even planned a short training series, encouraging junior engineers and interns to complete the same lab Rohan did. “We’ll turn this lab into a company-standard onboarding task,” Jordan said.

That simple one-hour exercise now had long-term ripple effects — both in improving visibility and promoting a culture of accountability.

---

### 8️⃣ Why This Matters in Every IT Team

Behind every cloud dashboard are real people making fast decisions, and without clear alerts, things can slip through the cracks. Whether you’re a solo admin or part of a global team like BrightOps, a restart with no explanation can cause hours of confusion.

With the right alerting strategy, teams stay informed, focused, and ready — without surprises. For Ayesha, Rohan, and the rest of the BrightOps crew, this lab wasn’t just practice — it was preparation for the real-world chaos that IT teams face every day.

> 💡 **Lesson:** A 5-minute alert rule can prevent a 5-hour investigation. That's the power of small actions in cloud operations.
