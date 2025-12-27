# 🌩️ Day-2: GCP Hierarchy & Cost Management

## 📌 What this session is about

* Why **hierarchy is critical** in cloud
* Understanding **GCP resource hierarchy**
* How GCP helps in **cost visibility & optimization**
* Projects, billing accounts & budget alerts

---

## 1️⃣ Quick Recap of Day-1

* What is cloud computing
* Why cloud > traditional IT
* Why choose **Google Cloud Platform**
* GCP free account & Cloud Shell
* Basic cloud terminology

---

## 2️⃣ Why Do We Need Hierarchy in Cloud?

### 🏢 Problem in Traditional IT

* All applications run on:

  * Same servers
  * Same data center
* ❌ No clear cost breakdown:

  * Which team is spending how much?
  * Which service is costly?
* ❌ Cost optimization becomes guesswork

### 🔍 Result

* Poor **cost visibility**
* Wasted infrastructure
* Hard to scale responsibly

![Image](https://www.nutanix.com/theforecastbynutanix/business/cto-guide-to-cost-savings-in-hci-vs-traditional-it-infrastructure/_jcr_content/root/container/componentContainer/container_basic_3826/componentContainer/image_2091778944.coreimg.png/1604519488558/img-cost-reduction.png)

![Image](https://mainstreetitsolutions.com/wp-content/uploads/2025/06/Comparing-On-Premises-Servers.jpg)

---

## 3️⃣ How Cloud Solves This Problem

### 💡 Cloud Advantage

Cloud platforms introduce **structured hierarchy** to:

* Track costs **per team**
* Track costs **per service**
* Optimize spending **intelligently**

### 🎯 Key Outcomes

* ✅ Cost visibility
* ✅ Cost optimization
* ✅ Accountability per team/service

---

## 4️⃣ GCP Resource Hierarchy (Very Important 🔥)

### 🧱 GCP Hierarchy Levels

1. **Organization**
2. **Folders**
3. **Projects**
4. **Resources**

![Image](https://d33wubrfki0l68.cloudfront.net/eaddeba5e864fe63444fe247f7a7277b427e42c2/ed88b/gcpimages/02-architecture/resource-hierarchy-overview.png)

![Image](https://docs.cloud.google.com/static/resource-manager/img/cloud-hierarchy.svg)

---

## 5️⃣ Organization (Top Level)

### 📌 What is an Organization?

* Represents a **company’s cloud identity**
* Root node of GCP hierarchy

### 🏢 How it is created?

* Through **Google Workspace** (not Gmail)
* Uses company domain:

  * `user@company.com`

### 👨‍💼 Real-World Setup

* Management creates admin account:

  * `googlecloudadmin@company.com`
* Cloud engineers configure hierarchy under this

⚠️ **Free GCP accounts cannot create organizations**

---

## 6️⃣ Folders (Environment Isolation)

### 📂 Purpose of Folders

* Logical grouping
* Mostly used for **environments**

### Common Folder Structure

* `dev`
* `staging`
* `production`

### Benefits

* ✅ Clear separation
* ✅ Cost isolation per environment
* ✅ Better access control

![Image](https://docs.cloud.google.com/resource-manager/img/cloud-hierarchy.svg)

![Image](https://images.surferseo.art/851bcb3d-3d1a-41b5-89a4-7d48ecdc89ec.png)

---

## 7️⃣ Projects (Team / Service Level)

### 📦 What is a Project?

* Container where **actual work happens**
* Belongs inside a folder (or directly under org)

### Examples

* `payments-dev`
* `ui-prod`
* `orders-staging`

### Why Projects Matter

* Billing is attached **at project level**
* Permissions are managed **per project**

⚠️ **Free tier users can create projects directly (no org/folder)**

---

## 8️⃣ Resources (Actual GCP Services)

### 🔧 What are Resources?

* Compute Engine (VMs)
* Cloud Storage
* Databases
* Load Balancers
* Networking components

📌 **Resources always live inside projects**

---

## 9️⃣ Enabling APIs in GCP

### ⚠️ Important Concept

> You **cannot use a service** unless its API is enabled.

### Example

To create a VM:

* Enable **Compute Engine API**

### Ways to Enable APIs

* GCP Console (UI)
* Cloud Shell using `gcloud` commands

![Image](https://i.sstatic.net/E8niR.png)

![Image](https://lucidgen.com/wp-content/uploads/2022/11/how-to-enable-api-in-google-cloud-1.png)

---

## 🔟 Billing Accounts in GCP

### 💳 Free Trial Billing

* Auto-created
* Tracks usage of free credits

### 🏢 Organization Billing

* **Paid billing account**
* Can be linked to:

  * Multiple projects

### Key Capabilities

* Attach billing to projects
* Detach billing (stop charges)

![Image](https://docs.cloud.google.com/static/billing/docs/images/resource-hierarchy-overview.png)

![Image](https://docs.cloud.google.com/static/billing/docs/images/subaccounts.png)

---

## 1️⃣1️⃣ Budget & Billing Alerts (VERY IMPORTANT 🔔)

### 🎯 Why Budget Alerts?

* Prevent accidental overspending
* Protect beginners & learning accounts

### Example Budget

* Name: `payments-budget`
* Period: Monthly

### Alert Thresholds

* 50%
* 90%
* 100%
  (based on actual or forecasted spend)

### Notifications

* Email alerts when limits are crossed

![Image](https://support.terra.bio/hc/article_attachments/360087680792)

![Image](https://miro.medium.com/v2/resize%3Afit%3A1400/0%2AJG5e8C_pdkO_BuYt.png)

---

## 1️⃣2️⃣ Why GCP Billing Is Better Than Traditional IT

### Traditional IT

* Pay first
* No visibility
* No granular control

### Cloud (GCP)

* See cost per:

  * Project
  * Environment
  * Team
* Discuss & resize resources
* Optimize continuously

---

## ✅ Final 1-Minute Revision

* GCP hierarchy = **cost control**
* Org → Folder → Project → Resource
* Billing attached at **project level**
* APIs must be enabled before using services
* Budget alerts prevent surprises 💰
