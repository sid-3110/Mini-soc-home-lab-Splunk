## Windows Brute Force Attack Simulation

### Objective
To simulate a brute force authentication attack against a Windows endpoint
and observe how failed login attempts are logged and ingested into Splunk.

---

### Attack Method
Multiple incorrect password attempts were made against a valid Windows user account
within a short time window.

This simulates a brute force attempt commonly seen in real SOC environments.

---

### Logs Generated
- Windows Security Event Log
- Event ID: 4625 (Failed Logon)

Each failed attempt generated a security event containing:
- Target username
- Logon type
- Timestamp
- Failure reason

---

### Evidence
Screenshots captured:
- Windows Event Viewer showing Event ID 4625
- Splunk search results confirming log ingestion
- Aggregated view showing repeated failures

---

### SOC Observation
A single failed login is normal.
Multiple failed logins targeting the same account in a short period
is suspicious and requires further analysis.

This behavior will be used to create a detection rule in Splunk.
![WhatsApp Image 2026-01-23 at 5 21 45 PM](https://github.com/user-attachments/assets/1c8ba769-36d5-4be1-aa1d-a93063ba6570)
![WhatsApp Image 2026-01-23 at 5 29 30 PM](https://github.com/user-attachments/assets/3938e929-299a-4246-80d2-019c74602475)
