# [3] Creating Azure Policies

This lab guide provides enterprise-ready, scenario-driven walkthroughs for mastering key Azure administrator tasks aligned with the AZ-104 certification.

**📝 Lab 3: Creating Azure Policies – Step-by-Step Walkthrough**

**Organization:** *BrightOps Solutions*

**Characters:** Ayesha (Cloud Admin), Rohan (Cloud Architect)

**Purpose:** Learn how to apply an Azure Policy to restrict resource creation to a specific region.

---

## ✅ Overview

In this hands-on lab, you'll follow Ayesha, a junior cloud admin at **BrightOps Solutions**, as she creates and tests a location-restriction policy in Azure. The goal is to **only allow resources to be deployed in the "UK South" region**, ensuring compliance with company and regional requirements.

---

## 🛠️ Step 1: Log into Azure Portal

1. Open a browser and navigate to the [Azure Portal](https://portal.azure.com/).
2. Sign in using your Azure credentials.
3. Make sure you're working within the right subscription.

---

## 📍 Step 2: Create a Resource Group

We'll use a dedicated resource group for this lab.

1. In the search bar at the top, type `Resource groups` and select it.
2. Click **+ Create**.
3. Fill in the following:

   * **Subscription:** Your default subscription
   * **Resource Group Name:** `rg-brightops-ayesha`
   * **Region:** UK South
4. Click **Review + create**, then **Create**.

---

## 📋 Step 3: Assign a Policy to Restrict Allowed Locations

1. In the top search bar, type `Policy` and open the **Policy** service.
2. On the **Overview** page, click the **Scope selector** (three-dot icon).
3. Choose **`rg-brightops-ayesha`** as the target resource group, then click **Select**.

---

## 🔍 Step 4: Find and Assign the Built-in Policy

1. From the left-hand menu under **Authoring**, click **Definitions**.
2. In the search bar, type **Allowed locations**.
3. Select the built-in policy named **Allowed locations** to view details.
4. Click **Assign policy**.

In the **Basics** tab:

* **Assignment name:** `policy-allow-uksouth-only`
* **Description:** `Restrict all resources to UK South region`
* **Policy enforcement:** Enabled
* Confirm that **Scope** is set to `rg-brightops-ayesha`.

Click **Next** to continue.

---

## 🌍 Step 5: Set Allowed Region

In the **Parameters** tab:

1. For **Allowed locations**, select **UK South** from the dropdown.
2. Click **Review + create**, then **Create** to deploy the policy assignment.

---

## 🚫 Step 6: Test the Policy with a Disallowed Region

Let’s test if the policy works by trying to create a resource in a different region.

1. In the Azure Portal, search for and open **Virtual Networks**.

2. Click **+ Create**.

3. In the **Basics** tab:

   * **Subscription:** Your default subscription
   * **Resource group:** `rg-brightops-ayesha`
   * **Name:** `vnet-brightops-test01`
   * **Region:** East US (intentionally incorrect)

4. Click **Review + create**.

You should see a **validation error**. Click on it to confirm that the region is disallowed by policy.

---

## ✅ Step 7: Deploy Resource in the Allowed Region

Now test again using the correct region.

1. Go back to the **Basics** tab.
2. Change the **Region** to **UK South**.
3. Click **Review + create**, then **Create**.

The deployment should succeed, proving that the policy allows only the approved region.

---

## 🧹 Step 8: Clean Up

After testing, it’s good practice to clean up to avoid unnecessary charges.

1. Go to the **Resource groups** section.
2. Select `rg-brightops-ayesha`.
3. Click **Delete resource group**.
4. Type the name to confirm and complete the deletion.

---

## 🎓 Summary

In this lab, Ayesha successfully used Azure Policy to:

* Limit the creation of resources to a specific region
* Test the enforcement by attempting deployment in an unapproved region
* Understand how policies support compliance and governance

**Skill Unlocked:** Cloud governance using Azure Policy
**Next Step:** Explore other built-in policies like allowed VM sizes or required tags.

---

**Great job! You’ve just taken your first step into managing Azure responsibly and effectively.** 🌍🔐
