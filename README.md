# 🔐 Splunk SIEM Lab – SOC Monitoring Project

A hands-on SOC/SIEM lab using **Splunk Enterprise on Kali Linux** and **Splunk Universal Forwarder on Windows 10** to collect, analyze, and detect security events.

This project simulates a real-world SOC environment where Windows logs are forwarded to Splunk for threat detection and monitoring.

---

## 🧠 Architecture

```
Windows 10 (Universal Forwarder)
        |
        |  TCP 9997
        ▼
Kali Linux (Splunk Enterprise)
Indexer + Search Head
```

---

## 🛠️ Technologies Used

- Splunk Enterprise 10.x
- Splunk Universal Forwarder
- Kali Linux
- Windows 10
- Sysmon
- VirtualBox / VMware
- NAT / Host-Only Networking

---

## 🎯 Objectives

- Deploy a working SIEM solution  
- Collect Windows Security, System & Application logs  
- Monitor Sysmon and PowerShell activity  
- Detect authentication events and suspicious behavior  
- Gain SOC analyst hands-on experience  

---

## 📦 Log Sources Collected

| Source                 | Index      |
|------------------------|------------|
| Windows Security Logs  | windows    |
| Windows System Logs    | windows    |
| Sysmon Logs            | sysmon     |
| PowerShell Logs        | powershell |

---

## 🔎 Detection Use Cases

- Login Success / Failure  
- Process Creation  
- Network Connections  
- PowerShell Script Execution
