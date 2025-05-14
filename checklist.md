# ✅ AD Lab 1.0 – Build Checklist

This file tracks the full lab build process. It’s a live document and will grow as the lab evolves.

---

## 🔨 Current Status

### 🧱 VM Setup
- [x] Windows 10 installed
- [x] Server 2022 installed
- [ ] Kali ISO downloaded
- [ ] Splunk installer downloaded
- [x] Snapshots created (baseline)

---

### 🖧 Networking
- [ ] NAT adapter enabled for internet access
- [ ] Host-Only adapter created for internal lab
- [ ] Static IP set on Server
- [ ] VMs can ping each other

---

### 🛠️ Server 2022 Configuration
- [ ] Rename to `DC01`
- [ ] Set static IP (Host-Only network)
- [ ] Install Active Directory Domain Services (AD DS)
- [ ] Promote to domain controller
- [ ] Configure DNS and domain: `adlab.local`

---

### 💼 Windows 10 Configuration
- [ ] Rename to `WIN10-CLT`
- [ ] Join `adlab.local` domain
- [ ] Create and test login with domain user

---

### 🧪 Tools & Red Team Setup
- [ ] Install Kali Linux
- [ ] Install Splunk (Free version)
- [ ] Enable Windows Event Forwarding (WEC)
- [ ] Install Sysmon
- [ ] Connect logs to Splunk

---

### 📖 Documentation Tasks
- [x] README created
- [x] Diagram added
- [ ] Screenshot VM configs
- [ ] Add GitHub lab page link to portfolio
- [ ] Document any errors/fixes
