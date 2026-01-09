# passive-network-scanner
Passive Network Vulnerability Scanner (Python, SOC‑style reports)

# Passive Network Vulnerability Scanner

![Python](https://img.shields.io/badge/Python-3.13-blue?logo=python&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

A **modular passive network vulnerability scanner** built in Python, designed for cybersecurity students, SOC analysts, and penetration testers.  
It supports multi-target scanning, plugin-based vulnerability checks, learning mode, and generates **JSON & SOC-style HTML reports**.

---

## Features

- ✅ Passive scanning (safe & non-intrusive)  
- ✅ Multi-target & subnet support (single IPs, multiple IPs, CIDR notation)  
- ✅ Service banner grabbing and fingerprinting  
- ✅ Plugin-based vulnerability engine for extensibility (add new service checks without modifying core code)  
- ✅ Learning mode explaining why a service may be risky  
- ✅ JSON and HTML SOC-style report generation  
- ✅ Configurable timeout and retries  
- ✅ CLI tool installable system-wide (`passive-scan`)  

---

## Installation (Kali Linux / Linux)

1. Clone the repository:
```bash
git clone https://github.com/<your-username>/passive-network-scanner.git
cd passive-network-scanner
Create and activate a virtual environment:

python3 -m venv venv
source venv/bin/activate
Install dependencies:

pip install -r requirements.txt

Make the scanner executable:

chmod +x scanner
sudo mv scanner /usr/local/bin/passive-scan

Scan a single IP
passive-scan -t 127.0.0.1 --mode standard

Scan multiple IPs
passive-scan -t 127.0.0.1,192.168.1.10 --mode quick

Scan a subnet
passive-scan -t 192.168.1.0/30 --mode passive

Plugin System

The scanner is modular:

vuln_plugins/
 ├── ssh.py
 ├── ftp.py
 └── http.py
