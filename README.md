# Active Directory Lab 1.0 (In Progress)

This project documents my journey building an enterprise-style Active Directory environment in VirtualBox. The goal is to gain hands-on experience with domain controllers, user and group management, and network security concepts commonly used in blue team operations.

I’m currently following a video tutorial series and building out each part step-by-step while documenting issues, lessons learned, and improvements along the way.
 
---

## Planned Lab Topology

*A network diagram will be added here once the image is finalized and exported from draw.io.*

---

## Tools & Technologies

- VirtualBox
- Windows Server 2019 (Domain Controller)
- Windows 10 (Domain-joined client)
- Kali Linux (for testing and simulation)
- Draw.io (topology diagramming)

---

## What This Lab Will Include

- Installing and configuring a domain controller (DC)
- Creating and managing user accounts in Active Directory
- Joining Windows 10 to the domain
- Simulating attacks using Kali Linux
- Testing detections and logging with built-in tools
- Possible integration of Atomic Red Team four testing
---

## Why I’m Building This Lab

As a cybersecurity student at WGU and a Navy veteran, I’m building this home lab to learn by doing. I want to show hiring managers that I’m serious about transitioning into blue team work, and that I understand how enterprise systems function under the hood.

---

## Status

**Currently working on:**  
- Creating the VirtualBox network  
- Installing Windows Server  
- Drafting the topology diagram  

More updates and screenshots will be added soon.

---

## Author

Steven Loucks  
Cybersecurity Student | WGU | Navy Veteran  
[stevenloucks.tech](https://stevenloucks.tech)

---

## Lab Build Checklist (Work in Progress)

- [x] Install VirtualBox
- [ ] Create isolated network
- [~] Install Windows Server (DC) – *Not started*
- [~] Install Windows 10 – *In progress; ISO loaded but setup not completed*
- [~] Install Kali Linux – *In progress; install launched but unverified*
- [ ] Promote Server to domain controller
- [ ] Join Windows 10 to domain
- [ ] Create users, OUs, and GPOs
- [ ] Test login + Group Policy
- [ ] Capture logs or screenshots
- [ ] Add notes or errors here as needed...

---

**Status:** In Progress  
**Current Focus:** Troubleshooting Win10 and Kali installs  
**Next Step:** Finalize OS installations and verify clean boots

---

## Troubleshooting Log

This section tracks issues I’ve encountered while building the lab and what I did (or plan to do) to fix them.

- **[05/12/2025]** Windows 10 installation launched but not yet verified complete. ISO loaded inside VirtualBox; need to check post-install boot.
- **[05/12/2025]** Kali Linux install started but needs confirmation. Possibly missing guest additions or network setup.
- **[05/12/2025]** Draw.io diagram effort paused — current version cut off content when saved. Will rebuild from screenshot with clean layout tonight.
- **[05/12/2025]** No working NAT/isolated network tested yet. This will be focus after OS installs are confirmed.

*More entries will be added as lab development continues.*
