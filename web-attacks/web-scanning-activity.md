## Web Scanning Activity (Rule 100100)

### Summary
An external host (139.59.143.102) performed automated reconnaissance against the web server by probing multiple known API and application endpoints.

### Observed Behavior
- Requests to:
  - /v3/api-docs
  - /swagger-ui.html
  - /actuator/env
  - /info.php
- Multiple rapid requests indicating automation
- User-agent identified as scanner (iscanner)

### Outcome
- Server returned HTTP 404 (resource not found)
- No successful exposure of endpoints

### MITRE ATT&CK Mapping
- Tactic: Reconnaissance
- Technique: Active Scanning (T1595)

### Analyst Notes
This activity represents pre-exploitation reconnaissance. No compromise occurred, but the host is actively being targeted by automated scanning tools.
<img width="1687" height="1192" alt="100100" src="https://github.com/user-attachments/assets/0817fd8e-89b2-4aa8-bcb4-69495544d734" />
