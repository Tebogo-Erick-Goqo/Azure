# ☁️ Cloud Computing

## 📌 What is Cloud Computing?

**Cloud computing** is the delivery of computing services over the internet instead of relying only on local physical infrastructure.

These services can include:

* 🖥️ Compute
* 💾 Storage
* 🗄️ Databases
* 🌐 Networking
* 🔐 Security
* 📊 Analytics
* 🤖 Artificial Intelligence
* ⚙️ Applications

Instead of an organisation purchasing and maintaining all the required physical hardware, it can use resources provided by a cloud provider such as **Microsoft Azure**.

---

## ☁️ What is Microsoft Azure?

**Microsoft Azure** is Microsoft's cloud computing platform.

Azure provides a large collection of cloud services that organisations can use to build, deploy, manage, and scale applications and infrastructure.

Examples include:

* Azure Virtual Machines
* Azure App Service
* Azure Functions
* Azure Storage
* Azure SQL Database
* Azure Virtual Network
* Microsoft Entra ID
* Azure Monitor

---

# 🏢 Traditional IT vs Cloud Computing

## Traditional On-Premises Infrastructure

An organisation purchases and manages its own infrastructure.

```text
Organisation
     │
     ├── Physical Servers
     ├── Storage
     ├── Networking
     ├── Data Centre
     ├── Electricity
     ├── Cooling
     └── IT Maintenance
```

The organisation is responsible for purchasing, maintaining, securing, and replacing the infrastructure.

---

## Cloud Computing

The organisation consumes infrastructure and services from a cloud provider.

```text
Organisation
      │
      │ Internet
      ▼
Cloud Provider
      │
      ├── Compute
      ├── Storage
      ├── Networking
      ├── Databases
      └── Other Cloud Services
```

The cloud provider manages much of the underlying physical infrastructure.

---

# 💰 Capital Expenditure vs Operational Expenditure

Cloud computing changes how organisations can spend money on IT infrastructure.

## CapEx — Capital Expenditure

**CapEx** is spending money upfront to purchase physical assets.

Examples:

* Buying servers
* Purchasing networking equipment
* Building a data centre
* Buying storage hardware

### Example

An organisation spends **R1,000,000** building and equipping a server room.

That is a capital investment.

---

## OpEx — Operational Expenditure

**OpEx** is spending money on services and resources as they are used.

Examples:

* Cloud services
* Electricity
* Software subscriptions
* Maintenance services

Cloud computing often allows organisations to move from large upfront infrastructure costs toward an operational, consumption-based model.

---

# 🔄 Consumption-Based Model

A **consumption-based model** means that customers generally pay for the cloud resources they consume.

Instead of purchasing a physical server upfront, an organisation can provision cloud resources and pay according to its usage and pricing agreement.

### Simple Example

```text
Traditional IT

Buy Server
     ↓
Pay Upfront
     ↓
Own Hardware
     ↓
Maintain Hardware


Cloud

Provision Resource
     ↓
Use Resource
     ↓
Pay According to Usage
     ↓
Scale When Required
```

---

# 🧑‍💻 Cloud Service Models

Cloud services are commonly divided into three main service models:

* **IaaS**
* **PaaS**
* **SaaS**

These models determine how much responsibility belongs to the customer and how much is handled by the cloud provider.

---

## 🖥️ IaaS — Infrastructure as a Service

**IaaS** provides virtualised infrastructure such as:

* Virtual machines
* Storage
* Networking
* Operating systems

The customer has more control but also more responsibility.

### Azure Example

**Azure Virtual Machines**

### Easy way to remember

> **IaaS = I manage more.**

---

## ⚙️ PaaS — Platform as a Service

**PaaS** provides a managed platform for developing and running applications.

The cloud provider manages more of the underlying infrastructure.

The developer can focus more on the application rather than managing servers.

### Azure Examples

* Azure App Service
* Azure Functions
* Azure SQL Database

### Easy way to remember

> **PaaS = I focus on the application.**

---

## 📱 SaaS — Software as a Service

