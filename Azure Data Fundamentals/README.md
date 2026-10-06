# ☁️ Azure Fundamentals (AZ-900) Notes

Welcome to my **Microsoft Azure Fundamentals (AZ-900)** study repository.

This repository contains my personal notes, concepts, examples, and revision material as I build my understanding of **Microsoft Azure cloud services** and prepare for the **AZ-900: Microsoft Azure Fundamentals** certification.

The goal of this repository is to document my learning journey and create a practical reference that I can use for revision and future Azure development work.

---

## 📚 What You'll Find Here

This repository covers the core concepts included in the Azure Fundamentals learning path:

* ☁️ Cloud Computing Fundamentals
* 🌐 Microsoft Azure Fundamentals
* 🏗️ Azure Architecture and Services
* 💰 Azure Management and Governance
* 🔐 Azure Security
* 💳 Azure Pricing and Cost Management
* 📊 Azure Monitoring and Management
* 🗄️ Azure Storage
* 🖥️ Azure Compute
* 🌎 Azure Networking
* 🗃️ Azure Databases
* 🔄 Azure Integration Services
* 🤖 Azure AI and Machine Learning Fundamentals
* 🧰 Azure Management Tools
* 📝 AZ-900 Revision Notes

---

# 🗂️ Repository Structure

```text
Azure-Fundamentals/
│
├── README.md
│
├── 01-Cloud-Concepts/
│   ├── Cloud-Computing.md
│   ├── Cloud-Models.md
│   ├── Shared-Responsibility.md
│   └── Cloud-Benefits.md
│
├── 02-Azure-Architecture/
│   ├── Azure-Regions.md
│   ├── Availability-Zones.md
│   ├── Resource-Groups.md
│   ├── Subscriptions.md
│   └── Management-Groups.md
│
├── 03-Azure-Compute/
│   ├── Virtual-Machines.md
│   ├── Virtual-Machine-Scale-Sets.md
│   ├── App-Service.md
│   ├── Containers.md
│   └── Azure-Functions.md
│
├── 04-Azure-Networking/
│   ├── Virtual-Networks.md
│   ├── VPN.md
│   ├── ExpressRoute.md
│   ├── Load-Balancer.md
│   ├── Application-Gateway.md
│   └── Azure-DNS.md
│
├── 05-Azure-Storage/
│   ├── Storage-Accounts.md
│   ├── Blob-Storage.md
│   ├── File-Storage.md
│   ├── Queue-Storage.md
│   └── Disk-Storage.md
│
├── 06-Azure-Databases/
│   ├── Azure-SQL.md
│   ├── Cosmos-DB.md
│   └── Database-Concepts.md
│
├── 07-Azure-Security/
│   ├── Microsoft-Defender-for-Cloud.md
│   ├── Microsoft-Sentinel.md
│   ├── Azure-Key-Vault.md
│   ├── Microsoft-Entra-ID.md
│   └── RBAC.md
│
├── 08-Azure-Management/
│   ├── Azure-Portal.md
│   ├── Azure-CLI.md
│   ├── Azure-PowerShell.md
│   ├── Azure-Resource-Manager.md
│   └── Azure-Advisor.md
│
├── 09-Azure-Governance/
│   ├── Azure-Policy.md
│   ├── Resource-Locks.md
│   ├── Tags.md
│   └── Management-Groups.md
│
├── 10-Azure-Cost-Management/
│   ├── Azure-Pricing.md
│   ├── Cost-Management.md
│   ├── Pricing-Calculator.md
│   └── Service-Level-Agreements.md
│
└── 11-Revision/
    ├── AZ-900-Quick-Revision.md
    ├── Important-Definitions.md
    └── Practice-Questions.md
```

---

# ☁️ 1. Cloud Computing Fundamentals

## What is Cloud Computing?

Cloud computing is the delivery of computing services such as:

* Servers
* Storage
* Databases
* Networking
* Software
* Analytics
* AI

over the internet.

Instead of purchasing and maintaining physical infrastructure, organisations can consume computing resources from cloud providers.

### Major Cloud Providers

* Microsoft Azure
* Amazon Web Services (AWS)
* Google Cloud Platform (GCP)

---

## Cloud Deployment Models

### Public Cloud

Infrastructure is owned and operated by a cloud provider and shared among multiple customers.

**Example:**

Microsoft Azure

### Private Cloud

Cloud infrastructure is dedicated to a single organisation.

### Hybrid Cloud

A combination of public and private cloud environments.

```text
Private Cloud
     │
     │
     ▼
 ┌─────────┐
 │ Hybrid  │
 │  Cloud  │
 └─────────┘
     ▲
     │
     │
Public Cloud
```

---

# 🏗️ 2. Azure Architecture

Important Azure architecture concepts include:

* Azure Regions
* Region Pairs
* Availability Zones
* Resources
* Resource Groups
* Subscriptions
* Management Groups

