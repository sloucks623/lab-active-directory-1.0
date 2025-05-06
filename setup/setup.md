
# Active Directory Lab 1.0 – Setup Instructions

This file documents the setup and configuration steps based on Myfdir’s YouTube tutorial for building a Windows AD lab in VirtualBox.

---

## Lab Requirements

- VirtualBox installed
- Windows Server 2019 ISO
- Windows 10 Pro ISO
- Host OS: Windows 11 (or equivalent)

---

## VM Configuration

### Windows Server 2019 (DC01)

- 2 CPUs, 4096MB RAM
- Static IP: 192.168.56.10
- Host-only adapter
- Installed AD DS, DNS, DHCP

### Windows 10 (WIN10)

- 2 CPUs, 4096MB RAM
- Host-only adapter
- DHCP (from DC01)
- Will be joined to the domain

---

## Step-by-Step Progress (checklist format)

- [ ] Install Windows Server 2019 VM
- [ ] Configure static IP and hostname
- [ ] Promote to Domain Controller
- [ ] Install DHCP and configure scope
- [ ] Create AD users, OUs, and groups
- [ ] Install Windows 10 VM
- [ ] Join client to domain
- [ ] Apply and test GPOs

---

## Notes

- Admin account created: `Admin01`
- Domain name used: `corp.local`
- VM Host-only network: `vboxnet0`

---

*Documented by Steven Loucks – Cybersecurity Portfolio Project*

