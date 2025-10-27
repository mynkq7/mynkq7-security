# Cybersecurity Notes

These are my personal notes and understanding of cybersecurity concepts after completing the Google Cybersecurity course.  
I wrote this in my own words to revise, share knowledge, and track my journey in cybersecurity.

---

## 1. Fundamentals

### CIA Triad
- Confidentiality: Only authorized users can access data.  
- Integrity: Data remains accurate and unaltered.  
- Availability: Systems and data are accessible when needed.  
**Quick recall:** C = secrecy, I = correctness, A = uptime

### Threats, Vulnerabilities and Risks
- Threat: Potential cause of harm (malware, hackers, insider threats)  
- Vulnerability: Weakness in a system  
- Risk: Likelihood of a threat exploiting a vulnerability × impact  

**Risk = Threat × Vulnerability × Impact**

### Security Principles
- Least Privilege: Provide only the minimum access required  
- Defense in Depth: Multiple layers of security  
- Zero Trust: Never trust, always verify  
- Separation of Duties: Split responsibilities to reduce fraud or mistakes

### Defense in Depth Layers
| Layer | Examples |
|--------|---------|
| Perimeter | Firewalls, user authentication |
| Network | Network monitoring, access controls |
| Endpoint | Antivirus, EDR tools |
| Application | MFA, secure development practices |
| Data | Encrypt and protect sensitive data (PII, financial data) |

### CVE and Vulnerability Scoring
- CVE: Public list of known vulnerabilities  
- CNA: Organizations authorized to assign CVEs  
- CVSS: Severity scoring system (4.0+ Medium, 5.0+ High)

### OWASP and OSINT
- OWASP: Publishes Top 10 web application vulnerabilities  
- OSINT: Collecting information from publicly available sources

---

## 2. Threat Actors and Attacks

### Threat Actors
| Actor | Motivation | Example |
|--------|------------|---------|
| Script Kiddie | Fun or curiosity | Uses pre-made tools |
| Hacktivist | Political or social causes | Anonymous-like groups |
| Insider | Revenge or financial gain | Employee misuse of access |
| Nation-State | Espionage or warfare | APT groups |
| Cybercriminal | Money | Ransomware groups |

### Social Engineering
Stages: Preparation → Establish Trust → Persuasion → Disconnect  
Prevention: Awareness training, policies, and verification procedures

**Phishing Types:**
- Spear Phishing (Targeted)
- Whaling (Executives)
- Smishing (SMS)
- Vishing (Voice or phone)

### Malware
Types: Virus, Worm, Trojan, Ransomware, Spyware, Cryptojacking  
Signs: System lag, high CPU, crashes, battery drain, unknown processes

### Web-Based Attacks
| Attack | Description |
|--------|-------------|
| SQL Injection | Unauthorized database queries via input fields |
| XSS (Cross-Site Scripting) | Inject malicious scripts into web apps |

### Password and Authentication Attacks
Attacks: Brute Force, Dictionary, Credential Stuffing, Pass-the-Hash  
Prevention: MFA, strong passwords, hashing + salting, CAPTCHA  
Tools: Hashcat, John the Ripper, Aircrack-ng, THC Hydra

---

## 3. Network Monitoring and Analysis

### Network Traffic
Data transferred across networks (HTTP, HTTPS, FTP, etc.)

### Indicators of Compromise (IoCs)
Signs of a possible breach, such as:  
- Suspicious IPs  
- Login at unusual times  
- Malware signatures

### Data Exfiltration
Unauthorized transfer of data from a system  
Detection: Large outbound transfers, unknown FTP/SSH connections

### What to Log
- Source and destination IPs  
- Protocols (TCP, UDP, HTTP, etc.)  
- Amount of data transferred  
- Timestamp of events

### Monitoring and Baselines
- Establish normal network behavior  
- Detect deviations or anomalies

### Tools
- IDS/IPS (Intrusion Detection/Prevention Systems)  
- Packet Sniffers (Wireshark, tcpdump)  
- SIEM (Splunk, Chronicle, QRadar)

### Packet Structure
Header → Payload → Footer  
Pcap files: Store captured network packets

---

## 4. Threat Modeling

### Process
1. Define Scope  
2. Inventory Assets  
3. Identify Threats  
4. Characterize Environment  
5. Analyze Threats  
6. Mitigate Risk  
7. Document and Evaluate

### Tools and Frameworks
- STRIDE, DREAD  
- PASTA Framework  
- Attack Trees

---

## 5. Vulnerability Assessment and Penetration Testing

### Vulnerability Assessment
Goal: Identify vulnerabilities before attackers exploit them  
Steps: Identify → Scan → Assess Risk → Remediate

### Types of Scans
- External, Internal  
- Authenticated vs Unauthenticated  
- Comprehensive vs Limited

### Penetration Testing
Simulated ethical hacking to test system defenses

| Team | Role |
|------|------|
| Red Team | Attack |
| Blue Team | Defend |
| Purple Team | Coordinate between Red and Blue |

Test Types: Black-box, White-box, Grey-box, Bug bounty

---

## 6. Security Operations and Incident Response

### SOC Levels
| Level | Task |
|--------|------|
| L1 | Monitor and escalate alerts |
| L2 | Investigate and tune alerts |
| L3 | Forensics, advanced analysis |

### NIST Incident Response Lifecycle
1. Preparation  
2. Detection and Analysis  
3. Containment  
4. Eradication  
5. Recovery  
6. Lessons Learned

### Chain of Custody
Tracks evidence handling with:
- Item number  
- Date and time  
- Released by / received by  
- Purpose of transfer

---

## 7. Logs, Telemetry and Detection Technologies

### Logs
Records of system or network activity  
Types: System, Network, Security, Application, Authentication

### Telemetry
Continuous data from devices for monitoring and incident detection

### IDS Types
- HIDS: Host-based intrusion detection  
- NIDS: Network-based intrusion detection  
Detection Methods: Signature or anomaly-based

### SIEM
Security tools that collect, correlate and analyze logs for suspicious activity

---

## 8. Linux, SQL, CI/CD, DevSecOps, Cloud and Tools

### Linux Basics
Commands:  
- `ls -l` (list with details)  
- `chmod` (change permissions)  
- `chown` (change ownership)  
- `sudo` (run as admin)

### SQL Basics
- SELECT, INSERT, UPDATE, DELETE

### CI/CD and DevSecOps
- Integrate security in development pipelines  
- SAST, DAST, IaC scanning

### Cloud Security
Focus areas:  
- IAM (Identity and Access Management)  
- MFA (Multi-Factor Authentication)  
- Encryption  
- Monitoring and configuration management

### Common Tools
Wireshark, Splunk, Nessus, Metasploit, Burp Suite, Kali Linux, Hashcat, John the Ripper

---

## 9. Real-World Case Studies and Learning

- Study incidents like ransomware, supply-chain attacks, data breaches  
- Analyze attacker TTPs (Tactics, Techniques, Procedures)  
- Update detection rules, playbooks, response strategies
