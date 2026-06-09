# 🛡️ Zero Trust Architecture — Web Application

<div align="center">

![ZTA Banner](https://img.shields.io/badge/Zero%20Trust-Never%20Trust%20Always%20Verify-00B4D8?style=for-the-badge&logo=shield&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-Containerized-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Security](https://img.shields.io/badge/Security-RBAC%20%7C%20IAM-0077B6?style=for-the-badge&logo=lock&logoColor=white)
![Status](https://img.shields.io/badge/Status-Active-00C853?style=for-the-badge)

**A role-based access control web application demonstrating Zero Trust Architecture principles — containerized with Docker and secured with session-based access enforcement.**

*Developed by [Himanshu Soni](https://github.com/YOUR_USERNAME) · Naviotech Solutions Pvt. Ltd. · Cybersecurity Division · 2025*

</div>

---

## 📌 Table of Contents

- [About the Project](#-about-the-project)
- [Core ZTA Principles](#-core-zta-principles)
- [Features](#-features)
- [Project Structure](#-project-structure)
- [Tech Stack](#-tech-stack)
- [Getting Started](#-getting-started)
- [Demo Credentials](#-demo-credentials)
- [Access Control Flow](#-access-control-flow)
- [Security Test Results](#-security-test-results)
- [Screenshots](#-screenshots)
- [Roadmap](#-roadmap)
- [References](#-references)
- [License](#-license)

---

## 📖 About the Project

This project implements a **Zero Trust Architecture (ZTA)** web application as a proof-of-concept for enterprise-grade security. It demonstrates how the *"Never Trust, Always Verify"* philosophy can be applied in a real-world, containerized environment.

The application enforces strict **role-based access control (RBAC)** — every request is validated against an active session, users cannot self-assign roles, and unauthorized access attempts are blocked and logged regardless of how they originate (direct URL, privilege escalation, or unauthenticated bypass).

> This project was built as part of an enterprise cybersecurity initiative and serves as a practical demonstration for academic and portfolio purposes.

---

## 🔐 Core ZTA Principles

| Principle | Implementation |
|-----------|---------------|
| **Never Trust, Always Verify** | Every page load validates the active session role server-side |
| **Least Privilege** | Users access only the resources their role permits — nothing more |
| **Micro-Segmentation** | Admin and Employee dashboards are completely isolated environments |
| **Continuous Monitoring** | All access attempts (success and failure) are logged and alerted |
| **Minimal Attack Surface** | Login portal exposes only Username, Password, and Login — no role selector |

---

## ✨ Features

- 🔒 **Single Entry Point** — One login portal for all users; roles assigned server-side only
- 👤 **Admin Dashboard** — Manage Users, View Security Logs, Configure Access Policies
- 👷 **Employee Dashboard** — View Tasks, Update Profile, Submit Reports
- 🚫 **Privilege Escalation Blocked** — Employee attempting admin URL gets Access Denied
- 🔗 **Direct URL Bypass Blocked** — Unauthenticated access to any protected page is denied
- ⚠️ **Invalid Credentials Handling** — Generic error message prevents user enumeration attacks
- 🐳 **Fully Dockerized** — Two-container deployment (Nginx web app + MySQL 8 database)

---

## 📁 Project Structure

```
ZTA/
├── app/
│   ├── index.html          # Zero Trust Login Portal (single entry point)
│   ├── admin.html          # Admin Dashboard (admin-role only)
│   └── employee.html       # Employee Dashboard (employee-role only)
└── Dockerfile              # Docker build configuration
```

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | HTML5, JavaScript |
| Web Server | Nginx |
| Database | MySQL 8 |
| Containerization | Docker |
| Architecture | Zero Trust (NIST SP 800-207) |

---

## 🚀 Getting Started

### Prerequisites

Make sure you have the following installed:
- [Docker Desktop](https://www.docker.com/products/docker-desktop/) (v20+)
- Git

### Installation & Run

**1. Clone the repository**
```bash
git clone https://github.com/YOUR_USERNAME/ZTA.git
cd ZTA
```

**2. Build the Docker image**
```bash
docker build -t zta-webapp .
```

**3. Run the container**
```bash
docker run -d -p 8080:80 --name zta-container zta-webapp
```

**4. Open in your browser**
```
http://localhost:8080
```

### Using Docker Compose (Recommended)

If a `docker-compose.yml` is present:
```bash
docker-compose up -d
```

This starts both the web app (port `8080`) and the MySQL database simultaneously.

### Stop & Clean Up
```bash
docker stop zta-container
docker rm zta-container
```

---

## 🔑 Demo Credentials

> ⚠️ **Warning:** These are demo credentials for testing only. **Never use these in a production environment.**

| Role | Username | Password |
|------|----------|----------|
| 🔴 Admin | `admin` | `admin123` |
| 🔵 Employee | `employee` | `emp123` |

---

## 🔄 Access Control Flow

```
User visits app
      │
      ▼
┌─────────────────────┐
│  Zero Trust Login   │  ← Single entry point for ALL users
│     Portal          │
└────────┬────────────┘
         │
    Credentials validated server-side
         │
    ┌────┴────┐
    │         │
  Admin    Employee
    │         │
    ▼         ▼
┌───────┐ ┌──────────┐
│ Admin │ │ Employee │
│ Dash  │ │  Dash    │
└───────┘ └──────────┘

If Employee tries Admin URL ──► Access Denied ✗
If Unauthenticated tries any URL ──► Redirected to Login ✗
If Wrong credentials entered ──► Invalid Credentials (generic) ✗
```

---

## 🧪 Security Test Results

| Test Scenario | Method | Result |
|---------------|--------|--------|
| Admin login | Valid credentials | ✅ Redirected to Admin Dashboard |
| Employee login | Valid credentials | ✅ Redirected to Employee Dashboard |
| Privilege escalation | Employee → Admin URL | ❌ Access Denied |
| Direct URL bypass | Unauthenticated → Admin URL | ❌ Redirected to Login |
| Invalid credentials | Wrong password | ❌ Generic error (no enumeration) |
| Brute-force simulation | Repeated wrong attempts | ❌ All attempts rejected |
| Session validation | All pages on load | ✅ Role checked on every request |

---

## 📸 Screenshots

> Add your screenshots in a `/screenshots` folder and update the paths below.

| Login Portal | Admin Dashboard | Employee Dashboard |
|---|---|---|
| ![Login](screenshots/login.png) | ![Admin](screenshots/admin.png) | ![Employee](screenshots/employee.png) |

| Access Denied | Invalid Credentials |
|---|---|
| ![Denied](screenshots/access-denied.png) | ![Invalid](screenshots/invalid-creds.png) |

---

## 🗺️ Roadmap

- [x] Role-based login portal
- [x] Admin and Employee dashboards
- [x] Session-based access control
- [x] Docker containerization
- [ ] Add `docker-compose.yml` for one-command setup
- [ ] Implement actual MFA (TOTP)
- [ ] Replace `alert()` popups with styled UI notifications
- [ ] Add login attempt logging to database
- [ ] Integrate SIEM-style dashboard for audit logs
- [ ] Add HTTPS/TLS support via Let's Encrypt

---

## 📚 References

1. [NIST SP 800-207 — Zero Trust Architecture](https://csrc.nist.gov/publications/detail/sp/800-207/final) (2020)
2. Kindervag, J. — *"Build Security Into Your Network's DNA: The Zero Trust Network Architecture"* — Forrester Research, 2010
3. [Docker Documentation — Container Security & Networking](https://docs.docker.com)
4. [OWASP Authentication Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html)
5. [Microsoft Zero Trust Architecture Framework](https://learn.microsoft.com/security/zero-trust)
6. Gartner — *SIEM & UEBA Best Practices for Enterprise Security Monitoring* (2023)
7. [AES-256 — NIST FIPS PUB 197](https://csrc.nist.gov/publications/detail/fips/197/final) / [TLS — RFC 5246](https://datatracker.ietf.org/doc/html/rfc5246)

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

<div align="center">

Made with 🔐 by **Himanshu Soni** · Naviotech Solutions Pvt. Ltd.

*"Never Trust. Always Verify."*

</div>
