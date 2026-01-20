## Sysmon Configuration (Windows Endpoint)

### Overview
Sysmon (System Monitor) is a Windows system service that provides detailed visibility
into endpoint activity such as process creation, network connections, and file changes.

In this lab, Sysmon was deployed on the Windows endpoint to enhance detection
capabilities and support SOC-level investigations.

---

### Why Sysmon is Important for SOC
Windows Event Logs alone are often insufficient for deep investigations.
Sysmon provides high-fidelity telemetry that helps SOC analysts:

- Track process execution
- Analyze command-line activity
- Detect suspicious network connections
- Identify potential malware behavior
- Correlate endpoint activity with SIEM alerts

---

### Sysmon Installation

Sysmon was installed using Microsoft Sysinternals.

Steps:
1. Download Sysmon from:
   https://learn.microsoft.com/sysinternals/downloads/sysmon

2. Extract the Sysmon files.

3. Open **PowerShell as Administrator**.

4. Install Sysmon with the default configuration:

```powershell
sysmon64.exe -accepteula -i


