# [3] Creating Azure Policies

This lab guide provides enterprise-ready, scenario-driven walkthroughs for mastering key Azure administrator tasks aligned with the AZ-104 certification.

**🌍 Title: “Keeping Cloud Operations Compliant – A Global Team’s Policy-Driven Challenge”**

---

### 1️⃣ Setting the Stage: A Global Team Faces a Growing Cloud Footprint

At **BrightOps Solutions**, a mid-sized cloud consulting firm based in London, teams from around the world collaborate to support enterprise clients. Among the diverse staff are **Rohan**, a cloud solutions architect from Mumbai, and **Ayesha**, a junior cloud administrator based in Birmingham. They recently joined a new project to streamline cloud governance for a growing retail chain that’s expanding its operations across Europe.

The client has been rapidly adopting Azure, but their internal teams keep creating resources in different regions—some even outside the UK. This triggered concerns over compliance with data residency laws, especially for customer information. “We need a clear way to *limit where resources are created*, or we’re going to end up with a security headache,” their team lead Jordan remarked in a planning call.

---

### 2️⃣ The Problem: Region Chaos and Compliance Headaches

During a routine audit, Ayesha noticed that some virtual machines were deployed in the **East US** region—despite the client operating solely in the UK. This not only raised eyebrows but also set off internal alarms about GDPR compliance and budget inefficiency. “Why are we paying for services halfway across the world?” Jordan asked. No one had a clear answer.

Rohan chimed in thoughtfully, “I think it’s just a lack of guardrails. Anyone can choose any region when deploying resources.” This realization led the team to a crucial conclusion: **they needed a policy-based control system** to restrict where cloud resources could be deployed.

---

### 3️⃣ The Spark: Discovering Azure Policy

In their weekly strategy sync, Jordan introduced the team to a feature called **Azure Policy**. “It allows us to enforce rules, like restricting regions or preventing the use of expensive VM sizes,” he explained. Rohan got excited—this sounded like exactly what they needed to solve their issue with non-compliant deployments.

“Let’s run a test in our lab environment,” suggested Ayesha, eager to get hands-on. They chose a resource group called `rg-labresources` and decided to create a policy that only allows resources to be deployed in the **UK South** region. “This will be our first step in rolling out governance,” Rohan smiled.

---

### 4️⃣ Policy in Action: Setting the Guardrails

Ayesha took the lead. She logged into the Azure portal and searched for the **Policy** service. “Found it,” she announced to the team over a Teams call. After choosing the right scope, she selected the **Allowed locations** built-in policy. She named the assignment “Allow UK South for rg-labresources” and added a note: *Allow resources to be created in UK South only*.

“Make sure policy enforcement is turned on,” Rohan reminded her. After setting UK South in the Parameters tab, she clicked **Review + create** and deployed the policy. “Done! Now let’s test it.”

---

### 5️⃣ The Test: Blocking the Wrong Move

To test the new rule, Ayesha tried creating a **virtual network** in the `rg-labresources` group—but set the region to **East US**. “Let’s see if it catches this,” she said with curiosity. As expected, the validation failed. She clicked the error message and saw the explanation: *Deployment region is not allowed by policy*.

“Nice! That’s exactly what we want,” Jordan cheered. Ayesha then changed the region to **UK South**, and the validation passed. “Boom. Policy accepted. Resource deployed,” she said, feeling a surge of confidence. The team knew they were on the right path.

---

### 6️⃣ Why It Matters: Scaling Governance the Right Way

The small test carried big implications. By using Azure Policy, the team at BrightOps could **scale governance without slowing down innovation**. Instead of policing every deployment manually, they were putting smart rules in place that would do it for them.

“Eventually, we’ll apply this to all production environments,” Rohan said. “And we can expand the policies to include cost control, VM sizes, and even tagging.” Ayesha nodded. “This makes it way easier for junior admins like me to stay compliant without second-guessing every decision.”

---

### 7️⃣ Reflecting on the Win: Team Growth and Client Trust

Later that week, Jordan shared their success with the client. “We’ve implemented location-based restrictions in Azure using policy assignments,” he explained. “Now you won’t have resources showing up outside your intended regions.” The client’s CTO smiled. “That’s exactly the kind of proactive thinking we need.”

Back at BrightOps, the win wasn’t just technical—it was cultural. Rohan and Ayesha felt empowered. “It’s great knowing we’re building not just systems—but trust,” Ayesha said during their Friday wrap-up. Rohan agreed: “This lab was short, but the impact is long-term.”

---

### 8️⃣ The Bigger Picture: Policies as the Foundation of Cloud Trust

In the fast-moving world of cloud, it’s easy to focus only on speed and flexibility. But **governance is what turns cloud into a reliable platform**. The lab on Azure Policy wasn’t just about checking boxes—it was about creating an environment where teams can move fast *safely*.

With just a half-hour lab, the BrightOps team took the first step toward building a trusted, well-governed cloud foundation—one policy at a time.
