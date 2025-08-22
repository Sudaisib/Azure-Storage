

---

# ☁️ **Azure Storage Projects Portfolio** 🚀

Welcome to my **Azure Storage Projects Portfolio!**

This repository is dedicated to documenting practical, hands-on examples and best practices for setting up and managing **Azure Storage Accounts**. It’s designed as both a self-learning tool and a reference for other cloud beginners or professionals looking to master **Microsoft Azure Storage Services**.

---

## 📌 **Table of Contents** 🗂️

1️⃣ **[Introduction](#-introduction)**

2️⃣ **[Projects Overview](#-projects-overview)**

🔹 **[Project 1: Building Blocks of the Cloud — How to Create and Secure an Azure Storage Account](#-project-1-building-blocks-of-the-cloud--how-to-create-and-secure-an-azure-storage-account)**

🔹 **[Project 2: Building a Resilient Public Website with Azure Storage: High Availability, Soft Delete, and Blob Versioning in Action](#-project-2-building-a-resilient-public-website-with-azure-storage-high-availability-soft-delete-and-blob-versioning-in-action)**

🔹 **[Project 3: Designing Secure and Cost-Effective Private Storage with Azure: Redundancy, Access Control, and Lifecycle Management](#-project-3-designing-secure-and-cost-effective-private-storage-with-azure-redundancy-access-control-and-lifecycle-management)**

🔹 **[Project 4: End-to-End Azure Files Deployment: From Storage Accounts to Restoring Data Securely](#-project-4-end-to-end-azure-files-deployment-from-storage-accounts-to-restoring-data-securely)**

🔹 **[Project 5: Azure Lock & Key: Controlling Storage Access](#-project-5-azure-lock--key-controlling-storage-access)**

3️⃣ **[Types of Storage Services](#-types-of-storage-services)**

4️⃣ **[Comparison of Azure Storage Services](#-comparison-of-azure-storage-services)**

5️⃣ **[Getting Started](#-getting-started)**

6️⃣ **[Technologies & Tools](#-technologies--tools)**

7️⃣ **[Security Best Practices](#-security-best-practices)**

8️⃣ **[Monitoring & Cost Optimization](#-monitoring--cost-optimization)**

9️⃣ **[Additional Resources & Learning](#-additional-resources--learning)**

🔟 **[Documentation & References](#-documentation--references)**

1️⃣1️⃣ **[Contact Information](#-contact-information)**

---

## 📖 **Introduction**

A **Storage Account** in Azure is like the foundational **home** or **vault** where all your cloud storage lives. Think of it as a unique, secure space on Microsoft’s cloud platform where you organize, manage, and control access to data storage services. It is a **fundamental, top-level resource** that provides a secure, scalable, and highly available container for storing different types of data in the cloud.

A Storage Account is not just raw space — it comes with **built-in capabilities** that automatically handle critical concerns like redundancy, availability, security, performance, and scalability, without you needing to manage physical hardware or complex infrastructure. For example, Azure can automatically replicate your data within a datacenter or across regions to protect it from hardware failures or natural disasters. It also gives you a unified way to set permissions, monitor usage, and apply security measures like encryption. You control who can upload, read, or modify the data inside.

---

## 📚 **Projects Overview** 🏗️

Below are practical, focused guides that show how to build, secure, and manage Azure Storage Accounts in real-world scenarios.

### 🔹 **Project 1: Building Blocks of the Cloud — How to Create and Secure an Azure Storage Account**

📌 **Introduction:**
This project is your **hands-on starting point** for understanding the foundational building blocks of Azure Storage. You’ll learn how to create a **Resource Group**, deploy a **Storage Account**, configure core settings like redundancy and secure transfer, and apply basic security controls — all through the Azure Portal.

✅ **Key Features:**

* Creating a **Resource Group** to organize resources logically.
* Deploying a **unique Storage Account** with proper naming and region selection.
* Enforcing **Secure Transfer** and setting **Minimum TLS version**.
* Selecting the right **redundancy level (LRS, GRS)** for durability.
* Restricting access using **network rules and shared key settings**.

🛠️ **Technologies Used:**

* **Azure Portal** — GUI for manual deployment.
* **Azure Resource Manager (ARM)** — Infrastructure orchestration behind the scenes.
* **Azure Storage Services** — Blob, File, Queue, and Table basics.
* **Azure Activity Log** — For tracking resource creation and changes.

📖 **Read the full project:**
[📂 Building Blocks of the Cloud](https://github.com/Sudaisib/Azure-Storage/blob/main/Create%20and%20Secure%20an%20Azure%20Storage%20Account/README.md)

---

### 🔹 **Project 2: Building a Resilient Public Website with Azure Storage: High Availability, Soft Delete, and Blob Versioning in Action**

📌 **Introduction:**
This project demonstrates how to host a **public static website** using **Azure Blob Storage**, with a strong focus on **high availability**, **data protection**, and **versioning** strategies. Learn how to enable the static website feature, implement **Soft Delete** to recover accidentally deleted blobs, and configure **Blob Versioning** for point-in-time recovery.

✅ **Key Features:**

* Configure **Static Website Hosting** in an Azure Storage Account.
* Implement **Soft Delete** to safeguard against accidental deletions.
* Enable **Blob Versioning** to maintain historical versions of content.
* Test and verify data durability and failover scenarios.

🛠️ **Technologies Used:**

* **Azure Blob Storage Static Website Hosting** — to serve static HTML/CSS/JS files.
* **Soft Delete** — to recover deleted blobs.
* **Blob Versioning** — to maintain and restore previous file versions.
* **Azure Portal** — for configuration and management.
* **Azure Storage Explorer** — for easy blob management.
* **Azure Resource Manager (ARM)** — for resource deployment and consistency.

📖 **Read the full project:**
[📂 Building a Resilient Public Website](https://github.com/Sudaisib/Azure-Storage/edit/main/Effective%20Private%20Storage%20with%20Azure/README.md)

---

### 🔹 **Project 3: Designing Secure and Cost-Effective Private Storage with Azure: Redundancy, Access Control, and Lifecycle Management**

📌 **Introduction:**
This project focuses on creating a secure and efficient private storage solution using Azure Storage. The configuration includes **private containers**, **access control via Shared Access Signatures (SAS)**, **geo-redundant backup**, and **lifecycle rules** to automatically optimize cost by moving unused files to cooler tiers. It’s perfect for businesses that need internal document protection, controlled B2B sharing, and disaster recovery.

✅ **Key Features:**

* Deploy a **Geo-Redundant** storage account for high availability.
* Create **Private Containers** with no anonymous access.
* Use **SAS Tokens** to give secure, time-limited access to external collaborators.
* Implement **Lifecycle Management** rules to tier down stale data and save on costs.
* Configure **Object Replication** to back up data from public to private containers.

🛠️ **Technologies Used:**

* **Azure Blob Storage**
* **SAS Tokens** for fine-grained access
* **Lifecycle Management Policies**
* **Object Replication**
* **Azure Portal** and **Storage Explorer**

📖 **Read the full project:**
[📂 Designing Secure and Cost-Effective Private Storage](https://dev.to/sudaisib/designing-secure-and-cost-effective-private-storage-with-azure-redundancy-access-control-and-4ok7)

---

### 🔹 **Project 4: End-to-End Azure Files Deployment: From Storage Accounts to Restoring Data Securely**

📌 **Introduction:**
This project dives into deploying **Azure File Shares**, managing access via **Azure Active Directory (AAD)** or **Storage Account Keys**, backing up with **Azure Backup**, and finally performing a secure restore. You'll gain hands-on experience with Azure Files in both Windows and Linux environments.

✅ **Key Features:**

* Create and configure an **Azure Storage Account** with File service enabled
* Deploy and mount **Azure File Shares** on Windows and Linux VMs
* Use **Access Keys**, **SAS URLs**, and **Azure AD DS Authentication**
* Enable **Azure Backup** for file shares
* Perform **file-level restore** from recovery points

🛠️ **Technologies Used:**

* **Azure File Shares**
* **Azure Virtual Machines**
* **Azure Backup & Recovery Vault**
* **Azure AD DS** (Active Directory Domain Services)
* **PowerShell / Bash** for mounting shares

📖 **Read the full project:**
[📂 End-to-End Azure Files Deployment](https://github.com/Sudaisib/Azure-Storage/blob/main/End-to-End%20Azure%20Files%20Deployment/README.md)

---

### 🔹 **Project 5: Azure Lock & Key: Controlling Storage Access**

📌 **Introduction:**
This project focuses on the **security side of Azure Storage**, teaching you how to manage **who can access files, for how long, and under what conditions**. You’ll set up containers, configure access tiers, create file shares, issue temporary access through **SAS tokens**, and finally **revoke access** by rotating keys.

✅ **Key Features:**

* Create and configure a **Blob Container**.
* Upload and manage files with **Hot/Cold tiers** for cost optimization.
* Create and use **Azure File Shares** for collaboration.
* Generate **SAS Tokens** for time-limited, secure file sharing.
* Rotate **Access Keys** to revoke unauthorized or expired access.

🛠️ **Technologies Used:**

* **Azure Blob Storage**
* **Azure File Shares**
* **Shared Access Signatures (SAS)**
* **Access Keys & Key Rotation**
* **Azure Portal**

📖 **Read the full project:**
[📂 Azure Lock & Key: Controlling Storage Access](https://github.com/Sudaisib/Azure-Storage/blob/main/Azure%20Lock%20&%20Key:%20Controlling%20Storage%20Access/README.md)

---

## 📂 **Types of Storage Services**

Azure Storage offers multiple **data services** within a Storage Account. Each is designed for different use cases:

**🔹 Blob Storage** — For storing unstructured data like images, videos, documents, backups, or big data files. It’s highly scalable for petabyte-scale storage.

**🔹 File Storage** — Provides shared file storage accessible via SMB protocol. Great for lift-and-shift scenarios, shared drives, or legacy app migration.

**🔹 Queue Storage** — Offers reliable message queuing for large-scale distributed applications. Ideal for decoupling components and processing workloads asynchronously.

**🔹 Table Storage** — A NoSQL key-value store for semi-structured datasets, like user data or IoT logs. Cost-effective and scalable for massive datasets.

**🔹 Disk Storage** — Though not part of the standard Storage Account, Azure also offers managed disks for VM storage — optimized for OS disks, app data, and snapshots.

---

### 📊 **Comparison of Azure Storage Services**

| Storage Service   | Best For                     | Access Protocol | Data Type          | Example Use Cases                     |
| ----------------- | ---------------------------- | --------------- | ------------------ | ------------------------------------- |
| **Blob Storage**  | Unstructured data            | HTTP/HTTPS      | Text, binary       | Backups, images, videos, logs         |
| **File Storage**  | Shared file system           | SMB             | Files, folders     | File shares, lift-and-shift, app data |
| **Queue Storage** | Messaging between components | HTTP/HTTPS      | Messages           | Decoupled apps, order processing      |
| **Table Storage** | Structured NoSQL storage     | HTTP/HTTPS      | Key-value entities | User data, IoT telemetry              |
| **Disk Storage**  | VM block storage             | -               | OS/App disks       | Persistent disks for VMs              |

---

## 🚀 **Getting Started**

1️⃣ Clone this repository:

```bash
git clone https://github.com/<your-username>/azure-storage-projects.git
cd azure-storage-projects
```

2️⃣ Explore each project’s folder for **step-by-step guides** and resources.

3️⃣ Deploy resources using **Azure Portal**, **Azure CLI**, or **PowerShell**.

4️⃣ Remember to monitor your resources to avoid unnecessary costs.

---

## 🛠 **Technologies & Tools**

* **Microsoft Azure Portal**
* **Azure Resource Manager (ARM)**
* **Azure CLI**
* **Azure PowerShell**
* **Storage Explorer**
* **Azure Monitor**
* **RBAC and IAM**

---

## 🔐 **Security Best Practices**

* Enforce **HTTPS only** connections.
* Set **Minimum TLS version** to 1.2+.
* Use **RBAC** for granular access control.
* Disable shared keys when not needed.
* Enable **Activity Log** monitoring.
* Encrypt data at rest and in transit.

---

## 📈 **Monitoring & Cost Optimization**

* Use **Azure Cost Management + Billing** for spend tracking.
* Configure **Storage Lifecycle Management** rules to archive or delete stale data.
* Choose appropriate redundancy tiers (LRS, GRS, RA-GRS).
* Monitor **Activity Logs** for unusual access or changes.
* Delete unused blobs and containers.

---

## 📚 **Additional Resources & Learning**

* Explore **Azure Learning Paths** on Microsoft Learn.
* Try **Azure Sandbox** for free resource practice.
* Join **Azure Community Events** and user groups.
* Read **Azure Architecture Center** best practices.

---

## 📜 **Documentation & References**

* 📖 [Azure Storage Overview](https://learn.microsoft.com/en-us/azure/storage/common/storage-introduction)
* 📖 [Blob Storage Documentation](https://learn.microsoft.com/en-us/azure/storage/blobs/)
* 📖 [Azure CLI Storage Reference](https://learn.microsoft.com/en-us/cli/azure/storage)
* 📖 [Azure Architecture Center](https://learn.microsoft.com/en-us/azure/architecture/)

---

## 📩 **Contact Information**

📧 **Email:** [oladosuadeniyi39@gmail.com](mailto:oladosuadeniyi39@gmail.com)

🌐 **LinkedIn:** [Oladosu Ibrahim](https://www.linkedin.com/in/oladosu-ibrahim)

🐙 **GitHub:** [Sudaisib](https://github.com/Sudaisib)

---

## 📜 **License**

Licensed under the **MIT License** — feel free to fork, adapt, and share with credit.

---

## 🚀 **Thank You!**

Thank you for exploring this **Azure Storage Projects Portfolio** — may it serve as a valuable guide as you build, secure, and optimize your cloud storage solutions!

