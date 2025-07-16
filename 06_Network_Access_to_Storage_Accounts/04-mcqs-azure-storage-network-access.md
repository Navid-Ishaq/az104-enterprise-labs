
# 🔐 Azure Security MCQs – Lab 6: Network Access to Storage Accounts

> High-quality, scenario-based MCQs for AZ-500 interview readiness and certification preparation.

---

## 📘 Topic Overview:
This MCQ set is based on **Lab 6: Network Access to Storage Accounts**, focusing on secure access to Azure **Storage Accounts** via **Private Endpoints**, **Virtual Networks**, and **Storage Explorer** within a **Windows VM**.

---

### ✅ Questions

**Q1. Why was a private endpoint used for the storage account in this lab?**

(a) To improve performance during uploads  
(b) To enable encryption of storage data  
(c) To restrict access to the storage account via a private IP  
(d) To configure DNS forwarding  

✅ **Correct Answer:** (c)  
💡 **Explanation:** A **private endpoint** provides secure access to an Azure resource over a private IP address from within a virtual network, removing the need for public access.

---

**Q2. What was the purpose of disabling public access during storage account creation?**

(a) It enables geo-replication  
(b) It allows NSG rules to apply directly  
(c) It forces access to happen only over private endpoint  
(d) It is required for Standard_LRS performance tier  

✅ **Correct Answer:** (c)  
💡 **Explanation:** Disabling public access ensures that only **private endpoint traffic** can reach the storage account, increasing security.

---

**Q3. In the virtual network setup, why was a custom subnet address (10.0.0.0/24) used?**

(a) To ensure compatibility with the VM image  
(b) To define IP range for private endpoint and VM  
(c) To enforce encryption at subnet level  
(d) Required for GRS redundancy  

✅ **Correct Answer:** (b)  
💡 **Explanation:** Defining a subnet IP range ensures that **VMs and endpoints** deployed in the same subnet can communicate securely.

---

**Q4. What command helps validate private DNS resolution inside the VM?**

(a) ping stgnxtnav001.blob.core.windows.net  
(b) curl stgnxtnav001  
(c) nslookup stgnxtnav001.blob.core.windows.net  
(d) az login  

✅ **Correct Answer:** (c)  
💡 **Explanation:** `nslookup` checks if the **blob endpoint** resolves correctly using **private DNS** when connected through a **private endpoint**.

---

**Q5. Why was Azure Storage Explorer installed inside the VM?**

(a) To download operating system logs  
(b) To manage VM snapshots  
(c) To upload and explore storage account blobs  
(d) Required to connect via RDP  

✅ **Correct Answer:** (c)  
💡 **Explanation:** **Azure Storage Explorer** enables you to manage blob containers, file shares, and other storage elements from within the VM environment.

---

**Q6. What happens if the VM is deployed in a different virtual network than the private endpoint?**

(a) It will automatically create a peering  
(b) Access to the storage account might fail  
(c) The VM will still access the blob using public DNS  
(d) GRS will automatically replicate data  

✅ **Correct Answer:** (b)  
💡 **Explanation:** The VM must be in the **same VNet or properly peered** network to access the resource via private endpoint.

---

**Q7. Which access method was used in Storage Explorer to connect to the storage account?**

(a) Azure AD sign-in  
(b) SAS Token  
(c) Connection String  
(d) Shared File Mount  

✅ **Correct Answer:** (c)  
💡 **Explanation:** The lab used a **connection string** obtained from the **Access Keys** section of the storage account to authenticate.

---

**Q8. What type of redundancy was selected during storage account setup?**

(a) LRS  
(b) ZRS  
(c) GRS  
(d) GZRS  

✅ **Correct Answer:** (c)  
💡 **Explanation:** **GRS (Geo-redundant storage)** replicates your data to a secondary region for higher availability.

---

**Q9. Why was the VM deployed into the same subnet as the private endpoint?**

(a) For easier NSG control  
(b) To support boot diagnostics  
(c) To enable private IP communication  
(d) For better performance of SSD  

✅ **Correct Answer:** (c)  
💡 **Explanation:** Being in the same **subnet** allows the VM to access the storage account using the **private endpoint IP**.

---

**Q10. What initial setting had to be turned off in Server Manager to allow browser downloads?**

(a) RDP Access  
(b) IE Enhanced Security Configuration  
(c) Windows Firewall  
(d) PowerShell Execution Policy  

✅ **Correct Answer:** (b)  
💡 **Explanation:** **IE Enhanced Security Configuration** limits downloads and browsing; turning it off allows downloading tools like Storage Explorer.

---

> _"Real security isn't just about locks and firewalls — it's about understanding the path and respecting the limits."_  
> — Jamalu  
> — **Siraat AI Academy**

