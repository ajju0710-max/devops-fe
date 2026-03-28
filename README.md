# devops-fe
# 🚀 Meetz — AI DevOps Assistant Platform

Meetz is a **web-based SaaS platform** that enables teams to automate DevOps workflows using AI.
It provides a secure, approval-driven system for building, deploying, and managing infrastructure through natural language and structured execution.

---

## 🧠 Core Concept

> **Prompt → Approval → Execution → Observability → Learning**

Meetz allows developers to interact with infrastructure using AI while enforcing **enterprise-grade guardrails, approvals, and auditability**.

---

## ✨ Phase-1 Features

### 🤖 AI Assistant

* Natural language DevOps execution
* Log analysis (pasted / uploaded / fetched)
* Dockerfile generation
* Suggest fixes and optimizations
* Converts actions into **Change Requests**

---

### ⚙️ Build & Deploy

* Build Docker images
* Push to registries
* Manage version tags (Patch / Release)
* Kubernetes & Docker support

---

### 🔐 Image Security

* Vulnerability scanning
* Severity classification (Critical / High / Medium)
* AI-based remediation suggestions

---

### 📜 Logs & Insights

* Real-time log streaming (WebSocket-ready)
* 7-day log retention
* AI-assisted log analysis

---

### 🐳 Dockerfile AI

* Generate Dockerfiles from app context
* Edit and version control

---

### 🔗 Integrations

* Git: GitHub / GitLab
* Registry: DockerHub / JFrog / Harbor
* Deployment: Kubernetes / Docker
* Notifications: Slack / Email
* Issue Tracking: Jira

---

### 🧾 Change Requests (Core Engine)

* Every action becomes an approval request
* Tracks:

  * Commands
  * File changes
  * Execution logs
* Status lifecycle:

  * `PENDING → APPROVED → EXECUTED`

---

### 🛡️ Policies & Guardrails

* Command whitelisting
* Execution restrictions
* AI safety controls

---

### 🚨 Incidents & Knowledge Base

* Auto-create incidents on failure
* AI suggests solutions
* Store solutions for future reuse
* Tagged by users

---

### 💻 Command Console

* Execute shell commands (approval required)
* AI-assisted command suggestions

---

## 🔐 Role-Based Access (RBAC)

| Capability       | Admin             | Developer    |
| ---------------- | ----------------- | ------------ |
| Deploy           | ✅                 | ❌            |
| Approve Requests | ✅                 | ❌            |
| Modify Configs   | ✅                 | ✅            |
| Execute Commands | ✅ (with approval) | Request-only |
| View Logs        | ✅                 | ✅            |

---

## 🏗️ Architecture Overview

### Frontend

* Next.js (App Router)
* TypeScript
* Tailwind CSS
* Zustand (state management)
* Axios (API layer)

---

### Core Design Principles

* ❌ No hardcoded configs
* ✅ Centralized configuration
* ✅ Feature-based modular architecture
* ✅ Approval-first execution model
* ✅ GitOps-friendly workflows

---

## 📁 Project Structure

```
src/
├── app/                  # Routing (Next.js)
├── components/           # UI + Layout
├── features/             # Domain modules
├── config/               # Centralized configs
├── services/             # API layer
├── store/                # Global state
├── hooks/                # Custom hooks
├── utils/                # Helpers
├── types/                # Type definitions
```

---

## ⚙️ Configuration (No Hardcoding)

All configs are managed via:

* `config/env.ts`
* `config/navigation.config.ts`
* `config/integrations.config.ts`

### Example:

```
NEXT_PUBLIC_API_URL=https://api.meetz.co.in
```

---

## 🔄 Execution Flow

```
User Prompt / Action
        ↓
AI Processing
        ↓
Change Request Created
        ↓
Admin Approval
        ↓
Execution (K8s / Docker / Git)
        ↓
Logs Streamed + Stored
        ↓
Incident Created (if failure)
        ↓
AI Suggestion + Knowledge Base Update
```

---

## 🔗 GitOps Integration

* All changes are committed to Git
* Tracks:

  * User identity
  * File modifications
* Supports:

  * Helm charts
  * docker-compose

---

## 📡 Logs System

* WebSocket-based streaming (planned)
* Sources:

  * Kubernetes
  * Docker
  * Build pipelines
* Retention: **7 days**

---

## 🚀 Getting Started

### 1. Clone Repository

```
git clone https://github.com/your-org/meetz.git
cd meetz
```

---

### 2. Install Dependencies

```
npm install
```

---

### 3. Setup Environment

Create `.env.local`:

```
NEXT_PUBLIC_API_URL=http://localhost:3000
```

---

### 4. Run Development Server

```
npm run dev
```

---

### 5. Open Application

```
http://localhost:3000
```

---

## 🎨 UI/UX Principles

* Dark/Light theme (system default)
* AI-first interface
* Approval visibility
* Real-time feedback
* Minimal friction workflows

---

## 🔮 Future Roadmap

* Multi-tenant SaaS (organizations)
* Billing & subscription (Stripe)
* Advanced RBAC
* Observability dashboards
* AI model fine-tuning (incident learning)
* Kubernetes multi-cluster support

---

## ⚠️ Security Considerations

* All executions require approval
* Guardrails enforced on AI actions
* Role-based restrictions
* Audit logs for all operations

---

## 🤝 Contribution

Currently private development.
Contribution guidelines will be added in future.

---

## 📌 License

Proprietary (Meetz Platform)

---

## 💡 Vision

> Build an intelligent DevOps platform where AI doesn’t just assist—but operates safely, transparently, and at scale.

---

## 🔗 Branding

**Product Name:** Meetz
**Tagline:** *Prompt. Execute. Deploy.*

---
