Cybersecurity Notes

These are my personal notes and understanding of cybersecurity concepts after completing the Google Cybersecurity course.
I wrote this in my own words to revise, share knowledge, and track my journey in cybersecurity.

1. Fundamentals
CIA Triad

Confidentiality: Only authorized users can access data.

Integrity: Data remains accurate and unaltered.

Availability: Systems and data are accessible when needed.

Quick recall: C = secrecy, I = correctness, A = uptime

Threats, Vulnerabilities, Risks

Threat: Potential cause of harm (malware, hackers, insider threats)

Vulnerability: Weakness in a system

Risk: Likelihood of threat exploiting vulnerability × impact

Formula:
Risk = Threat × Vulnerability × Impact

Security Principles

Least Privilege: Grant minimum access required.

Defense in Depth: Multiple layers of security.

Zero Trust: Always verify, never trust.

Separation of Duties: Split responsibilities to reduce errors/fraud.

Defense in Depth Layers

Perimeter Layer: Firewalls, user authentication

Network Layer: Network monitoring, authorization

Endpoint Layer: Antivirus, endpoint protection

Application Layer: MFA, security embedded in apps

Data Layer: Protect critical data (PII, financial info)

CVE & Vulnerability Scoring

Exposure: Mistake exploitable by a threat.

CVE (Common Vulnerabilities and Exposures): Public list of vulnerabilities.

CNA: Organizations that validate CVEs.

CVSS: Severity scoring (e.g., 4.0+ Medium, 5.0+ High).

OWASP & OSINT

OWASP: Publishes Top 10 web app vulnerabilities.

OSINT: Gathering information from public sources for cybersecurity investigations.

2. Threat Actors & Attacks
Threat Actors
Actor	Motivation	Example
Script Kiddie	Fun / challenge	Uses ready-made tools
Hacktivist	Political / social	Anonymous-like groups
Insider	Revenge / financial gain	Employee misusing access
Nation-State	Espionage / warfare	APT groups (targeted attacks)
Cybercriminal	Money	Ransomware gangs
Social Engineering

Stages: Prepare → Establish Trust → Persuasion → Disconnect

Prevention: Awareness, training, managerial controls

Phishing Variants:

Spear: Targeted phishing

Whaling: Targeting executives

Smishing: SMS phishing

Vishing: Voice/phone phishing

Malware

Types: Virus, Worm, Trojan, Ransomware, Spyware, Cryptojacking

Signs: System slowdowns, high CPU, crashes, battery drain, unexpected electricity use

Web-Based Exploits

SQL Injection: Unauthorized DB queries via input fields

XSS (Cross-Site Scripting): Inject malicious scripts into web apps (Reflected, Stored, DOM-based)

Password & Authentication Attacks

Attacks: Brute Force, Dictionary, Reverse Brute Force, Credential Stuffing, Pass-the-Hash

Prevention: MFA, password policies, hashing & salting, CAPTCHA

Tools: Aircrack-ng, Hashcat, John the Ripper, Ophcrack, THC Hydra

3. Network Monitoring & Analysis
Network Traffic

Data transmitted across networks (HTTP, HTTPS, etc.).

Monitoring helps detect abnormal patterns and anomalies.

Indicators of Compromise (IoC)

Observable signs that indicate a potential breach.

Examples: Suspicious IPs, unusual login times, malware signatures.

Data Exfiltration

Unauthorized transmission of data from a system.

Detection: Large/unusual data transfers, unexpected outbound connections.

Network Communications (What to log)

Source & destination IP

Protocols used

Amount of data transferred

Date & time of transactions

Monitoring & Baselines

Continuous monitoring establishes a baseline of normal behavior.

Detect deviations and trigger investigations.

Flow Analysis

Flow: Movement of packets between endpoints (includes ports, protocols).

Ports: For example, port 443 → HTTPS.

Command & Control (C2)

Channels attackers use to control compromised hosts remotely.

Network Operations Center (NOC)

Focus: uptime, performance, and network health (not the same as SOC).

Network Monitoring Tools

IDS/IPS: Intrusion Detection / Prevention Systems

Packet Sniffers / Protocol Analyzers: Wireshark, tcpdump

SIEM / Logging: Collect and analyze event data

Packets & Packet Analysis

Structure: Header → Payload → Footer

Pcap files: Capture packet data for offline analysis

Data Exfiltration Kill Chain (Typical Steps)

