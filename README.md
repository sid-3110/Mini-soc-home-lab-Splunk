# 🛡️ Mini SOC Home Lab (Splunk SIEM)

## 📌 Project Overview
This project demonstrates a hands-on Mini Security Operations Center (SOC) built using **Splunk SIEM**.
The lab focuses on log ingestion, attack simulation, alert detection, investigation, and escalation from a **SOC Analyst L1 perspective**.

---

## 🧱 Lab Architecture
- **SIEM:** Splunk Enterprise
- **Endpoints:** Windows & Linux
- **Log Sources:**
  - Windows Event Logs
  - Sysmon
  - Linux Authentication Logs
  - Firewall Logs
- **Forwarding:** Splunk Universal Forwarder

---

## 🔧 What Was Implemented
- Centralized log collection using Splunk
- Windows & Linux endpoint onboarding
- Authentication attack simulations
- Detection rules using SPL
- Alert investigation & triage
- IOC analysis
- SOC escalation documentation

---

## 🚨 Attack Scenarios Simulated
- Windows brute-force login attempts
- Password spraying attacks
- Linux SSH authentication attacks
- Suspicious process / malware-like behavior

---

## 🔍 SOC Analyst Activities
- Alert validation
- Log correlation
- False positive identification
- True positive escalation
- Documentation & handover notes

---

## 📂 Repository Structure
Each folder in this repository represents a real SOC function:
- `setup/` – Environment & endpoint configuration
- `attack-simulations/` – Simulated attacks
- `detections/` – SIEM detection logic
- `investigations/` – Alert analysis cases
- `escalation-notes/` – L1 → L2 escalation workflow
- `ioc-analysis/` – Threat intelligence checks

---

## 🎯 Skills Demonstrated
- SIEM fundamentals (Splunk)
- Log analysis
- Detection engineering (basic SPL)
- Incident investigation
- SOC documentation & communication

---

## 🧠 Disclaimer
This project was built for **educational and defensive security purposes only**.
