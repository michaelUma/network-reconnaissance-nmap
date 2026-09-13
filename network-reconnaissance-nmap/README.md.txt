<div align="center">

# 🛰️ Network Reconnaissance with Nmap

### *Host Discovery · Port Scanning · Service Enumeration · Risk Analysis*

![Made with Nmap](https://img.shields.io/badge/Made%20with-Nmap-000000?style=for-the-badge&logo=nmap&logoColor=white)
![Platform](https://img.shields.io/badge/Platform-Kali%20Linux-557C94?style=for-the-badge&logo=kalilinux&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-2ea44f?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)

</div>

<br>

> ⚠️ **Disclaimer:** All scanning and enumeration in this project was performed exclusively against systems within an **authorized, isolated virtual lab environment**. No unauthorized systems were accessed, scanned, or targeted. This repository is intended for educational and portfolio purposes only.

<br>

## <div align="center">📑 Table of Contents</div>

* [🔍 Overview](#-overview)
* [🎯 Objectives](#-objectives)
* [🧰 Tools Used](#-tools-used)
* [🧭 Methodology](#-methodology)
* [💻 Reconnaissance Commands](#-reconnaissance-commands)
  * [1. Host Discovery](#1-host-discovery)
  * [2. TCP Port Scanning](#2-tcp-port-scanning)
  * [3. Service & Version Detection](#3-service--version-detection)
* [📊 Findings](#-findings)
* [🛡️ Security Recommendations](#️-security-recommendations)
* [📸 Screenshots](#-screenshots)
* [✅ Conclusion](#-conclusion)
* [👤 Author](#-author)

<br>

## <div align="center">🔍 Overview</div>

This project demonstrates practical **network reconnaissance** using **Nmap** in an authorized, controlled lab environment.

The objective was to identify active hosts, discover exposed TCP ports, enumerate running services, and analyze the security implications of network exposure — mirroring the reconnaissance phase of a real-world penetration test.

<br>

## <div align="center">🎯 Objectives</div>

- 🖧 Identify active hosts within the authorized lab environment
- 🔓 Discover open TCP ports
- 🛠️ Identify services running on discovered ports
- 🔎 Perform service and version enumeration
- 📝 Document reconnaissance results
- ⚠️ Identify potential security risks
- 💡 Provide security recommendations based on the findings

<br>

## <div align="center">🧰 Tools Used</div>

| Tool | Purpose |
|:--|:--|
| 🐉 **Kali Linux** | Operating system / attack platform |
| 🛰️ **Nmap 7.99** | Host discovery, port scanning, and service enumeration |
| 💻 **Linux Command Line** | Command execution and workflow |
| 🖥️ **Virtualized Lab Environment** | Safe, isolated, authorized testing environment |

<br>

## <div align="center">🧭 Methodology</div>

The assessment followed a standard network reconnaissance workflow:

1. **Network configuration identification**
2. **Host discovery**
3. **TCP port scanning**
4. **Service and version detection**
5. **Result analysis**
6. **Security recommendations**
7. **Documentation**

<br>

## <div align="center">💻 Reconnaissance Commands</div>

### 1. Host Discovery

Identify which hosts on the network are active before scanning further.

```bash
nmap -sn TARGET_IP/24
```

> `-sn` performs a ping scan only (no port scan), used to sweep the subnet for live hosts.

<br>

### 2. TCP Port Scanning

Scan the discovered host(s) for open TCP ports.

```bash
nmap -p- TARGET_IP
```

> `-p-` scans all 65,535 TCP ports rather than just the default top 1,000.

<br>

### 3. Service & Version Detection

Enumerate the services and versions running on open ports.

```bash
nmap -sV -sC -p PORT1,PORT2,PORT3 TARGET_IP
```

> `-sV` detects service/version info, `-sC` runs Nmap's default enumeration scripts against open ports.

<br>

## <div align="center">📊 Findings</div>

> *Replace this section with your actual scan output summary.*

| Host | Open Ports | Service | Version | Risk Level |
|:--|:--|:--|:--|:--:|
| `TARGET_IP` | 22 | SSH | OpenSSH 8.x | 🟡 Medium |
| `TARGET_IP` | 80 | HTTP | Apache 2.4.x | 🟢 Low |
| `TARGET_IP` | 445 | SMB | Samba 4.x | 🔴 High |

<br>

## <div align="center">🛡️ Security Recommendations</div>

- 🔐 Disable or restrict unused/unnecessary services
- 🔄 Patch and update outdated service versions
- 🧱 Implement a firewall to restrict exposed ports to trusted hosts
- 👀 Enable logging and monitoring for scan/connection attempts
- 🔑 Enforce strong authentication on exposed services (e.g. SSH, SMB)

<br>

## <div align="center">📸 Screenshots</div>

<div align="center">

| Host Discovery | Port Scan | Service Enumeration |
|:--:|:--:|:--:|
| *Add screenshot* | *Add screenshot* | *Add screenshot* |

</div>

<br>

## <div align="center">✅ Conclusion</div>

This reconnaissance exercise highlighted how easily exposed hosts, open ports, and outdated services can be identified using freely available tools like Nmap. The exercise reinforces the importance of minimizing attack surface, keeping services patched, and applying the principle of least exposure in any network environment.

<br>

## <div align="center">👤 Author</div>

<div align="center">

Made with 🖤 by **[Your Name]**

[![GitHub](https://img.shields.io/badge/GitHub-Profile-181717?style=for-the-badge&logo=github)](https://github.com/yourusername)

</div>