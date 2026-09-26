# 🔐 Microsoft Cloud SOC Lab – Matome Mabitsi

Welcome to my Microsoft Cloud Security Operations Center (SOC) Lab.

This project demonstrates the design, deployment, monitoring, and security investigation of a cloud-first environment built using Microsoft security technologies.

The lab focuses on real-world security operations activities including:

- Identity and Access Management
- Security Monitoring
- Threat Detection
- Threat Hunting
- Incident Response
- Microsoft Defender XDR
- Microsoft Entra ID
- Conditional Access
- Multi-Factor Authentication (MFA)
- Microsoft Defender for Endpoint
- Microsoft Defender for Office 365
- Zero Trust Security

All activities were performed in a dedicated lab environment using Microsoft trial services, synthetic users, and authorized devices.

---

# 👋 About Me

I am a **Cloud Engineer** with a passion for cybersecurity, cloud security, and security operations.

My goal is to develop practical, hands-on security skills by building real-world lab environments that simulate how modern organizations protect identities, endpoints, email, and cloud services.

This project demonstrates my ability to:

- Deploy Microsoft security solutions
- Investigate security incidents
- Conduct threat hunting
- Implement Zero Trust controls
- Document investigations professionally

---

# 🎯 Project Objectives

The main objectives of this project were to:

✅ Build a Microsoft Cloud Security Environment

✅ Deploy Microsoft Defender XDR

✅ Implement Multi-Factor Authentication

✅ Configure Conditional Access

✅ Secure Microsoft Entra Identities

✅ Monitor User Activity

✅ Investigate Security Alerts

✅ Perform Threat Hunting

✅ Simulate Security Incidents

✅ Document Findings Using GitHub

---

# 🏗 Lab Architecture

```text
Internet
    │
    │
  kali1
    │
    │
Microsoft Cloud
│
├── Microsoft Entra ID
├── Microsoft 365 Admin Center
├── Microsoft Defender XDR
├── Defender for Endpoint
├── Defender for Office 365
├── Conditional Access
├── MFA
├── Identity Protection
├── Attack Simulation Training
└── Advanced Hunting
│
├── LAB-ADMIN01
│   Windows 11
│
└── LAB-USER01
    Windows 11
```

---

# 🖼 Architecture Diagram

> Add architecture screenshot here

Architecture/architecture-diagram.png

---

# 🧰 Technologies Used

## Microsoft Security Technologies

- Microsoft 365 E5 Trial
- Microsoft Entra ID
- Microsoft Defender XDR
- Microsoft Defender for Endpoint
- Microsoft Defender for Office 365
- Microsoft Authenticator
- Conditional Access
- Identity Protection
- Microsoft Secure Score
- Attack Simulation Training
- Advanced Hunting

## Operating Systems

- Windows 11
- Kali Linux

## Virtualization

- Hyper-V

## Documentation

- GitHub
- Markdown

---

# 👥 Users Created

The following cloud identities were created.

| User | Purpose |
|--------|---------|
| labglobaladmin | Global Administrator |
| securityadmin | Security Administrator |
| alice | Finance Employee |
| bob | HR Employee |
| finance | Finance Test Account |
| hr | Human Resources Test Account |
| attacksim | Security Testing Account |

---

# 🛡 Security Controls Implemented

## Multi-Factor Authentication (MFA)

MFA was enabled for all laboratory users.

### Objectives

- Prevent password-only compromise
- Improve account security
- Align with Zero Trust principles

### Evidence

> Add screenshot

Screenshots/mfa-configuration.png

---

## Security Groups

Created groups:

```text
GRP-Lab-Admins
GRP-SOC
GRP-Finance
GRP-HR
GRP-Employees
GRP-CA-Pilot
```

These groups were used for role assignment and Conditional Access targeting.

### Evidence

> Add screenshot

Screenshots/security-groups.png

---

## Conditional Access

The following Conditional Access policies were created.

### Policy 1

Require MFA for Administrators

### Policy 2

Require MFA for Users

### Policy 3

Block Legacy Authentication

Policies were first deployed in Report Only mode and then tested before enforcement.

### Evidence

> Add screenshot

Screenshots/conditional-access.png

---

# 📊 Secure Score Assessment

Microsoft Secure Score was reviewed to assess the tenant security posture.

Activities included:

- Reviewing recommendations
- Identifying security gaps
- Planning remediation actions

### Evidence

> Add screenshot

Screenshots/secure-score.png

---

# 🖥 Microsoft Defender XDR Deployment

Microsoft Defender XDR was deployed and configured.

Areas reviewed included:

- Incidents
- Alerts
- Assets
- Devices
- Threat Analytics
- Reports
- Email Security

### Evidence

> Add screenshot

Screenshots/defender-dashboard.png

---

# 🛡 Microsoft Defender for Endpoint

LAB-USER01 was onboarded to Microsoft Defender for Endpoint.

Activities included:

- Device onboarding
- Device health verification
- Security monitoring
- Endpoint visibility

### Evidence

> Add screenshot

Screenshots/device-onboarding.png

---

# 🔍 Threat Hunting

Threat hunting was performed using Microsoft Defender Advanced Hunting.

---

## Query 1 – Recent Device Events

```kusto
DeviceEvents
| where Timestamp > ago(1d)
```

---

## Query 2 – PowerShell Activity

```kusto
DeviceProcessEvents
| where FileName contains "powershell"
```

