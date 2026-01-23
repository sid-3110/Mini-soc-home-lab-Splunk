## SOC Escalation Note: L1 to L2

### Alert Name
Windows Brute Force Authentication Attempt

---

### Alert Summary
Multiple failed authentication attempts were detected against a Windows user account
within a short time window. The alert was triggered based on repeated Event ID 4625
logs indicating possible brute force activity.

---

### Detection Source
- SIEM: Splunk
- Log Source: Windows Security Event Logs
- Event ID: 4625 (Failed Logon)

---

### Initial L1 Analysis
The alert was reviewed to determine whether the activity represented normal user
behavior or malicious intent.

Analysis performed:
- Reviewed failed authentication events in Splunk
- Identified repeated failures targeting the same user account
- Observed consistent source IP across attempts
- Activity occurred outside normal business hours
- No corresponding successful login events (Event ID 4624) detected

---

### Findings
- Authentication failures followed a repetitive pattern
- No user justification or expected activity identified
- Behavior aligns with brute force or credential guessing attempts
- No evidence of successful compromise at the time of analysis

---

### Classification
True Positive – Brute Force Authentication Attempt

---

### Impact Assessment
- Potential risk of account compromise if attack continues
- Possible precursor to further malicious activity
- No confirmed data loss or system compromise at this stage

---

### Action Taken by L1
- Alert validated as a true positive
- Relevant logs and evidence collected
- Incident escalated to SOC L2 for further investigation and response

---

### Recommended L2 Actions
- Review historical authentication activity for the affected account
- Check for similar activity on other systems
- Consider account password reset or temporary lockout
- Assess need for source IP blocking or additional monitoring

---

### Evidence Provided
- Splunk search results showing Event ID 4625 spikes
- Aggregated failed login statistics
- Time-based correlation of events

---

### L1 Analyst Notes
Early escalation was performed to reduce the risk of account compromise.
No remediation actions were taken at L1 level as per SOC procedures.
