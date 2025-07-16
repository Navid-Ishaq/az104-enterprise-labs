
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

