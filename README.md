<img width="600" alt= "image" src="https://i.imgur.com/1V5ohep.png">

🏗️🚧👷‍♂️ UNDER CONSTRUCTION 🚧🏗️👷‍♂️
# 🧠 Blue Skynet: AI Defense Cloud Infrastructure

Welcome to **Blue Skynet**, a fictional AI defense technology startup focused on protecting next-generation networks using machine learning and proactive cloud security. This project simulates the **entire cloud journey** of a startup — from day one infrastructure setup, to monitoring, budgeting, and compliance.

You are the **Cloud Architect/Security Engineer** responsible for designing and deploying the startup's secure Azure-based environment, following best practices and aligning with NIST 800-53 and Microsoft certification frameworks (AZ-104, AZ-305, AZ-500, AI-900, AI-102).

---

## 🌐 Live Website

**Demo URL:** [Blue SkyNet ](https://blue-skynet-webapp-b8c2cyfucxemaqas.eastus2-01.azurewebsites.net)


## 📖 Story & Intent

### 🚀 The Mission

Blue Skynet's mission is to deliver an **AI-first defense platform** capable of detecting and neutralizing cyber threats in real-time.

The company is founded by a small team of:

* **CEO (Alicia Reyes)** – focused on fast, cost-conscious delivery
* **CTO/AI Lead (Marcus Lee)** – wants secure compute + data for model training
* **HR Manager (Tamika Johnson)** – needs role-based access to sensitive employee files
* **IT Intern (Jordan)** – learning the ropes, requires limited access

You're brought in to build their **secure cloud infrastructure** from scratch.

---

## 🧱 Architecture Overview

<img width="600" alt= "image" src="https://i.imgur.com/kPjecBb.png">

**Website Hosting (Production Simulation):**

* Hosted via **Azure Static Web Apps** or **Blob Storage (Static Site)**
* Protected by:

  * **HTTPS-only access**
  * **Azure Front Door** (optional WAF and geo-filtering)
  * **Private endpoint** or **IP restriction**
  * **Entra ID authentication** (optional RBAC login per role)

**Optional Security Add-Ons:**

* Key Vault integration (store site secrets or keys securely)
* Azure Policy to block insecure or non-compliant deployments
* Microsoft Sentinel alerts for public access or failed login patterns
* Application Insights for user behavior logging



**Core Azure Components:**

* Azure VNet with 4 virtual machines:

  * Domain Controller (optional)
  * Intranet App Server (Windows)
  * Vulnerable/Unpatched VM (Windows 10)
  * Linux Web Server
* Azure Key Vault for secrets
* Microsoft Entra ID with role-based access
* Log Analytics + Microsoft Sentinel for monitoring
* ARM/Bicep for infrastructure as code
* Azure Policy-as-Code (SC-12, region lock, encryption enforcement)
* Budgeting via Cost Management + alert rules

---

## 🧪 Step-by-Step Setup

### 1. 🔧 Initial Infrastructure

💬 **Staff Interaction (CEO):**

<img width="600" alt= "image" src="https://i.imgur.com/pfKKREn.jpeg">



<img width="600" alt= "image" src="https://i.imgur.com/p4ny1vn.png">


<img width="600" alt= "image" src="https://i.imgur.com/WAAf6pm.png">


### 2. 👥 Identity & Access

<img width="600" alt= "image" src="https://i.imgur.com/LGJ9hus.png">

📸 **Capture:**

* [ ] Entra ID roles setup — *demonstrate RBAC assignments for HR Manager, Intern, Dev*
* Set up Microsoft Entra ID users:

  * HR Manager, Intern, Dev, Admin roles
* Assign RBAC roles (Reader, Contributor, Custom RBAC)

### 3. 🛡️ Security Hardening

<img width="600" alt= "image" src="https://i.imgur.com/1NEG9Q8.jpeg">


* [ ] Key Vault creation and secrets stored — *show access policies and key names*
* [ ] PowerShell script being executed on VM — *screenshot script output*
* [ ] Policy assignment in Azure Policy blade — *screenshot policy assignment (SC-12, region lock)*
* Apply STIGs via PowerShell (for Windows VMs)
* Store credentials/secrets in Key Vault
* Enable Defender for Cloud (free tier)
* Create & assign Azure Policies:

  * SC-12 encryption enforcement
  * Restrict to approved regions

### 4. 🔍 Monitoring & Logging

<img width="600" alt= "image" src="https://i.imgur.com/ofcoDb9.png">



📸 **Capture:**

* [ ] Microsoft Sentinel rule alerts / dashboard — *show alert rules or workbook view*

📸 **Capture:**

* [ ] Microsoft Sentinel rule alerts / dashboard — *show alert rules or workbook view*
* Set up Log Analytics Workspace
* Connect VMs to it
* Enable diagnostic settings for VMs, Storage, Key Vault
* Deploy Microsoft Sentinel and connect workspace
* Create analytic rule (e.g., failed login alerts)

### 5. 📊 Budgeting

📨 **Internal Email (to CEO):**

<img width="600" alt= "image" src="https://i.imgur.com/3yBQua9.jpeg">

📸 **Capture:**

* [ ] Cost analysis chart & budget alert — *chart from Cost Management + alert config screen*

📸 **Capture:**

* [ ] Cost analysis chart & budget alert — *chart from Cost Management + alert config screen*
* Set monthly budget (e.g. \$25)
* Create budget alert at 80%
* Export cost chart and CSV

### 6. 🔬 Vulnerability Scanning

📨 **Internal Slack (to Security Channel):**

> *"Running Nessus scans today. Expecting high-priority findings on the unpatched VM. Will remediate with PowerShell, then rescan and archive reports."*

📸 **Capture:**

* [ ] Tenable Nessus scan results (before & after remediation) — *export or screenshot findings from Nessus Essentials*

📸 **Capture:**

* [ ] Tenable Nessus scan results (before & after remediation) — *export or screenshot findings from Nessus Essentials*
* Install Nessus Essentials agent on Windows/Linux VMs
* Run baseline scan
* Remediate issues (manual + PowerShell)
* Rescan and export results

---

## 📚 Certifications Mapped

| Certification | Key Areas Demonstrated                              |
| ------------- | --------------------------------------------------- |
| AZ-104        | Identity, VMs, NSG, Storage, Key Vault              |
| AZ-305        | Architecture design, Policy, DR, Cost control       |
| AZ-500        | Defender, Sentinel, Encryption, RBAC, Logs          |
| AI-900        | Mission-level AI awareness, cloud integration       |
| AI-102        | Project framework for AI deployment (future add-on) |

---

## 📎 Project Folder Structure

```bash
/blue-skynet/
├── README.md
├── /bicep/
├── /scripts/
├── /branding/
├── /policies/
├── /sentinel/
├── /screenshots/
├── /cost-tracking/
├── /nessus-reports/
├── architecture-diagram.png
```

---

## 🧠 NIST 800-53 Mapping (Sample)

| Control | Description              | Implemented In             |
| ------- | ------------------------ | -------------------------- |
| AC-2    | Account Management       | Entra ID RBAC              |
| SC-12   | Cryptographic Protection | Storage, Key Vault, Policy |
| AU-2    | Audit Events             | Sentinel, Diagnostic Logs  |
| SI-2    | Flaw Remediation         | Nessus + STIG scripts      |
| CA-7    | Continuous Monitoring    | Sentinel, Log Analytics    |

---

## 🧩 Web Hosting & Protection in Azure

To simulate real-world hosting and security, the Blue Skynet GitHub Pages site is deployed in Azure using a hardened and production-aware design.

### 🚀 Use Case

> "To simulate real-world hosting, I deployed the Blue Skynet website on Azure Static Web Apps, integrated Entra ID for login, and restricted HR dashboard access via role-based auth. Logging and alerts are managed through Application Insights and Sentinel."

### 🧰 Azure Hosting Stack

* **Azure Static Web Apps**: Public-facing GitHub Pages deployment with continuous integration
* **HTTPS-Only**: Secured transport layer enforced
* **Azure Front Door**: Optional DDoS protection, routing, and WAF
* **Private Endpoint / IP Restrictions**: Limit access by network
* **Entra ID Authentication**: Optional role-based login simulation (HR, Intern, Dev)

### 🔐 Security Enhancements

* **Key Vault**: Protect site credentials, secrets
* **Azure Policy**: Block deployments without HTTPS or encryption
* **Microsoft Sentinel**: Log access attempts and alerts on anomalies
* **Application Insights**: Log site usage patterns and behaviors

📸 **Capture:**

* [ ] Static site deployment view in Azure portal — *show Static Web App or Blob config*
* [ ] Entra ID login screen (if implemented)
* [ ] Sentinel or App Insights logs related to web access

---

# 🌟 Blue Skynet Project Wrap-Up & Roadmap

## 🔺 Project Wrap-Up

The **Blue Skynet** project successfully simulates a realistic cloud security deployment for a fictional AI defense startup. The core infrastructure was designed and deployed using Microsoft Azure services and hardened to reflect real-world compliance, cost control, and monitoring requirements.

### 🌟 Key Wins:

* Built a secure, scalable Azure infrastructure from scratch
* Applied DISA STIGs and ran Nessus vulnerability scans
* Integrated Microsoft Sentinel for incident detection and alerting
* Configured Azure Key Vault, Defender for Cloud, and RBAC controls
* Simulated internal workflows and access policies using role-based scenarios
* Mapped to real-world certifications: **AZ-104, AZ-305, AZ-500, AI-900, SC-200**
* Demonstrated alignment with **NIST 800-53** controls such as SC-12, AC-2, AU-2, CA-7, and SI-2

This project serves as a dynamic learning artifact, a professional portfolio piece, and a strong demonstration of cloud security and infrastructure skills.

---

## 🔭 What's Next for Blue Skynet?

Blue Skynet was designed with future extensibility in mind. The following enhancements can build on the foundation and expand coverage for additional certifications and real-world scenarios:

* 🤖 **Azure OpenAI Integration**: Simulate secure AI services (e.g., chatbots, document classification) for AI-102 use cases
* 📈 **Compliance Dashboard**: Build a visual matrix linking STIG/NIST controls to resource configurations and audit status
* 🚀 **CI/CD Pipelines**: Use GitHub Actions or Azure DevOps to automatically deploy Bicep templates and update policies
* 📄 **Internal Chatbox Simulation**: Add an Azure Bot (or static front-end) to simulate internal staff communication via a portal
* 📊 **Web App Enhancements**: Convert the current static site to a role-based dashboard (e.g., HR Portal, Intern Sandbox)
* 🚫 **Access Review Workflows**: Add Azure Entitlement Management and Privileged Identity Management (PIM)
* 🚨 **M365 Defender Simulation (SC-200)**: Extend threat detection by simulating attacks or alerts in Defender for Endpoint, Office 365, or Cloud Apps

> ✨ *Blue Skynet is not a static lab—it's a living platform to grow your real-world skillset and expand toward DevSecOps, AI security, and compliance-driven cloud deployments.*

---
















