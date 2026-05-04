# 🛡️ Moses's Security Operations Center

### 👨‍💻 SOC Analyst | Blue Teamer | Threat Hunter

Welcome to my digital workshop. I focus on **defensive security**, monitoring network telemetry, and building resilient environments. I believe that security is not a product, but a continuous process of detection and response.

---
### 🏅 Certifications
| Certification | Issuer | Status |
| :--- | :--- | :--- |
| **CompTIA Security+** | CompTIA | ✅ Achieved |
| **Cisco CyberOps Associate** | Cisco | ✅ Achieved |
| **Certified in Cybersecurity (CC)** | ISC2 | ✅ Achieved |
| **Introduction to log Analysis** | Red Team Leaders | ✅ Achieved |

---
### 🔬 Home SOC Lab
I built and operate a two-machine SOC home lab running a realistic mini-enterprise environment.

#### **Infrastructure**
| Component | Technology | Role |
| :--- | :--- | :--- |
| **Firewall/Router** | pfSense | Network segmentation, NAT, firewall rules |
| **SIEM** | Wazuh | Alert generation, log correlation, compliance |
| **Attack Machine** | Kali Linux | Red team simulations |
| **Domain Controller** | Windows Server 2019 | Active Directory, DNS, GPO |
| **Domain Client** | Windows Enterprise | Endpoint monitoring target |
| **Hypervisor** | VirtualBox | VM management on both hosts |

---

#### **Network Architecture**
```text
[Internet]
     |
[Home Router] (192.168.x.1)
     |
     +--- Machine A (Windows 11 Host)
     |    ├── pfSense VM (WAN: 192.168.8.x | LAN: 10.0.0.x | OPT1: 10.0.10.x | OPT2: 10.0.20.x)
     |    └── Wazuh Server (10.0.10.x - Isolated Management Segment)
     |
     | (Physical Ethernet Bridge)
     |
     +--- Machine B (Windows 10 Host)
          ├── Kali Linux (10.0.20.x - Isolated Attacker Segment)
          ├── Windows Server 2019 (DC01: 10.0.0.x)
          └── Windows Enterprise (WKSTN01: 10.0.0.x)
```
---

#### **What I've Built and Configured**
* ✅ **pfSense firewall** with multi-interface routing (WAN/LAN/OPT1/OPT2)
* ✅ **Network segmentation** — attack segment isolated from AD/management
* ✅ **Wazuh SIEM** with live alert ingestion from 2 Windows agents
* ✅ **Sysmon** deployed on both Windows machines for enhanced telemetry
* ✅ **Active Directory domain (SOCLAB.local)** with DC and joined client
* ✅ **Wazuh agents** reporting to SIEM with MITRE ATT&CK mapping
* ✅ **pfSense firewall rules** with default-deny and explicit allow policies
* ✅ **Centralized agent configuration** pushed from Wazuh manager

---

### 🔴 SOC Simulations
| # | Simulation | Tools | Detection | MITRE | Status |
|---|---|---|---|---|---|
| 001 | Network Reconnaissance | Nmap | Wazuh custom rule 100020 — Event 5152 | T1046 | ✅ Complete |
| 002 | SMB Credential Stuffing (ATO) | netexec | Wazuh rules 18152, 18154 — Events 4625, 4740 | T1110.003 | ✅ Complete |
| 003 | Insider Threat — Privileged Abuse | PowerShell (native) | Wazuh rules 18110, 63102 — Events 4720, 1102 | T1078.002, T1070.001 | ✅ Complete |
| 004 | Lateral Movement via SMB | netexec | Wazuh rules 100020, 100021 — Events 4624, 4769 | T1021.002, T1558.003 | ✅ Complete |

---

### 🛠️ Technical Skills
* **Security Tools:** Wazuh, pfSense, Kali Linux, Nmap, Hydra, Metasploit, enum4linux, Sysmon, Wireshark
* **Infrastructure:** Windows Server 2019, Active Directory, Group Policy, VirtualBox, pfSense
* **Concepts:** SIEM / Log Analysis, Incident Detection, Firewall Rule Management, Network Segmentation, MITRE ATT&CK, Windows Event IDs
* **Compliance:** PCI DSS, HIPAA, GDPR, NIST (Wazuh-mapped)

---

#### **📊 Key Windows Event IDs I Monitor**
* `4625` Failed logon (Brute force detection)
* `4624` Successful logon (Lateral movement)
* `4720` Account created (Persistence)
* `4726` Account deleted (Defense evasion)
* `4648` Explicit credential use (Pass-the-hash)
* `4672` Special privileges assigned (Privilege escalation)
* `5152` WFP blocked packet (Network anomaly)

---

### 📁 Featured Repositories
* [**soc-home-lab**][soc-home-lab](https://github.com/Moses-Kinuthia/soc-home-lab) – Full documentation of my SOC lab architecture and configs.
* [**simulation-writeups**][simulation-writeups](https://github.com/Moses-Kinuthia/simulation-writeups) – Incident-style writeups for each SOC simulation.

---

### 🤝 Connect with Me
* **LinkedIn:** www.linkedin.com/in/moses-waweru-kinuthia

> "The quiet professional of the network; seeing everything, staying hidden until the alert fires."

<!--
