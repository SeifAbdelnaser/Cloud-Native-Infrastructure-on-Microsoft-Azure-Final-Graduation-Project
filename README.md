# Cloud-Native-Infrastructure-on-Microsoft-Azure-Final-Graduation-Project
"Final Graduation Project: Cloud-Native Infrastructure on Microsoft Azure"
# ☁️ Cloud-Native Infrastructure on Microsoft Azure

> A cloud-native enterprise infrastructure deployed on Microsoft Azure, integrating Windows Server 2022, Ubuntu Server, Active Directory, Azure Networking, Nginx Reverse Proxy, Docker, and enterprise storage services.

![Azure](https://img.shields.io/badge/Microsoft-Azure-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)
![Windows Server](https://img.shields.io/badge/Windows%20Server-2022-0078D6?style=for-the-badge&logo=windows)
![Ubuntu](https://img.shields.io/badge/Ubuntu-24.04-E95420?style=for-the-badge&logo=ubuntu)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx)
![Active Directory](https://img.shields.io/badge/Active%20Directory-Windows-blue?style=for-the-badge)

---

# 📌 Overview

This project demonstrates the design and implementation of a **Cloud-Native Enterprise Infrastructure** on Microsoft Azure.

The environment simulates a production-ready enterprise network where Windows and Linux platforms operate under a unified infrastructure, providing centralized identity management, secure networking, highly available web services, enterprise file sharing, containerized workloads, and automated backup solutions.

---

# 🎯 Project Objectives

- Deploy secure Azure cloud infrastructure
- Build an Active Directory environment
- Integrate Linux with Active Directory
- Configure enterprise storage services
- Implement Layer 7 Load Balancing
- Deploy containerized workloads
- Automate backup and disaster recovery

---

# 🏗 Architecture

## Infrastructure Overview

```
                    Microsoft Azure

                Azure Virtual Network
                 192.168.1.0/24
                        │
        ┌───────────────┴────────────────┐
        │                                │
  Server Subnet                    Client Subnet
        │                                │
        │                          Windows 11
        │
 ┌───────────────┐
 │ Primary DC    │
 │ Windows 2022  │
 │ AD DS + DNS   │
 │ IIS           │
 └───────────────┘
          │
          │ Replication
          │
 ┌───────────────┐
 │ Additional DC │
 │ Windows Core  │
 │ IIS           │
 └───────────────┘
          │
          │
 ┌────────────────────────────┐
 │ Ubuntu Server              │
 │                            │
 │ • Nginx Reverse Proxy      │
 │ • Samba                    │
 │ • Docker                   │
 │ • Automated Backup         │
 │ • Linux AD Integration     │
 └────────────────────────────┘
```

---

# 🖼 Architecture Diagram



```

<img width="1275" height="705" alt="WhatsApp Image 2026-07-23 at 5 15 41 AM" src="https://github.com/user-attachments/assets/8769eb69-8732-445e-97be-6c56a321ad65" />

---

# 🖥 Virtual Machines

| Machine | Role |
|---------|------|
| PDC | Active Directory, DNS, IIS |
| ADC | Additional Domain Controller, IIS |
| Ubuntu Server | Nginx, Samba, Docker, Backup |
| Windows 11 | Domain Client |

---

# 🌐 Azure Infrastructure

- Azure Virtual Network
- Network Security Groups (NSGs)
- Server Subnet
- Client Subnet
- Static IP Assignment
- Firewall Rules

---

# 🔐 Identity Management

- Active Directory Domain Services
- DNS
- Organizational Units
- Security Groups
- Group Policy Objects (GPO)
- Password Policies
- Account Lockout Policy
- Remote Desktop Policy

---

# 🐧 Linux Integration

Ubuntu Server joined to Active Directory using:

- Kerberos
- SSSD
- Realmd
- Samba
- Winbind

---

# 📂 Storage Services

Implemented:

- Samba File Server
- Access Control Lists (ACLs)
- Sticky Bit
- File Screening
- Storage Quotas

---

# 🌍 Web Services

The project uses a Layer 7 Reverse Proxy.

```
Internet

     │

www.final.local

     │

 Nginx Reverse Proxy

     │

 ┌─────────────┐
 │             │
PDC IIS     ADC IIS
```

Features:

- Nginx Reverse Proxy
- IIS
- Load Balancing
- Health Checks

---

# 🐳 Docker

Docker Engine deployed on Ubuntu Server for containerized workloads.

Features

- Container Isolation
- Persistent Storage
- Automation

---

# 💾 Backup & Disaster Recovery

Implemented:

- Linux Cron Jobs
- Automated Backups
- Compressed Archives
- Recovery Storage
- Disaster Recovery Workflow

---

# 📷 Screenshots

## Azure Infrastructure



## Active Directory



## Group Policy



## DNS



## Samba



## Nginx Reverse Proxy


## Docker


## Backup Automation


# 🧪 Validation

✔ Active Directory Authentication

✔ Linux Domain Join

✔ Samba File Access

✔ Layer 7 Load Balancing

✔ File Screening

✔ Storage Quotas

✔ Docker Deployment

✔ Automated Backup

---

# 🛠 Technologies

- Microsoft Azure
- Windows Server 2022
- Ubuntu Server 24.04
- Active Directory
- DNS
- Group Policy
- Azure Virtual Network
- Network Security Groups
- Samba
- Nginx
- Docker
- IIS
- Kerberos
- SSSD
- Linux ACL
- Bash
- Cron Jobs

---

# 📚 Skills Demonstrated

- Cloud Infrastructure
- Windows Administration
- Linux Administration
- Identity Management
- Azure Networking
- Storage Administration
- High Availability
- Automation
- Disaster Recovery
- Technical Documentation

---

# 👥 Team

Developed as the final project for the **System Administration Internship at Education For Employment (EFE)**.

---

# 👨‍💻 Author

**Saif Abdelnasser**

- [LinkedIn](https://www.linkedin.com/in/seif-abdelnaser-7a3b03226)
- [GitHub](https://github.com/SeifAbdelnaser)


---

⭐ If you found this project interesting, feel free to star the repository.
