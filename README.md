<div align="center">

```
███████╗███████╗██████╗  ██████╗     ████████╗██████╗ ██╗   ██╗███████╗████████╗
╚══███╔╝██╔════╝██╔══██╗██╔═══██╗    ╚══██╔══╝██╔══██╗██║   ██║██╔════╝╚══██╔══╝
  ███╔╝ █████╗  ██████╔╝██║   ██║       ██║   ██████╔╝██║   ██║███████╗   ██║   
 ███╔╝  ██╔══╝  ██╔══██╗██║   ██║       ██║   ██╔══██╗██║   ██║╚════██║   ██║   
███████╗███████╗██║  ██║╚██████╔╝       ██║   ██║  ██║╚██████╔╝███████║   ██║   
╚══════╝╚══════╝╚═╝  ╚═╝ ╚═════╝        ╚═╝   ╚═╝  ╚═╝ ╚═════╝ ╚══════╝   ╚═╝  
  
```



````markdown
# 🛡️ Zero Trust Architecture (ZTA) Enterprise Security Project

> Minor Project 2 – Cyber Security
>
> **Author:** Himanshu Soni  
> **Technology:** Docker, Nginx, HTML, Access Control Simulation  
> **Domain:** Cyber Security & Zero Trust Architecture (ZTA)

---

# 📌 Project Overview

This project demonstrates the implementation of a **Zero Trust Architecture (ZTA)** model using Docker containers and a secure web portal.

The project follows the Zero Trust principle:

> **"Never Trust, Always Verify"**

Users are authenticated before access is granted, and role-based access control (RBAC) is used to restrict unauthorized activities.

The implementation simulates an enterprise security environment where employees and administrators have different access privileges.

---

# 🎯 Objectives

- Implement Zero Trust principles
- Simulate secure enterprise access control
- Demonstrate Role-Based Access Control (RBAC)
- Validate authentication mechanisms
- Prevent unauthorized access attempts
- Deploy application using Docker containers
- Test insider and external threat scenarios

---

# 🏗️ System Architecture

```text
User
 │
 ▼
Login Page
 │
 ▼
Authentication
 │
 ├──────────────┐
 ▼              ▼
Employee     Admin
Dashboard   Dashboard
 │              │
 ▼              ▼
Access Control & Security Policies
```

---

# 🔒 Zero Trust Features Implemented

## 1. Identity Verification

- User authentication required
- Login validation
- Session management

## 2. Role-Based Access Control (RBAC)

- Employee Role
- Administrator Role

Permissions are granted based on assigned roles.

## 3. Continuous Verification

- Access checked before page access
- Unauthorized requests blocked

## 4. Session Control

- Session timeout simulation
- Login redirection after logout

## 5. Threat Prevention

- URL tampering protection
- Unauthorized dashboard access prevention

---

# 🐳 Docker Implementation

The project is containerized using Docker.

### Docker Components

- Dockerfile
- Docker Compose
- Nginx Web Server
- Secure Web Portal

### Build Container

```bash
docker build -t secureportal .
```

### Run Container

```bash
docker run -d -p 9090:80 secureportal
```

### Using Docker Compose

```bash
docker-compose up -d
```

### Access Application

```text
http://localhost:9090/login.html
```

---

# 📁 Project Structure

```text
zero-trust-architecture-enterprise-security

├── login.html
├── employee_dashboard.html
├── admin_dashboard.html
├── nginx.conf
├── Dockerfile
├── docker-compose.yml
│
├── setup_guide_docker.md
├── rbac_policy.md
├── mfa_configuration.md
├── insider_threat_test.md
├── external_threat_test.md
├── results.md
│
├── 1_Project_Overview.docx
├── 2_Methodology.docx
├── 3_Findings.docx
├── Minor_Project2_ZeroTrust_Report.docx
│
├── ZTA_Presentation_HimanshuSoni.pptx
│
└── Screenshots
```

---

# 📷 Screenshots Included

The repository contains project execution screenshots:

### Docker Deployment

- Docker Desktop Container Running
- Container Details
- Project Folder Structure

### Authentication Testing

- Login Page
- Wrong Password Attempt
- Access Denied Error

### Employee Dashboard

- Dashboard Overview
- Tasks & Quick Actions
- Session Timer

### Admin Dashboard

- Security Logs
- User Controls
- Access Management

### Security Validation

- URL Tampering Attempt
- Unauthorized Access Blocked
- Redirect to Login

---

# 👥 User Roles

## Employee

Allowed:

- View dashboard
- Access assigned resources
- View tasks

Restricted:

- Access admin panel
- Modify security settings

## Administrator

Allowed:

- Access admin dashboard
- View security logs
- Manage users
- Manage permissions

---

# 🔐 Security Controls

## RBAC

Role-based permission enforcement.

## MFA Configuration

Supports:

- Google Authenticator
- Microsoft Authenticator
- Authy
- Hardware Security Keys

## Session Security

- Automatic session expiration
- Secure login workflow

## URL Protection

Direct access to protected pages is blocked.

---

# 🧪 Security Testing

## Insider Threat Testing

Tested:

- Employee accessing admin resources
- Privilege escalation attempts
- Unauthorized page access

## External Threat Testing

Tested:

- Login bypass attempts
- URL manipulation
- Unauthorized requests

## Results

| Test Category | Status |
|---------------|---------|
| Authentication | ✅ Passed |
| RBAC | ✅ Passed |
| Access Control | ✅ Passed |
| Docker Deployment | ✅ Passed |
| URL Protection | ✅ Passed |
| Session Management | ✅ Passed |

---

# 📊 Findings

- Zero Trust significantly reduces unauthorized access risks.
- RBAC effectively enforces least-privilege access.
- Docker provides isolated deployment environments.
- Continuous verification improves security posture.
- URL tampering and privilege escalation attempts are successfully blocked.

---

# 🚀 Future Enhancements

- Database integration
- Real MFA implementation
- JWT authentication
- LDAP/Active Directory integration
- Audit logging system
- SIEM integration
- Kubernetes deployment
- Micro-segmentation implementation

---

# 📚 Technologies Used

- Docker
- Docker Compose
- Nginx
- HTML5
- CSS3
- JavaScript
- Cyber Security Concepts
- Zero Trust Architecture

---

# 📖 References

- NIST SP 800-207 Zero Trust Architecture
- CISA Zero Trust Maturity Model
- OWASP Security Guidelines
- Docker Official Documentation

---

# 👨‍💻 Author

**Himanshu Soni**

Minor Project 2  
Zero Trust Architecture Implementation using Docker

---

## ⭐ Key Principle

> **Never Trust. Always Verify.**
>
> Every user, device, and request must be authenticated and authorized before access is granted.
````

This version looks professional on GitHub and directly matches the files and screenshots present in your ZIP project.
