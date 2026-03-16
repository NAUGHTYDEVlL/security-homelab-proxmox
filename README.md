# security-homelab-proxmox
This project documents the design and operation of a personal cybersecurity homelab built using virtualization. The lab simulates a basic enterprise security monitoring environment for practicing threat detection, log analysis, and system hardening.

The lab was built using Proxmox VE and includes multiple virtual machines for monitoring and testing.

_____________________________________________________________________________________________________________________________________________
Lab Architecture

The lab currently includes three virtual machines:

VM                 Purpose
___________________________________________________
ubuntu-web	  |     Linux web server running Apache
siem-wazuh	  |     Security monitoring platform
wireguard	    |     Secure VPN access to the lab

_____________________________________________________________________________________________________________________________________________
Security Tools Used

SIEM
Wazuh

Web Server
Apache HTTP Server

Network Tools
Nmap
Wireshark
Burp Suite


Security Monitoring

Logs from the Apache web server are ingested into Wazuh for monitoring and analysis.
The SIEM environment allows investigation of:

suspicious HTTP requests
automated scanning activity
attack attempts against the web server

_____________________________________________________________________________________________________________________________________________
Attacks Observed

While monitoring the lab environment, several automated attack attempts were detected from international IP addresses.
Examples included:

SQL injection attempts
directory traversal attempts
automated vulnerability scanning

Analysis of the logs showed that the requests resulted in HTTP 404 responses, indicating unsuccessful exploitation attempts.

_____________________________________________________________________________________________________________________________________________

Defensive Measures Implemented

To reduce the attack surface of the lab environment:

unused services were removed
unnecessary assets were disabled
system hardening practices were applied