"""

# 🔐 Professional-Level Azure Security MCQs

## Point 10 – Real-World MCQs for Hiring & Mastery

🎯 **Topic Focus:** Secure Network Access to Storage Accounts

🛠 **Source Context:** Lab on private endpoints, VNets, storage access, and NSG-based segmentation.

---

### **Q1. Why might an organization prefer a private endpoint over a service endpoint when securing storage access?**

(a) Private endpoints are cheaper to implement

(b) Private endpoints offer DNS-based filtering for public access

(c) Private endpoints isolate traffic at the network layer and assign a private IP address

(d) Service endpoints provide better auditing capabilities

✅ **Correct Answer:** (c)
💡 **Explanation:** Private endpoints map storage resources directly into your VNet via a private IP, ensuring traffic stays on the Microsoft backbone. Unlike service endpoints, they block public exposure entirely.

---

### **Q2. Ayesha from **DevStreamCloud** created a storage account with public access disabled. However, users outside the VNet still accessed the blob service. What likely went wrong?**

(a) NSG was misconfigured to allow outbound internet access

(b) The storage account was not added to the trusted services list

(c) The storage firewall was set to allow All Networks

(d) The subnet was not associated with a private endpoint

✅ **Correct Answer:** (c)
💡 **Explanation:** Even if public access is disabled, if the storage firewall allows all networks, external traffic can still connect.

---

### **Q3. What tool is most appropriate for verifying DNS resolution of a storage account via a private endpoint inside a VM?**

(a) Telnet
(b) Curl
(c) nslookup
(d) netstat

✅ **Correct Answer:** (c)
💡 **Explanation:** `nslookup` helps confirm that the DNS name resolves to a private IP, validating the private endpoint's effect.

---

### **Q4. In which scenario does a private endpoint NOT improve security?**

(a) When storage is accessed from an on-premises network via VPN

(b) When access is restricted to specific VNets

(c) When storage access logs are required for audit

(d) When a workload is public-facing and deployed in multiple regions

✅ **Correct Answer:** (d)
💡 **Explanation:** Private endpoints are regional and VNet-specific. For global public-facing services, they may add complexity, not clarity.

---

### **Q5. What happens when you create a private endpoint for the blob sub-resource?**

(a) All sub-resources are automatically secured

(b) Only blob traffic is redirected through the private IP

(c) File share traffic is redirected as well

(d) NSG automatically blocks public IPs

✅ **Correct Answer:** (b)
💡 **Explanation:** Private endpoints are scoped per sub-resource, like blob, file, queue, etc. Blob traffic only is routed through the endpoint.

---

### **Q6. Sofia needs to troubleshoot why Azure Storage Explorer inside her VM cannot access the storage account via private endpoint. Which issue is LEAST likely to be the cause?**

(a) IE Enhanced Security is enabled
(b) The wrong connection string is used
(c) The VM is in the wrong subnet
(d) The blob sub-resource is not assigned a managed identity

✅ **Correct Answer:** (d)
💡 **Explanation:** Blob sub-resources don’t require a managed identity to connect using a connection string.

---

### **Q7. Taylor wants to deploy 10 VMs across 3 subnets, all needing access to a private storage account. What’s the best architectural step?**

(a) Assign a private endpoint to each VM

(b) Create a private endpoint per subnet

(c) Use one private endpoint and route all subnets through it

(d) Enable public access with IP firewall rules

✅ **Correct Answer:** (b)
💡 **Explanation:** For full isolation, assigning a private endpoint per subnet ensures that each segment has scoped, private access.

---

### **Q8. Which setting ensures a VM cannot access the internet unless explicitly permitted?**

(a) Subnet DNS override
(b) NSG with denied outbound rules
(c) Application Gateway
(d) VNet Peering is disabled

✅ **Correct Answer:** (b)
💡 **Explanation:** NSGs can control outbound traffic. Blocking all outbound traffic and allowing only what’s required is a common zero-trust step.

---

### **Q9. Alex from **SkyBridgeTech** deployed a private endpoint, but users still see public DNS names resolving. What should he verify?**

(a) VNet DNS is set to Azure default resolver

(b) He disabled Azure Private DNS integration

(c) The storage account firewall is misconfigured

(d) Azure Policy is blocking private DNS creation

✅ **Correct Answer:** (a)
💡 **Explanation:** If DNS is not set to resolve via Azure Private DNS Zone, users will still resolve public endpoints.

---

### **Q10. What’s the main risk of forgetting to remove the default address space in a VNet configuration?**

(a) VNet will be publicly accessible

(b) Private endpoint will not be created

(c) Overlapping IP ranges may cause connectivity failures

(d) You can't deploy VMs in the subnet

✅ **Correct Answer:** (c)
💡 **Explanation:** Default IP ranges like `10.0.0.0/16` can conflict with other VNets, leading to subnet overlap and routing issues.

---

### **Q11. When you see the `$logs` container in Azure Blob, what does it represent?**

(a) Billing history

(b) Diagnostic logs generated by Azure

(c) Access logs from Microsoft support

(d) Resource cost breakdown

✅ **Correct Answer:** (b)
💡 **Explanation:** `$logs` is an automatically generated container holding storage analytics logs — useful for auditing.

---

## ✨ Final Note from Jamalu

> *“These aren’t just questions. They’re quiet challenges — asking if you’re ready not just to pass… but to protect.”*
> — Jamalu
> — **Siraat AI Academy**

---
