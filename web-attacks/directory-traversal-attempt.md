## Directory Traversal Attempt (Rule 100102)

### Summary
An external IP attempted to access sensitive system files using a directory traversal payload.

### Observed Request
/test=../../../../etc/passwd

### Indicators
- Use of "../" pattern to escape web root
- Targeting Linux system file (/etc/passwd)
- Request made via curl (automated/manual probing)

### Outcome
- Request detected and flagged by Wazuh
- No evidence of successful file access

### MITRE ATT&CK Mapping
- Tactic: Initial Access
- Technique: Exploit Public-Facing Application (T1190)

### Analyst Notes
This is a direct exploitation attempt. If successful, it could expose system-level information. Proper input validation and web server hardening are critical.
<img width="1673" height="1043" alt="100102" src="https://github.com/user-attachments/assets/462e3ad5-2f46-4a92-b112-716e9c0f76cc" />
