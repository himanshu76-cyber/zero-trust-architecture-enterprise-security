<div align="center">

```
███████╗███████╗██████╗  ██████╗     ████████╗██████╗ ██╗   ██╗███████╗████████╗
╚══███╔╝██╔════╝██╔══██╗██╔═══██╗    ╚══██╔══╝██╔══██╗██║   ██║██╔════╝╚══██╔══╝
  ███╔╝ █████╗  ██████╔╝██║   ██║       ██║   ██████╔╝██║   ██║███████╗   ██║   
 ███╔╝  ██╔══╝  ██╔══██╗██║   ██║       ██║   ██╔══██╗██║   ██║╚════██║   ██║   
███████╗███████╗██║  ██║╚██████╔╝       ██║   ██║  ██║╚██████╔╝███████║   ██║   
╚══════╝╚══════╝╚═╝  ╚═╝ ╚═════╝        ╚═╝   ╚═╝  ╚═╝ ╚═════╝ ╚══════╝   ╚═╝  
  
```

# 🛡️ Zero Trust Architecture Enterprise Security

**Project Type** Cybersecurity • Docker • Zero Trust • Access Control

A practical Zero Trust Architecture (ZTA) implementation designed to demonstrate secure enterprise access control using Docker containers, authentication mechanisms, and role-based authorization policies.

This project simulates a small enterprise environment where users must be continuously verified before accessing protected resources, following the Zero Trust principle:

> **Never Trust, Always Verify**

---

## ✨ Project Overview

This project demonstrates how modern organizations can secure internal resources using Zero Trust concepts.

The simulation includes:

* Secure login authentication
* Employee and Admin role separation
* Role-Based Access Control (RBAC)
* Docker-based deployment
* Insider threat simulation
* External attack testing
* Access restriction and verification

The project highlights how organizations can reduce security risks by continuously validating users rather than trusting network location alone.

---

## 🎯 Objectives

* Implement Zero Trust Architecture principles
* Demonstrate secure authentication workflows
* Enforce Role-Based Access Control (RBAC)
* Simulate enterprise user management
* Prevent unauthorized access attempts
* Test insider and external threat scenarios
* Deploy security controls using Docker

---

## 📊 Key Outcomes

* Dockerized secure web application deployed successfully
* Employee and Admin roles implemented
* Unauthorized dashboard access blocked
* URL manipulation attempts prevented
* Access permissions enforced through RBAC
* Security controls validated through testing
* Enterprise-style Zero Trust environment simulated

These results demonstrate how Zero Trust security can significantly reduce the risk of unauthorized access.

---

## 🧩 Project Structure

```text
.
├── screenshots/
│   ├── login_page.png
│   ├── employee_dashboard.png
│   ├── admin_dashboard.png
│   ├── docker_container_running.png
│   ├── unauthorized_access_test.png
│   └── security_validation.png
│
├── documentation/
│   ├── setup_guide_docker.md
│   ├── rbac_policy.md
│   ├── mfa_configuration.md
│   ├── insider_threat_test.md
│   ├── external_threat_test.md
│   └── results.md
│
├── report/
│   └── ZeroTrust_Report.docx
│
├── presentation/
│   └── ZeroTrustArchitecture.pptx
│
├── docker/
│   ├── Dockerfile
│   ├── docker-compose.yml
│   └── nginx.conf
│
├── web/
│   ├── login.html
│   ├── employee_dashboard.html
│   └── admin_dashboard.html
│
└── README.md
```

---

## 🖼️ Included Assets

### Screenshots

The screenshot collection demonstrates:

* Login authentication process
* Employee dashboard access
* Administrator dashboard access
* Docker container deployment
* Security policy enforcement
* Unauthorized access prevention

### Documentation

Detailed implementation guides are included covering:

* Docker deployment
* RBAC configuration
* MFA recommendations
* Threat testing procedures
* Security validation results

### Presentation

A PowerPoint presentation is included for:

* Viva demonstrations
* Academic submissions
* Project reviews
* Security awareness sessions

### Final Report

The project report contains:

* Project methodology
* Architecture design
* Testing procedures
* Security analysis
* Findings and recommendations

---

## 🔐 Security Features

### Authentication

Users must verify their identity before access is granted.

### Role-Based Access Control (RBAC)

Permissions are assigned according to user roles.

### Session Security

Sessions are managed and validated to prevent unauthorized access.

### Continuous Verification

Access requests are continuously checked against security policies.

### Threat Protection

The system is tested against common insider and external attack scenarios.

---

## 🐳 Docker Deployment

### Build Docker Image

```bash
docker build -t zta-security .
```

### Run Container

```bash
docker run -d -p 9090:80 zta-security
```

### Verify Running Containers

```bash
docker ps
```

### Access Application

```text
http://localhost:9090
```

---

## 🛠️ Tech Stack

* Docker
* Docker Compose
* Nginx
* HTML
* CSS
* JavaScript
* RBAC Policies
* Zero Trust Architecture Principles

---

## 📈 Findings Summary

The project demonstrates that security should not rely solely on network boundaries.

Key observations include:

* User identity verification is critical.
* Least-privilege access reduces attack surface.
* RBAC effectively limits unauthorized actions.
* Continuous validation strengthens enterprise security.
* Docker simplifies deployment and testing environments.

The strongest lesson is simple:

> Trust should never be assumed. Every request must be verified.

---

## 🚀 How to Present This Project

This repository can be used for:

* Minor Project 2 submission
* Cybersecurity demonstrations
* Docker implementation showcase
* Academic viva presentations
* Portfolio projects
* Enterprise security awareness sessions

---

## 👨‍💻 Author

**Himanshu Soni**

Minor Project 2

Zero Trust Architecture Enterprise Security

---

## 📌 Note

This project is created for educational and demonstration purposes. The implementation focuses on learning Zero Trust principles, secure access control, and containerized deployment in a controlled environment.
