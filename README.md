# Integrating an Ubuntu Web Server into a SOC Lab: Docker, DVWA, and Wazuh Detection

## Project Overview

This project documents the expansion of my SOC lab by integrating a dedicated Ubuntu Web Server into an existing enterprise-style SOC environment.

The existing lab already included Active Directory, Windows and Ubuntu endpoints, Kali Linux, and Wazuh SIEM. In this project, I added an Ubuntu Web Server, installed Docker, deployed DVWA as a vulnerable web application, configured Wazuh log collection, created custom Wazuh detection rules, and validated DVWA web attack activity in the Wazuh dashboard.

This project is divided into two parts:

- **Part 1:** Ubuntu Web Server, Docker, and DVWA Deployment
- **Part 2:** DVWA Web Attack Detection Using Wazuh SIEM

---

## Lab Environment

The lab environment includes:

- Windows Server with Active Directory
- Windows 10 endpoint
- Ubuntu endpoint
- Kali Linux attacker machine
- Ubuntu Web Server
- Docker and Docker Compose
- DVWA
- Wazuh SIEM
- VirtualBox NAT Network

---

## Lab Architecture

```text
Kali Linux
   |
   | Web attack simulation
   v
Ubuntu Web Server
   |
   | Docker container
   v
DVWA Web Application
   |
   | Docker logs
   v
Wazuh Agent
   |
   | Log forwarding
   v
Wazuh SIEM Dashboard
```

---

## Repository Structure

```text
soc-lab-ubuntu-web-server-dvwa/
│
├── README.md
│
├── Integrating an Ubuntu Web Server into a SOC Lab Part 1.pdf
│── Integrating an Ubuntu Web Server into a SOC Lab Part 2.pdf

```

---

## Key Learnings

This project helped me understand:

- How to integrate a web server into a SOC lab
- How to deploy DVWA using Docker
- How containerized applications generate logs
- How to configure Wazuh to collect Docker logs
- How to create custom Wazuh local rules
- How brute force and SQL injection activity can appear in logs
- How to investigate Wazuh alerts from a SOC analyst perspective

---

## Future Improvements

Future improvements for this lab may include:

- Creating frequency-based brute force detection rules
- Creating payload-based SQL injection detection rules
- Adding MITRE mapping directly inside Wazuh local rules
- Detecting XSS attacks
- Detecting command injection attacks
- Detecting insecure file upload attacks
- Integrating ModSecurity or another web application firewall
- Comparing Docker logs, Apache logs, and WAF logs
- Deploying additional PHP web applications for vulnerability testing

---
