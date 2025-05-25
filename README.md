# siem-internship-phase-1
Welcome to the repository for the SIEM Internship Phase-1.
The goal of this Practical cybersecurity internship is to establish a personal SOC(Security Operations Centre)lab, simulate hostile tactics, and identify them using Splunk as the SIEM. Every use case aims to present fundamental ideas in threat detection, alerting, log gathering, and parsing.


🎓**Goal of the Internship**
 Create a working SIEM setup using Splunk Free.
 Gather logs using Universal Forwarder from Windows computers.
 Adversarial method simulation.
 Identify suspious activities and send out alerts based on actual attack trends.
 Professional document detection engineering tasks.


**Architecture of the Lab**
**Host Machine:** Splunk Web Interface is operating on the host computer.
**Windows 11 VM:** Splunk Universal Forwarder, Event logs, and Sysmon on the target computer.
**Kali linux VM:** used to simulate attacks with programs such as crackmapexec and Hydra.
Using Splunk Universal Forwarder, logs from the Windows virtual machine are transferred to the host Splunk instance.


📊 **Applied Use Cases**
**1. Brute Force Login Detection**
**Technique:** Multiple failed login attempts followed by successful login
**Event IDs:** 4625 (Failure), 4624 (Success)
**Tools:** Hydra(Kali), Windows Security logs
**Goal:** Within five minutes, identify brute force attempts that are followed by a successful privileged login from the same IP.







