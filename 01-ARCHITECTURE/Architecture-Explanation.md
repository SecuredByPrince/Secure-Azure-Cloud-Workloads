# Architecture Explanation

## Secure Azure Cloud Workloads

## Enterprise Cloud Security Engineering & Cloud-Native Security Operations Platform

---

# Architecture Overview

The Secure Azure Cloud Workloads architecture was designed to demonstrate how Azure-native security services can be integrated to improve:
- workload visibility
- telemetry centralization
- governance maturity
- threat detection capability
- operational monitoring
- incident investigation readiness
- cloud-native operational resilience

The implementation combines:
- Microsoft Sentinel
- Microsoft Defender for Cloud
- Azure Monitor
- Log Analytics Workspace
- Microsoft Entra ID
- Azure Bastion
- Network Security Groups (NSGs)
- Kusto Query Language (KQL)

into a layered cloud-native security operations and governance architecture.

---

# Architecture Objectives

The architecture was designed to:
- centralize telemetry visibility
- improve operational monitoring
- strengthen workload segmentation
- reduce administrative exposure
- improve governance visibility
- improve threat investigation capability
- support cloud-native SIEM operations
- improve enterprise operational preparedness

---

# High-Level Architecture

<p align="center">
  <img src="./Architecture-Diagram.png" width="1000"/>
</p>

---

# Core Architecture Components

| Component | Purpose |
|---|---|
| Microsoft Sentinel | SIEM operations and incident investigations |
| Defender for Cloud | Governance visibility and posture management |
| Azure Monitor | Telemetry collection and monitoring |
| Log Analytics Workspace | Centralized telemetry analytics |
| Azure Bastion | Secure administrative access |
| Microsoft Entra ID | Identity and authentication visibility |
| NSGs | Traffic filtering and segmentation |
| KQL | Threat hunting and operational investigations |

---

# Architecture Zones

The environment is segmented into dedicated operational and security zones to improve:
- workload isolation
- monitoring visibility
- administrative control
- governance visibility
- operational resilience

---

# Internet Zone

The Internet Zone represents untrusted external connectivity entering the environment.

This layer includes:
- Public IP exposure
- ingress traffic boundaries
- internet-facing connectivity

Security controls:
- Network Security Groups
- segmentation boundaries
- monitoring visibility
- telemetry analytics

---

# External Access Zone

The External Access Zone controls inbound workload access.

This layer includes:
- Azure Load Balancer
- NSG-controlled traffic filtering
- controlled workload exposure

This improves:
- ingress visibility
- workload access control
- segmentation enforcement
- exposure management

---

# Cloud Workload Zone

The Cloud Workload Zone hosts segmented application infrastructure and monitored workloads.

This layer includes:
- Web Tier subnet
- Application Tier subnet
- Data Tier subnet
- Azure Virtual Machines
- Azure SQL Database
- Storage Accounts

Segmentation improves:
- workload isolation
- lateral movement reduction
- operational monitoring consistency
- attack surface reduction

---

# Administrative Zone

The Administrative Zone isolates privileged management access.

This includes:
- Azure Bastion
- Jumpbox VM
- Azure Key Vault

This design improves:
- secure administration
- privileged access visibility
- credential protection
- administrative monitoring

---

# Monitoring & Logging Zone

The Monitoring & Logging Zone centralizes telemetry collection and operational analytics.

This layer includes:
- Azure Monitor
- Log Analytics Workspace

This improves:
- telemetry ingestion
- workload monitoring
- operational analytics
- centralized visibility

---

# Security Operations Zone

The Security Operations Zone centralizes investigations and threat detection workflows.

This includes:
- Microsoft Sentinel
- analytics rules
- incidents
- threat hunting workflows
- investigation dashboards

This improves:
- incident visibility
- operational investigations
- telemetry correlation
- cloud-native threat detection

---

# Governance & Compliance Zone

The Governance Zone improves security posture visibility and governance monitoring.

This includes:
- Microsoft Defender for Cloud
- Secure Score
- posture recommendations
- governance analytics

This improves:
- remediation prioritization
- governance visibility
- posture management
- operational maturity awareness

---

# Identity & Access Management Zone

The Identity Zone centralizes authentication visibility and access governance.

This includes:
- Microsoft Entra ID
- Conditional Access
- identity telemetry
- authentication monitoring

