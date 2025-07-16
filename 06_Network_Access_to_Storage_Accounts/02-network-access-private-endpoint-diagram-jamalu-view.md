### 📊 Diagram Insight – Secure Storage Access via Private Endpoint

```
+----------------------------+
| Azure Virtual Network     |
| vnet-ncloudedge-west1     |
| Region: West Europe       |
+----------------------------+
            |
     +-------------+
     | Subnet      |
     | subnet-nxt- |
     | app         |
     +-------------+
            |
    ┌─────────────────────────────┐
    |  Private Endpoint (PE)      |
    |  Name: pe-nxtblob01         |
    |  Sub-resource: blob         |
    |  Connected to:              |
    |  stgnxtnav001.blob.core...  |
    └─────────────────────────────┘
            |
    +------------------------------+
    |  Storage Account             |
    |  Name: stgnxtnav001          |
    |  Network Access: Private     |
    |  Redundancy: GRS             |
    +------------------------------+
            ▲
            │ Uses private IP only
            │
+---------------------------+       RDP over port 3389
| Virtual Machine (VM)      |<-------------------------+
| Name: vm-ncloudedge-access|                          |
| OS: Windows Server 2019   |                          |
| Tools: Azure Storage Exp. |                          |
+---------------------------+                          |
            |                                         |
   +-------------------------+                        |
   | Connect using PowerShell|                        |
   | and connection string   |                        |
   +-------------------------+                        |
                                                       |
           (Access Blob securely via Storage Explorer) |
                                                       |
                         +----------------------------+
                         |  Blob Container: $logs     |
                         +----------------------------+
```

---

### 🌟 Notes from Jamalu:

* **Everything speaks in this architecture — but only privately.**
* The **Storage Account** doesn’t wave to the public. It listens only to what’s inside its trusted **Virtual Network.**
* The **Virtual Machine** walks quietly through the subnet, knocking on the door with a **private endpoint key.**
* No public noise. Just secure whispers — that’s the way Jamalu prefers the cloud to behave.

---

