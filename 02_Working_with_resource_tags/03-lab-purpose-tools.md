# [2] Working with resource tags

This lab guide provides enterprise-ready, scenario-driven walkthroughs for mastering key Azure administrator tasks aligned with the AZ-104 certification.

### 🏷️ *Tag It Right: Understanding Azure Resource Tagging and VM Management*

---

#### 🧭 What This Lab Is All About

This lab is a simple, hands-on introduction to how organizations can stay organized in the cloud using **Azure resource tags**. You’ll learn how to create a virtual machine (VM), apply a tag to it, and then use that tag to find or manage the resource.

At first glance, this might sound like a tiny task. But in real-world cloud environments—especially in growing companies like **BrightOps Group**—these small steps make a **big difference**. Emma, an operations lead at BrightOps, recently realized that untagged cloud resources were causing budget confusion and tracking headaches. This lab shows how tags can help teams like Emma’s *bring clarity and structure* to their virtual machines and other cloud tools.

---

#### 🏢 Why This Lab Matters in the Real World

Imagine you're managing a big office with hundreds of items—desks, chairs, laptops—but none of them are labeled. You wouldn’t know which belong to which department, who’s using what, or what needs to be retired. That’s what cloud environments can feel like without **resource tagging**.

In the real world, IT admins like **Alex** at TechNest Solutions use Azure tags to track who owns a resource (like a virtual machine), what it’s for (e.g., "Testing" or "Finance"), or when it was created. Tags help with budgeting, cleanup, auditing, and planning. This lab helps you practice these real-life habits so you’re ready when your company needs it most.

---

#### 💻 What Is a Virtual Machine (VM)?

In Task 1, you create a **Virtual Machine** using the **Azure Virtual Machines** service. Think of a VM as a computer that lives in the cloud instead of on your desk. It has an operating system, storage, and computing power—but you don’t need to worry about buying hardware or maintaining it physically.

In this lab, Emma creates a VM called `resizeVM` for her IT team. It runs **Windows Server 2019**, just like a real Windows computer. VMs like this are often used for testing software, running apps, or simulating environments—without needing a separate physical machine.

By the end of this task, you’ll have created your own cloud-based computer. That’s a powerful thing—even if it’s just for practice!

---

#### 📦 What Is a Resource Group?

Before creating a VM, you’re asked to pick or create a **Resource Group**. Think of this as a **folder** where related Azure resources are stored together. It helps keep things organized.

For example, if Emma’s team is working on a project called “Migration2025,” all the VMs, databases, and storage for that project could go into one resource group. If they ever decide to delete the project, they can remove everything inside the folder at once. This is much easier than hunting down each item separately.

In the lab, you use a resource group like `rg-labresources`. It’s a small but essential step toward better organization and cleaner cloud management.

---

#### 🏷️ What Are Azure Tags (And Why Use Them)?

The heart of this lab is understanding **Azure Tags**. Tags are like **labels or sticky notes** you attach to cloud resources. Each tag has a **name** and a **value**—for example, “Department = IT.”

Emma uses tags to identify which team owns a resource. Later, when someone looks at a list of 50 VMs, they can filter and say, “Show me only the ones used by IT.” This saves time, prevents mistakes, and makes cleanup easier.

Alex, the IT admin at TechNest, once told Emma, “A tag today saves ten headaches tomorrow.” This lab shows exactly how true that is.

---

#### 🔍 What Is Filtering by Tag?

In Task 3, you use the Azure portal to **filter resources by their tags**. It’s like using the “Search” or “Sort by” feature in Excel—but for cloud items.

Let’s say Emma needs to clean up unused resources after a busy quarter. Instead of checking each VM, she filters the view to show only items tagged with `Department = IT`. Instantly, she knows what belongs to the IT department and what can be reviewed.

Filtering by tag helps teams find what they need fast—and avoid deleting something important by mistake.

---

#### 🧰 How These Tools Work Together

Here’s how it all connects:

* You create a **Virtual Machine**, which becomes a usable cloud-based computer.
* You store it inside a **Resource Group**, helping you organize related items.
* You attach a **Tag** to that VM, adding context (like who owns it).
* You use **Filtering** to find that VM later using the tag.

All these tools work like parts of a smart filing system. Without tags or groups, it’s like having a messy room with cables, laptops, and notes scattered everywhere. With these tools, Emma and her team can stay in control—even when the cloud gets crowded.

---

#### 🚀 Takeaways for Beginners

For someone like Grace, a new hire at NovaEdge Systems, this lab is a simple but powerful first step. Before doing it, she thought Azure was only for complex, high-level tasks. But now she sees how everyday tools—like creating VMs or tagging—help real teams work smarter.

“I always thought tagging was optional,” she told Emma during a training session. “But now I get why it’s a best practice.”

And that’s the real win of this lab: not just learning the *how*, but understanding the *why*.

---

#### 📝 Final Thoughts: Small Habits, Big Impact

This lab shows that even the smallest actions—like naming a VM or adding a tag—have ripple effects in cloud environments. They improve clarity, boost team coordination, and reduce waste.

Emma, Alex, and Grace now treat tagging as a standard part of every project. Because once you’ve experienced how organized and powerful a well-tagged environment can be—you won’t go back to chaos.

Whether you’re just getting started or helping manage a growing cloud portfolio, this lab helps you build the habits that keep your Azure environment clean, clear, and ready for anything.