Initial Access

Lateral Movement & Pivoting

Discovery of Assets

Collection & Preparation

Exfiltration

Defensive Measures: Strong authentication, network monitoring, asset protection, DLP, EDR, SIEM alerts.

4. Threat Modeling
Process

Define Scope — What systems/assets are in scope?

Inventory Assets — Catalog important resources.

Identify Threats — Who might attack and how?

Characterize Environment — Understand attacker capabilities and goals.

Analyze Threats — Find attack paths and gaps.

Mitigate Risk — Prioritize controls and remediation.

Evaluate Findings — Document and iterate.

Tools / Frameworks

Attack Trees

PASTA Framework (7 stages)

STRIDE / DREAD (as applicable)

5. Vulnerability Assessment & Penetration Testing
Vulnerability Assessment

Goal: Find weak points before attackers do.

Process: Identification → Scanning → Risk Assessment → Remediation

Scan Types: External, Internal, Authenticated, Unauthenticated, Link, Comprehensive

Penetration Testing

Simulated ethical attacks to validate vulnerabilities and controls.

Team Roles: Red (attack), Blue (defend), Purple (collaboration)

Test Types: Open-box, Closed-box, Partial-knowledge, Bug bounty

6. Security Operations & Incident Response
SOC Levels

L1: Monitor & escalate alerts

L2: Investigate alerts, tune detection rules

L3: Forensics, malware analysis, advanced response

SOC Manager: Reporting, coordination, policy

NIST Incident Response Lifecycle

Preparation

Detection & Analysis

Containment

Eradication

Recovery

Lessons Learned

Detection, Analysis & Threat Intelligence
Detection

Prompt discovery using sensors and SIEM rules.

SIEM Examples: Splunk, Chronicle, IBM QRadar

Analysis

Validate alerts, triage incidents, identify IoCs.

Threat Intelligence (TI)

Who: Attackers

What: Types of attacks (phishing, ransomware)

How: TTPs (Tactics, Techniques, Procedures)

Why: Motivation (financial, political, espionage)

Where/When: Targets and timing info

TI Types: Strategic, Tactical, Operational, Technical

Crowdsourcing in Cybersecurity

Use the security community and ethical hackers to discover vulnerabilities (bug bounties, public reporting).

Playbooks

Predefined procedures for responding to incidents.

Types: Non-automated, Semi-automated, Automated

Triage Questions (Example)

Is there anything out of the ordinary?

Are there multiple failed login attempts?

Are there logins outside working hours?

Containment, Eradication & Recovery

Containment: Limit the blast radius and stop further damage.

Eradication: Remove malware, patch vulnerabilities, close access.

Recovery: Restore systems, re-image, reset credentials, validate.

Chain of Custody

Document evidence handling to ensure integrity in investigations.

Custody Log (example columns):

Item # | Date & Time | Released by | Purpose of Transfer

Evidence Description (example columns):

Item # | Quantity | Description (host, MAC, IP)

Documentation & Reporting

Essential for transparency, audits, and lessons learned.

Final reports inform improvements and prevent blame — focus on learning.

7. Logs, Telemetry & Detection Tech
Logs

Records of system events (date, time, actor, action).

Types: Network, System, Application, Security, Authentication

Formats: syslog, JSON, XML, CSV

Telemetry

Continuous collection of data used for detection and investigation.

IDS (Intrusion Detection System)

Types: HIDS (Host-based), NIDS (Network-based)

Detection Method: Signature analysis, anomaly detection

Example Tool: Suricata

SIEM

Collects and correlates logs to identify patterns and anomalies.

8. Linux, SQL, CI/CD, DevSecOps, Cloud & Tools
Linux Basics

Commands: ls -l, chmod, chown, sudo

SQL Basics

Queries: SELECT, INSERT, UPDATE, DELETE

CI/CD & DevSecOps

Integrate security into build and deployment pipelines (IaC scanning, SAST, DAST).

Cloud Security

Focus: IAM, MFA, encryption, monitoring, secure configurations

Common Tools

Wireshark, Splunk, Nessus, Metasploit, Burp Suite, Kali Linux, Hashcat, John the Ripper

9. Real-World Case Studies & Learning

Study incidents (ransomware, data exfiltration, supply-chain attacks) to learn attacker TTPs and improve defenses.

Document lessons learned and update playbooks, detection rules, and training
