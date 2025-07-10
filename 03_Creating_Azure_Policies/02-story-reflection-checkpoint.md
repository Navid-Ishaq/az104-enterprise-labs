# [3] Creating Azure Policies

This lab guide provides enterprise-ready, scenario-driven walkthroughs for mastering key Azure administrator tasks aligned with the AZ-104 certification.

**🪞 Title: “Guardrails in the Cloud – Ayesha’s First Step Toward Confident Governance”**

---

### 1️⃣ Before the Lab: Curiosity and a Bit of Nerves

When Ayesha first heard that she’d be leading a test run for Azure Policy at **BrightOps Solutions**, she felt both excited and nervous. As a junior cloud administrator still getting used to Azure’s many tools, the idea of applying policies across resources seemed like a big responsibility. “What if I mess up the settings and block everything?” she half-joked during their team sync.

Rohan, her mentor and fellow teammate, smiled reassuringly. “That’s why we use a lab environment. It’s a safe place to learn. Mistakes here help us grow.” With that encouragement, Ayesha felt a bit more at ease. She was curious to see how setting a region restriction through Azure Policy would actually work.

---

### 2️⃣ Starting Out: A Guided Step into Policy

On the day of the lab, Ayesha logged into the Azure portal, her checklist ready. She opened the **Policy** service, remembering Rohan’s earlier advice: “Read each step slowly, and think about why you're doing it—not just how.”

Following the steps, she selected the **Allowed locations** policy and began setting it up for their test resource group, `rg-labresources`. She typed the assignment name, added a description, and selected **UK South** from the dropdown. Everything seemed straightforward so far. “Huh,” she said aloud, “this is actually... kind of fun?”

---

### 3️⃣ A Small Surprise: The Test That Failed on Purpose

After completing the policy assignment, it was time to test it. Ayesha moved to the Virtual Network section and tried to create a new network in **East US**—outside of the allowed region. When the validation failed, she smiled. “It worked! It really blocked the wrong region like it was supposed to.”

Jordan, their team lead, popped into the Teams chat. “Saw the update—looks like it’s doing its job!” Ayesha shared a screenshot of the validation error. Everyone celebrated the small success. It felt good to see a policy doing exactly what it promised.

---

### 4️⃣ Completing the Task: A Clear Win

Ayesha went back, changed the region to **UK South**, and successfully deployed the network. “That’s all I needed to see,” she said proudly. The lab wrapped up with a cleanup of the test resources, and Ayesha made sure nothing was left behind.

The team agreed: the task was completed just as planned. There were no unexpected errors, no confusing steps, and—best of all—it helped Ayesha understand not just how to use Azure Policy, but *why* it matters.

---

### 5️⃣ Learning Moment: Simplicity Behind the Scenes

What surprised Ayesha the most was how **simple** the process felt. “When I first heard about policy enforcement, I thought it would be super complicated. But it’s more about being thoughtful and clear with what we want to allow.”

Rohan nodded during their debrief. “That’s exactly it. Governance isn’t about locking things down—it’s about guiding people to do things the right way.” Ayesha realized how important small guardrails could be, especially in large organizations with many people working in the cloud.

---

### 6️⃣ Building Confidence: From Unsure to Empowered

By the end of the lab, Ayesha’s confidence had noticeably grown. “I used to rely on others to set these kinds of rules. Now I feel like I can help define them too.” She felt empowered to take part in more governance-related tasks—and even suggested they explore policies for naming conventions next.

Jordan was impressed. “This is the kind of initiative we love to see. You’re not just checking boxes—you’re understanding the *why* behind each step.” Ayesha beamed. She wasn’t just completing labs anymore—she was growing into a cloud governance contributor.

---

### 7️⃣ Looking Ahead: Policies with a Purpose

With the success of the lab behind her, Ayesha began thinking bigger. What if they rolled out similar policies across other client environments? What if they created templates for region-based restrictions and shared them across BrightOps?

She shared her thoughts with Rohan. “If we make policies part of our setup from day one, we won’t need to fix things later,” she said. Rohan grinned. “Now you’re thinking like a governance architect.”

---

### 8️⃣ Final Thoughts: A Strong First Step

In just thirty minutes, Ayesha went from feeling uncertain to **owning the process**. She understood that policies weren’t about limiting creativity—they were about **building structure and trust**. And for someone still early in her cloud career, that shift in perspective meant everything.

As she closed her laptop for the day, she smiled. “I thought I was just doing a simple lab,” she said to herself, “but I think I just found my place in the bigger picture.”
