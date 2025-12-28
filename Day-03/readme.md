# 🌩️ Day-3: GCP IAM (Identity & Access Management)

## 📌 What this session is about

* Understanding **GCP IAM** (most used GCP service)
* Difference between **Authentication vs Authorization**
* IAM components: **Identities, Roles, Permissions, Policies**
* How IAM fits into **GCP hierarchy**
* Hands-on IAM using **Console & Cloud Shell**

---

## 1️⃣ Context: Where IAM Fits in GCP

From previous days, you now know:

* **Day-1:** What cloud is & why GCP
* **Day-2:** GCP hierarchy
  (Organization → Folder → Project → Resource)

👉 **Day-3 answers an important question:**

> *Who can access these resources, and what exactly can they do?*

That responsibility belongs to **Google Cloud Platform IAM**.

---

## 2️⃣ What is GCP IAM?

### 📖 Definition

IAM stands for **Identity and Access Management**.

It controls:

* ✅ **Authentication** → *Who are you?*
* ✅ **Authorization** → *What are you allowed to do?*

### Why IAM is Critical

* It is the **most frequently used GCP service**
* Every action in GCP goes through IAM
* A single wrong permission can:

  * Delete production resources
  * Create huge billing impact
  * Cause security incidents

---

## 3️⃣ Real-Life Analogy: Bank Security System 🏦

### 🏢 Bank Areas

* **Help Desk** → Public area
* **Employee Bay** → Employees only
* **Bank Safe** → Highly restricted

![Image](https://help-iris.co.uk/education/financialsv6/projectfiles/images/users/user_groups_access_levels.png)

![Image](https://marvel-b1-cdn.bc0a.com/f00000000310757/www.fortinet.com/content/dam/fortinet/images/cyberglossary/authentication-vs-authorization-one-.jpg)

---

### 👮 Security Guard = Authentication

* Verifies identity:

  * Customer ID
  * Employee ID
  * Fingerprint
* Confirms *who you are*

➡️ This is **authentication**

---

### 🚪 Access Rules = Authorization

Even after entering the bank:

* **Customer** → Help desk only
* **Employee** → Help desk + employee bay
* **Manager** → All areas including safe

➡️ This is **authorization**

### 🔑 Key Insight

> Authentication lets you **enter**,
> Authorization decides **where you can go**.

👉 **Authorization is more important than authentication** in cloud security.

---

## 4️⃣ Mapping the Bank Analogy to GCP

### 🧩 Bank → GCP Mapping

| Bank Concept        | GCP Equivalent                                |
| ------------------- | --------------------------------------------- |
| Bank areas          | GCP services (Compute, GKE, Storage, Billing) |
| Security guard      | IAM service                                   |
| Customer / Employee | IAM identities                                |
| Access rules        | IAM roles & permissions                       |

![Image](https://images.ctfassets.net/w6r2i5d8q73s/7tAgPbiyGnz01PKJzWByz5/c4b4b47d2448da10e12988827a1f39be/GCP-diagramm-maker_hero_standard_sub-use-case_img_EN.png)

![Image](https://storage.googleapis.com/gweb-cloudblog-publish/images/2_Cloud_SQL_IAM.max-1500x1500.jpg)

---

## 5️⃣ Authentication in GCP (Who are you?)

### 👤 IAM Identities (Members)

IAM identifies *who* is making a request.

#### Types of Identities

1. **Users**

   * Real people
   * Example: `user@company.com`

2. **Groups**

   * Collection of users
   * Example:

     * `developers@company.com`
     * `devops@company.com`
   * ✅ Easier access management

3. **Service Accounts**

   * Used by applications & services
   * Example:

     * VM accessing Cloud Storage
   * GCP auto-creates default service accounts

4. **Domains**

   * Used for SSO & enterprise identity federation

---

## 6️⃣ Authorization in GCP (What can you do?)

### 🔐 Why Authorization is Dangerous if Misconfigured

Without proper authorization:

* Junior dev can:

  * Modify billing alerts
  * Create expensive clusters
  * Delete production workloads

👉 IAM **prevents accidents and misuse**

---

## 7️⃣ Core IAM Building Blocks (MOST IMPORTANT 🔥)

### 🧱 IAM Components

#### 1️⃣ Permissions (Lowest Level)

* Smallest unit of access
* Examples:

  * `compute.instances.create`
  * `storage.buckets.get`

➡️ Too granular to manage directly

---

#### 2️⃣ Roles (Collection of Permissions)

Roles bundle permissions together.

### Types of Roles

* **Predefined Roles**

  * Viewer
  * Editor
  * Owner

* **Custom Roles**

  * Create your own
  * Follow **least privilege principle**

![Image](https://framerusercontent.com/images/ylkmUQSc7oeeFhCibLPsY0oBGYM.png?height=1125\&width=2000)

![Image](https://storage.googleapis.com/gweb-cloudblog-publish/images/least-privilege-cloud-functions-blog-hero.max-2600x2600.png)

---

#### 3️⃣ Policies (The Glue)

A **policy** binds:

* **Who** → Identity
* **What** → Role (permissions)
* **Where** → Resource

📌 Core IAM formula:

```
WHO can do WHAT on WHICH resource
```

---

## 8️⃣ IAM and GCP Hierarchy (Inheritance Concept)

IAM can be applied at:

1. **Organization level**

   * Applies to all folders & projects

2. **Folder level**

   * Applies to projects inside the folder

3. **Project level**

   * Applies only to that project

![Image](https://docs.cloud.google.com/static/iam/img/policy-inheritance.svg)

![Image](https://docs.cloud.google.com/static/iam/img/resource-hierarchy-pubsub-1.svg)

⚠️ **Permissions flow downward (inheritance)**

---

## 9️⃣ Practical IAM – Using GCP Console

### 🔧 Steps Demonstrated

1. Create project: `day3-iam`
2. Go to:

   * **IAM & Admin → IAM**
3. Click **Grant Access**
4. Add user email
5. Assign role (e.g., Viewer)
6. Modify role if needed

### Custom Role Creation

* IAM & Admin → Roles
* Define:

  * Role name
  * Permissions

---

## 🔟 Practical IAM – Using Cloud Shell (CLI)

### Key Commands Used

* Create project
* Set active project
* Bind IAM role using:

  * `gcloud projects add-iam-policy-binding`

📌 Console = visual clarity
📌 CLI = automation & DevOps workflows

---

## 1️⃣1️⃣ Why IAM is the MOST USED GCP Service

Because:

* Every API call checks IAM
* Every service depends on IAM
* Every security model starts with IAM

👉 **No IAM = No Cloud Security**

---

## ✅ Final 1-Minute Revision

* IAM = Identity + Access control
* Authentication ≠ Authorization
* Identities → Roles → Permissions → Policies
* IAM follows GCP hierarchy
* Always follow **least privilege**
