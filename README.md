# Integrating an Ubuntu Web Server into a SOC Lab: Docker and DVWA Deployment

## Overview

This project is Part 1 of my SOC lab expansion. In this phase, I integrated a dedicated Ubuntu Web Server into my existing SOC lab environment, installed Docker, and deployed DVWA as a containerized vulnerable web application.

The goal of this project was to prepare a realistic web application target for future attack simulation and detection using Wazuh SIEM.

## Lab Components

- Ubuntu Server
- Docker
- Docker Compose
- DVWA
- Kali Linux
- VirtualBox NAT Network
- Wazuh SIEM

## What I Completed

- Installed Ubuntu Server in VirtualBox
- Connected the server to the existing SOC lab network
- Verified connectivity between Kali Linux and Ubuntu Server
- Installed Docker and Docker Compose
- Deployed DVWA using Docker
- Fixed Docker port binding for network access
- Accessed DVWA from Kali Linux
- Prepared the environment for future Wazuh detection

## Lab Architecture

Kali Linux → Ubuntu Web Server → Docker → DVWA

## Report

The full PDF report is available.

## Next Phase

Part 2 will focus on Wazuh log collection, Docker log monitoring, custom Wazuh rules, brute force detection, and SQL injection detection.
