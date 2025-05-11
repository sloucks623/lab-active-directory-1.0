# 🧠 Active Directory Lab 1.0 — MyDFIR Home Lab Project

This project is a fully documented build of the **MyDFIR Active Directory Home Lab** series. The goal is to simulate a real-world enterprise AD environment using VirtualBox, allowing me to learn core skills in system administration, networking, user management, and security monitoring.

---

## 🎯 Purpose

As a cybersecurity student, I built this lab to gain practical experience in managing Active Directory and its surrounding ecosystem. Every step mirrors a real-world scenario — from setting up a Domain Controller and configuring NAT to simulating adversary behavior. This lab will serve as portfolio proof to hiring managers that I can architect and troubleshoot enterprise-level systems.

---

## 🧰 Tools & Technologies Used

| Tool                | Purpose                            |
|---------------------|------------------------------------|
| VirtualBox          | VM virtualization platform         |
| Windows Server 2019 | Domain Controller OS               |
| Windows 10          | Client machine OS                  |
| draw.io             | Lab topology diagram               |
| Kali Linux          | Adversary simulation               |
| Sysmon              | Endpoint event logging             |
| Splunk              | Log analysis and correlation       |
| Atomic Red Team     | Simulated attack framework         |

---

## 🗂️ Project Structure

```plaintext
lab-active-directory-1.0/
│
├── assets/
│   └── ad-lab1-topology.drawio      # Original diagram file
│   └── ad-lab1-topology.png         # Exported topology image
│
├── part1_domain-controller.md
├── part2_nat-setup.md
├── part3_users-and-ous.md
├── part4_client-join-domain.md
├── part5_monitoring-and-attacks.md
│
└── README.md                        # This file
