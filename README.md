# 🧠 Active Directory Lab 1.0 — MyDFIR Home Lab Project

This project is a fully documented build of the **Active Directory Home Lab** tutorial series by **MyDFIR** on YouTube. The goal is to simulate a real-world enterprise AD environment using VirtualBox, providing hands-on experience with domain setup, network configuration, user management, and security monitoring.

---

## 🎯 Purpose

As a cybersecurity student, I built this lab to deepen my understanding of Windows domain environments and Active Directory. Every step follows enterprise-style practices — from configuring NAT and DNS to simulating attacks — to prepare me for real-world IT and security roles.

This lab also serves as a portfolio project to **demonstrate to hiring managers** that I can independently plan, configure, troubleshoot, and document an enterprise-style AD environment.

---

## 📺 Tutorial Reference

This lab follows the full YouTube series:

> **[Active Directory Home Lab (YouTube) — by MyDFIR](https://www.youtube.com/watch?v=5OessbOgyEo)**  
> Part 0 – Intro + Tools  
> Parts 1–5 cover domain setup, NAT, users/OUs, client join, monitoring, and attack simulation.

---

## 🧰 Tools & Technologies Used

| Tool                | Purpose                            |
|---------------------|------------------------------------|
| VirtualBox          | Virtual machine host               |
| Windows Server 2019 | Domain Controller OS               |
| Windows 10          | Client machine OS                  |
| draw.io             | Visual topology diagram            |
| Kali Linux          | Simulated attacker machine         |
| Sysmon              | Event log collection               |
| Splunk              | Log analysis and detection         |
| Atomic Red Team     | Simulated adversary techniques     |

---

## 🗂️ Project Structure

```plaintext
lab-active-directory-1.0/
│
├── assets/
│   └── ad-lab1-topology.drawio      # Original editable diagram
│   └── ad-lab1-topology.png         # Exported image for README
│
├── part1_domain-controller.md
├── part2_nat-setup.md
├── part3_users-and-ous.md
├── part4_client-join-domain.md
├── part5_monitoring-and-attacks.md
│
└── README.md                        # This file
