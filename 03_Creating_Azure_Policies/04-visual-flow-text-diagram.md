# [3] Creating Azure Policies

This lab guide provides enterprise-ready, scenario-driven walkthroughs for mastering key Azure administrator tasks aligned with the AZ-104 certification.

**🗺️ Title: “Visualizing Cloud Control – A Beginner’s Guide to Azure Policy with Ayesha & Rohan”**

---

## 🔳 **Text-Based Diagram: Step-by-Step View of Azure Policy Lab**

```
+-----------------------------+
|   Login to Azure Portal    |
+-------------+---------------+
              |
              v
+-----------------------------+
| 1. Open "Policy" Service    |
+-------------+---------------+
              |
              v
+-----------------------------------------+
| 2. Set Scope (choose a resource group)  |
+----------------+------------------------+
                   |
                   v
+-----------------------------------------+
| 3. Find "Allowed locations" policy      |
|    (under Definitions)                  |
+----------------+------------------------+
                   |
                   v
+-----------------------------------------+
| 4. Assign Policy                        |
| - Name: Allow UK South...              |
| - Description: Only allow UK South     |
| - Enforce: Enabled                     |
| - Set Region: UK South                 |
+----------------+------------------------+
                   |
                   v
+-------------------------------+
| 5. Review + Create Policy     |
+-------------------------------+
                   |
                   v
+-----------------------------+
| 6. Open Virtual Networks    |
+-----------------------------+
              |
              v
+--------------------------------------------+
| 7. Try to create VNet in East US           |
| → Validation Fails (blocked by policy)     |
+--------------------------------------------+
              |
              v
+--------------------------------------------+
| 8. Change region to UK South               |
| → Validation Passes, VNet is created       |
+--------------------------------------------+
              |
              v
+-----------------------------+
| 9. Delete all resources     |
+-----------------------------+
```

---

## 1️⃣ **Setting the Scene: Meet the Team and the Mission**

At **BrightOps Solutions**, junior cloud admin **Ayesha** and her mentor **Rohan** are working on a governance project. Their mission is simple but important: make sure their team can only create Azure resources in approved locations—in this case, the **UK South** region. This prevents accidental deployments in far-off data centers, which can lead to compliance or performance issues.

“This is a perfect beginner lab,” Rohan told Ayesha, “It’s like putting up a smart roadblock in Azure that says ‘Only UK South, please!’ Let’s walk through it one step at a time.” Ayesha, feeling both curious and a little nervous, opened her laptop and got started.

---

## 2️⃣ **Getting Started: Opening the Right Door**

Ayesha began by logging into the **Azure Portal**. “First thing,” she said to herself, “search for the **Policy** service.” This is the tool that helps set the rules for what’s allowed or not in Azure.

Opening the Policy service is like stepping into a control room. It doesn’t do anything flashy on its own, but it gives you access to set up **guardrails**—those behind-the-scenes rules that keep everything organized and safe.

---

## 3️⃣ **Choosing the Scope: Deciding Where the Rule Applies**

Next up was the **Scope selector**. This little feature is where Ayesha chose **which part of her cloud environment** the rule would apply to. She selected a test resource group called `rg-labresources`.

Rohan explained it simply: “Think of scope like putting up a fence. You decide if the fence goes around a house, a neighborhood, or the entire city. Here, we’re just fencing off one small area so we can test safely.”

---

## 4️⃣ **Finding and Assigning the Right Policy**

Inside the Policy section, Ayesha went to **Definitions** and searched for “Allowed locations.” Azure has a pre-built policy ready to go. It’s like choosing a rule template from a shelf—no need to build it from scratch.

She clicked **Assign Policy**, gave it a name, added a quick description, and set it to **UK South**. Most importantly, she made sure **Policy enforcement** was turned on. “If that switch is off, the policy is just a suggestion,” Rohan reminded her. “We want it to actually block anything outside of UK South.”

---

## 5️⃣ **Time to Test: Breaking the Rule (On Purpose)**

Now it was time for the fun part—**testing the rule**. Ayesha opened the **Virtual Networks** service and tried to create a new network in **East US**, a region that wasn’t allowed. Just like they hoped, the validation failed. “This is great! It stopped me!” she laughed.

She clicked the error message and confirmed it was the policy doing its job. This step helped her see the **real-world value** of the rule. It wasn’t just an invisible setting—it was protecting their work from costly mistakes.

---

## 6️⃣ **Fixing the Test: Choosing the Right Region**

To complete the lab, Ayesha went back and changed the region to **UK South**. This time, validation passed, and she was able to deploy the virtual network successfully.

This simple moment made a big impact. “It’s kind of like getting the green light at a traffic stop,” she said. “If I follow the rule, everything moves smoothly. If I don’t, the system says ‘Hold on!’”

---

## 7️⃣ **Cleaning Up and Wrapping Up**

After confirming everything worked, Ayesha cleaned up the test resources. This is always a good habit when using cloud labs—it avoids unnecessary costs and keeps things tidy.

She took a moment to reflect. “That was actually easier than I thought,” she told Rohan. “And now I understand why policies matter. They’re like smart helpers keeping everyone on track.”

---

## 8️⃣ **The Bigger Lesson: Small Rule, Big Impact**

Through this simple lab, Ayesha learned that **Azure Policy** isn’t about limiting freedom—it’s about **giving structure**. It ensures that teams don’t make mistakes or break company rules accidentally.

With just a few clicks, she had created a rule that stopped improper deployments and reinforced best practices. For Ayesha and BrightOps, this was a small but powerful first step in building a smarter, safer cloud environment.

---

**✅ Final Thought:** Azure Policy may look like just another tool, but when used wisely, it becomes your **cloud’s silent guardian**—always watching, always protecting.
