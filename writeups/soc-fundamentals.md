# Security Operations Center (SOC) and Incident Response

---

## Overview

SOC has some resources available as form of security solutions.  
These solutions integrate whole company systems and networks to monitor from one centralized location.

### Main Purpose

- **Detect and Respond**

> Continuous monitoring is required to detect and respond to security incidents.

---

## Detection

- Detect vulnerabilities  
- Detect unauthorized activity  
- Detect policy violations  
- Detect intrusions

---

## Response

Once an incident is detected, certain steps are taken to respond:

- Minimizing the effect  
- Performing root cause analysis of the incident

---

## Three Pillars of SOC

### 1. People

#### SOC L1
- Anything detected by the security solution passes through these analysts first.  
- Perform basic alert triage to determine if a detection is harmful.  
- Report these detections through proper channels.

#### SOC L2
- Perform deeper investigations.  
- Correlate data from multiple resources for analysis.

#### SOC L3
- Comes from L1 and L2 analysts.  
- Look for threat indicators.  
- Support in incident response activities (containment, eradication, and recovery).

#### Security Engineer
- Works on security solutions.  
- Deploy and configure security solutions.

#### Detection Engineer
- Builds logic behind security solutions to detect harmful activities.  
- Establishes rules for alerting security solutions.

#### SOC Manager
- Manages the SOC team.  
- Provides support and ensures workflow.  
- Remains in contact with the CISO to provide updates on SOC security posture and efforts.

---

### 2. Process

#### Alert Triage
- Focuses on analyzing the specific alert.  
- Determines the severity of alerts.  
- Helps prioritize.

**All about answering the 5 W’s:**

| W | Description |
|---|--------------|
| **What** | A malicious file was detected on one of the hosts inside the organization network. |
| **When** | The file was detected at 13:20 on June 5, 2025. |
| **Where** | The file was detected in the directory of host “GEORGE PC.” |
| **Who** | The file was detected for the user George. |
| **Why** | Investigation found the file was downloaded from a pirated software-selling website. |

These detected harmful alerts need to be escalated to higher-level analysts for a timely response and resolution, along with the **5 W’s** and **screenshots**.

Sometimes the reported detection highly points to malicious critical activities.  
In this situation, a high-level team initiates an **incident response**.

---

## Incident Response

### Incidents

Any unauthorized event, planned or accidental, that negatively impacts digital assets.  

Examples:
- Denial of service  
- Data leaks  
- Security breaches  
- Malware infections  

---

### Incident Response Framework

#### 1. Preparation
Building necessary resources to handle the incident.

**Resources include:**
- Developing incident response teams  
- Having proper incident response plans in place  
- Deploying necessary security solutions  

---

#### 2. Identification
Looking for abnormal behaviors that may indicate an incident.

**Involves:**
- Using various security solutions and techniques  
- Monitoring abnormal events  

**Common Tools:**
- **SIEM:** Collects logs in a centralized location and correlates them to identify incidents.  
- **AV:** Detects known malicious programs and scans regularly.  
- **EDR:** Protects endpoints, contains and eradicates advanced threats.

---

#### 3. Containment
Minimizing the impact of the attack.  
Usually done by:
- Isolating the victim machine  
- Disabling compromised user accounts

---

#### 4. Eradication
- Removing the threat from the affected environment  
- Ensuring the environment is clean

---

#### 5. Recovery
- Recovering affected systems from backups or rebuilding them  
- Testing and validating recovered systems before reuse

---

#### 6. Lessons Learned
- Document gaps in detection and analysis  
- Improve processes for future incidents  

---

### Playbooks vs Runbooks

| Term | Description |
|------|--------------|
| **Playbook** | Step-by-step instructions to deal with incidents. |
| **Runbook** | Step-by-step execution of specific steps during different incidents. |

---

### Incident Response Teams (CIRT)

- Called on demand  
- Handle critical incidents  
- Perform deep forensic analysis  
- Recover breached systems  
- Identify hidden threats  
- Support SOC with analysis  

**Incident Response Team Roles:**
- Forensic Lead  
- CSIRT Manager  
- Threat Intelligence Expert  
- Threat Hunting Expert  
- Malware Analyst  

---

### Specialized Defensive Roles

#### Digital Forensic Analyst
- Uncovers hidden threats in memory and disk.

#### Threat Intelligence Analyst
- Gathers data about emerging threat groups.

#### Application Security Engineer
- Maintains a secure software development lifecycle.

#### AI Researcher
- Studies AI threats and develops defensive strategies.

---

### 3. Technology

Security solutions minimize the SOC team’s manual effort to detect and respond to threats.  

**Common Tools:**
- SIEM  
- EDR  
- Firewalls  

---
