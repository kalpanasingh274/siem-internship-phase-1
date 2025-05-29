# siem-internship-phase-1
Welcome to the repository for the SIEM Internship Phase-1.
The goal of this Practical cybersecurity internship is to establish a personal SOC(Security Operations Centre)lab, simulate hostile tactics, and identify them using Splunk as the SIEM. Every use case aims to present fundamental ideas in threat detection, alerting, log gathering, and parsing


**🎓 Internship Objective**
- Set up a functional SIEM environment (Splunk Free edition)
- Collect logs from Windows machines via Universal Forwarder
- Simulate adversarial techniques
- Detect and alert on suspicious activity based on real-world attack patterns
- Document detection engineering tasks professionally
  # 📚 Lab Architecture
- Host Machine: Running Splunk Web Interface
- Windows 10 VM: Target machine with Sysmon, Event Logs, and Splunk Universal Forwarder
- Kali Linux VM: Used for attack simulation using tools like hydra and crackmapexec
- Logs from the Windows VM are shipped to the host Splunk instance using Splunk Universal Forwarder.


**📊 Use Cases Implemented**
# 1. Brute Force Login Detection
 - **Technique:** A successful login after several unsuccessful attempts
 - **Event IDs:** 4625 (Failure), 4624 (Success)
 - **Tools:** Hydra (Kali), Windows Security Logs
 -   **Goal:** Within five minutes, identify brute force attempts that are followed by a successful privileged login from the same IP.


**2. Suspicious Logon Times**
- **Techinque:** Outside of business hours, a privileged login
- **Event ID:** 4624
- **Logic:** Detect admin logins beyond 7 PM or before 9 AM


**3. Lateral Movement via RDP**
-  **Technique:** RDP logins using valid credentials after failed attempts
-  **Event ID:** 4624 (LogonType=10), 4625
-  **Goal:** Identify attempts at lateral movement and compare them to prior failures.


**5. Hidden User Account Creation**
-  **Technique:** Adding a new user to the Administrators group
-  **Event IDs:** 4720 (Account Created), 4732 (User added to group)
-  **Goal:** Detect creation of suspicious accounts and privilege escalation


**🗃️ Folder Structure**

**siem-internship-phase-1/**
- ├── use-case-1-brute-force-login/
- │   ├── screenshots/
- │   ├── detection-logic/
- │   └── writeups/
- ├── use-case-2-suspicious-logon-time/
- ├── use-case-3-lateral-movement-rdp/
- ├── use-case-4-log-tampering/
- ├── use-case-5-hidden-user-creation/
- └── README.md

**Each folder contains:**

- **screenshots/:** Attack simulation, log entries, query results, and alerts
- **detection-logic/:** Detection queries used in Splunk (SPL)
-  **writeups/:** **Scenario explanation, objective, tools used, detection mapping


**🌍 Tools Used**
- **SIEM:** Splunk Free
- **Monitoring Tools:** Sysmon, Event Viewer
- **Attack Tools:** crackmapexec, PowerShell, net user, wevtutil
- **Forwarder:** Splunk Universal Forwarder for log shipping


**📄 Submission Checklist**
- ✅   Screenshots of each detection scenario
- ✅   SPL queries for alert logic
- ✅   Markdown writeups per use case
- ✅  Logs demonstrating detection in Splunk


**🚀 Outcome**
#  After finishing this project, I discovered:
- End-to-end log forwarding and detection engineering
- SPL query writing and alert creation in Splunk
- Threat simulation and mapping to MITRE ATT&CK
- GitHub documentation best practices


**🌟 Special Thanks**
- To the open-source community whose tools enabled this effort, as well as to the mentors and community resources who provided assistance along the road.

  - Explore each use case folder to view the detection logic's documentation, screenshots, and queries.
 

# 📆 2025










