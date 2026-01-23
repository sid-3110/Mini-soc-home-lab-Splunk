## IOC Analysis: IP Reputation

### Objective
To analyze the reputation of source IP addresses involved in suspicious
authentication activity and determine whether they are associated with
known malicious behavior.

---

### IOC Type
- Indicator Type: IP Address
- Source: Authentication failure events

---

### Context
During the investigation of a Windows brute force authentication alert,
a single source IP address was observed making repeated failed login
attempts against a valid user account.

The IP was extracted from Splunk logs for further validation.

---

### Tools Used
- VirusTotal
- AbuseIPDB
- AlienVault OTX (optional)

---

### Analysis Performed

#### VirusTotal
- Checked IP reputation
- Reviewed community detection reports
- Identified any historical malicious activity

#### AbuseIPDB
- Checked abuse confidence score
- Reviewed categories such as brute force, scanning, or credential abuse
- Observed number of reports and reporting timeframe

---

### Findings
- The IP address has been reported for suspicious authentication activity
- Abuse reports indicate possible brute force behavior
- No evidence that the IP belongs to trusted infrastructure

---

### SOC Interpretation
The IP reputation supports the hypothesis that the authentication failures
were malicious rather than user error.

This strengthens the classification of the alert as a true positive.

---

### Impact on Investigation
- Increased confidence in escalation decision
- Provided additional context to SOC L2
- Helped rule out false positive scenarios

---

### Analyst Notes
IOC analysis should be used as supporting evidence and not as the sole
decision factor. Behavioral patterns and log correlation remain primary
drivers for SOC decisions.