**SaaS** provides complete software applications over the internet.

The customer generally uses the application without managing the underlying infrastructure.

### Examples

* Microsoft 365
* Microsoft Teams
* Outlook.com

### Easy way to remember

> **SaaS = I use the software.**

---

# 📊 IaaS vs PaaS vs SaaS

| Model    | Customer Responsibility                  | Example                |
| -------- | ---------------------------------------- | ---------------------- |
| **IaaS** | More control over infrastructure and OS  | Azure Virtual Machines |
| **PaaS** | Focus mainly on application development  | Azure App Service      |
| **SaaS** | Mainly use and configure the application | Microsoft 365          |

### Responsibility

```text
More Customer Responsibility
            │
            ▼
          IaaS
            │
          PaaS
            │
          SaaS
            │
            ▼
More Provider Responsibility
```

---

# 🌍 Cloud Deployment Models

Cloud environments can also be classified according to how the infrastructure is deployed.

## ☁️ Public Cloud

Cloud infrastructure is provided by a cloud provider and made available to customers over the internet.

### Examples

* Microsoft Azure
* Amazon Web Services
* Google Cloud

---

## 🏢 Private Cloud

Cloud infrastructure is dedicated to a single organisation.

The organisation has greater control over the environment but may have more responsibility for managing the infrastructure.

---

## 🔀 Hybrid Cloud

A **hybrid cloud** combines private and public cloud environments.

For example:

```text
Organisation's
Private Environment
        │
        │
        ▼
   Hybrid Cloud
        ▲
        │
        │
   Microsoft Azure
   Public Cloud
```

An organisation might keep certain systems on-premises while using Azure for other workloads.

---

# 🧠 Key Terms to Remember

| Term                        | Meaning                                                  |
| --------------------------- | -------------------------------------------------------- |
| **Cloud Computing**         | Delivery of computing services over the internet         |
| **Azure**                   | Microsoft's cloud computing platform                     |
| **CapEx**                   | Upfront spending on physical assets                      |
| **OpEx**                    | Ongoing operational spending                             |
| **Consumption-Based Model** | Pay based on cloud resources/services consumed           |
| **IaaS**                    | Infrastructure as a Service                              |
| **PaaS**                    | Platform as a Service                                    |
| **SaaS**                    | Software as a Service                                    |
| **Public Cloud**            | Cloud infrastructure provided to customers by a provider |
| **Private Cloud**           | Cloud environment dedicated to one organisation          |
| **Hybrid Cloud**            | Combination of public and private cloud environments     |

---

# 🎯 AZ-900 Exam Focus

Make sure you can explain:

* What cloud computing is
* What Microsoft Azure is
* The difference between CapEx and OpEx
* The consumption-based model
* IaaS vs PaaS vs SaaS
* Public vs Private vs Hybrid cloud
* Who has responsibility in each service model
* Why organisations use cloud computing

---

# 📝 Quick Revision

### What is cloud computing?

> The delivery of computing services over the internet.

### What is IaaS?

> Infrastructure as a Service — provides infrastructure such as virtual machines, storage, and networking.

### What is PaaS?

> Platform as a Service — provides a managed platform for developing and running applications.

### What is SaaS?

> Software as a Service — provides complete software applications over the internet.

### What is a hybrid cloud?

> A combination of public and private cloud environments.

### What is CapEx?

> Upfront investment in physical infrastructure and assets.

### What is OpEx?

> Ongoing operational spending for services and resources.

### What is the consumption-based model?

> Paying for cloud resources according to usage or the applicable pricing model.

---

## ⭐ Key Takeaway

```text
Cloud Computing
      │
      ├── Service Models
      │      ├── IaaS
      │      ├── PaaS
      │      └── SaaS
      │
      ├── Deployment Models
      │      ├── Public
      │      ├── Private
      │      └── Hybrid
      │
      └── Financial Models
             ├── CapEx
             └── OpEx
```

**Core idea:**

> Cloud computing allows organisations to consume computing resources and services without having to own and manage all the underlying physical infrastructure themselves.

ivate infrastructure.