---

## Query 3 – Network Activity

```kusto
DeviceNetworkEvents
| where Timestamp > ago(1d)
```

---

## Evidence

> Add screenshot

Screenshots/advanced-hunting.png

---

# 🚨 Security Investigations

---

# Incident 001

## Suspicious Cloud Login Activity

### Scenario

Several failed sign-in attempts were generated using the controlled testing account:

```text
attacksim
```

Activity originated from:

```text
kali1
```

### Investigation

Reviewed:

- Sign-in Logs
- Authentication Details
- Conditional Access Results
- IP Information
- Login Success/Failure

### Findings

- Failed authentication attempts recorded
- Successful MFA login validated
- Conditional Access policy evaluation confirmed

### Evidence

> Add screenshot

Incidents/INC-001/signin-logs.png

---

# Incident 002

## Conditional Access Enforcement

### Scenario

User access attempts were tested against Conditional Access policies.

### Investigation

Reviewed:

- Policy Evaluation
- Access Decisions
- MFA Requirements
- Report-Only Results

### Findings

- Policies evaluated correctly
- Access control worked as expected

### Evidence

> Add screenshot

Incidents/INC-002/ca-results.png

---

# Incident 003

## Endpoint Security Alert

### Scenario

A Microsoft Defender for Endpoint simulation was executed on:

```text
LAB-USER01
```

### Investigation

Reviewed:

- Alert Details
- Incident Severity
- Device Timeline
- Process Activity
- Security Recommendations

### Findings

- Alert generated successfully
- Investigation workflow completed
- Incident documented

### Evidence

> Add screenshot

Incidents/INC-003/endpoint-alert.png

---

# Incident 004

## Phishing Simulation

### Scenario

A phishing simulation campaign was launched using:

```text
Microsoft Attack Simulation Training
```

### Target

```text
alice
```

### Investigation

Reviewed:

- Email Delivery
- Email Opens
- Link Clicks
- User Responses
- Training Results

### Findings

- User interaction successfully tracked
- Security awareness capability demonstrated

### Evidence

> Add screenshot

Incidents/INC-004/phishing-simulation.png

---

# 🧠 Incident Response Workflow

The following incident response process was used throughout the project.

## 1. Identify

- Detect alerts
- Validate events

## 2. Investigate

- Review evidence
- Analyze timelines
- Correlate data

## 3. Contain

- Revoke sessions
- Reset passwords
- Restrict access

## 4. Eradicate

- Remove threats
- Correct security issues

## 5. Recover

- Restore services
- Confirm normal operations

## 6. Lessons Learned

- Document findings
- Improve security posture

---

# 🔐 Zero Trust Implementation

The project was aligned to Microsoft Zero Trust principles.

---

## Verify Explicitly

Implemented:

- MFA
- Conditional Access
- Sign-In Monitoring

### Evidence

> Add screenshot

Screenshots/verify-explicitly.png

---

## Use Least Privilege

Implemented:

- Security Administrator Roles
- Role-Based Access Control
- Group-Based Administration

### Evidence

> Add screenshot

Screenshots/least-privilege.png

---

## Assume Breach

Implemented:

- Security Monitoring
- Threat Hunting
- Incident Response

### Evidence

> Add screenshot

Screenshots/assume-breach.png

---

# 📁 Repository Structure

```text
Microsoft-Cloud-SOC-Lab
│
├── README.md
├── Architecture
├── Secure-Score
├── Identity
├── Conditional-Access
├── Defender
├── Threat-Hunting
├── Incidents
├── Screenshots
├── Incident-Response
└── Lessons-Learned
```

---

# 📈 Skills Demonstrated

## Cloud Security

- Microsoft 365 Security
- Microsoft Entra ID
- Identity Protection
- Conditional Access

## Security Operations

- Alert Investigation
- Incident Response
- Threat Hunting
- Security Monitoring

## Microsoft Security

- Microsoft Defender XDR
- Defender for Endpoint
- Defender for Office 365

## Defensive Security

- MFA Deployment
- Access Control
- Authentication Security
- Zero Trust

---

# 🚀 Future Enhancements

Planned future improvements include:

- Microsoft Sentinel Integration
- Analytics Rules
- Threat Intelligence
- Automated Response Playbooks
- Microsoft Security Copilot
- Additional Hunting Queries
- Security Dashboards

---

# 📜 Lessons Learned

Key lessons learned from this project:

- Identity security is the first line of defense.
- MFA remains one of the most effective security controls.
- Microsoft Defender XDR provides centralized visibility across identities, endpoints, and email.
- Threat hunting improves detection effectiveness.
- Incident documentation is essential in security operations.
- Zero Trust principles improve security across the environment.

---

# ✅ Project Outcome

This project successfully demonstrated:

✅ Microsoft Entra ID Administration

✅ Microsoft Defender XDR Operations

✅ Conditional Access Deployment

✅ MFA Implementation

✅ Threat Hunting

✅ Incident Response

✅ Security Monitoring

✅ Phishing Simulation

✅ Endpoint Security

✅ Zero Trust Security

✅ Security Documentation

---

# 🔗 Connect With Me

**Matome Mabitsi**

Cloud Engineer | Aspiring Cybersecurity Engineer

- LinkedIn: https://www.linkedin.com/in/matome-mabitsi12/
- Website: https://matomemabitsi.co.za

---
