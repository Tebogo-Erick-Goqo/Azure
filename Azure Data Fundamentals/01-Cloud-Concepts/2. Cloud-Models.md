# ☁️ Cloud Models

Cloud models describe **how cloud services are deployed** and **how much responsibility is shared between the cloud provider and the customer**.

There are two main categories to understand for AZ-900:

1. **Cloud Deployment Models**

   * Public Cloud
   * Private Cloud
   * Hybrid Cloud

2. **Cloud Service Models**

   * Infrastructure as a Service (IaaS)
   * Platform as a Service (PaaS)
   * Software as a Service (SaaS)

---

# 🌍 1. Cloud Deployment Models

Deployment models describe **where cloud infrastructure is hosted and who it is dedicated to**.

## ☁️ Public Cloud

A **public cloud** is a cloud environment provided by a cloud service provider.

The provider owns and manages the physical infrastructure, while customers consume the available services.

### Examples

* Microsoft Azure
* Amazon Web Services (AWS)
* Google Cloud

### 💻 Example I Can Relate To

If I build a **C# ASP.NET Core Web API**, I could deploy it to Microsoft Azure instead of purchasing and managing my own physical server.

```text
C# ASP.NET Core API
        ↓
     Azure
        ↓
    Internet
        ↓
      Users
```

Azure provides the cloud infrastructure needed to run my application.

### Remember

> **Public Cloud = Cloud infrastructure provided by a cloud provider.**

---

# 🏢 Private Cloud

A **private cloud** is a cloud environment dedicated to a single organisation.

The organisation has greater control over the environment, but may also have greater responsibility for managing it.

### 💻 Example I Can Relate To

Imagine a company has internal applications and databases that it wants to keep within its own controlled environment.

```text
Company
   │
   ├── Internal Network
   ├── Servers
   ├── Databases
   └── Private Cloud
```

The company can manage its own infrastructure and control who has access to it.

### Remember

> **Private Cloud = Cloud environment dedicated to one organisation.**

---

# 🔀 Hybrid Cloud

A **hybrid cloud** combines a private/on-premises environment with a public cloud environment.

This allows an organisation to keep some systems internally while using cloud services for other workloads.

### 💻 Example I Can Relate To

Imagine I have an application consisting of:

* C# / ASP.NET Core API
* React frontend
* SQL Server database

The company could keep its existing SQL Server database on-premises while hosting the application in Azure.

```text
          Company
             │
      ┌──────┴──────┐
      │             │
      ▼             ▼
 On-Premises       Azure
      │             │
 SQL Server     C# API / App
      │             │
      └──────┬──────┘
             │
           Users
```

This is a **hybrid cloud** because the organisation is using both on-premises/private infrastructure and public cloud services.

### Why use Hybrid Cloud?

A company may need to keep some systems on-premises because of:

* Existing infrastructure
* Legacy applications
* Security requirements
* Compliance requirements
* Data requirements
* Gradual cloud migration

### Remember

> **Hybrid Cloud = Public Cloud + Private/On-Premises environment.**

---

# 📊 Deployment Model Comparison

| Model             | Description                                                        | Example                                       |
| ----------------- | ------------------------------------------------------------------ | --------------------------------------------- |
| **Public Cloud**  | Cloud infrastructure provided by a cloud provider                  | Deploying a C# API to Azure                   |
| **Private Cloud** | Cloud environment dedicated to one organisation                    | Company's internal cloud                      |
| **Hybrid Cloud**  | Combination of public cloud and private/on-premises infrastructure | SQL Server on-premises + application in Azure |

---

# 🛠️ 2. Cloud Service Models

Cloud service models describe **how much of the technology stack the cloud provider manages**.

The three main service models are:

```text
IaaS
 ↓
PaaS
 ↓
SaaS
```

As we move from **IaaS → PaaS → SaaS**, the cloud provider manages more of the underlying infrastructure.

---

# 🖥️ IaaS — Infrastructure as a Service

**IaaS** provides the fundamental infrastructure required to run applications and systems.

This can include:

* Virtual machines
* Storage
* Networking
* Operating systems

The customer has more control but also more responsibility.

## 💻 Example I Can Relate To

Suppose I need to run a **C# application on a Windows Server**.

I could create an **Azure Virtual Machine**.

I would then be responsible for things such as:

* Operating system configuration
* Installing .NET
* Application configuration
* Application deployment
* Security configuration
* Updates and maintenance

```text
Azure
  │
  ▼
Virtual Machine
  │
  ├── Windows
  ├── .NET
  ├── C# Application
  └── Configuration
```

Azure provides the virtualised infrastructure, while I manage much of what runs on it.

### Remember

> **IaaS = I manage more.**

---

# ⚙️ PaaS — Platform as a Service

**PaaS** provides a managed platform for developing and running applications.

The cloud provider manages more of the underlying infrastructure, allowing developers to focus on their applications.

