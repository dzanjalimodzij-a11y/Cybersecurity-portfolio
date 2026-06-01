# Lab Setup — Windows Sysmon Detection Lab

## Environment Overview

| Component | Details |
|-----------|---------|
| Virtualisation Platform | [e.g., VMware Workstation / VirtualBox / Hyper-V] |
| Network Type | Host-only / NAT isolated — no internet access from lab VMs |
| VM 1 — Workstation | Windows 10 Pro (version [X]) |
| VM 2 — Domain Controller | Windows Server 2019 (version [X]) |
| SIEM Host | [Running on host machine / separate VM — specify] |

---

## Network Diagram

> 📁 Insert network diagram here or reference `../../assets/diagrams/sysmon-lab-network.png`

```
[PLACEHOLDER — Add network diagram]

Example layout:
  Attacker/Analyst (Host OS)
        |
  [Host-only Network: 192.168.x.0/24]
        |
  ┌─────────────┐     ┌─────────────────────┐
  │  Win10 WS   │────▶│  Win Server 2019 DC │
  │ 192.168.x.10│     │   192.168.x.5       │
  └─────────────┘     └─────────────────────┘
```

---

## Step-by-Step Setup

### 1. Virtual Machine Configuration

- Created two Windows VMs in [hypervisor name]
- Both VMs placed on an isolated host-only network
- Disabled internet access on lab VMs to contain simulated activity
- Configured static IP addresses for consistent log attribution

### 2. Active Directory Setup

- Promoted Windows Server 2019 to Domain Controller
- Domain name: `[PLACEHOLDER — e.g., lab.local]`
- Created test user accounts for simulation purposes
- Joined Windows 10 workstation to domain

### 3. Sysmon Installation

```powershell
# Download Sysmon from Microsoft Sysinternals
# https://docs.microsoft.com/en-us/sysinternals/downloads/sysmon

# Install with configuration file
sysmon64.exe -accepteula -i sysmonconfig.xml
```

- Configuration file used: [e.g., SwiftOnSecurity sysmon-config / Olaf Hartong modular config]
- Key event IDs enabled: 1 (Process Create), 3 (Network Connect), 7 (Image Load), 8 (CreateRemoteThread), 10 (ProcessAccess), 11 (FileCreate), 12/13 (Registry), 17/18 (Pipe), 22 (DNS Query)

### 4. Log Forwarding to SIEM

> *[Add steps specific to your chosen SIEM — Splunk Universal Forwarder / Elastic Winlogbeat / Wazuh Agent]*

```
[PLACEHOLDER — Add your log forwarding configuration steps here]
```

### 5. SIEM Configuration

- Created index/data stream for Sysmon events
- Configured field mappings for key Sysmon fields (Image, ParentImage, CommandLine, etc.)
- Verified log ingestion with a test process creation event

---

## Verification Checklist

- [ ] Both VMs running and joined to domain
- [ ] Sysmon installed and service running on both VMs
- [ ] Sysmon events visible in Event Viewer (Event Log: Microsoft-Windows-Sysmon/Operational)
- [ ] Logs forwarding successfully to SIEM
- [ ] SIEM index receiving events in near real-time
- [ ] Test detection rule firing correctly

---

## Screenshots

> 📁 Add screenshots to `screenshots/` folder

- `[PLACEHOLDER]` — Sysmon service running (services.msc)
- `[PLACEHOLDER]` — Sysmon events in Event Viewer
- `[PLACEHOLDER]` — SIEM receiving logs
