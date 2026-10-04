[Arjun R Pillai](#top)

[Experience](#experience) [Projects](#projects) [Evidence](#evidence) [Certifications](#certifications) [Education](#education) [Contact](#contact)

Open to SOC L1 and IT support roles

# Arjun R Pillai

$ SOC L1 Analyst

- SOC L1 Analyst
- IT Help Desk
- Technical Support

I triage alerts, investigate incidents and keep endpoints running. A year on a support desk taught me to close tickets inside SLA. A SOC training internship and a set of documented home labs taught me to read the logs behind them.

[View projects](#projects) [Get in touch](#contact)

Alert queue · lab replay

**1,464**events

**1,327**auth failures

**13**successful logins

CRITICAL

Rule 40112 · SSH brute force then login

Real Hydra attack on my own lab VM. Triaged, then mapped to MITRE ATT&CK.

T1110

Brute Force

→

T1078

Valid Accounts

→

T1021

Remote Services

**7**documented lab projects

**12+**custom Snort rules written

**100+**Snort events triaged

**500+**packets analysed in Wireshark

**11+**2023–2025 breaches researched

**5**open-source SIEMs compared

Security operations

### Detect, triage, escalate

- Wazuh
- ELK / Kibana
- Splunk
- IBM QRadar (trial)
- TheHive
- Jira
- Snort
- Wireshark
- MITRE ATT&CK
- Alert triage
- IOC extraction

Help desk and support

### Fix it, document it, close it

- Ticket resolution within SLA
- Windows install and reimaging
- Endpoint software setup
- User accounts and onboarding
- IP addressing
- DNS
- LAN troubleshooting
- Windows
- Linux

Foundations

### Frameworks and tooling

- NIST CSF
- ISO 27001:2022
- PCI DSS
- OWASP Top 10
- Nessus
- OpenVAS
- Qualys CE
- Python
- Bash
- Kali Linux
- Packet Tracer

Experience

## From the help desk to the SIEM

Two roles. One taught me to resolve problems fast, the other to find them in the logs.

**May 2026 – Present**Remote

### Cybersecurity Intern, SOC Training Programme

CyberXchange

- Deployed Wazuh and ELK SIEM on a cloud VPS. Integrated firewall, application, IDS/IPS and endpoint logs, and built a custom Kibana dashboard to visualise attacks.
- Investigated simulated port scan, SQL injection and USB data exfiltration incidents. Identified source IPs, exact timestamps and log locations, raised TheHive tickets with email alerts to stakeholders and followed up to closure.
- Wrote SIEM detection rules for SQL injection, DDoS and consecutive firewall login failures. Analysed sample pcap files and documented findings.
- Documented security log quality parameters against international standards. Explored Splunk and IBM QRadar trial interfaces.
- Researched 11+ major 2023–2025 breaches and vulnerabilities (root cause, attack path, impact) and compared 5 open-source SIEM tools on strengths and trade-offs.
- Installed Nessus Essentials, explored Qualys Community Edition, and built a Packet Tracer lab with inter-network routing and ACL traffic filtering.

- Wazuh
- ELK
- TheHive
- Splunk
- Nessus
- Packet Tracer

**May 2025 – May 2026**Kochi, Kerala

### Technical Support Engineer

TeknogenX Private Limited

- Resolved helpdesk tickets end to end within SLA targets.
- Handled Windows OS installation, reimaging and endpoint software setup.
- Configured IP addressing, DNS and LAN connectivity.
- Managed user accounts and onboarding across Windows and Linux environments.

- Windows
- Linux
- DNS
- LAN
- SLA

Projects

## Labs I built, attacked and investigated

Each one has a write-up. I run the attack, then work the alert like an L1 analyst would.

FEATUREDWazuh · Hydra

### SOC Home Lab: SSH Brute Force Detection

Ran a real Hydra attack against a lab VM and watched it surface in Wazuh. Triaged the critical Rule 40112 alert, separated the failed attempts from the successful logins, and mapped the kill chain to MITRE ATT&CK.

- Wazuh
- Hydra
- MITRE ATT&CK
- Alert triage

Events generated**1,464**

Authentication failures**1,327**

Successful logins**13**

Kill chain**T1110 → T1078 → T1021**

RED + BLUEActive Directory

### Kerberoasting: Domain Compromise to Forensics

Built a Windows Server 2022 domain controller (corp.local) with an SPN on a service account. Attacked it from Kali with Impacket and Hashcat, cracked the weak service password offline, then used event logs 4769, 4728, 4672 and 4624 to trace the whole intrusion. Fixed clock skew (KRB_AP_ERR_SKEW) with ntpdate.

Case file

Goal

Attack a domain, then find the evidence.

Setup

Windows Server 2022 DC, SPN on SQL_SVC, Kali with Impacket and Hashcat.

Result

Service ticket cracked offline, admin share reached, events 4769 / 4728 / 4672 / 4624 traced.

- Windows Server 2022
- Impacket
- Hashcat
- Event logs

SIEMSplunk Enterprise

### Centralized Log Analysis with Splunk

Built a Universal Forwarder pipeline across 3+ Linux and Windows endpoints. Wrote 5+ SPL dashboards and threat-hunting queries.

Case file

Goal

Centralize Linux and Windows logs and hunt in them.

Setup

Universal Forwarder on 3+ endpoints, 5+ SPL dashboards.

Result

Searchable single pane for threat-hunting queries.

- Splunk
- SPL
- Universal Forwarder
- Threat hunting

IDSSnort

### Kali Snort IDS

Deployed Snort in a 3-VM lab and wrote 12+ custom rules. Triaged 100+ events as true or false positives and wrote IOC-based incident reports.

Case file

Goal

Detect hostile traffic with custom signatures.

Setup

Snort in a 3-VM lab, 12+ custom rules.

Result

100+ events triaged true or false positive, IOC-based incident reports.

- Snort
- Kali
- IOCs

PCAPWireshark

### Wireshark DoS / DDoS Analysis

Simulated ICMP, UDP and TCP floods. Analysed 500+ packets, extracted 10+ IOCs and wrote a Tier 1 incident report with a firewall escalation playbook.

Case file

Goal

Recognise flood attacks in packet captures.

Setup

ICMP, UDP and TCP flood simulations in Wireshark.

Result

500+ packets analysed, 10+ IOCs, Tier 1 report with firewall escalation playbook.

- Wireshark
- Tier 1 report
- Playbook

DECEPTIONHoneypot

### Active Decoy Honeypot

Ran a Pentbox listener on port 80 in Kali. It logged source IP, User-Agent and timestamp for each connection and raised a real-time red-screen alert on an unauthorized attempt.

Case file

Goal

Study unauthorized access attempts.

Setup

Pentbox listener on port 80 in Kali.

Result

Logged source IP, User-Agent and timestamp. Red-screen alert fired on an unauthorized connection.

- Pentbox
- Kali
- Threat intel

PYTHONIntegrity monitoring

### The Sentinel: File Integrity Monitor

A Python tool that takes a SHA-256 baseline of a directory, re-scans every 2 seconds and flags new, modified and deleted files in near real time.

Case file

Goal

Detect unauthorized change in a watched directory.

Setup

Python script, SHA-256 baseline of /vault, re-scan every 2 seconds.

Result

Flags new, modified and deleted files. Tested with a simulated append to a file.

- Python
- SHA-256
- FIM

Lab evidence

## Screenshots from the labs, up close

Real captures from my write-ups. Click to zoom, drag to pan, and tap the glowing dots on the first image to read the numbers the way I triaged them.

Click image to zoom · drag to pan

Certifications

## Credentials

Two industry certifications, plus the courses and job simulations behind them.

CSA

### Certified SOC Analyst (CSA v2)

Issuer

EC-Council

Passed

08 March 2026

Renewable

01 April 2027

Cert ID

ECC0195784326

CICSA

### Certified IT Infrastructure & Cyber SOC Analyst (CICSA v3)

Issuer

RedTeam Hacker Academy

Date

15 February 2026

Cert ID

RTXSTU1558014800

Courses

### Learning programmes

- Connect and Protect: Networks and Network Security Google · Coursera
- Play It Safe: Manage Security Risks Google · Coursera
- Ethical Hacking with AI NSDC · Skill India

Virtual job simulations

### Forage

- Mastercard Cybersecurity Forage
- TCS Cybersecurity Analyst (IAM) Forage
- Deloitte Cyber Forage

Education

## Where I studied

2025 – 2026

### Cyber SOC Analyst Program (CICSA v3)

RedTeam Hacker Academy, Kochi

2020 – 2023

### B.Sc. Computer Science

Swamy Saswathikananda College, Kerala

Contact

## Hiring for L1 or support? Let's talk.

Based in Kottayam, Kerala. Available for SOC L1 Analyst, IT Help Desk and Technical Support roles.

[linkedin.com/in/arjunrpillai-socLinkedIn](https://www.linkedin.com/in/arjunrpillai-soc) [github.com/arjunrajeevpillaiGitHub](https://github.com/arjunrajeevpillai)

Arjun R Pillai · Kottayam, KeralaSOC L1 · Help Desk · Tech Support