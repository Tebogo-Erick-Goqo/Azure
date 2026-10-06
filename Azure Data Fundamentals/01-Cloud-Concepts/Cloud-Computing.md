# ☁️ Cloud Models

Cloud models describe **how cloud services are provided** and **how much responsibility the customer has versus the cloud provider**.

There are two important groups of cloud models to understand:

1. **Cloud deployment models**

   * Public Cloud
   * Private Cloud
   * Hybrid Cloud

2. **Cloud service models**

   * IaaS
   * PaaS
   * SaaS

---

# 1. 🌍 Cloud Deployment Models

Deployment models describe **where the cloud infrastructure is hosted and who has access to it**.

---

## ☁️ Public Cloud

A **public cloud** is a cloud environment where infrastructure and services are provided by a cloud provider.

Examples of major public cloud providers include:

* Microsoft Azure
* Amazon Web Services (AWS)
* Google Cloud

The cloud provider owns and manages the underlying physical infrastructure.

### 🧑🏾‍💻 Example I Can Relate To

Imagine I build a **C# ASP.NET Core Web API**.

Instead of buying a physical server and installing Windows Server, .NET, networking equipment, etc., I could deploy the API to **Microsoft Azure**.

```text
My C# API
    ↓
Azure
    ↓
Internet
    ↓
Users
```

Azure provides the infrastructure needed to run the application.

I don't need to own the physical server.

### Easy way to remember

> **Public Cloud = Provider owns the infrastructure, I consume the services.**

---

# 🏢 Private Cloud

A **private cloud** is a cloud environment dedicated to a single organisation.

The infrastructure isn't shared with other organisations in the same way as a public cloud environment.

An organisation may have more control over the environment, but it can also have more responsibility for managing it.

### 🧑🏾‍💻 Example I Can Relate To

Imagine a company has internal applications containing sensitive business information.

Instead of putting everything into a public cloud environment, the company could operate a private cloud environment within its own infrastructure.

For example:

```text
Company
   │
   ├── Internal Servers
   ├── Internal Database
   ├── Internal Network
   └── Private Cloud
```

As someone with **IT support, development and testing experience**, you can think of this as an environment where the organisation has much more direct control over the infrastructure.

### Easy way to remember

> **Private Cloud = Cloud environment dedicated to one organisation.**

---

# 🔀 Hybrid Cloud

A **hybrid cloud** combines **private/on-premises infrastructure with public cloud services**.

This allows an organisation to keep some workloads internally while using cloud services for others.

### 🧑🏾‍💻 Example I Can Relate To

Imagine I'm working on an application with:

* A C# backend
* SQL Server
* React frontend

The company might keep its existing SQL Server database on-premises but host the application in Azure.

```text
             Company
                │
        ┌───────┴───────┐
        │               │
        ▼               ▼
 On-Premises          Azure
        │               │
    SQL Server     C# API / App
        │               │
        └───────┬───────┘
                │
             Users
```

This is a **hybrid environment** because part of the solution is on-premises and part is in the public cloud.

### Why might a company do this?

Maybe the company already has:

* Existing databases
* Legacy applications
* Internal infrastructure
* Security requirements
* Systems that aren't ready to move to the cloud

It can gradually introduce Azure without moving everything at once.

### Easy way to remember

> **Hybrid = Some things stay here, some things move to the cloud.**

---

# 📊 Deployment Model Comparison

| Model             | Infrastructure                | Example I Can Relate To                  |
| ----------------- | ----------------------------- | ---------------------------------------- |
| **Public Cloud**  | Cloud provider                | Deploying a C# API to Azure              |
| **Private Cloud** | Dedicated to one organisation | Company's internal cloud infrastructure  |
| **Hybrid Cloud**  | Combination of environments   | SQL Server on-premises + C# API in Azure |

---

# 2. 🛠️ Cloud Service Models

Service models describe **how much of the technology stack the cloud provider manages**.

The three main models are:

```text
IaaS
 ↓
PaaS
 ↓
SaaS
```

As we move from **IaaS → PaaS → SaaS**, the cloud provider manages more for us.

---

# 🖥️ IaaS — Infrastructure as a Service

**IaaS** provides the basic infrastructure needed to run systems.

This can include:

* Virtual machines
* Storage
* Networking
* Operating systems

The customer has significant control over the environment.

---

## 🧑🏾‍💻 Example I Can Relate To

Imagine I need to run a **C# application on a Windows Server**.

I could create an **Azure Virtual Machine**.

I would have to deal with things such as:

* Operating system
* Installing .NET
* Application configuration
* Updates
* Security configuration
* Application deployment

Azure provides the virtualised infrastructure, but I still manage much of the environment.

```text
Azure
 │
 └── Virtual Machine
       │
       ├── Windows
       ├── .NET
       ├── C# Application
       └── Configuration
```

### Easy way to remember

> **IaaS = I get the infrastructure and manage more myself.**

---

# ⚙️ PaaS — Platform as a Service

**PaaS** provides a managed platform for developing and running applications.

The cloud provider handles more of the infrastructure.

This allows developers to focus more on their applications.

---

## 🧑🏾‍💻 Example I Can Relate To

Imagine I've built an **ASP.NET Core Web API**.

