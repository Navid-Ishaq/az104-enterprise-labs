# [2] Working with resource tags

This lab guide provides enterprise-ready, scenario-driven walkthroughs for mastering key Azure administrator tasks aligned with the AZ-104 certification.

### 🧩 *“Tag, Track, and Tidy Up: A Clear Guide to Managing Azure Resources”*

---

### 🗺️ **Text-Based Visual Diagram: Step-by-Step Workflow**

```
[ Start Lab ]
     |
     v
[Log in to Azure Portal]
     |
     v
[Create Virtual Machine]
     |
     |-- Choose Resource Group → e.g., rg-labresources
     |-- Name VM → resizeVM
     |-- Choose Region → East US
     |-- Choose Image → Windows Server 2019
     |-- Select Size → B1s
     |-- Set Username/Password
     |-- Select Disk → Standard SSD
     |
     v
[Click Review + Create → Create VM]
     |
     v
[Go to Resource Groups → rg-labresources]
     |
     v
[Open resizeVM → Go to Tags]
     |
     |-- Add Tag:
     |     Name: Department
     |     Value: IT
     |
     v
[Apply Tag]
     |
     v
[Go Back to Resource Group]
     |
     v
[Click 'Add Filters' → Select Tag: Department = IT]
     |
     v
[View Filtered Resources → Confirm visibility]
     |
     v
[Delete All Resources]
     |
     v
[ End Lab ]
```

---

### 👥 **Meet the Team at BrightTech Solutions**

At **BrightTech Solutions**, a growing IT consultancy, Sarah (project coordinator), Mike (junior cloud admin), and John (senior engineer) are working together to improve how they manage their cloud resources. Sarah recently noticed their Azure environment was getting messy—resources were being created but not always cleaned up or labeled clearly.

“I couldn’t tell which VM belonged to which team,” Sarah said during their team sync. “We need a better system or we’ll start losing track.”

That’s when John suggested they try a lab on **resource tagging in Azure**. It would be a safe way to learn the basics and practice good habits for real-world work.

---

### 🧱 **Building the Foundation: Creating a Virtual Machine**

Mike was a bit nervous—he hadn’t created a VM on his own before. But Sarah encouraged him: “We’ll follow the steps together. It’s like building a Lego set. One block at a time.”

They started in the **Azure Portal**, clicking “+ Create” under Virtual Machines. As the screen prompted them for details, they selected a **resource group** (`rg-labresources`), gave the machine a name (`resizeVM`), picked the region (East US), and set up the operating system (Windows Server 2019).

John jumped in to explain, “This VM is just like a virtual computer. You’re telling Azure where to place it, what it runs, and how strong it should be.” Once everything looked good, Mike hit **Create**—and just like that, the VM was on its way.

---

### 🏷️ **Labeling for Clarity: Adding a Tag**

Once the VM was created, Sarah asked, “Okay, but how do we know it’s ours when we look at the dashboard later?”

“That’s where tags come in,” John replied. “They’re like sticky notes on your lunchbox at work: ‘This one belongs to Mike.’”

They opened the virtual machine, clicked on the **Tags** option from the menu, and added a new tag:

* **Name:** Department
* **Value:** IT

“Nice,” Sarah said. “Now anyone on our team can filter and find it later.”

With just one label, their VM was now connected to a department, making it easier to find, manage, or delete later on.

---

### 🔍 **Finding What Matters: Using Filters**

A few moments later, they returned to the **Resource Group** section and tried the filter feature. Mike clicked **“Add filters”**, chose the tag name “Department,” selected the value “IT,” and hit apply.

Suddenly, the clutter cleared, and only the tagged resource was visible.

“This is like looking for emails in your inbox using labels,” Sarah said. “It narrows things down fast.”

The team realized that this small habit—tagging and filtering—could save hours of detective work later. No more guessing or accidentally deleting something important.

---

### 🧹 **Clean and Clear: Deleting the Resources**

Once they were done reviewing the process, John gave the final instruction: “Now that we’ve practiced, it’s time to clean up. Let’s delete the VM.”

Mike hesitated. “Are we sure we’re not deleting something important?”

“See that tag?” John pointed. “We know this was created for the lab. It’s safe to remove.”

They deleted all the resources in the group with confidence. No second-guessing. No mystery leftovers.

---

### 💡 **Why It All Matters**

Later, over a coffee break, Sarah reflected on what they had just done.

“At first, I thought tagging was just extra work. But now I get it—it’s how we stay in control when things get busy,” she said.

Mike nodded. “It’s like naming files properly on your desktop. It seems small, but it saves so much time later.”

John smiled. “And now you two can teach the rest of the team how to do it right.”

---

### 🚀 **Next Steps and Real-World Confidence**

After completing the lab, the BrightTech team felt much more confident about handling real Azure environments. They decided to create a **company-wide tagging policy**—a simple guide so everyone would use consistent tags across all projects.

What started as a beginner lab turned into a better way of working together.

Now when Sarah looks at the Azure dashboard, she doesn’t see confusion—she sees **clarity**, thanks to a few well-placed tags.

> “It’s like turning on the lights in a messy room,” she said.
> “Everything just makes more sense.”

---

This lab isn’t just about clicking buttons. It’s about learning to manage cloud spaces in a way that keeps your team calm, your projects clean, and your workday running smoothly.
