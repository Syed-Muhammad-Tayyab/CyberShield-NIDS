<div align="center">

# 🛡️ CyberShield-NIDS

### Real-Time Network Intrusion Detection & Threat Alerting System

<em>Catch the threat before it catches you.</em>

![Banner](https://capsule-render.vercel.app/api?type=waving&color=0:1e2327,100:0f4c75&height=200&section=header&text=CyberShield-NIDS&fontSize=45&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Network%20Intrusion%20Detection%20System&descAlignY=58&descSize=18)

[![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)
[![Build](https://img.shields.io/github/actions/workflow/status/Syed-Muhammad-Tayyab/CyberShield-NIDS/ci.yml?style=for-the-badge&logo=githubactions&logoColor=white)](#)
[![Issues](https://img.shields.io/github/issues/Syed-Muhammad-Tayyab/CyberShield-NIDS?style=for-the-badge&logo=github)](../../issues)
[![Stars](https://img.shields.io/github/stars/Syed-Muhammad-Tayyab/CyberShield-NIDS?style=for-the-badge&logo=github&color=gold)](../../stargazers)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=for-the-badge)](CONTRIBUTING.md)

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=22&duration=3000&pause=1000&color=00FF9C&center=true&vCenter=true&width=600&lines=Sniffing+packets+in+real-time...;Detecting+anomalies+with+ML...;Alerting+before+the+breach...;Built+for+Blue+Teams+%F0%9F%94%B5" alt="Typing SVG" />

</div>

---

## 📜 Table of Contents

- [About The Project](#-about-the-project)
- [Key Features](#-key-features)
- [Tech Stack](#-tech-stack)
- [Architecture](#-architecture)
- [Getting Started](#-getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#-usage)
- [Screenshots](#-screenshots)
- [Roadmap](#-roadmap)
- [Contributing](#-contributing)
- [License](#-license)
- [Contact](#-contact)

---

## 📖 About The Project

**CyberShield-NIDS** is a lightweight, real-time Network Intrusion Detection System built to monitor live traffic, flag suspicious behavior (port scans, brute-force attempts, ARP spoofing, DoS patterns), and alert the operator through a clean terminal and web dashboard.

It was designed as a learning-friendly blue-team tool — simple enough to read end-to-end, yet modular enough to extend with your own detection rules or ML-based anomaly scoring.

> ⚠️ **For educational and authorized lab/testing environments only.** Do not deploy against networks you do not own or have explicit permission to monitor.

---

## ✨ Key Features

| 🔍 Feature | 📄 Description |
|---|---|
| **Live Packet Sniffing** | Captures and parses packets in real time using `scapy` |
| **Signature-Based Detection** | Flags known attack patterns (SYN floods, port scans, ARP spoofing) |
| **Anomaly Scoring** | Lightweight statistical/ML model flags unusual traffic spikes |
| **Alert Dashboard** | Live web dashboard with charts, logs & severity levels |
| **Rule Engine** | Add custom detection rules via simple YAML config |
| **Exportable Logs** | JSON / CSV export for SIEM ingestion (e.g. Wazuh, Splunk) |
| **Email / Webhook Alerts** | Push critical alerts to Slack, Discord, or email instantly |

---

## 🧰 Tech Stack

<div align="center">

![Python](https://img.shields.io/badge/-Python-black?style=flat-square&logo=python)
![Scapy](https://img.shields.io/badge/-Scapy-black?style=flat-square&logo=wireshark)
![Flask](https://img.shields.io/badge/-Flask-black?style=flat-square&logo=flask)
![SQLite](https://img.shields.io/badge/-SQLite-black?style=flat-square&logo=sqlite)
![Docker](https://img.shields.io/badge/-Docker-black?style=flat-square&logo=docker)
![Linux](https://img.shields.io/badge/-Linux-black?style=flat-square&logo=linux)

</div>

---

## 🏗️ Architecture

```
┌────────────────┐     ┌──────────────────┐     ┌───────────────────┐
│  Packet Sniffer │ --> │  Detection Engine │ --> │   Alert Manager    │
│   (Scapy)       │     │ (Rules + Anomaly) │     │ (Dashboard/Webhook)│
└────────────────┘     └──────────────────┘     └───────────────────┘
         │                      │                         │
         ▼                      ▼                         ▼
   Raw Traffic Log        Flagged Events            Live Alerts + Logs
```

---

## 🚀 Getting Started

### Prerequisites

- Python 3.10+
- `libpcap` / `Npcap` (for packet capture)
- Root/Administrator privileges (required for raw socket access)

### Installation

```bash
# Clone the repository
git clone https://github.com/Syed-Muhammad-Tayyab/CyberShield-NIDS.git
cd CyberShield-NIDS

# Create a virtual environment
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

---

## 🖥️ Usage

```bash
# Start the sniffer with default rules
sudo python main.py --interface eth0

# Start with the web dashboard
sudo python main.py --interface eth0 --dashboard

# Run with a custom rule set
sudo python main.py --interface eth0 --rules config/custom_rules.yaml
```

Then open the dashboard at:

```
http://localhost:5000
```

---

## 📸 Screenshots

| Dashboard | Live Alerts |
|---|---|
| `[ add screenshot here ]` | `[ add screenshot here ]` |

---

## 🗺️ Roadmap

- [x] Core packet sniffing engine
- [x] Signature-based rule detection
- [x] Web dashboard with live charts
- [ ] ML-based anomaly detection module
- [ ] SIEM integration (Wazuh / ELK)
- [ ] Dockerized deployment
- [ ] Multi-interface distributed sensors

See [open issues](../../issues) for the full list of proposed features.

---

## 🤝 Contributing

Contributions make the open-source community amazing. Any contributions are **greatly appreciated**.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

Distributed under the **MIT License**. See `LICENSE` for more information.

---

## 📬 Contact

<div align="center">

**Syed Muhammad Tayyab**

[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Syed-Muhammad-Tayyab)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](#)

⭐ **If this project helped you, consider giving it a star!** ⭐

![Footer](https://capsule-render.vercel.app/api?type=waving&color=0:0f4c75,100:1e2327&height=100&section=footer)

</div>
