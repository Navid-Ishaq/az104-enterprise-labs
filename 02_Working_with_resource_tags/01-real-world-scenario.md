# [2] Working with resource tags

This lab guide provides enterprise-ready, scenario-driven walkthroughs for mastering key Azure administrator tasks aligned with the AZ-104 certification.

### 💼 *Keeping Things in Order: How Emma’s Team Tackled Azure Tagging for IT Resources*

---

#### 🏢 The Challenge at BrightOps Technologies

Emma is the Operations Lead at **BrightOps Technologies**, a fast-growing startup that builds productivity tools for remote teams. Over the past year, their cloud usage has skyrocketed — they’ve spun up virtual machines (VMs) for testing, development, and demos. But lately, Emma has noticed a problem: *nobody knows what resources belong to which team anymore.*

"Why are we paying for three virtual machines named ‘test-vm’ with no context?" she asked Liam, the company's IT administrator, during a Friday check-in.

Liam sighed. "That’s the issue. We’re creating stuff quickly, but we’re not tracking anything properly. We need a better system."

And so, the need to *bring order to their cloud chaos* began.

---

#### 👩‍💻 Meet the Team: Roles and Realizations

Emma oversees internal operations. Her focus is making sure resources are being used efficiently — and that nothing gets forgotten or left running unnecessarily. Liam, meanwhile, handles the actual cloud infrastructure. He's tech-savvy but juggling many tasks.

Jordan, a junior engineer, had just started helping out with VM deployments. “I’ve been setting up test environments,” he admitted in a meeting, “but I didn’t realize we had to label things. I thought IT would just know.”

Emma realized they weren’t just dealing with a technical gap — they had a communication gap too.

“It’s no one’s fault,” she said gently. “But we need to start tagging our resources. It’s the only way we’ll keep track of who owns what.”

---

#### 🌐 Why Tags Matter in the Real World

Liam explained it like this: “Think of tags like sticky notes. When you spin up a virtual machine or any Azure resource, a tag tells you what it’s for — like whether it’s part of the IT team, Marketing, or DevOps.”

Emma nodded. “And later, we can sort or filter them easily — just like folders or labels.”

They all agreed this could save them time and money. No more guessing which machine belongs to whom, or deleting something by mistake. It could also help during audits or budgeting, especially when reviewing cloud bills.

So, they decided to run a test: create a VM, tag it properly, and see how well the system could track and filter it.

---

#### 🛠️ A Small Lab with a Big Lesson

Liam kicked off the demo. “We’ll call this VM `resizeVM`. Let’s say it’s part of our IT department’s test suite. We’ll tag it that way.”

He walked Jordan through it:

> “Go to the Azure portal, create a virtual machine, and call it `resizeVM`. Make sure to choose a lightweight option — we don’t need anything powerful for now.”

Jordan followed along. “Okay, B1s size… Region East US… all set. What's next?”

> “Now, we tag it. Click on the Tags section and add: Name = Department, Value = IT. This tells everyone it’s an IT resource.”

Jordan smiled. “That’s it? That’s pretty simple.”

---

#### 🔍 Using Tags to Filter and Manage

Next, Liam showed them how to filter.

“Let’s pretend it’s next month, and we want to see *only* IT-related resources. Instead of checking one-by-one, we filter by tag: Department = IT.”

Emma watched as the portal narrowed the view instantly. “That’s so helpful. We can clean up old machines or monitor costs by department.”

They even practiced deleting the resource, just to see how easy cleanup became when everything was labeled clearly.

> “Without a tag,” Liam added, “you’d hesitate before deleting anything. You’d think: 'What if this is critical?' But with tags? No second-guessing.”

---

#### 💬 Team Takeaways: Communication Is Key

Later that afternoon, the team reflected on what they learned.

“I used to think tags were just an extra step,” Jordan admitted. “But now I see — it’s how you keep cloud stuff from turning into a mess.”

Emma agreed. “This isn’t just about Azure. It’s about working smarter. If we all agree to tag our resources properly, we’ll avoid confusion later.”

They decided to create a simple tagging policy for the company — something easy to follow but consistent.

---

#### 📘 From Lab to Real Life

What started as a simple Azure lab became something much more meaningful: a shared understanding between operations and IT. By creating a virtual machine, adding a tag, and filtering resources, the team learned how *clarity and ownership* could make cloud management smoother.

For BrightOps, this wasn’t just a technical skill — it was a culture shift. And it all started with a sticky-note-like tag.

---

#### ✅ Final Thoughts

This hands-on task helped Emma, Liam, and Jordan learn a critical best practice in cloud management — one that’s often overlooked when teams are moving fast. Through one small VM and a tag called “IT,” they built a foundation for better resource management, accountability, and teamwork.

> As Emma put it best:
> *“In the cloud, a little labeling goes a long way.”*
