# Attack Surface Reduction Lab

A cybersecurity lab project demonstrating Linux server hardening and attack surface reduction using Ubuntu Server, Nmap, Nessus, pfSense, auditd, and Wireshark.

---

## Overview

This project focuses on minimizing the attack surface of an Ubuntu Linux server by:

- Identifying exposed services
- Disabling unnecessary services
- Hardening SSH
- Configuring firewall rules
- Monitoring security events
- Comparing security scans before and after hardening

---

## Objectives

- Reduce exposed services
- Secure SSH configuration
- Configure firewall rules
- Validate security improvements
- Monitor blocked traffic
- Analyze network traffic changes

---

## Tools Used

| Tool | Purpose |
|------|---------|
| Ubuntu Server | Target system |
| Nmap | Port scanning |
| Nessus | Vulnerability scanning |
| pfSense | Firewall |
| auditd | Linux auditing |
| Wireshark | Packet analysis |

---

## Lab Workflow

1. Deploy Ubuntu Server
2. Perform initial Nmap scan
3. Identify unnecessary services
4. Disable unused services
5. Harden SSH
6. Configure pfSense firewall
7. Perform post-hardening scan
8. Run Nessus vulnerability assessment
9. Enable auditd logging
10. Capture and compare network traffic

---

## SSH Hardening

- Changed default SSH port
- Disabled root login
- Disabled password authentication
- Limited login attempts
- Enabled SSH key authentication

Example:

```text
Port 2222
PermitRootLogin no
PasswordAuthentication no
MaxAuthTries 3
```

---

## Firewall Rules

| Service | Port | Action |
|----------|------|--------|
| SSH | 2222 | Allow |
| HTTPS | 443 | Allow |
| All Others | Any | Deny |

---

## Attack Surface Comparison

| Feature | Before | After |
|----------|--------|-------|
| Open Ports | 22, 80, 111, 631 | 2222, 443 |
| Root Login | Enabled | Disabled |
| Firewall | Default | Hardened |
| Password Login | Enabled | Disabled |
| Audit Logging | Disabled | Enabled |

---

## Results

- Reduced exposed services
- Hardened SSH access
- Implemented restrictive firewall policy
- Logged authentication events with auditd
- Reduced network traffic exposure
- Improved vulnerability assessment results

---

## Skills Demonstrated

- Linux Administration
- Linux Hardening
- Network Security
- Firewall Configuration
- Vulnerability Assessment
- Security Monitoring
- Packet Analysis
- Security Auditing

---

## Screenshots

### Nmap Scan (Before)

![Before](screenshots/nmap_before.png)

### Nmap Scan (After)

![After](screenshots/nmap_after.png)

### Nessus Scan

![Nessus](screenshots/nessus_after.png)

### pfSense Rules

![Firewall](screenshots/pfsense_rules.png)

### Wireshark Capture

![Wireshark](screenshots/wireshark_after.png)

---

## Future Improvements

- Fail2Ban integration
- AppArmor policy enforcement
- SELinux implementation
- Automated compliance scanning
- CIS Benchmark validation
- SIEM integration

---

## Author

Your Name

Cybersecurity Portfolio Project