### Azure Hierarchy

```text
Management Groups
       │
       ▼
Subscriptions
       │
       ▼
Resource Groups
       │
       ▼
Resources
```

---

# 🖥️ 3. Azure Compute

Azure provides several ways to run applications and workloads.

### Azure Virtual Machines

Provides virtualised servers running in Azure.

Useful when you need:

* Operating system control
* Custom software
* Server-level configuration

### Azure App Service

A platform-as-a-service offering for hosting:

* Web applications
* REST APIs
* Mobile backends

### Azure Functions

A serverless compute service used to execute code in response to events.

Common use cases:

* API endpoints
* Automation
* Event processing
* Scheduled tasks

### Containers

Containers package an application and its dependencies into a portable unit.

---

# 🌐 4. Azure Networking

Important networking services include:

### Azure Virtual Network (VNet)

Provides private networking within Azure.

### Azure VPN Gateway

Creates encrypted connections between networks.

### Azure ExpressRoute

Provides a private connection between an organisation's network and Azure.

### Azure Load Balancer

Distributes network traffic across multiple resources.

### Application Gateway

Provides application-level traffic management and includes features such as Web Application Firewall capabilities.

### Azure DNS

Provides DNS hosting and name resolution.

---

# 🗄️ 5. Azure Storage

Azure provides multiple storage solutions.

## Blob Storage

Used for unstructured data such as:

* Images
* Videos
* Documents
* Backups
* Logs

## Azure Files

Provides managed file shares.

## Queue Storage

Used for storing messages between application components.

## Disk Storage

Provides persistent disks for Azure Virtual Machines.

---

# 🗃️ 6. Azure Databases

Azure provides multiple database technologies.

### Azure SQL Database

Managed relational database service based on Microsoft SQL Server.

### Azure Cosmos DB

Globally distributed NoSQL database designed for high availability and scalability.

---

# 🔐 7. Azure Security

Security is a major component of Azure.

Important services and concepts include:

* Microsoft Entra ID
* Azure Role-Based Access Control (RBAC)
* Microsoft Defender for Cloud
* Microsoft Sentinel
* Azure Key Vault
* Zero Trust

---

## Microsoft Entra ID

Microsoft Entra ID provides identity and access management.

It can be used to manage:

* Users
* Groups
* Applications
* Authentication
* Access

---

## Azure RBAC

Role-Based Access Control determines what users and services are allowed to do with Azure resources.

Example roles include:

* Owner
* Contributor
* Reader

---

## Azure Key Vault

Used to securely store:

* Secrets
* Encryption keys
* Certificates

---

# 🛡️ 8. Azure Governance

Azure governance helps organisations control and manage their Azure environment.

Important concepts include:

* Azure Policy
* Resource Locks
* Tags
* Management Groups
* Role-Based Access Control

### Azure Policy

Azure Policy can enforce organisational rules and standards.

Example:

> Only allow resources to be deployed in approved regions.

### Resource Locks

Resource locks can help prevent accidental deletion or modification.

---

# 💰 9. Azure Pricing and Cost Management

Azure uses consumption-based pricing for many services.

You generally pay for the resources and services that you use.

Important concepts:

* Azure Pricing Calculator
* Azure Cost Management
* Service Level Agreements (SLAs)
* Service Lifecycle
* Free Azure Services
* Reservations
* Azure Hybrid Benefit

---

# 📊 10. Azure Management Tools

Azure provides several ways to manage resources.

## Azure Portal

A web-based graphical interface for managing Azure resources.

## Azure CLI

Command-line interface for managing Azure resources.

Example:

```bash
az login
```

## Azure PowerShell

PowerShell-based management of Azure resources.

## Azure Cloud Shell

Browser-accessible shell environment that supports Azure CLI and PowerShell.

## Azure Resource Manager

Azure's deployment and management service.

---

# 🤖 11. Azure AI Fundamentals

Azure provides AI and machine learning services for building intelligent applications.

Important areas include:

* Machine Learning
* Computer Vision
* Natural Language Processing
* Generative AI
* Speech
* Document Intelligence

The goal at the AZ-900 level is to understand **what these services are used for**, rather than becoming an AI specialist.

---

# 📈 12. Monitoring and Management

Azure provides tools for monitoring infrastructure and applications.

Important services include:

### Azure Monitor

Collects and analyses monitoring data from Azure resources and applications.

### Log Analytics

Used to query and analyse log data.

### Application Insights

Provides application performance monitoring.

### Azure Advisor

Provides recommendations relating to areas such as:

* Cost
* Security
* Reliability
* Performance
* Operational excellence

---

# 🧠 Important AZ-900 Concepts

These are concepts I am focusing on understanding rather than simply memorising.

