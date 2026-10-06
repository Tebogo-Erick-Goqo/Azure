# 🔐 Shared Responsibility Model

The **Shared Responsibility Model** describes how security, management, and maintenance responsibilities are divided between the **cloud provider** and the **customer**.

The important idea is:

> **Moving to the cloud does not mean the cloud provider is responsible for everything.**

Some responsibilities remain with the customer.

The exact division depends on the cloud service being used.

---

# ☁️ What Does "Shared Responsibility" Mean?

When using Microsoft Azure, there are two parties:

```text
┌─────────────────────────────┐
│      Cloud Provider         │
│        Microsoft            │
└─────────────────────────────┘
              │
              │ Shared
              │ Responsibility
              ▼
┌─────────────────────────────┐
│          Customer           │
│        Organisation         │
└─────────────────────────────┘
```

Microsoft is responsible for the security and operation of the Azure infrastructure.

The customer is still responsible for things such as:

* Data
* User accounts
* Access permissions
* Application configuration
* Security settings
* Appropriate use of cloud resources

---

# 🏢 On-Premises vs Cloud

The easiest way to understand the model is to compare traditional on-premises infrastructure with cloud services.

## 🖥️ On-Premises

If a company runs its own physical servers, it may be responsible for almost everything.

```text
Organisation
     │
     ├── Physical Building
     ├── Physical Servers
     ├── Networking
     ├── Storage
     ├── Operating System
     ├── Applications
     ├── Data
     └── Security
```

The organisation has a large amount of responsibility.

---

# ☁️ Cloud

When the organisation moves infrastructure to Azure, Microsoft takes responsibility for the physical Azure infrastructure.

```text
Microsoft
     │
     ├── Physical Datacentres
     ├── Physical Servers
     ├── Physical Networking
     └── Physical Infrastructure

Customer
     │
     ├── Applications
     ├── Data
     ├── Users
     ├── Access
     └── Configuration
```

The responsibilities are shared.

---

# 🧱 The Responsibility Stack

A useful way to understand this is to think about the technology stack.

```text
┌─────────────────────────┐
│         Data            │ ← Customer
├─────────────────────────┤
│       Application       │ ← Customer
├─────────────────────────┤
│        Runtime          │
├─────────────────────────┤
│      Operating System   │
├─────────────────────────┤
│      Virtual Network    │
├─────────────────────────┤
│      Physical Hosts     │
├─────────────────────────┤
│      Physical Network   │
├─────────────────────────┤
│      Datacenter         │
└─────────────────────────┘
```

The amount of responsibility changes depending on whether we use **IaaS, PaaS, or SaaS**.

---

# 🖥️ IaaS Responsibility

With **Infrastructure as a Service**, the customer has more responsibility.

### Example I Can Relate To

Imagine I deploy my **C# application onto an Azure Virtual Machine**.

Microsoft provides the physical infrastructure and virtualisation.

I am responsible for more of the environment.

For example:

* Operating system
* Installing .NET
* Application configuration
* Application
* Data
* User access
* Security configuration
* Updates and patches for the OS, where applicable

```text
Microsoft
    │
    ├── Physical infrastructure
    ├── Datacenter
    └── Physical networking
           │
           ▼
Customer
    │
    ├── Windows
    ├── .NET
    ├── C# Application
    ├── Data
    └── Configuration
```

### Remember

> **IaaS = More customer responsibility.**

---

# ⚙️ PaaS Responsibility

With **Platform as a Service**, Microsoft manages more of the underlying environment.

### Example I Can Relate To

Suppose I deploy my **ASP.NET Core API to Azure App Service**.

I don't need to manage the underlying physical server or operating system in the same way I would with a Virtual Machine.

I focus more on:

* C# application
* API
* Application configuration
* Data
* Authentication and authorisation
* Application security
* User access

Microsoft manages more of the underlying platform.

```text
Microsoft
    │
    ├── Physical infrastructure
    ├── Networking
    ├── Operating system
    └── Managed platform
           │
           ▼
Customer
    │
    ├── C# API
    ├── Application configuration
    ├── Data
    └── Access
```

### Remember

> **PaaS = Provider manages more; customer focuses on the application.**

---

# 📱 SaaS Responsibility

With **Software as a Service**, the provider manages even more.

### Example I Can Relate To

Think about **SharePoint Online**.

Microsoft manages the underlying:

* Physical infrastructure
* Servers
* Networking
* Operating systems
* SharePoint platform

But the customer is still responsible for how the service is used.

For example:

* Users
* Permissions
* Access
* Data
* Site configuration
* Sharing settings
* Security configuration

```text
Microsoft
    │
    ├── Physical infrastructure
    ├── Operating system
    ├── Platform
    └── Application
           │
           ▼
Customer
    │
    ├── Users
    ├── Permissions
    ├── Data
    └── Configuration
```

### Remember

> **SaaS = Provider manages most of the technology; customer still manages how the software is used.**

---

# 📊 IaaS vs PaaS vs SaaS

The easiest way to understand the model is:

| Responsibility      | IaaS      | PaaS      | SaaS      |
| ------------------- | --------- | --------- | --------- |
| Physical datacenter | Microsoft | Microsoft | Microsoft |
| Physical network    | Microsoft | Microsoft | Microsoft |
| Physical servers    | Microsoft | Microsoft | Microsoft |
| Virtualisation      | Microsoft | Microsoft | Microsoft |
| Operating system    | Customer  | Microsoft | Microsoft |
| Runtime             | Customer  | Microsoft | Microsoft |
| Application         | Customer  | Customer  | Microsoft |
| Data                | Customer  | Customer  | Customer  |
| Users & access      | Customer  | Customer  | Customer  |

