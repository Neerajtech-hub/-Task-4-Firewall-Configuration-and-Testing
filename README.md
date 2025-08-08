# Task 4 — Firewall Configuration and Testing

## Overview
In this task, I configured firewall rules on both *Linux (UFW & iptables)* and *Windows (Windows Defender Firewall)* to enhance system security.  
The goal was to block specific ports, allow required services, and verify changes.

---

## *Part A — Linux (UFW & iptables)*

### 1. Initial Firewall Status
- Checked the initial UFW status.
- *File:* ufw_raw.txt

```bash
sudo ufw status verbose


---

2. UFW GUI View

Opened UFW GUI to visually inspect and manage rules.

File: ufw_gui.png



---

3. Blocking a Specific Port (Port 23 — Telnet)

Added a firewall rule to block inbound traffic on TCP port 23.

Verified status after blocking.

File: ufw_status_after_blocklist.txt


sudo ufw deny 23/tcp
sudo ufw status verbose


---

4. Allowing SSH (Port 22) Access

Allowed SSH for remote management.

Verified final firewall rules.

File: ufw_status_after_final.txt


sudo ufw allow 22/tcp
sudo ufw status verbose


---

5. Listing iptables Rules

Captured iptables configuration for backup and verification.

File: iptables_list.txt


sudo iptables -L -n -v


---

Part B — Windows (Windows Defender Firewall)

1. Opening Windows Defender Firewall

Opened Windows Security → Firewall & network protection → Advanced settings.



---

2. Creating Inbound Rule to Block Port 23

1. In Advanced Settings, select Inbound Rules → New Rule.


2. Rule Type: Port


3. Protocol: TCP, Specific Local Port: 23


4. Action: Block the connection


5. Apply to: Domain, Private, Public profiles


6. Name the rule (e.g., Block Telnet Port 23).




---

3. Screenshots Taken

File: (Add your Windows screenshot filenames here)



---

Summary

Linux: Configured UFW & iptables to block Telnet (Port 23), allow SSH (Port 22), verified rules, and saved outputs/screenshots.

Windows: Configured Windows Defender Firewall to block Port 23 and documented steps with screenshots.

All required outputs and evidence are saved as files for submission.



---

Files for Submission

1. ufw_gui.png


2. ufw_raw.txt


3. ufw_status_after_blocklist.txt


4. ufw_status_after_final.txt


5. iptables_list.txt


6. (Windows screenshots — Win screenshot1, screenshot2, screenshot3, screenshot4)


7. Few Linux Screenshots - Linux Screenshot1, Linux Screenshot2, Linux Screenshot3, Linux Screenshot5)




---

Prepared by: Neeraj Kumar
Date: August 2025