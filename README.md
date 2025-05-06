# Active Directory Lab 1.0  
*A VirtualBox-based enterprise environment built from scratch*

![Status](https://img.shields.io/badge/status-in--progress-orange)  
[My Portfolio](https://stevenloucks.tech) | [LinkedIn](https://www.linkedin.com/in/steven-loucks)

---

## Overview

This lab follows the [Myfdir Active Directory YouTube tutorial](https://www.youtube.com/@myfdir) to build a basic enterprise Active Directory environment. It simulates a small internal network using VirtualBox, with a domain controller (Windows Server 2019) and a Windows 10 client.

---

## Lab Objectives

- [ ] Install and configure a Windows Server 2019 domain controller (DC01)
- [ ] Set static IP, hostname, and promote to a domain controller
- [ ] Install and configure DNS and DHCP
- [ ] Create Organizational Units (OUs), users, and groups
- [ ] Join Windows 10 client to the domain (WIN10)
- [ ] Apply and verify Group Policy Objects (GPOs)

---

## Lab Topology

| Hostname | Role              | OS                  | IP Address       |
|----------|-------------------|---------------------|------------------|
| DC01     | Domain Controller | Windows Server 2019 | 192.168.56.10    |
| WIN10    | Client Workstation| Windows 10 Pro      | DHCP (Static Reserve) |

> **Network:** VirtualBox Host-Only Adapter (vboxnet0)

---

## Tools & Resources

| Tool / Resource        | Description                                  |
|------------------------|----------------------------------------------|
| VirtualBox             | VM hypervisor for lab isolation              |
| Windows Server 2019 ISO| Evaluation image used for domain controller |
| Windows 10 ISO         | Evaluation image for domain-joined client    |
| Myfdir's YouTube Series| Step-by-step visual guidance for setup       |

---

## Folder Structure

| Folder        | Contents                                    |
|---------------|---------------------------------------------|
| `/setup/`     | Step-by-step setup notes and configuration  |
| `/screenshots/` | Visuals of setup and system states        |
| `/gpos/`      | Documentation or exports of Group Policies  |
| `/scripts/`   | PowerShell or batch files used in the lab   |

---

## Referenced Modules

| Module Repo | Purpose |
|-------------|---------|
| _Coming Soon_ | Windows Server Secure Setup |
| _Coming Soon_ | GPO Best Practices Bundle |

---

## Screenshots

_Add these as you go, to show progress and outcomes:_

- Server Manager roles screen
- AD Users & Computers layout
- DNS zone config
- DHCP lease confirmation
- Client joined to domain
- GPO results (e.g., password policy, login banner)

---

## Progress Tracker

- [x] Repository created and structured
- [ ] Setup documented in `setup/setup.md`
- [ ] Screenshots added
- [ ] GPOs defined or exported
- [ ] Lab linked from portfolio
- [ ] Final review + polish

---

## License

This project is licensed under the [MIT License](LICENSE)

---

*Built by Steven Loucks — Cybersecurity Portfolio Project*