## 💻 Example I Can Relate To

Suppose I've developed an **ASP.NET Core Web API**.

Instead of creating a Virtual Machine and configuring the operating system myself, I could use **Azure App Service**.

```text
My C# / ASP.NET Core API
            ↓
      Azure App Service
            ↓
       Azure manages
      the infrastructure
```

I can focus more on:

* C# development
* REST APIs
* Application configuration
* Testing
* Deployment

while Azure handles more of the underlying platform.

### Remember

> **PaaS = I focus more on the application.**

---

# 📱 SaaS — Software as a Service

**SaaS** provides a complete software application over the internet.

The cloud provider manages the underlying infrastructure, platform, and application.

The customer mainly uses and configures the software.

## 💻 Example I Can Relate To

**SharePoint Online** is a useful example for me because I have worked with SharePoint and Microsoft technologies.

With SharePoint Online, I don't need to:

```text
Buy physical server
       ↓
Install Windows Server
       ↓
Install SharePoint
       ↓
Configure infrastructure
       ↓
Maintain physical hardware
```

Microsoft provides the service.

I can instead focus on:

* SharePoint sites
* Lists
* Libraries
* Permissions
* Power Apps
* Power Automate
* Business solutions

### Other Examples

* Microsoft Teams
* Microsoft 365
* Outlook Online

### Remember

> **SaaS = I use the software.**

---

# 🧱 IaaS vs PaaS vs SaaS

Think about running a **C# application**.

## IaaS

```text
Azure
 ↓
Virtual Machine
 ↓
Windows
 ↓
.NET
 ↓
C# Application
```

I manage more.

---

## PaaS

```text
Azure
 ↓
App Service
 ↓
C# Application
```

Azure manages more of the infrastructure.

---

## SaaS

```text
Microsoft
 ↓
Complete Application
 ↓
I use it
```

The provider manages almost everything.

---

# 📊 Responsibility Comparison

| Responsibility          | IaaS     | PaaS     | SaaS     |
| ----------------------- | -------- | -------- | -------- |
| Physical infrastructure | Provider | Provider | Provider |
| Networking              | Shared   | Provider | Provider |
| Operating system        | Customer | Provider | Provider |
| Runtime                 | Customer | Provider | Provider |
| Application             | Customer | Customer | Provider |
| Data                    | Customer | Customer | Customer |
| User access             | Customer | Customer | Customer |

### The Main Idea

```text
More Customer Responsibility
            ↑
            │
           IaaS
            │
           PaaS
            │
           SaaS
            │
            ↓
More Provider Responsibility
```

---

# 🧠 A Simple Way to Remember

Think about your own development experience.

### IaaS

> **"Give me the server. I'll handle the rest."**

Example:

**Azure Virtual Machine + C# application**

---

### PaaS

> **"Give me the platform. I'll build the application."**

Example:

**Azure App Service + ASP.NET Core API**

---

### SaaS

> **"Give me the software. I'll use it."**

Example:

**SharePoint Online / Microsoft 365**

---

# 🔄 Deployment vs Service Models

These two concepts are easy to confuse.

### Deployment Model

Answers:

> **Where is the cloud environment and who is it for?**

Examples:

* Public
* Private
* Hybrid

### Service Model

Answers:

> **How much does the cloud provider manage?**

Examples:

* IaaS
* PaaS
* SaaS

---

# 🎯 AZ-900 Exam Focus

Make sure you understand these questions:

### Which service model provides the most customer control?

**IaaS**

### Which service model provides a managed platform for applications?

**PaaS**

### Which service model provides complete software?

**SaaS**

### Which deployment model combines public and private/on-premises environments?

**Hybrid Cloud**

### Which deployment model is provided by cloud providers such as Azure?

**Public Cloud**

### A C# application is running on an Azure Virtual Machine. Which service model?

**IaaS**

### A C# ASP.NET Core application is hosted on Azure App Service. Which service model?

**PaaS**

### A user accesses SharePoint Online without managing the underlying servers. Which service model?

**SaaS**

---

# 📝 Quick Revision

```text
DEPLOYMENT MODELS

Public
→ Cloud provider infrastructure

Private
→ Dedicated to one organisation

Hybrid
→ Public + Private/On-Premises


SERVICE MODELS

IaaS
→ Infrastructure
→ More customer control

PaaS
→ Managed platform
→ Focus on applications

SaaS
→ Complete software
→ Mainly use/configure
```

---

# ⭐ Key Takeaway

The easiest way to understand the cloud service models is to think about **responsibility**.

> **IaaS:** I manage more infrastructure.

> **PaaS:** I focus on developing and running my application.

> **SaaS:** I mainly use the finished software.

For deployment models:

> **Public:** Cloud provider infrastructure.

> **Private:** Dedicated to one organisation.

> **Hybrid:** Combination of public cloud and private/on-premises infrastructure.

