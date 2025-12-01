---
title: "Event 6"
type: "page"
---

# EVENT REPORT: **AWS Cloud Mastery Series #3 — Security on AWS**

&emsp;**Date:** Saturday, November 29, 2025  
&emsp;**Time:** 8:30 AM – 12:00 PM  
&emsp;**Location:** AWS Vietnam Office, Bitexco Financial Tower, District 1, Ho Chi Minh City

&emsp;**Objective:** Deliver deep knowledge across all five pillars of the AWS Well-Architected *Security Pillar* — including services, core principles, and defensive strategies.

---

## AGENDA SUMMARY

| Time              | Topic                                             | Key Focus                                                                                |
|:------------------|:--------------------------------------------------|:-----------------------------------------------------------------------------------------|
| **08:30 – 08:50** | Opening & Security Foundations                    | Shared Responsibility Model, threat landscape in Vietnam.                                |
| **08:50 – 09:30** | **Pillar 1 — Identity & Access Management (IAM)** | Modern IAM design, Roles, Policies, IAM Identity Center, SCP, MFA, Access Analyzer demo. |
| **09:30 – 09:55** | **Pillar 2 — Detection**                          | CloudTrail, GuardDuty, Security Hub, Detection-as-Code model.                            |
| **10:10 – 10:40** | **Pillar 3 — Infrastructure Protection**          | VPC segmentation, SG vs NACL, WAF, Network Firewall, workload security.                  |
| **10:40 – 11:10** | **Pillar 4 — Data Protection**                    | Encryption at-rest/in-transit, KMS, Secrets Manager, data classification.                |
| **11:10 – 11:40** | **Pillar 5 — Incident Response**                  | IR lifecycle, playbooks, incident automation using Lambda/Step Functions.                |
| **11:40 – 12:00** | Closing & Q&A                                     | Pitfalls, study roadmap for AWS Security Specialty.                                      |

---

## SECURITY PILLAR — DEEP TECHNICAL LEARNINGS

### 1. Security Foundations & Core Principles

- Emphasis on **Least Privilege**, **Zero Trust**, and **Defense-in-Depth**.
- Shared Responsibility Model clearly defines roles:
    - AWS secures **the Cloud** (infrastructure, hardware)
    - Customers secure **in the Cloud** (data, IAM, configuration)

---

### 2. Pillar 1 — Identity & Access Management (IAM)

- Avoid **long-term credentials** — rely on **Roles + Temporary Access**.
- Multi-account governance using **SCPs** and **Permission Boundaries**.
- Mini-demo using **Access Analyzer** for policy validation & risk detection.

---

### 3. Pillar 2 — Detection

- **CloudTrail** for full API logging (organization-wide).
- **GuardDuty** ML-driven threat detection.
- **Security Hub** for consolidated security findings.
- Detection-as-Code for automated rule deployment & alerting.

---

### 4. Pillar 3 — Infrastructure Protection

- VPC segmentation for tier separation (Web / App / DB).
- Difference between **Security Groups (stateful)** vs **Network ACLs (stateless)**.
- Edge protection using **WAF + AWS Shield** for DDoS and L7 attack defense.

---

### 5. Pillar 4 — Data Protection

- Encryption required end-to-end: **at-rest & in-transit**.
- **AWS KMS** for key management, rotation, and policy control.
- **Secrets Manager** for secure storage + automatic rotation of sensitive credentials.

---

### 6. Pillar 5 — Incident Response

- IR lifecycle: **Prepare → Detect → Respond → Recover**.
- Automated remediation with **Lambda / Step Functions playbooks**.
- Key response actions: **snapshot, isolate, evidence capture**.

---

## EVALUATION & NEXT STEPS

### Evaluation

This event outlined a complete and structured blueprint for AWS security — not only service-by-service, but as a full architectural strategy following the Well-Architected Framework. Extremely valuable for developers and Ops teams deploying production workloads under Zero-Trust standards.

### Recommended Next Steps

1. Use Security Pillar checklist to evaluate ongoing projects — with focus on IAM + Data Encryption.
2. Enable **CloudTrail + GuardDuty** in development environments and begin writing Detection-as-Code rules.
3. Study deeper toward **AWS Security Specialty** certification to reinforce long-term skill trajectory.

---

## Event Photos

![](/images/4-Events/Event6.1.jpg)  
![](/images/4-Events/Event6.2.jpg)  
![](/images/4-Events/Event6.3.jpg)  
![](/images/4-Events/Event6.4.jpg)  
![](/images/4-Events/Event6.5.jpg)  
![](/images/4-Events/Event6.6.jpg)