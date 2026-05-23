# Azure Environment Setup

### Overview

This section establishes the Azure environment used across the Azure Security Lab. It provides the foundational infrastructure for logging, monitoring, and security detection using Microsoft Sentinel and Defender for Cloud.

The environment supports:

- centralised logging
- cloud security monitoring
- endpoint telemetry collection
- threat detection
- incident response workflows
- future attack simulation scenarios

This setup serves as the base platform for the Sentinel SOC, Defender for Cloud monitoring, identity security testing, and incident response labs contained in this repository.

---

## Objectives

This lab focuses on:

- Configuring foundational Azure security resources
- Deploying and configuring Log Analytics Workspace
- Enabling Microsoft Sentinel for SIEM monitoring
- Connecting Azure Virtual Machine telemetry
- Integrating security data connectors
- Configuring Windows logging and auditing
- Validating telemetry ingestion using KQL
- Preparing the environment for future detection engineering and threat hunting labs

---

## Architecture

![architecture](architecture-diagram.jpg)

---

## Environment Deployment

### 1. Azure Resource Configuration

Configure core Azure resources required for the security lab environment.

![Resource Group](screenshots/01-resource-group.png)

### 2. Log Analytics Workspace

Deploy a Log Analytics Workspace for centralised log ingestion and retention.

![Log Analytics](screenshots/02-log-analytics.png)

### 3. Microsoft Sentinel Enablement

Enable Microsoft Sentinel for SIEM-based monitoring and detection.

![Sentinel Enabled](screenshots/03-sentinel-enabled.png)

### 4. Data Connector Integration

Configure data connectors to ingest security telemetry from Azure and Windows sources.

![Data Connectors](screenshots/04-data-connectors.png)

### 5. Virtual Machine Telemetry

Validate that the Azure VM is sending security logs to Log Analytics.

![VM Telemetry](screenshots/05-vm-telemetry.png)


### 6. Windows Security Logging

Enable Windows auditing policies for security event generation.

![Windows Auditing](screenshots/06-windows-auditing.png)

### 7. KQL Validation

Run KQL queries to confirm log ingestion and visibility.

![KQL Validation](screenshots/07-kql-query.png)

---

## Outcome

This environment provides a centralised Azure security monitoring platform capable of supporting:

- detection engineering
- threat hunting
- cloud monitoring
- identity security analysis
- incident response simulations
- SOC investigation workflows
