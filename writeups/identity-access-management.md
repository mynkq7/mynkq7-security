
# Identity and Access Management

**Identity and Access Management (IAM)**

Identity and Access Management is a core component of cybersecurity that ensures the right individuals get the right access to the right information at the right time.

It is a framework of policies, procedures, and technologies used to manage:

- Who the person is (Identity)
- What they can access (Authorization)
- How they can prove themselves (Authentication)

---

## Core Components of IAM

| Component | Description | Examples |
| --- | --- | --- |
| Identity | Creating, managing, and deleting users | Active Directory, Azure AD |
| Authorization | Determining what users can access | Role-Based Access Control (RBAC) |
| Authentication | Verifying user identity before giving access | MFA, Authenticator Apps, Biometrics, OAuth |
| Single Sign-On (SSO) | One login grants access to multiple apps | Google Workspace, Okta |
| Multi-Factor Authentication (MFA) | Verifying users with two or more factors | Authenticator Apps, OTPs, Security Keys |
| Audit and Compliance | Tracking who accessed what | SIEM Logs, Audit Records |
| Privileged Access Management | Controlling access to sensitive admin accounts | CyberArk, BeyondTrust |

---

## IAM Flow

1. User requests access (login to a portal)
2. System authenticates the user
3. IAM checks authorization using RBAC policies
4. Access is granted or denied
5. Logs and monitoring are maintained for audits

---

## IAM Models

- **RBAC (Role-Based Access Control)**
    
    Access based on roles like "Admin", "Analyst", etc.
    
- **ABAC (Attribute-Based Access Control)**
    
    Access based on attributes like user, environment, and resource.
    
- **PBAC (Policy-Based Access Control)**
    
    Uses fine-grained policies combining RBAC and ABAC.
    
- **Zero Trust IAM**
    
    "Never trust, always verify" — continuously authenticates users.
    

---

## IAM in Practice

| Function | Purpose | Notes |
| --- | --- | --- |
| Onboarding and Offboarding | Automatically provisioning and deprovisioning users |  |
| Least Privilege Enforcement | Users get only the access they need |  |
| Access Reviews | Periodic verification of who has access to what |  |
| Audit Trails | Forensics and compliance with frameworks like GDPR, ISO 27001, etc. |  |
| SSO and Federation | Centralized login for multiple apps via SAML and OAuth |  |

---

## Threats Prevented by IAM

- Account Takeovers
- Privilege Escalation
- Insider Threats
- Data Exfiltration
- Shadow IT Access
- Password Reuse and Weak Authentication
