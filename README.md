<img width="600" alt= "image" src="https://i.imgur.com/1V5ohep.png">

# 🧠 Blue Skynet: AI Defense Cloud Infrastructure

Welcome to **Blue Skynet**, a fictional AI defense technology startup focused on protecting next-generation networks using machine learning and proactive cloud security. This project simulates the **entire cloud journey** of a startup — from day one infrastructure setup, to monitoring, budgeting, and compliance.

You are the **Cloud Architect/Security Engineer** responsible for designing and deploying the startup's secure Azure-based environment, following best practices and aligning with NIST 800-53 and Microsoft certification frameworks (AZ-104, AZ-305, AZ-500, AI-900, AI-102).

---

## 🌐 Live Website

**Demo URL:** [https://your-website-url.com](https://your-website-url.com)
*(Note: Replace with your deployed static site or web app URL)*

---

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

!\[Architecture Diagram Placeholder]
*Insert full Azure architecture diagram with VMs, Key Vault, Sentinel, NSGs, Entra ID, and cost controls here.*

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

> "We need this live by end of the week — but I can't afford a surprise Azure bill. Show me a plan and a budget alert."

🧑‍💻 **My Response (Cloud Architect):**

> "Absolutely. I’ve already scoped out a low-cost environment using B1s VMs with auto-shutdown and budget alerts configured in Cost Management. You’ll have daily visibility into spend.""We need this live by end of the week — but I can't afford a surprise Azure bill. Show me a plan and a budget alert."

📸 **Capture:**

* [ ] Initial VM deployments (Azure portal) — *show resource group, region, B1s size, tags*
* [ ] NSG rules configuration — *highlight inbound/outbound rule setup*
* Deploy resource group and VNet
* Use Bicep or ARM templates to provision:

  * 4 VMs (Windows & Linux), all B1s
  * NSGs + Subnets
  * Storage (LRS)
  * Key Vault (Standard tier)
* Enable auto-shutdown

### 2. 👥 Identity & Access

💬 **Staff Interaction (HR Manager):**

> "I need secure access to employee contracts, but Jordan (intern) should not be able to see these. Can we set that up in the portal?"

🧑‍💻 **My Response (Cloud Architect):**

> "Yes, I’ll configure Entra ID with role-based access and assign you exclusive permissions to the HR file share while isolating intern access to a test VM only.""I need secure access to employee contracts, but Jordan (intern) should not be able to see these. Can we set that up in the portal?"

📸 **Capture:**

* [ ] Entra ID roles setup — *demonstrate RBAC assignments for HR Manager, Intern, Dev*
* Set up Microsoft Entra ID users:

  * HR Manager, Intern, Dev, Admin roles
* Assign RBAC roles (Reader, Contributor, Custom RBAC)

### 3. 🛡️ Security Hardening

💬 **Staff Interaction (AI Lead):**

> "Security is non-negotiable. Can you guarantee our Key Vault secrets and encrypted model storage won't get leaked?"

🧑‍💻 **My Response (Cloud Architect):**

> "Definitely. I’ve configured Azure Key Vault with RBAC, enabled logging and soft delete, and enforced encryption policies across all storage accounts via Azure Policy-as-Code.""Security is non-negotiable. Can you guarantee our Key Vault secrets and encrypted model storage won't get leaked?"

📸 **Capture:**

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

📨 **Internal Slack (to AI Lead & Dev):**

> *"Sentinel is live. Log Analytics connected. I’ve added an alert for failed RDP attempts and will demo dashboard tomorrow. Let me know if you want anomaly detection added too."*

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

> *Subject: Azure Budget Controls Configured*
> *"Hi Alicia, I’ve set the monthly Azure budget at \$25. Alerts will trigger at 80%. I've also exported a sample cost chart you can review in our shared folder."*

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

## ✅ Summary

This project presents a **comprehensive cloud infrastructure simulation** for a fictional startup, incorporating real security, governance, and identity techniques. All while tracking costs and showcasing readiness for cloud + AI certification roles.

---

> 💡 Next Phase: Add Azure OpenAI integration + AI app logic for full AI-102 coverage

