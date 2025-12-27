
# 🌩️ Day-1: Introduction to Cloud Computing & Google Cloud Platform (GCP)

## 📌 What this session is about

* Fundamentals of **Cloud Computing**
* Why companies moved from **on-premise → cloud**
* Introduction to **Google Cloud Platform**
* Cloud types, core terminology, and GCP free tier

---

## 1️⃣ Life Before Cloud Computing (On-Premise Era)

### 🏢 Example: E-commerce Company (2010 – “Flip Zone”)

**Initial setup:**

* Application hosted on:

  * Personal laptops → ❌ not scalable
  * Physical servers in company-owned data centers

### 🚨 Problems with On-Prem Infrastructure

* ❌ Limited computing power
* ❌ Hard to scale during traffic spikes
* ❌ Requires full **System Admin + Networking + Security** teams
* ❌ Hardware failures = downtime
* ❌ Data center maintenance (power, cooling, security)

![Image](https://www.researchgate.net/publication/386059406/figure/fig1/AS%3A11431281292145430%401732384151900/A-High-Level-Infrastructure-Diagram-representation-of-an-on-prem-Data-Center.png)

![Image](https://www.veritis.com/wp-content/uploads/2019/03/cloud-vs-on-premise-it-infrastructure-model-of-your-choice-thumb-2.jpg)

---

## 2️⃣ The Biggest Pain: 💰 Cost Problem

### Why on-prem is expensive?

* Huge **upfront investment** (servers, racks, networking)
* Resources are **underutilized**

  * Example: Server used only 30–40% most of the time
* Scaling = buy more hardware (slow + costly)

➡️ **Paying for capacity you *might* need, not what you actually use**

---

## 3️⃣ Birth of Public Cloud ☁️

### What changed?

* Cloud providers (starting with **Amazon Web Services**) built **global data centers**
* Companies could **rent infrastructure**

### 🔑 Core Idea

> **Pay only for what you use**

### Benefits:

* ✅ No upfront hardware cost
* ✅ Scale up/down anytime
* ✅ No data center maintenance
* ✅ Faster innovation

![Image](https://www.tutorialspoint.com/cloud_computing/images/cloud_computing-public_cloud_model.jpg)

![Image](https://rms.softrax.com/wp-content/uploads/2023/10/Pros-and-Cons-PAYG-Pricing.png)

---

## 4️⃣ What is Cloud Computing?

### 📖 Definition

Cloud computing is a model where **compute, storage, and networking** are delivered as services over the internet, without owning physical hardware.

### You manage:

* Applications
* Data

### Cloud provider manages:

* Servers
* Networking
* Storage
* Security of data centers

---

## 5️⃣ Cloud Providers Overview

### Major Players

* **Amazon Web Services**
* **Microsoft Azure**
* **Google Cloud Platform**

### Important Insight

* Features are **almost similar**
* Real competition is on:

  * ⚡ Performance
  * 📈 Scalability
  * 🔐 Security
  * 🌍 Global reach

---

## 6️⃣ Why GCP? (GCP’s USP)

### 🔥 GCP Strengths

* High **performance & scalability**
* Same infrastructure that runs:

  * Gmail
  * YouTube
  * Google Search

### Why this matters?

* Proven at **internet scale**
* Designed for **massive traffic handling**

![Image](https://storage.googleapis.com/gweb-cloudblog-publish/images/infrastructure-3.max-2000x2000.png)

![Image](https://holori.com/wp-content/uploads/2024/06/GCP-regions-map.jpeg)

---

## 7️⃣ Types of Cloud Models

### ☁️ Public Cloud

* Infrastructure owned by provider
* Accessible to anyone
* Examples: AWS, Azure, GCP

### 🏢 Private Cloud (On-Prem)

* Company owns & manages everything
* Used by banks, government, healthcare
* High control, high cost

### 🔁 Hybrid Cloud

* Mix of public + private
* Sensitive data → private
* Non-critical workloads → public

![Image](https://media.geeksforgeeks.org/wp-content/uploads/20211123123930/Group2-660x330.jpg)

![Image](https://d1tzxux72fvryy.cloudfront.net/Mf353c7cb8bb15cdd874593eb21f472271720187176830/preview/Mf353c7cb8bb15cdd874593eb21f472271720187176830.png)

---

## 8️⃣ Creating a Free GCP Account

### Requirements

* Google account
* Visit 👉 `cloud.google.com`

### 🎁 Free Tier Benefits

* **$300 free credits**
* Limited free services, such as:

  * 1 E2-micro VM/month
  * 5 GB standard storage

⚠️ Exceed limits → charges apply

---

## 9️⃣ Cloud Shell 🖥️

### What is Cloud Shell?

* Browser-based terminal
* Pre-installed:

  * gcloud CLI
  * kubectl
  * terraform

### Benefits

* ❌ No local installation
* ✅ Instant access to GCP resources

![Image](https://docs.cloud.google.com/static/shell/docs/images/cloudshelltutorial.png)

![Image](https://cloud.google.com/static/shell/docs/images/launch-within-docs.png)

---

## 🔟 Essential Cloud Computing Terminology

### 🧩 Virtualization

* One physical server → multiple virtual machines
* Maximizes resource usage

![Image](https://www.dnsstuff.com/wp-content/uploads/2019/10/what-is-server-virtualization.png)

![Image](https://www.researchgate.net/profile/Andrei_Tchernykh/publication/333209316/figure/fig1/AS%3A776644243505153%401562177825090/The-architecture-of-the-virtual-machine-hypervisor-based-on-9.ppm)

### 🖥️ Virtual Machine (VM)

* Software-based computer
* Runs its own OS

---

### 🔌 API (Application Programming Interface)

* How programs talk to each other
* UI → Humans
* CLI → Commands
* API → Applications

---

### 🌍 Region

* Geographic area (e.g., Mumbai, Frankfurt)

### 🏢 Availability Zone (AZ)

* Multiple data centers inside a region
* Provides redundancy & fault isolation

![Image](https://dgtlinfra.com/wp-content/uploads/2023/10/Cloud-Regions-and-Availability-Zones-Example-Diagram.png)

![Image](https://dgtlinfra.com/wp-content/uploads/2023/10/Cloud-Regions-and-Availability-Zones-Example-Diagram.png.webp)

---

### 📈 Scalability

* Handle more requests when traffic increases

### 🎯 Elasticity

* Auto scale **up & down** based on demand

### ⚡ Agility

* Quickly adapt to changing requirements

---

### 🟢 High Availability

* System remains available even during failures

### 🛡️ Fault Tolerance

* System continues to work even if components fail

### 🔁 Disaster Recovery

* Backup & restore strategy after major outages

---

### ⚖️ Load Balancing

* Distributes traffic across multiple servers
* Prevents overload & improves performance

![Image](https://www.znetlive.com/blog/wp-content/uploads/2017/05/Load-Balancer-Diagram.png)

![Image](https://miro.medium.com/v2/resize%3Afit%3A1400/1%2AGb7hi5pqKmYYxEIUCJylHw.gif)

---

## ✅ Final Summary (1-Minute Revision)

* Cloud = **rent infrastructure**
* Pay-as-you-go model saves cost
* GCP excels in **performance & scalability**
* Understand **regions, zones, VM, scalability**
* Cloud Shell simplifies management