This improves:
- sign-in visibility
- identity investigations
- access governance
- authentication analytics

---

# Telemetry Architecture

The architecture centralizes telemetry through Azure-native monitoring services.

```text
Azure Workloads
        ↓
Azure Monitor
        ↓
Log Analytics Workspace
        ↓
Microsoft Sentinel
        ↓
Analytics Rules
        ↓
Incidents & Investigations
```

This telemetry pipeline improves:
- centralized monitoring
- telemetry analytics
- operational investigations
- detection workflows
- governance visibility

---

# Threat Detection Workflow

The architecture supports end-to-end detection and investigation workflows.

Example workflow:

```text
External Access Attempt
        ↓
Authentication Failure
        ↓
Azure Monitor Telemetry
        ↓
Log Analytics Ingestion
        ↓
Sentinel Analytics Rule Triggered
        ↓
Incident Created
        ↓
SOC Investigation Initiated
```

This improves:
- threat visibility
- operational readiness
- telemetry correlation
- investigation capability

---

# Security Design Principles

## Centralized Visibility

Telemetry from workloads and cloud services is centralized into Log Analytics and Microsoft Sentinel for investigation and analytics.

---

## Segmentation

Subnets and NSGs reduce unnecessary exposure and improve workload isolation.

---

## Secure Administration

Azure Bastion reduces public administrative exposure while improving privileged access visibility.

---

## Governance Visibility

Defender for Cloud improves posture visibility, remediation awareness, and governance monitoring.

---

## Layered Monitoring

The architecture combines:
- workload telemetry
- identity telemetry
- governance analytics
- SIEM investigations

to improve operational awareness.

---

# Zero Trust Alignment

The architecture aligns conceptually with Zero Trust principles.

| Zero Trust Principle | Implementation |
|---|---|
| Verify Explicitly | Identity telemetry and Conditional Access |
| Least Privilege Access | Segmented workloads and Bastion access |
| Assume Breach | Threat hunting and centralized investigations |

---

# Attack Surface Reduction Strategy

The architecture reduces operational exposure through:
- segmented workloads
- NSG-controlled traffic filtering
- secure administrative access
- centralized telemetry monitoring
- governance visibility
- layered monitoring controls

This reduces:
- lateral movement risk
- unmanaged administrative exposure
- operational blind spots
- telemetry fragmentation

---

# Enterprise Security Engineering Skills Demonstrated

This project demonstrates practical experience involving:
- SIEM engineering
- cloud-native monitoring
- threat hunting
- KQL investigations
- governance monitoring
- incident investigations
- workload telemetry analytics
- operational security workflows

---

# Real-World Relevance

This implementation reflects realistic enterprise operational workflows involving:
- cloud-native SIEM operations
- governance monitoring
- authentication investigations
- telemetry analytics
- workload monitoring
- incident response
- posture management
- operational threat investigations

The environment demonstrates how Azure-native security services improve:
- operational visibility
- governance maturity
- workload awareness
- cloud-native threat visibility
- operational preparedness

---

# Recommended Architecture Evidence

Capture screenshots for:
- Sentinel dashboards
- Secure Score visibility
- telemetry analytics
- incident investigations
- workload monitoring
- governance dashboards
- authentication monitoring
- architecture overview
- threat hunting investigations

Store screenshots inside:

```text
01-ARCHITECTURE/Screenshots/
```

---

# Suggested Screenshot Names

```text
architecture-overview.png
sentinel-dashboard.png
secure-score-overview.png
telemetry-analytics.png
incident-investigation.png
workload-monitoring-dashboard.png
governance-dashboard.png
authentication-monitoring.png
threat-hunting-overview.png
```

---

# Final Architecture Summary

The Secure Azure Cloud Workloads architecture demonstrates how layered monitoring, segmentation, governance visibility, SIEM integration, telemetry analytics, and cloud-native investigations improve:
- operational visibility
- governance maturity
- workload monitoring
- incident investigation readiness
- threat detection capability
- enterprise operational preparedness

through practical implementation of Microsoft Sentinel, Microsoft Defender for Cloud, Azure Monitor, Log Analytics Workspace, Microsoft Entra ID, Azure Bastion, NSGs, Secure Score analytics, and KQL-based operational investigations within Azure environments.

---