Instead of creating a Virtual Machine and configuring the operating system myself, I could use **Azure App Service**.

```text
My responsibility
       │
       ▼
C# / ASP.NET Core API
       │
       ▼
Azure App Service
       │
       ▼
Azure manages more
of the infrastructure
```

I can focus on:

* C# code
* APIs
* Application configuration
* Deployment
* Testing

while Azure handles much of the underlying platform infrastructure.

### Another example

Because I work with **Power Apps and Power Automate**, I can think about PaaS as the idea of using a managed platform where I focus on building the solution rather than maintaining the underlying servers.

### Easy way to remember

> **PaaS = Platform is managed for me; I focus on building the application.**

---

# 📱 SaaS — Software as a Service

**SaaS** provides a complete software application to the user.

The provider manages almost everything underneath the application.

The user mainly:

* Uses the application
* Configures available settings
* Manages their own data/access where applicable

---

## 🧑🏾‍💻 Example I Can Relate To

A good example is **Microsoft 365**.

When I use applications such as:

* Outlook
* Microsoft Teams
* SharePoint Online

I don't manage the underlying:

* Physical servers
* Operating systems
* Network infrastructure
* Application servers

Microsoft manages that infrastructure.

I simply use and configure the software.

### SharePoint Example

Since I've worked with **SharePoint**, this is an especially useful example.

With **SharePoint Online**, I don't need to:

```text
Buy Server
   ↓
Install Windows Server
   ↓
Install SharePoint
   ↓
Configure infrastructure
   ↓
Maintain physical server
```

Microsoft provides the service.

I can instead focus on things like:

* Sites
* Lists
* Libraries
* Permissions
* Power Automate
* Power Apps
* Business solutions

### Easy way to remember

> **SaaS = I use the software; the provider manages the platform underneath it.**

---

# 🧱 IaaS vs PaaS vs SaaS

Think about building and running a **C# application**.

### IaaS

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

I manage a lot.

---

### PaaS

```text
Azure
 ↓
App Service
 ↓
C# Application
```

Azure manages more of the infrastructure.

I focus more on my application.

---

### SaaS

```text
Microsoft
 ↓
Complete Application
 ↓
I use it
```

I mainly use the finished software.

---

# 📊 Responsibility Comparison

| Area                    | IaaS                         | PaaS              | SaaS                              |
| ----------------------- | ---------------------------- | ----------------- | --------------------------------- |
| Physical infrastructure | Microsoft                    | Microsoft         | Microsoft                         |
| Networking              | More customer responsibility | Mostly provider   | Provider                          |
| Operating system        | Customer                     | Provider          | Provider                          |
| Runtime                 | Customer                     | Provider          | Provider                          |
| Application             | Customer                     | Customer          | Provider                          |
| Data                    | Customer                     | Customer          | Customer                          |
| User access             | Customer                     | Customer          | Customer                          |
| Example                 | Azure VM                     | Azure App Service | SharePoint Online / Microsoft 365 |

The important idea is:

> **The further we move from IaaS → PaaS → SaaS, the more the cloud provider manages.**

---

# 🧠 A Simple Way to Remember the Models

Think about your own development experience.

### IaaS

**"Give me the server. I'll handle the rest."**

Example:

> Azure Virtual Machine + my C# application.

### PaaS

**"Give me a platform. I'll build my application."**

Example:

> Azure App Service + my ASP.NET Core API.

### SaaS

**"Give me the software. I'll use it."**

Example:

> SharePoint Online / Microsoft 365.

---

# 🎯 AZ-900 Exam Focus

Make sure you can answer these questions:

### Which model gives you the most control?

**IaaS**

---

### Which model lets developers focus more on applications?

**PaaS**

---

### Which model provides a complete application?

**SaaS**

---

### Which deployment model combines on-premises and public cloud?

**Hybrid Cloud**

---

### Which deployment model is provided by cloud providers such as Azure?

**Public Cloud**

---

### If I deploy a C# API to an Azure Virtual Machine, what service model is this?

**IaaS**

---

### If I deploy my C# API using Azure App Service, what service model is this?

**PaaS**

---

### If I use SharePoint Online without managing the underlying servers, what model does this represent?

**SaaS**

---

# 🔑 Quick Revision

```text
DEPLOYMENT MODELS

Public
  ↓
Provider's cloud

Private
  ↓
Dedicated to one organisation

Hybrid
  ↓
Public + Private/On-Premises


SERVICE MODELS

IaaS
  ↓
More control
More responsibility

PaaS
  ↓
Managed platform
Focus on application

SaaS
  ↓
Complete software
Mostly just use/configure
```

---

# ⭐ Key Takeaway

The easiest way for me to understand cloud models is to think about **how much I am responsible for**.

```text
                    CUSTOMER RESPONSIBILITY
                           ↑
                           │
                         IaaS
                           │
                         PaaS
                           │
                         SaaS
                           │
                           ↓
                    PROVIDER RESPONSIBILITY
```

**IaaS:** I manage more infrastructure.

**PaaS:** I focus on developing and running my application.

**SaaS:** I mainly use the finished software.

For deployment models:

**Public:** Cloud provider infrastructure.

**Private:** Dedicated cloud environment.

**Hybrid:** Combination of cloud and on-premises/private infrastructure.

