# 🔐 Zero Trust Architecture Implementation for Enterprise Access Control

![Project](https://img.shields.io/badge/Project-Minor%20Project%20II-blue)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![Architecture-Zero%20Trust-orange](https://img.shields.io/badge/Architecture-Zero%20Trust-orange)
![Year](https://img.shields.io/badge/Year-2026-lightgrey)
![License](https://img.shields.io/badge/License-MIT-green)

> A practical implementation of **Zero Trust Architecture (ZTA)** for secure enterprise access control using authentication, authorization, role-based access control, micro-segmentation, and continuous verification principles.

---

## 👤 Author

| Field | Details |
|-------|---------|
| **Name** | Himanshu Soni |
| **Project** | Minor Project II |
| **Organization** | Naviotech Solution Pvt Ltd |
| **Domain** | Cybersecurity · Zero Trust Architecture |
| **Year** | 2026 |

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Objectives](#-objectives)
- [Zero Trust Principles](#-zero-trust-principles)
- [System Architecture](#-system-architecture)
- [Security Features Implemented](#-security-features-implemented)
- [Access Control Model](#-access-control-model)
- [Authentication Workflow](#-authentication-workflow)
- [Results & Outcomes](#-results--outcomes)
- [Repository Structure](#-repository-structure)
- [Future Enhancements](#-future-enhancements)
- [References](#-references)

---

## 📌 Overview

Traditional security models assume that users inside a network can be trusted. However, modern cyber threats require a stronger approach.

This project implements a **Zero Trust Architecture (ZTA)** model based on the principle:

> **"Never Trust, Always Verify"**

The system continuously verifies user identity, role, and access privileges before granting access to enterprise resources.

---

## 🎯 Objectives

1. Implement a secure Zero Trust login portal
2. Enforce Role-Based Access Control (RBAC)
3. Prevent unauthorized access to protected resources
4. Apply micro-segmentation between employee and admin resources
5. Demonstrate continuous verification and least-privilege access
6. Improve enterprise security against insider and external threats

---

## 🛡️ Zero Trust Principles

| Principle | Description |
|------------|------------|
| Verify Explicitly | Authenticate every user before access |
| Least Privilege | Grant minimum required permissions |
| Assume Breach | Design security as if attackers are already present |
| Continuous Monitoring | Validate sessions continuously |
| Micro-Segmentation | Isolate critical resources |
| Identity-Centric Security | Security decisions based on identity |

---

## 🏗️ System Architecture

```text
                 ┌──────────────┐
                 │    User      │
                 └──────┬───────┘
                        │
                        ▼
              ┌──────────────────┐
              │ Login Portal     │
              └────────┬─────────┘
                       │
             Authentication & MFA
                       │
                       ▼
            ┌─────────────────────┐
            │ Access Control Unit │
            └───────┬─────────────┘
                    │
         ┌──────────┴──────────┐
         │                     │
         ▼                     ▼
 ┌───────────────┐    ┌───────────────┐
 │ Employee Zone │    │   Admin Zone  │
 └───────────────┘    └───────────────┘