| Concept           | What it means                                         |
| ----------------- | ----------------------------------------------------- |
| IaaS              | Infrastructure as a Service                           |
| PaaS              | Platform as a Service                                 |
| SaaS              | Software as a Service                                 |
| Public Cloud      | Shared cloud infrastructure                           |
| Private Cloud     | Dedicated cloud infrastructure                        |
| Hybrid Cloud      | Combination of public and private cloud               |
| Region            | Geographic Azure location                             |
| Availability Zone | Physically separate datacenter within an Azure region |
| Resource Group    | Logical container for Azure resources                 |
| Subscription      | Billing and access boundary                           |
| RBAC              | Controls access to Azure resources                    |
| Azure Policy      | Enforces organisational rules                         |
| Azure Monitor     | Monitoring and observability                          |
| Azure Advisor     | Provides optimisation recommendations                 |

---

# 🎯 AZ-900 Exam Areas

The Microsoft Azure Fundamentals certification focuses on several major areas:

### Describe Cloud Concepts

Topics include:

* Cloud computing
* Shared responsibility
* Cloud models
* Consumption-based model
* Benefits of cloud computing

### Describe Azure Architecture and Services

Topics include:

* Azure regions
* Availability zones
* Azure resources
* Compute
* Networking
* Storage
* Databases

### Describe Azure Management and Governance

Topics include:

* Azure Cost Management
* Azure Policy
* Resource locks
* Microsoft Entra ID
* RBAC
* Azure Monitor
* Azure Advisor

---

# 🧪 Practical Learning

Where possible, I will reinforce the theory with practical Azure exercises.

Examples include:

* Creating an Azure resource group
* Deploying an Azure Storage Account
* Creating a Virtual Machine
* Creating an App Service
* Working with Azure Functions
* Configuring a Virtual Network
* Exploring Microsoft Entra ID
* Assigning Azure RBAC roles
* Creating Azure Policies
* Monitoring resources with Azure Monitor
* Using Azure CLI
* Exploring the Azure Portal

---

# 📝 Study Method

My approach to learning Azure is:

```text
Learn the Concept
       ↓
Understand the Purpose
       ↓
Compare Similar Services
       ↓
Practice in Azure
       ↓
Take Notes
       ↓
Test My Knowledge
       ↓
Review Weak Areas
```

The goal is not only to pass AZ-900, but to develop a foundation that can be used in future:

* Software Development
* Cloud Development
* Power Platform
* DevOps
* IT Support
* Software Testing
* Azure-based application development

---

# 🚀 My Azure Learning Journey

I am building Azure knowledge as part of my broader IT career development.

My current technical interests include:

* C#
* .NET
* React
* SQL
* Microsoft Power Platform
* Power Apps
* Power Automate
* Power BI
* SharePoint
* Azure
* Software Testing
* QA / Compliance Testing

Azure is particularly relevant to my development journey because I want to understand how modern applications are deployed, managed, secured, monitored, and scaled in the cloud.

---

# 📌 Current Progress

* [x] Cloud Computing Fundamentals
* [x] Cloud Service Models
* [x] Cloud Deployment Models
* [ ] Azure Architecture
* [ ] Azure Compute
* [ ] Azure Networking
* [ ] Azure Storage
* [ ] Azure Databases
* [ ] Azure Security
* [ ] Azure Governance
* [ ] Azure Cost Management
* [ ] Azure Monitoring
* [ ] Azure AI Fundamentals
* [ ] AZ-900 Practice Questions
* [ ] AZ-900 Exam Preparation
* [ ] AZ-900 Certification

> This checklist will be updated as I progress through my Azure Fundamentals learning journey.

---

# 📚 Resources

Official Microsoft resources:

* Microsoft Learn
* Azure Documentation
* Azure Architecture Center
* Azure Pricing Calculator
* Azure Free Account

Additional resources and references will be added as I continue studying.

---

# 🔗 Related Projects

As I progress, I plan to connect my Azure learning with practical development projects involving technologies such as:

* C#
* .NET
* REST APIs
* React
* SQL Server
* Azure
* Microsoft Power Platform

---

# 👨🏾‍💻 About Me

I'm an IT professional with experience across:

* Software Development
* Microsoft Power Platform
* IT Support
* Software Testing
* QA and Compliance Testing

My development background includes **C#, .NET, React, SQL, APIs, and Microsoft technologies**, while my testing experience includes functional, regression, compliance, and application testing.

I am currently expanding my cloud knowledge with **Microsoft Azure** and working towards the **AZ-900 Azure Fundamentals** certification.

---

## ⭐ Why This Repository?

This repository is both a **study resource and a record of my technical growth**.

Rather than keeping my learning private, I'm documenting the concepts I learn, the practical exercises I complete, and the technologies I explore.

> **Learn → Build → Test → Document → Improve**

---

## 📜 Certification Goal

🎯 **Microsoft Certified: Azure Fundamentals (AZ-900)**

Status: **In Progress** 🚀

---

⭐ If you find these notes useful, feel free to explore the repository and follow along with my Azure learning journey.
