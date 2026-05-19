# Moses Kinuthia

### Security Operations Analyst | Banking Fraud & Detection Background

Banking professional transitioning into security operations. I bring fraud-detection,
KYC, and AML experience from a tier-1 bank to the SOC context — where business-domain
judgment and evidence-based investigation matter as much as technical tooling.

I built and operate a full SOC home lab from scratch, run adversarial simulations,
and document everything at analyst depth.

---

## Certifications

| Certification | Issuer | Status |
|---|---|---|
| CompTIA Security+ | CompTIA | ✅ Achieved |
| Cisco CyberOps Associate | Cisco | ✅ Achieved |
| Certified in Cybersecurity (CC) | ISC2 | ✅ Achieved |
| Microsoft SC-200 | Microsoft | 🔄 In Progress |

---

## SOC Home Lab

A two-machine, four-segment lab environment built and debugged from scratch.

| Component | Technology |
|---|---|
| Firewall / Router | pfSense (WAN / LAN / OPT1 management / OPT2 attack) |
| SIEM / XDR | Wazuh 4.x |
| Domain Controller | Windows Server 2019 — DC01 (SOCLAB.local) |
| Endpoint | Windows 10 Enterprise — WKSTNO1 |
| Attack Platform | Kali Linux (isolated OPT2 segment) |
| Endpoint Telemetry | Sysmon deployed via GPO |

Full architecture, configuration files, and build notes:
→ [soc-home-lab](https://github.com/Moses-Kinuthia/soc-home-lab)

---

## SOC Simulations

| # | Scenario | MITRE | Status | Report |
|---|---|---|---|---|
| 001 | SMB Brute Force → Account Takeover | T1110, T1078 | ✅ Complete | [SIM-001](https://github.com/Moses-Kinuthia/simulation-writeups/blob/main/simulations/SIM-001-SMB-Brute-Force.md) |
| 002 | Network Reconnaissance | T1046 | ✅ Complete | [SIM-002](https://github.com/Moses-Kinuthia/simulation-writeups/blob/main/simulations/SIM-002-Network-Recon.md) |
| 003 | AD Enumeration | T1087 | ✅ Complete | [SIM-003](https://github.com/Moses-Kinuthia/simulation-writeups/blob/main/simulations/SIM-003-AD-Enumeration.md) |
| 004 | Insider Threat — Backdoor + Log Clearing | T1136.001, T1070.001 | ✅ Complete | [SIM-004](https://github.com/Moses-Kinuthia/simulation-writeups/blob/main/simulations/SIM-004-Insider-Threat.md) |
| 005 | Lateral Movement — SMB Pivot + Kerberoasting | T1021.002, T1558.003 | ✅ Complete | [SIM-005](https://github.com/Moses-Kinuthia/simulation-writeups/blob/main/simulations/SIM-005-Lateral-Movement.md) |

---

## Technical Skills

**Security tooling:** Wazuh, pfSense, Sysmon, Kali Linux, Nmap, Hydra, Metasploit,
netexec, enum4linux, Wireshark

**Infrastructure:** Windows Server 2019, Active Directory, Group Policy, VirtualBox

**Detection & analysis:** SIEM rule writing (Wazuh OSSEC rule syntax, pcre2),
Windows Event ID analysis, MITRE ATT&CK mapping, log-based investigation

**Scripting:** Python (alert enrichment, API integration, log parsing),
PowerShell (AD administration, attack simulation)

**Compliance:** PCI-DSS, NIST CSF (via Wazuh SCA), Kenya Data Protection Act

---

## Key Windows Event IDs I Monitor

| Event ID | Detection Purpose |
|---|---|
| 4624 | Successful logon — baseline and ATO correlation |
| 4625 | Failed logon — brute force detection |
| 4720 | Account creation — persistence detection |
| 4728 / 4732 | Privileged group membership change |
| 4740 | Account lockout |
| 4769 | Kerberos TGS request — Kerberoasting detection |
| 1102 | Security audit log cleared — critical indicator |
| Sysmon 1 | Process creation — execution and lateral movement |
| 4104 | PowerShell script-block — enumeration visibility |

---

## Featured Repositories

| Repository | Description |
|---|---|
| [Financial-Fraud-Cyber-Threat-Detection-Pipeline](https://github.com/Moses-Kinuthia/Financial-Fraud-Cyber-Threat-Detection-Pipeline) | End-to-end detection engineering: ATO, insider threat, and lateral movement — mapped to MITRE, PCI-DSS, and banking fraud scenarios |
| [soc-home-lab](https://github.com/Moses-Kinuthia/soc-home-lab) | Full lab architecture, configuration files, and build narrative including real troubleshooting |
| [simulation-writeups](https://github.com/Moses-Kinuthia/simulation-writeups) | Incident-style investigation reports for each simulated attack |

---

## Connect

- LinkedIn: [linkedin.com/in/moses-waweru-kinuthia](https://linkedin.com/in/moses-waweru-kinuthia)
- Location: Nairobi, Kenya
