## Investigation Case: True Positive – Windows Brute Force Attack

### Alert Summary
An alert was triggered due to multiple failed authentication attempts
against a Windows user account within a short time window.

---

### Investigation Steps
- Reviewed failed login events (Event ID 4625)
- Identified repeated failures targeting the same account
- Verified no successful login events (Event ID 4624)
- Analyzed timing and source consistency

---

### Findings
- Clear brute force authentication pattern observed
- Activity occurred outside normal business hours
- No evidence of successful compromise at this stage

---

### Classification
True Positive – Brute Force Attack Attempt

---

### Action Taken
- Escalated alert to SOC L2 for further response
- Provided supporting evidence and context

---

### SOC Analyst Note
Early detection and escalation of authentication attacks
reduces the risk of account compromise and lateral movement.


