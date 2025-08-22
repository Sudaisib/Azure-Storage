
# 🔑 **Azure Lock & Key: Controlling Storage Access** 🛡️

<img width="1536" height="1024" alt="ChatGPT Image Aug 22, 2025, 05_27_12 PM" src="https://github.com/user-attachments/assets/d7130930-7c42-47d6-8abf-05ac7486f7a3" />

---

## 🗂️ **Table of Contents**

1️⃣ [📌 Introduction](#-introduction)

2️⃣ [⚙️ Prerequisites](#-prerequisites)

3️⃣ [📊 Key Security & Access Features](#-key-security--access-features)

4️⃣ [📦 Step 1: Create a Storage Container](#-step-1-create-a-storage-container)

5️⃣ [📤 Step 2: Upload Files & Manage Access Tiers](#-step-2-upload-files--manage-access-tiers)

6️⃣ [🗂️ Step 3: Create a File Share](#-step-3-create-a-file-share)

7️⃣ [🔐 Step 4: Control Access with SAS Tokens](#-step-4-control-access-with-sas-tokens)

8️⃣ [♻️ Step 5: Rotate Keys to Revoke Access](#-step-5-rotate-keys-to-revoke-access)

9️⃣ [📌 Conclusion](#-conclusion)

🔟 [📝 Blog Details](#-blog-details)

1️⃣1️⃣ [🤝 Connect & Share](#-connect--share)

---

## 📌 **Introduction**

Cloud storage isn’t just about saving data — it’s about **controlling access** to protect sensitive files. Azure Storage provides a flexible security model that allows you to:

* Store files in **containers** or **file shares**
* Control how often data is accessed with **tiers**
* Share content securely with **SAS (Shared Access Signatures)**
* Instantly **revoke access** by rotating account keys

This guide walks you through building a **secure and manageable storage strategy** using the “lock and key” approach — give access only when necessary, limit it, and take it back when required.

✅ Perfect for **students, DevOps engineers, cloud beginners, and IT teams**.

---

## ⚙️ **Prerequisites**

Before starting, ensure you have:

| Requirement                                 | Why It’s Needed                       |
| ------------------------------------------- | ------------------------------------- |
| **Active Azure Subscription**               | To create and manage storage accounts |
| **Basic knowledge of Azure Portal**         | Navigation and resource creation      |
| **Sample files (e.g., images, PDFs, CSVs)** | To upload and test access             |

---

## 📊 **Key Security & Access Features**

| **Feature**              | **What It Does**               | **Why It Matters**                  |
| ------------------------ | ------------------------------ | ----------------------------------- |
| **Storage Container**    | Logical grouping of blobs      | Organizes data like folders         |
| **Access Tiers**         | Hot / Cool / Archive           | Saves cost based on data usage      |
| **File Share (SMB/NFS)** | Share files like a local drive | Collaboration across VMs & users    |
| **SAS Tokens**           | Temporary, limited access      | Share without exposing account keys |
| **Key Rotation**         | Invalidate compromised tokens  | Instantly revoke unwanted access    |

---

## 📦 **Step 1: Create a Storage Container**

💡 **Definition:** Containers are like folders inside your Azure Storage Account, used to hold blobs (files).

**Steps:**

1. Open **Azure Portal** → Search *Storage Accounts*
2. Select your storage account → Navigate to **Containers**
3. Click **+ Container** → Name it `secure-container` → Create

✅ You now have a locked space for your files.

---

## 📤 **Step 2: Upload Files & Manage Access Tiers**

💡 **Access Tiers Explained:**

| **Tier**    | **Use Case**                                     | **Cost**                             |
| ----------- | ------------------------------------------------ | ------------------------------------ |
| **Hot**     | Frequently accessed data (e.g., active projects) | 💰 Higher                            |
| **Cool**    | Infrequently used data (e.g., backups)           | 💰 Lower                             |
| **Archive** | Long-term storage (rarely accessed)              | 💰 Lowest but retrieval cost applies |

**Steps:**

1. Open your container → Click **Upload**
2. Select a local file → Upload
3. Change **Access Tier** → Set to *Cool* if rarely accessed

✅ You’ve optimized performance vs. cost.

---

## 🗂️ **Step 3: Create a File Share**

💡 **Why File Shares?**
Unlike containers (object storage), **File Shares** support SMB/NFS protocols — meaning they behave like a traditional file server, accessible from VMs, desktops, or applications.

**Steps:**

1. In your storage account → Select **File Shares** → **+ File Share**
2. Name it `team-share` → Disable backup (optional) → Create
3. Open the file share → Click **Upload** → Add files

✅ You now have both object storage (blobs) and traditional file sharing.

---

## 🔐 **Step 4: Control Access with SAS Tokens**

💡 **Definition:** A **Shared Access Signature (SAS)** lets you share a file or container securely for a **limited time** with specific permissions.

**Example Permissions Table:**

| **Permission** | **Use Case**                       |
| -------------- | ---------------------------------- |
| **Read**       | Allow partner to view a file       |
| **Write**      | Allow app to upload data           |
| **Delete**     | Allow cleanup jobs to remove files |

**Steps:**

1. Select a file inside your container → Click **Generate SAS**
2. Choose **Signing Method: Account Key**
3. Set **Permissions: Read**
4. Restrict protocol: **HTTPS only**
5. Set start & expiry time → Generate SAS URL

✅ Share this link with a trusted partner. Once expired, it becomes useless.

---

## ♻️ **Step 5: Rotate Keys to Revoke Access**

💡 **Why It Matters:**
If someone gets hold of your SAS URL, they could access data until expiry. But rotating the **storage account keys** invalidates all SAS tokens at once.

**Steps:**

1. Navigate to your **Storage Account → Security + Networking → Access Keys**
2. For **Key 1**, click **Rotate Key** → Confirm
3. Try refreshing the old SAS URL → It will fail

✅ You’ve just revoked access instantly.

---

## 📌 **Conclusion**

You’ve now learned how to:

* 🔑 Create secure containers and file shares
* 📤 Upload & manage data across tiers
* 🔐 Control file access with SAS tokens
* ♻️ Revoke access instantly via key rotation

This **lock-and-key approach** ensures your Azure storage remains both **accessible** and **secure**, without compromising cost efficiency.

🔑 **Key Takeaway:** In Azure, true security means not just giving access — but controlling, limiting, and revoking it when necessary.

---

## 📝 **Blog Details**

Read the full blog with step-by-step screenshots and real-world scenarios:
🔗 **[👉 Azure Lock & Key Blog](https://dev.to/sudaisib/azure-lock-key-controlling-storage-access-1eio)**

---

## 🤝 **Connect & Share**

👍 Found this helpful?

✅ **Star this repo**

✅ **Share with your team**

✅ Connect on [LinkedIn](https://www.linkedin.com/in/oladosu-ibrahim/)

✅ Follow me on [Dev.to](https://dev.to/sudaisib) for more Azure tutorials!

