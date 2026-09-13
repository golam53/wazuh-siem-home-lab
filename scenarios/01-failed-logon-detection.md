# Scenario 1 — Windows Failed Logon Detection

## Overview

This scenario demonstrates how a Security Operations Center (SOC) analyst can use Wazuh to detect and investigate failed Windows authentication attempts.

Two controlled failed logon attempts were intentionally generated on the Windows 11 endpoint. The resulting security events were collected by the Wazuh agent, analyzed by the Wazuh server, and investigated through the Threat Hunting interface.

> **Lab note:** The failed authentication attempts in this scenario were intentionally generated for testing in a controlled environment.

---

## Objective

The goals of this scenario were to:

- Generate controlled failed Windows logon attempts
- Verify that Wazuh detects the authentication failures
- Filter SIEM telemetry to isolate relevant events
- Examine the underlying Windows Security event
- Understand the difference between a Wazuh alert and the raw event data
- Practice basic SOC investigation methodology

---

## Detection Workflow

```text
Windows 11 Endpoint
        │
        │ Failed authentication attempt
        ▼
Windows Security Log
        │
        │ Event ID 4625
        ▼
Wazuh Agent
        │
        ▼
Wazuh Manager
        │
        │ Rule evaluation
        ▼
Wazuh Rule 60122
        │
        ▼
Threat Hunting / SOC Investigation
