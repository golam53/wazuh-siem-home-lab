# 🛡️ Wazuh SIEM Home Lab

A hands-on Security Operations Center (SOC) home lab built with **Wazuh SIEM, Ubuntu Server, and Windows 11** to practice security monitoring, threat hunting, alert investigation, and endpoint detection.

Rather than only installing a SIEM, this project focuses on generating controlled security events, investigating the resulting alerts, and understanding the underlying telemetry.

## 🎯 Project Objectives

- Deploy a functional Wazuh SIEM environment
- Connect and monitor a Windows 11 endpoint
- Generate controlled security events
- Investigate alerts using Wazuh Threat Hunting
- Analyze Windows authentication failures
- Configure real-time File Integrity Monitoring (FIM)
- Understand Wazuh rules, severity levels, event fields, and cryptographic hashes

## 🏗️ Lab Architecture

```text
Windows 11 Endpoint
     windows-lab
          │
          │  Wazuh Agent
          │  Security Telemetry
          ▼
┌─────────────────────────┐
│   Ubuntu Server VM      │
│                         │
│   Wazuh Manager         │
│   Wazuh Indexer         │
│   Wazuh Dashboard       │
└────────────┬────────────┘
             │
             ▼
       SOC Investigation
       Threat Hunting
       Alert Analysis
