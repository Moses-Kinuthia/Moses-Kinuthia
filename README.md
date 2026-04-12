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
     |    ├── pfSense VM (WAN: 192.168.8.x | LAN: 10.0.0.x | OPT1: 10.0.10.x)
     |    └── Wazuh Server (10.0.10.x - Isolated Management Segment)
     |
     | (Physical Ethernet Bridge)
     |
     +--- Machine B (Windows 10 Host)
          ├── Kali Linux (10.0.0.x)
          ├── Windows Server 2019 (DC01: 10.0.0.x)
          └── Windows Enterprise (WKSTN01: 10.0.0.x)

---

### 📈 GitHub Stats
![My GitHub Stats](https://github-readme-stats.vercel.app/api?username=Moses-Kinuthia&show_icons=true&theme=tokyonight)

---

### 🤝 Connect with Me
* **LinkedIn:** www.linkedin.com/in/moses-waweru-kinuthia

> "The quiet professional of the network; seeing everything, staying hidden until the alert fires."

<!--
**Moses-Kinuthia/Moses-Kinuthia** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
