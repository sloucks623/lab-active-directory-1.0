# Active Directory Lab 1.0 – Executive Summary

This lab project replicates a functional enterprise environment based on the MyDFIR Active Directory tutorial series. 
It simulates real-world Red vs. Blue team scenarios for training in system administration, security hardening, domain control, and network monitoring.

## Key Components
- Windows Server 2019 Domain Controller (AD DS, DNS)
- Windows 10 Blue Team Workstation (Domain-joined)
- Kali Linux Red Team Attacker (Recon & enumeration tools)
- Ubuntu Server with SIEM Stack (Wazuh/Splunk-style logging)

## Lab Objectives
- Deploy and configure a Windows domain environment.
- Join client machines to domain and create user OUs.
- Apply group policies to enforce security settings.
- Simulate attacker behavior using Kali tools.
- Forward logs to a SIEM system for detection and analysis.

## Skills Demonstrated
- PowerShell automation (e.g., bulk user creation, role installs)
- Group Policy Management (GPMC, RSOP, gpupdate)
- Network configuration and DNS troubleshooting
- Red Team recon using tools like Nmap, SMBClient, Responder
- Event log forwarding and centralized monitoring (Syslog/SIEM)

## Toolset
VirtualBox, Windows Server 2019, Windows 10 Pro, Kali Linux, Ubuntu Server 22.04, 
Active Directory, GPMC, PowerShell, Wazuh/Splunk, and open-source Red Team tools.

---

This hands-on lab provides a practical foundation in domain management, attack simulation, and log analysis.
