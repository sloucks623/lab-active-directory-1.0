# Active Directory Lab 1.0

This hands-on lab follows Myfdir’s YouTube tutorial to build a basic Windows Active Directory environment using VirtualBox and evaluation ISOs. It simulates a small enterprise setup with a domain controller and client system.

## Objectives

- Set up a Windows Server 2019 (or 2022) Domain Controller
- Configure Active Directory Domain Services (AD DS)
- Install and configure DNS and DHCP
- Create Organizational Units (OUs), users, and groups
- Join a Windows 10 client to the domain
- Apply Group Policy Objects (GPOs)

## Tools Used

- VirtualBox
- Windows Server 2019 ISO
- Windows 10 ISO
- Myfdir's AD Lab Tutorial: [Watch on YouTube](https://www.youtube.com/@myfdir)

## Architecture Overview

| Host | Role                | OS                 | IP Address        |
|------|---------------------|--------------------|-------------------|
| DC01 | Domain Controller   | Windows Server 2019| 192.168.56.10     |
| WIN10| Client Workstation  | Windows 10 Pro     | DHCP (from DC01)  |

## Screenshots & Documentation

| Folder         | Description                                  |
|----------------|----------------------------------------------|
| `screenshots/` | Visuals of setup steps and final topology    |
| `setup/`       | Configuration steps and notes                |
| `gpos/`        | Exported or described Group Policies         |
| `scripts/`     | Any PowerShell scripts used (optional)       |

## Referenced Modules

- [Windows Server 2019 Domain Setup](https://github.com/StevenLoucks/module-winserver2019-setup) *(coming soon)*

## Status

- [x] Repo created
- [ ] Setup steps documented
- [ ] Screenshots uploaded
- [ ] GPOs summarized
- [ ] Lab linked to portfolio site

## License

MIT License (see LICENSE file)

---

*Built and documented by Steven Loucks – Cybersecurity Portfolio*
