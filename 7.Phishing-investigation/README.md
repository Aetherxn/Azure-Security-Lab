# Phishing Incident Investigation (SOC Simulation)

## Overview

Simulated investigation of a phishing email reported within a global payment provider SOC environment. Focused on email analysis, IOC extraction, and validating detection coverage using Azure security tools.

<img src="payment-provider.webp" alt="Global Payment Provider" width="750" height="350">

---

## Technologies Used

- Microsoft Sentinel (SIEM) — log correlation, IOC analysis, investigation
- Microsoft Defender for Office 365 — email and phishing analysis
- Microsoft Entra ID — identity and sign-in log correlation
- Azure Monitor — log visibility and telemetry

---

## Scenario

A user reported a suspicious email impersonating a trusted service provider. The email contained a link to a fake login page designed to capture credentials using a lookalike domain.

---

## Investigation Summary

- Analysed sender domain and reply-to mismatch
- Inspected email headers for authentication failures (SPF, DKIM, DMARC)
- Identified typosquatting domain used for impersonation
- Reviewed embedded URL and redirect behaviour
- Checked threat intelligence reputation for domain and IP
- Correlated indicators in Microsoft Sentinel
- Reviewed Entra ID sign-in logs for suspicious activity

---

## Key Findings (IOCs)

| IOC Type     | Value |
|--------------|------|
| Domain       | secure-payments-login[.]com |
| IP Address   | 185.xx.xx.xx |
| Sender Email | support@secure-payments-login[.]com |
| URL Path     | /verify/account/login |

---

## Security Improvements

- Recommended stricter SPF, DKIM, and DMARC enforcement
- Created Sentinel alert rules for SPF/DKIM failures and lookalike domains
- Improved phishing filtering in email security gateway
- Created Sentinel alerts for authentication failures tied to phishing activity
- Correlated email telemetry with identity sign-in logs
- Blocked malicious domains and IPs via threat intelligence feeds

---

## Key Learnings

- Phishing campaigns rely heavily on domain impersonation and urgency tactics
- Email authentication failures were the most reliable early indicator in this case
- Correlating Entra ID logs helped confirm no successful credential use
- No successful sign-ins were detected after click simulation
- Microsoft Sentinel is effective for linking phishing IOCs with user activity
- Detection engineering is key to reducing time to identify and respond to phishing attempts
