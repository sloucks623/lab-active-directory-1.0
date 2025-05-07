# Active Directory Lab 1.0 – Red vs Blue Lab Environment

This lab is built following the MyDFIR YouTube tutorial series. It simulates a real-world enterprise environment for practicing Blue Team defense, Red Team tactics, and centralized SIEM logging, using a variety of open-source and enterprise-grade tools.

---

## Lab Topology

> *[Custom network diagram will be inserted here later]*

This lab consists of four virtual machines connected in an isolated VirtualBox Internal Network (`10.0.0.0/24`):

- **Windows Server 2019 (DC01)**: Domain Controller running AD DS and DNS services
- **Windows 10 Pro (WIN10)**: Blue Team client machine joined to the domain
- **Kali Linux**: Red Team attacker box for network recon and attack emulation
- **Ubuntu Server 22.04 (SIEM01)**: Centralized logging server using Wazuh or Splunk

These VMs simulate a Red vs Blue scenario with log correlation, GPO enforcement, and adversary simulation tooling.

---

## Components & Roles

| VM Name   | Role                   | OS / Tools                                        | IP Address  |
|-----------|------------------------|--------------------------------------------------|-------------|
| DC01      | Domain Controller      | Windows Server 2019, AD DS, DNS                   | 10.0.0.5    |
| WIN10     | Blue Team Workstation  | Windows 10 Pro, GPMC, RDP, PowerShell             | 10.0.0.10   |
| Kali      | Red Team Attacker      | Kali Linux, Nmap, Impacket, Atomic Red Team       | 10.0.0.15   |
| SIEM01    | Logging Server         | Ubuntu Server 22.04, Wazuh / Splunk, NXLog        | 10.0.0.50   |

---

## Red Team & SIEM Components

- **Red Team (Kali):**
  - Tools: Nmap, CrackMapExec, Impacket, Responder, SMBClient, BloodHound (optional)
  - Adversary simulation: [Atomic Red Team](https://github.com/redcanaryco/atomic-red-team) used to trigger defensive detection logic

- **Blue Team (WIN10 + DC01):**
  - Tools: Group Policy Management Console, Event Viewer, PowerShell, RDP
  - Tasks: Enforce password and logon policies, monitor group membership and authentication behavior

- **SIEM/EDR (Ubuntu):**
  - Tools: Wazuh or Splunk, Log forwarders (Winlogbeat/NXLog), Sysmon
  - Role: Monitor and correlate Windows event logs, detect Atomic Red Team tests, visualize attacker patterns

---

## Setup Instructions

See the lab documentation inside this repository for:

- [x] Domain Controller promotion and DNS setup
- [x] Client configuration and domain join
- [x] User/Group/OUs with PowerShell
- [x] GPO implementation and enforcement
- [x] Atomic Red Team setup and test execution
- [x] SIEM configuration and log forwarding

---

## Executive Summary

For a concise overview of this lab and what it demonstrates technically, see the [Executive Summary](./EXECUTIVE_SUMMARY.md).

---

## Credits

This lab is based on the excellent [MyDFIR Active Directory Home Lab](https://www.youtube.com/@MyDFIR) video series, with added integration of open-source detection tools and Atomic Red Team.
