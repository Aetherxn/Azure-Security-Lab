# Microsoft Sentinel with KQL

## Overview 

This project demonstrates how Microsoft Sentinel is used in a SOC environment to detect and investigate security threats. It covers Analytics Rules, incident triage, threat hunting, and KQL-based investigations to validate alerts, correlate events, and understand attacker activity.

---

## Problem

Microsoft Sentinel generated a high-severity incident that suggested possible Command and Control (C2) activity. The incident contained several alerts related to suspicious sign-in attempts from an external IP address targeting disabled accounts.

As the SOC Level 1 Analyst, I needed to investigate the alerts, review the related logs and entities, and determine whether the activity posed a genuine threat to the organisation. Based on the evidence gathered during triage, I then had to decide if the incident should be escalated to the SOC Level 2 team for further investigation and threat hunting.

**Note:** *One major challenge in SOC environments is **alert fatigue**, where analysts are overwhelmed by large volumes of alerts, leading to slower response times and burnout. **Sentinel playbooks** help reduce this burden by automating tasks such as incident management, enrichment, investigation, and remediation, allowing analysts to focus on higher priority threats*.

---

## Azure Services Used

- Microsoft Sentinel
- Log Analytics Workspace
- Microsoft Entra ID (Azure AD)
- Azure Monitor

---

## Threat / Risk Addressed

---

## Implementation (Security Controls)

---

## Validation

---

## Key Learnings

- Understood what Analytics Rules and Rule Templates are and how they’re used to detect threats in Microsoft Sentinel
- Identified key parts of an Analytics Rule, including severity, data sources, scheduling, and MITRE ATT&CK mappings
- Created and enabled Analytics Rules from built-in templates and made basic customisations for the environment
- Gained hands-on experience using Analytics Rules to generate alerts and incidents in Sentinel

**To be Continued...**
