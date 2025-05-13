# Active Directory Lab 1.0 (In Progress)

This project documents my journey building an enterprise-style Active Directory environment in VirtualBox. The goal is to gain hands-on experience with domain controllers, user and group management, and network security concepts commonly used in blue team operations.

I’m currently following a video tutorial series and building out each part step-by-step while documenting issues, lessons learned, and improvements along the way.
 
---

## Planned Lab Topology
## Lab Topology Diagram

This diagram shows the full environment for AD Lab 1.0, based on MyDFIR's home lab design. It includes the domain controller, client, attacker, Splunk server, and network layout.

![AD Lab 1.0 Topology](/diagrams/ad-lab1.0.drawio.png)

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
## 🧰 Build Checklist

- [x] Install VirtualBox
- [ ] Create isolated network
- [~] Install Windows Server (Domain Controller) – *Not started*
- [x] Install Windows 10 – *VM downloaded and installed successfully*
- [~] Install Kali Linux – *Failed due to outdated tutorial (7-Zip method); switching to .ova method tonight*
- [ ] Promote Server to Domain Controller
- [ ] Join Windows 10 to Domain
- [ ] Create Users, OUs, and GPOs
- [ ] Configure Sysmon and Splunk Forwarder
- [ ] Send logs to Splunk server (192.168.10.10)
- [ ] Test login and Group Policy
- [ ] Capture logs or screenshots

---

---

## Server Install Notes (Student/Home Setup)

This lab uses the **free evaluation version** of Windows Server — legal and fully functional for 180 days. No license or enterprise resources are required.

> Note: Although the tutorial mentions Server 2019, the system may display Windows Server 2022 depending on the image used. This lab follows the 2019-based layout.

### Download Link:
[Windows Server Evaluation Center (Microsoft)](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server)

- Recommended: **Windows Server 2019 ISO** (Standard Desktop Experience)

---

### Step-by-Step: Installing Windows Server in VirtualBox

1. **Create VM**
   - Name: `WinServer2019`
   - Type: `Microsoft Windows`
   - Version: `Windows 2019 (64-bit)`
   - RAM: 4096 MB (or more)
   - Virtual hard disk: VDI, dynamically allocated, at least 50 GB

2. **Mount ISO**
   - Go to VM settings → Storage → Add ISO under Controller: IDE
   - Select the downloaded `.iso` file

3. **Start the VM and Install**
   - Choose: **Windows Server 2019 Standard Evaluation (Desktop Experience)**
   - Select “Custom Install”
   - Format the disk and proceed with installation

4. **Initial Setup**
   - After first reboot, set the local Administrator password
   - Skip license key — the Eval version activates automatically (180-day watermark)

---

---

## Server Install Notes (Student/Home Setup)

This lab uses the **free evaluation version** of Windows Server — legal and fully functional for 180 days. No license or enterprise resources are required.

> Note: Although the tutorial mentions Server 2019, the system may display Windows Server 2022 depending on the image used. This lab follows the 2019-based layout.

### Download Link:
[Windows Server Evaluation Center (Microsoft)](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server)

- Recommended: **Windows Server 2019 ISO** (Standard Desktop Experience)

---

### Step-by-Step: Installing Windows Server in VirtualBox

1. **Create VM**
   - Name: `WinServer2019`
   - Type: `Microsoft Windows`
   - Version: `Windows 2019 (64-bit)`
   - RAM: 4096 MB (or more)
   - Virtual hard disk: VDI, dynamically allocated, at least 50 GB

2. **Mount ISO**
   - Go to VM settings → Storage → Add ISO under Controller: IDE
   - Select the downloaded `.iso` file

3. **Start the VM and Install**
   - Choose: **Windows Server 2019 Standard Evaluation (Desktop Experience)**
   - Select “Custom Install”
   - Format the disk and proceed with installation

4. **Initial Setup**
   - After first reboot, set the local Administrator password
   - Skip license key — the Eval version activates automatically (180-day watermark)

---

To verify which version you're using:
```bash
winver

## 🛠️ Troubleshooting Log

- **[05/13/2025]** Windows Server ISO download failed due to network throttling.
- **[05/13/2025]** Kali Linux installation incomplete; verification pending.
- **[05/13/2025]** Attempted library network; encountered early closing hours and unfamiliar system layouts.
