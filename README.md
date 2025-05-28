# 🛡️ SOC Home Lab - Ubuntu Setup

This project documents the setup of a Security Operations Center (SOC) home lab using open-source tools on Ubuntu. The purpose of this lab is to simulate real-world security monitoring, threat detection, and incident response workflows for learning and experimentation.

---

## 📌 Objectives
- Build a functional SOC lab on a local Ubuntu system
- Collect and analyze logs using the ELK Stack (Elasticsearch, Logstash, Kibana)
- Monitor and detect malware, intrusions, and suspicious behavior
- Practice incident response and log correlation

---

## ⚙️ System Requirements
- OS: Ubuntu 20.04+ (tested on 22.04 LTS)
- RAM: 8 GB minimum (16 GB recommended)
- Disk: 50 GB+ free
- Privileged access (`sudo`)

---

## 📦 Installed Components

### 🔹 ELK Stack (Core SIEM)
- **Elasticsearch**: Stores and indexes log data
- **Logstash**: Ingests, processes, and forwards logs
- **Kibana**: Web UI for visualizing logs

### 🔹 Log Forwarders
- **Filebeat**: Lightweight shipper to forward system/app logs to Logstash

### 🔹 Detection Tools
- **ClamAV**: Antivirus scanner
- **Linux Malware Detect (LMD)**: Malware scanner with real-time monitoring
- **chkrootkit** & **rkhunter**: Rootkit detection tools

### 🔹 Network Monitoring
- **Wireshark**: Packet inspection
- **Suricata**: Network IDS/IPS
- **Zeek**: Advanced network traffic analysis

### 🔹 Host-Based Monitoring
- **Wazuh Agent**: EDR + Host IDS (with optional Wazuh Manager)
- **Sysmon for Linux** *(optional)*: Process + file activity logging

---

## 🛠️ Installation Steps

### Update System
```bash
sudo apt update && sudo apt upgrade -y