### Key pattern

```text
                 Customer Responsibility
                         ↓

IaaS  ████████████████████
PaaS  █████████████
SaaS  ███████

                         ↓
                 Provider Responsibility

IaaS  ███████
PaaS  █████████████
SaaS  ████████████████████
```

The more managed the service becomes, the more responsibility moves to the cloud provider.

---

# 🔐 Security Is Still Shared

One of the most important things to understand is:

> **Azure being secure does not automatically mean my application or data is secure.**

Microsoft can secure the underlying Azure infrastructure, but customers must configure their own resources correctly.

For example, Microsoft can provide a secure Azure environment, but I could still make a mistake by:

* Giving the wrong user too many permissions
* Exposing sensitive data
* Using weak authentication
* Misconfiguring a network
* Storing secrets insecurely
* Giving an application unnecessary access

---

# 👤 Example: Azure Application

Imagine I build a C# API and deploy it to Azure.

Microsoft is responsible for securing the underlying Azure infrastructure.

I am responsible for things such as:

```text
My C# Application
       │
       ├── Authentication
       ├── Authorisation
       ├── User permissions
       ├── Application security
       ├── Data
       ├── API configuration
       └── Secrets
```

If I accidentally expose a sensitive API endpoint, I cannot simply say:

> "Azure should have secured it."

The application and its configuration are still my responsibility.

---

# 🧪 Example From Software Testing

The Shared Responsibility Model is also relevant to **software testing and QA**.

Imagine I'm testing a C# application hosted in Azure.

I might test:

* Authentication
* Authorisation
* User permissions
* Application functionality
* API responses
* Input validation
* Error handling
* Data access
* Security-related behaviour

Microsoft is responsible for the underlying Azure infrastructure, but I still need to test whether **my application is behaving securely and correctly**.

This is particularly important when working with applications in regulated environments.

---

# 🔑 Identity and Access

A major customer responsibility is controlling **who can access Azure resources and applications**.

For example, Microsoft Entra ID can be used to manage identities.

Azure RBAC can control what users and services can do.

```text
User
  │
  ▼
Microsoft Entra ID
  │
  ▼
Authentication
  │
  ▼
Azure RBAC
  │
  ▼
Permissions
  │
  ▼
Azure Resource
```

The cloud provider provides these tools, but the organisation must configure them correctly.

---

# 🗄️ Example: Azure SQL

Suppose I use **Azure SQL Database** for an application.

Microsoft manages much of the underlying infrastructure and database platform.

However, I still need to think about:

* Who can access the database
* What permissions users have
* What data is stored
* Application authentication
* Database configuration
* Data protection
* Queries and application behaviour

### Example

My application:

```text
React
   ↓
ASP.NET Core API
   ↓
Azure SQL Database
```

Microsoft manages the underlying Azure SQL service.

I still need to make sure my application doesn't give every user unrestricted access to the database.

---

# 🧠 A Real-World Analogy

Think about renting a secure apartment.

The building owner is responsible for things like:

* Building structure
* Electricity infrastructure
* Common areas
* Security systems

But I am still responsible for:

* Locking my door
* Who I allow inside
* My belongings
* How I use the apartment

Cloud computing works similarly.

> **The provider secures the cloud infrastructure. The customer is responsible for securing what they put in and how they configure it.**

---

# 🎯 AZ-900 Exam Focus

You should understand that:

### Microsoft is generally responsible for:

* Physical datacentres
* Physical servers
* Physical networking
* Physical security
* Underlying Azure infrastructure

### The customer is generally responsible for:

* Data
* User accounts
* Access permissions
* Identity
* Application configuration
* Application security
* Correct resource configuration

The exact division changes depending on the service model.

---

# ❓ Quick AZ-900 Questions

### Who is responsible for physical datacentres in Azure?

**Microsoft**

---

### Who is responsible for the customer's data?

**The customer**

---

### Who is responsible for configuring user permissions?

**The customer**

---

### Who is responsible for the physical Azure servers?

**Microsoft**

---

### Who is responsible for securing a customer's C# application's authentication?

**The customer**

---

### Does moving an application to Azure mean Microsoft is responsible for everything?

**No.**

The customer still has responsibilities.

---

# 📝 Quick Revision

```text
SHARED RESPONSIBILITY

Microsoft
    │
    ├── Physical datacentres
    ├── Physical servers
    ├── Physical networking
    └── Azure infrastructure
          │
          │
          ▼
      CUSTOMER
          │
          ├── Data
          ├── Users
          ├── Permissions
          ├── Applications
          └── Configuration
```

### Service Model Relationship

```text
IaaS
↓
Customer manages more

PaaS
↓
Responsibilities are shared differently

SaaS
↓
Provider manages more
Customer still controls data,
users and access
```

---

# ⭐ Key Takeaway

> **Cloud security and management are shared responsibilities.**

The cloud provider is responsible for the security and operation of the underlying cloud infrastructure.

The customer remains responsible for things such as **data, identities, access, applications, and configuration**.

The more managed the service is:

**IaaS → PaaS → SaaS**

the more responsibility generally moves from the customer to the cloud provider.

However:

> **The customer never simply gives up all responsibility by moving to the cloud.**

