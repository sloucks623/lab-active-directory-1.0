# Active Directory Lab 1.0 – Installation Walkthrough and Notes

This guide provides exact step-by-step instructions for building the lab environment, including key notes from personal experience during setup and troubleshooting.

---

## 1. VirtualBox Setup
- Download: https://www.virtualbox.org
- Install with default settings.
- Create a new **Host-only Network** under File > Host Network Manager.
- Name it `ADLabNet`. No DHCP. Use IP range like 192.168.10.1/24.

## 2. Windows Server 2022
- New VM: 2 cores, 4–6GB RAM, 60GB disk
- Attach ISO and install OS
- Static IP: 192.168.10.5
- Rename system and enable RDP
- **Issue encountered:** GUI installer failed when using NAT+Internal adapter. Fixed by removing NAT and using internal-only.

## 3. Promote to Domain Controller
- In Server Manager: Add Roles > Active Directory Domain Services
- Use `dcpromo` or post-install wizard
- Domain: `adlab.local`
- Reboot to complete
- **Note:** DNS and DHCP configured automatically

## 4. Windows 10 Client
- Install Win10 on another VM
- IP: 192.168.10.100
- Join Domain: System > About > Join Domain
- Reboot, then login as domain user
- **Fix:** Time sync issues caused join to fail until DC and client clocks were aligned

## 5. Kali Linux
- Download ISO from https://kali.org
- Use VBox defaults; adjust memory and processors
- Adapter: Internal Network `ADLabNet`
- `sudo apt update && apt upgrade`
- Still need to test AD tools + attack surface

## 6. Splunk Free
- Download from https://splunk.com
- Choose Windows installer, run on Server
- Accept defaults. Create admin login.
- Verify: `https://localhost:8000`
- **Note:** Avoid installing on client or Kali. Use DC only.

## 7. Sysmon + Winlogbeat
- Sysmon: https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon
- Use SwiftOnSecurity config for best visibility
  - `Sysmon64.exe -accepteula -i sysmonconfig.xml`
- Winlogbeat:
  - Download from Elastic
  - Edit `winlogbeat.yml` to send logs to Splunk

## 8. Atomic Red Team
- `git clone https://github.com/redcanaryco/atomic-red-team.git`
- Install Pester in PowerShell
- Run Atomic tests manually or using `Invoke-AtomicTest`
- Confirm event logs show up in Splunk
- **To-do:** Add examples and mapped MITRE techniques

---

## Troubleshooting Log

- VM clock mismatch blocked domain join
- Windows Server GUI install failed when NAT was present
- File sharing between Kali and Windows VMs required enabling Guest Additions and folder sync
- Splunk login loop occurred — fixed by clearing cookies + verifying port 8000 access from localhost only

---

## Screenshots

_TODO: Insert link or folder path to relevant images once added._

---

**Return to main lab summary**: [README.md](../README.md)
