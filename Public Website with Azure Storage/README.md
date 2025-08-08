
---

# ☁️ **Building a Resilient Public Website with Azure Storage: High Availability, Soft Delete, and Blob Versioning in Action** 🚀

![ChatGPT Image Jul 9, 2025, 03_05_04 PM](https://github.com/user-attachments/assets/5f825561-6d0d-443f-b673-e6a1457bdacb)

---

## 🗂️ **Table of Contents**

1️⃣ [📌 Introduction](#-introduction)

2️⃣ [⚙️ Prerequisites](#-prerequisites)

3️⃣ [🧩 Architecture Overview](#-architecture-overview)

4️⃣ [📊 Key Configuration Table](#-key-configuration-table)

5️⃣ [📦 Step 1: Create a Storage Account with High Availability](#-step-1-create-a-storage-account-with-high-availability)

6️⃣ [🌐 Step 2: Enable Anonymous Public Access](#-step-2-enable-anonymous-public-access)

7️⃣ [📂 Step 3: Create a Blob Container](#-step-3-create-a-blob-container)

8️⃣ [⬆️ Step 4: Upload and Test Files](#-step-4-upload-and-test-files)

9️⃣ [♻️ Step 5: Enable Soft Delete](#-step-5-enable-soft-delete)

🔟 [🗃️ Step 6: Configure Blob Versioning](#-step-6-configure-blob-versioning)

1️⃣1️⃣ [📌 Conclusion](#-conclusion)

1️⃣2️⃣ [📝 Blog Details](#-blog-details)

1️⃣3️⃣ [🤝 Connect & Share](#-connect--share)

---

## 📌 **Introduction**

A public website is only as reliable as the storage layer that serves its content. When visitors land on your pages — whether it’s an e-commerce store, a documentation hub, a product showcase, or a personal portfolio — they expect your files to be available, up-to-date, and protected against loss.

**Azure Blob Storage** is a powerful, flexible solution for hosting static files such as images, HTML pages, CSS, PDFs, or any digital asset that should be publicly accessible. With Azure’s global infrastructure, your content is served quickly to users anywhere in the world.

But there’s more to building a resilient website than simply uploading files to the cloud. Accidental deletions, unwanted overwrites, and unexpected regional outages can all cause downtime and data loss if you don’t plan ahead.

This practical guide shows you how to combine **high availability**, **anonymous public access**, **soft delete**, and **blob versioning** — four core features that transform a simple storage account into a **robust, fault-tolerant hosting layer**.

By the end of this walkthrough, you’ll know how to:

✅ Keep your files accessible even if an entire Azure region goes down.

✅ Serve static content publicly without authentication barriers.

✅ Recover files accidentally deleted by developers, scripts, or users.

✅ Roll back changes to older file versions if something breaks.

This blueprint works for personal projects, company sites, product documentation, and any scenario where trust and availability matter.

---

## ⚙️ **Prerequisites**

Before you begin:
✅ An **active Azure subscription**

✅ Access to the **Azure Portal**

✅ Basic knowledge of cloud storage concepts (helpful but not mandatory)

---

## 🧩 **Architecture Overview**

At the core, you’ll deploy:

* **One Azure Storage Account** — your secure namespace for storing website data.
* **One Blob Container** — a logical unit to organize your website’s static files.

<img width="589" height="444" alt="image" src="https://github.com/user-attachments/assets/fa83e1ff-8922-4d6b-96e9-1e91b8066ad4" />

Once configured, this setup can serve files **publicly** to anyone worldwide — resiliently and securely.

---

## 📊 **Key Configuration Table**

| **Feature**              | **Purpose**                                     | **Recommended Setting**                        |
| ------------------------ | ----------------------------------------------- | ---------------------------------------------- |
| **Redundancy**           | Protects against regional failures              | Read-access Geo-Redundant Storage (**RA-GRS**) |
| **Public Access**        | Allows anyone to read website files anonymously | Enabled                                        |
| **Blob Container Level** | Controls access for uploaded blobs              | Blob (anonymous read access for blobs only)    |
| **Soft Delete**          | Recovers accidentally deleted files             | Enabled with 21-day retention                  |
| **Blob Versioning**      | Keeps historical versions of blobs              | Enabled                                        |

This table is a quick reference for the most important settings to ensure your storage is resilient and visitor-friendly.

---

## 📦 **Step 1: Create a Storage Account with High Availability**

1️⃣ In the **Azure Portal**, search *Storage accounts* ➜ **+ Create**

2️⃣ Create a **new Resource Group** (e.g., `Ibrahim`).

3️⃣ Give your Storage Account a unique name (`publicwebsite123`).

4️⃣ Click **Review + Create** ➜ **Create** ➜ **Go to Resource**

5️⃣ To ensure resilience, open **Data management > Redundancy** ➜ choose **Read-access Geo-redundant storage (RA-GRS)** ➜ **Save**

Your storage account is now protected against regional outages.

---

## 🌐 **Step 2: Enable Anonymous Public Access**

Your visitors shouldn’t have to log in to read your website’s files.

1️⃣ In your Storage Account, open **Settings > Configuration**

2️⃣ Make sure **Allow blob anonymous access** is **Enabled**

3️⃣ Click **Save**

---

## 📂 **Step 3: Create a Blob Container**

1️⃣ In **Data storage**, select **Containers** ➜ **+ Container**

2️⃣ Name it (`damilola`) ➜ **Create**

3️⃣ Open your container ➜ **Change access level** ➜ set to **Blob (anonymous read access for blobs only)** ➜ **OK**

Now, files in this container can be read by anyone with the link.

---

## ⬆️ **Step 4: Upload and Test Files**

1️⃣ Inside your container, click **Upload**, pick a file (image or doc) ➜ **Upload**

2️⃣ Click the uploaded file ➜ copy its **URL**

3️⃣ Paste the URL in a browser — the file should load directly!

---

## ♻️ **Step 5: Enable Soft Delete**

**What is Soft Delete?**
Soft Delete acts like a cloud recycle bin — deleted blobs are recoverable for a set period (e.g., 21 days).

1️⃣ In your Storage Account, open **Blob service > Soft delete**

2️⃣ Enable Soft Delete ➜ set retention period to **21 days** ➜ **Save**

🧩 **Try it:**
Delete your test file ➜ toggle **Show deleted blobs** ➜ find the file ➜ **Undelete** ➜ it’s restored!

---

## 🗃️ **Step 6: Configure Blob Versioning**

**What is Blob Versioning?**
Versioning automatically saves every change. Replace a file? Azure keeps the old version too.

1️⃣ In **Blob service**, select **Versioning** ➜ **Enable** ➜ **Save**

🧩 **Try it:**
Upload an updated version of your file (same name). Azure keeps both. You can restore older versions anytime.

---

## 📌 **Conclusion**

You now have a robust setup:
✅ **Highly available** files even during regional failures

✅ **Anonymous public access** for a seamless visitor experience

✅ **Soft Delete** to recover accidental deletions

✅ **Blob Versioning** to roll back unwanted changes

All using just a few clicks in **Azure Portal**.

---

## 📝 **Blog Details**

Read the complete step-by-step blog for detailed screenshots and extra insights:
🔗 **[👉 Read the full blog](https://dev.to/sudaisib/building-a-resilient-public-website-with-azure-storage-high-availability-soft-delete-and-blob-khd)**

---

## 🤝 **Connect & Share**

If you found this guide helpful:
✅ **Star this repo**

✅ **Share it** with your network

✅ Connect with me on [LinkedIn](https://www.linkedin.com/in/oladosu-ibrahim/)

✅ Follow for more **Azure, Cloud & Data tutorials!**

---




