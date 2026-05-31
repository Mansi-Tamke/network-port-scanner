# Network Port Scanner & Vulnerability Reporter

A Python-based network security tool that scans a target IP address for open ports,
identifies running services, classifies risk levels, and generates automated CSV reports.

## Features
- Scans ports 1–1024 on any target IP
- Identifies services running on each open port
- Classifies risk as HIGH / MEDIUM / LOW / INFO
- Multithreaded scanning for fast results
- Auto-generates a detailed CSV vulnerability report

## Tools & Technologies
- Python 3
- Socket library
- Python-nmap
- Threading module
- CSV module

## How to Run

### 1. Install dependencies
pip install python-nmap

### 2. Run the scanner
python scanner.py

### 3. Enter target IP when prompted
Enter target IP address: 192.168.1.x

## Sample Output
Port       Service         Risk Level
----------------------------------------
135        epmap           INFO
139        netbios-ssn     HIGH
445        microsoft-ds    HIGH

Scan completed in 5 seconds
Total open ports found: 3
Report saved as: report_192.168.1.x.csv

## Risk Classification
| Risk Level | Ports | Reason |
|------------|-------|--------|
| HIGH | 21, 23, 139, 445, 3389 | Commonly exploited, unencrypted |
| MEDIUM | 22, 80, 3306, 8080 | Require patching and monitoring |
| LOW | 443, 8443 | Secure but needs proper SSL config |
| INFO | Others | Review if port is necessary |

## Disclaimer
This tool is for educational purposes only.
Only scan systems you own or have permission to test.

## Author
Mansi Tamke — B.Tech Cybersecurity, Symbiosis Skills and Professional University# network-port-scanner
A Python-based network port scanner that detects open ports, identifies services, and classifies risk levels with automated CSV reporting
