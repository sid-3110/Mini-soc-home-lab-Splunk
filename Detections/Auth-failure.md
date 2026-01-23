## Detection: Windows Brute Force Authentication Attempt

### Alert Objective
To detect potential brute force attacks against Windows user accounts
by identifying repeated failed login attempts within a short time window.

---

### Log Source
- Windows Security Event Logs
- Event ID: 4625 (Failed Logon)

---

### Detection Logic
The detection identifies multiple failed authentication attempts
from the same source targeting the same user account within a 5-minute window.

---

### SPL Query
```spl
index=windows EventCode=4625
| bin _time span=5m
| stats count as failed_attempts by _time, Account_Name, src_ip
| where failed_attempts > 5


![WhatsApp Image 2026-01-23 at 5 54 08 PM](https://github.com/user-attachments/assets/b41b8a79-f80a-4636-bbc2-add130fda3d1)

