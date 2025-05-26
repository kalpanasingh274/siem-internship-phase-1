# siem-internship-phase-1
Welcome to the repository for the SIEM Internship Phase-1.
The goal of this Practical cybersecurity internship is to establish a personal SOC(Security Operations Centre)lab, simulate hostile tactics, and identify them using Splunk as the SIEM. Every use case aims to present fundamental ideas in threat detection, alerting, log gathering, and parsing


🎓 Internship Objective
Set up a functional SIEM environment (Splunk Free edition)
Collect logs from Windows machines via Universal Forwarder
Simulate adversarial techniques
Detect and alert on suspicious activity based on real-world attack patterns
Document detection engineering tasks professionally
📚 Lab Architecture
Host Machine: Running Splunk Web Interface
Windows 10 VM: Target machine with Sysmon, Event Logs, and Splunk Universal Forwarder
Kali Linux VM: Used for attack simulation using tools like hydra and crackmapexec
Logs from the Windows VM are shipped to the host Splunk instance using Splunk Universal Forwarder.







