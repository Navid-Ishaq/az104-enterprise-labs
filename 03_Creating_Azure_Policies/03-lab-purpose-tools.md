# [3] Creating Azure Policies

This lab guide provides enterprise-ready, scenario-driven walkthroughs for mastering key Azure administrator tasks aligned with the AZ-104 certification.

**🔐 Title: “Setting Cloud Guardrails – Understanding and Using Azure Policy”**

---

### 1️⃣ What This Lab Is About: Enforcing the Rules of the Cloud

At **BrightOps Solutions**, junior cloud administrator **Ayesha** and her mentor **Rohan** are working on a real-world problem—making sure that their company’s cloud resources are only created in approved regions. This lab helps them achieve exactly that, using something called **Azure Policy**.

In this lab, you’ll learn how to create and assign a **policy** in Azure that restricts where resources can be deployed. Think of it like putting up invisible “boundaries” so that cloud resources (like virtual machines or networks) can only be built in specific areas—kind of like saying, “Only build our servers in London, not New York or Tokyo.”

---

### 2️⃣ Why This Matters: Real-World Cloud Compliance and Cost Control

Imagine you're working for a company that handles sensitive customer data in the UK. You wouldn’t want that data stored in a data center in another country where different privacy laws apply. That’s why **restricting locations** is important—it helps protect data and follow local laws.

Also, deploying cloud resources in distant regions can drive up costs and slow down performance. With a simple Azure Policy, businesses like BrightOps can make sure their teams stay on track without needing to check every deployment manually. It’s like setting a company rule once and letting the system enforce it automatically.

---

### 3️⃣ Azure Policy: The Main Tool – Your Cloud’s Rulebook

**Azure Policy** is the star of this lab. Think of it as the **rulebook** for your cloud environment. Just like a building inspector makes sure homes follow safety codes, Azure Policy checks your cloud setup to make sure it follows the rules you’ve set—like which locations are allowed or what types of services can be used.

In this lab, Ayesha uses Azure Policy to **create a rule that only allows new resources to be built in the “UK South” region**. If someone tries to deploy something outside that area—like “East US”—the policy steps in and stops it. This helps keep things secure, organized, and compliant.

---

### 4️⃣ Scope Selector: Choosing Where Rules Apply

When Ayesha clicks on the **Scope selector**, she’s telling Azure *where* the rule should apply. The scope could be a subscription (which is like a folder for all cloud stuff), a resource group (a sub-folder), or even a specific resource.

In this case, she selects a **resource group**—think of it like picking a specific department in a company. She wants the rule to only apply to that department, so team members working there can only create resources in “UK South.” This way, you avoid applying rules too broadly or too narrowly.

---

### 5️⃣ Built-in Policy Definitions: Pre-Made Rules You Can Use

Instead of writing complex code, Azure provides **built-in policies**—ready-made rules that cover common business needs. Ayesha finds one called **“Allowed locations.”** This is a pre-written rule that simply asks: *Where should your resources be allowed to live?*

It’s like choosing a sign from a template that says, “Employees must park only in Lot A.” You don’t have to design the sign yourself—you just pick the one you need, fill in your preferences (like “UK South”), and post it.

---

### 6️⃣ Assigning the Policy: Putting the Rule Into Action

Once she finds the right policy, Ayesha assigns it. She gives it a name, explains what it does, and chooses **UK South** from a dropdown list. This step is like saying, “This is our official company rule, and it starts now.”

She also makes sure **Policy Enforcement** is turned on. Without this, the rule would just be a suggestion. With it turned on, Azure will actually *block* actions that break the rule—like someone trying to create a resource in “East US.”

---

### 7️⃣ Testing the Policy: Seeing the Rule in Action

To make sure the policy works, Ayesha tries to create a **Virtual Network** in the wrong region (East US). As expected, it fails. A validation message pops up, saying the location is not allowed. Success! The policy did its job.

She changes the region to **UK South**, and this time the virtual network is allowed to be created. This is like testing a new security badge at work—if it blocks the wrong doors and opens the right ones, you know it’s set up correctly.

---

### 8️⃣ The Takeaway: Simple Rules, Big Impact

In just 30 minutes, Ayesha learned how to set up and test an Azure Policy that helps her team avoid costly mistakes and stay compliant with regional regulations. She didn’t need coding or complex tools—just a good understanding of *what rule to set* and *where to apply it*.

This lab shows how **Azure Policy acts like your cloud’s silent helper**, always watching, always enforcing the rules. For beginners, this is a powerful first step into **cloud governance**—a way to create smart guardrails that protect your business without slowing anyone down.
