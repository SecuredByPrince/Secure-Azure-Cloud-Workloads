# Architecture Decisions

## Secure Azure Cloud Workloads

## Enterprise Cloud Security Engineering, Threat Visibility & Cloud-Native Security Operations Platform

---

# Architecture Decision Overview

This document explains the architectural decisions behind the Secure Azure Cloud Workloads project and how Azure-native security services were integrated to improve:
- telemetry visibility
- workload monitoring
- governance maturity
- incident investigations
- operational preparedness
- cloud-native threat visibility

The architecture combines:
- Microsoft Sentinel
- Microsoft Defender for Cloud
- Azure Monitor
- Log Analytics Workspace
- Microsoft Entra ID
- Azure Bastion
- Network Security Groups (NSGs)
- Kusto Query Language (KQL)

to create a layered cloud-native monitoring and security operations platform.

---

# Architecture Objectives

The architecture was designed to:
- centralize telemetry visibility
- improve monitoring consistency
- strengthen governance visibility
- reduce operational blind spots
- improve threat investigation capability
- improve workload operational awareness
- support cloud-native investigations
- improve operational resilience

---

# Architecture Diagram

<p align="center">
  <img src="./Architecture-Diagram.png" width="1000"/>
</p>

---

# Core Security Design Principles

| Security Principle | Implementation |
|---|---|
| Centralized Visibility | Microsoft Sentinel + Log Analytics |
| Least Privilege Access | Microsoft Entra ID + Conditional Access |
| Segmentation | Virtual Network + NSGs + Subnets |
| Secure Administration | Azure Bastion |
| Governance Visibility | Defender for Cloud |
| Telemetry Correlation | Azure Monitor + Sentinel |
| Layered Monitoring | Multiple telemetry sources |
| Assume Breach | Threat hunting + incident monitoring |
| Operational Preparedness | SIEM investigations + governance visibility |

---

# High-Level Security Architecture Flow

```text
Microsoft Entra ID
        ↓
Azure Resources
        ↓
Azure Monitor
        ↓
Log Analytics Workspace
        ↓
Microsoft Sentinel
        ↓
Threat Detection & Analytics
        ↓
Incidents & Investigations
        ↓
Governance & Response Activities
```

---

# Attack Surface Reduction Strategy

The architecture reduces enterprise cloud attack surface through:
- subnet segmentation
- NSG-controlled access
- Azure Bastion administrative access
- centralized telemetry visibility
- identity-centric monitoring
- governance monitoring
- workload telemetry analytics
- centralized SIEM investigations
- layered operational monitoring

These controls help reduce:
- unauthorized lateral movement
- unmanaged administrative exposure
- telemetry fragmentation
- governance inconsistencies
- operational blind spots

---

# Security Design Decisions

| Architecture Decision | Reason |
|---|---|
| Microsoft Sentinel | Centralize investigations and threat visibility |
| Defender for Cloud | Improve governance and posture visibility |
| Azure Monitor | Centralize workload telemetry collection |
| Log Analytics Workspace | Aggregate telemetry and support KQL analytics |
| Azure Bastion | Reduce public administrative exposure |
| NSGs | Restrict unnecessary traffic exposure |
| Segmented Subnets | Reduce lateral movement risk |
| Microsoft Entra ID | Centralize identity visibility |
| KQL | Improve operational investigations |
| Layered Monitoring | Improve detection and operational awareness |

---

# Architecture Zones Overview

## 1. Internet Zone

The Internet Zone represents untrusted external connectivity.

This zone includes:
- Public IP exposure
- internet ingress traffic
- external connectivity boundaries

Security controls include:
- NSG filtering
- controlled ingress
- layered monitoring
- telemetry visibility

---

## 2. External Access Zone

The External Access Zone controls inbound workload access.

This zone includes:
- Azure Load Balancer
- Network Security Groups
- controlled workload exposure

This layer improves:
- traffic filtering
- workload exposure control
- ingress visibility
- segmentation enforcement

---

## 3. Cloud Workload Zone

The Cloud Workload Zone hosts monitored workloads and segmented application infrastructure.

This includes:
- Web Tier subnet
- Application Tier subnet
- Data Tier subnet
- Azure Virtual Machines
- Azure SQL Database
- Storage Accounts

Segmentation improves:
- workload isolation
- operational control
- lateral movement reduction
- monitoring consistency

---

## 4. Administrative Zone

The Administrative Zone isolates privileged management access.

This zone includes:
- Azure Bastion
- Jumpbox VM
- Azure Key Vault

This design improves:
- privileged access control
- secure remote administration
- credential protection
- administrative monitoring

---

## 5. Monitoring & Logging Zone

The Monitoring & Logging Zone centralizes telemetry analytics.

This zone includes:
- Azure Monitor
- Log Analytics Workspace

This improves:
- telemetry ingestion
- workload visibility
- operational analytics
- centralized monitoring

---

## 6. Security Operations Zone

The Security Operations Zone centralizes investigations and detection workflows.

This zone includes:
- Microsoft Sentinel
- analytics rules
- incidents
- threat hunting workflows

This improves:
- incident visibility
- operational investigations
- telemetry correlation
- cloud-native detection capability

---

## 7. Governance & Compliance Zone

The Governance Zone improves posture management and governance visibility.

This includes:
- Microsoft Defender for Cloud
- Secure Score
- security recommendations
- governance analytics

This improves:
- posture visibility
- remediation prioritization
- governance maturity
- workload operational awareness

---

## 8. Identity & Access Management Zone

The Identity Zone centralizes authentication and access visibility.

This includes:
- Microsoft Entra ID
- Conditional Access
- authentication telemetry
- identity monitoring

This improves:
- authentication visibility
- access governance
- identity investigations
- operational awareness

---

# Telemetry & Detection Flow

The architecture centralizes telemetry through a layered operational pipeline.

```text
Cloud Workloads
        ↓
Azure Monitor
        ↓
Log Analytics Workspace
        ↓
Microsoft Sentinel
        ↓
Analytics Rules
        ↓
Alerts & Incidents
        ↓
SOC Investigations
        ↓
Response & Remediation
```

This workflow improves:
- telemetry centralization
- incident investigations
- detection consistency
- operational preparedness
- governance visibility

---

# Threat Detection Flow Example

The architecture supports end-to-end threat visibility workflows.

Example detection scenario:

```text
External Threat Actor
        ↓
Public IP Access Attempt
        ↓
Failed Authentication Attempts
        ↓
Azure Monitor Telemetry
        ↓
Log Analytics Ingestion
        ↓
Sentinel Analytics Rule Triggered
        ↓
Security Incident Created
        ↓
SOC Investigation Initiated
        ↓
Governance & Remediation Actions
```

This demonstrates:
- telemetry correlation
- incident generation
- threat visibility
- operational investigation readiness

---

# Why Microsoft Sentinel Was Selected

Microsoft Sentinel was selected to:
- centralize SIEM operations
- improve operational investigations
- correlate telemetry
- support KQL-based threat hunting
- improve incident visibility
- support operational detection workflows

Sentinel improves visibility into:
- authentication telemetry
- workload activity
- suspicious operational behavior
- governance-related findings
- operational anomalies

---

# Why Defender for Cloud Was Selected

Microsoft Defender for Cloud was selected to:
- improve governance visibility
- improve posture management
- centralize remediation visibility
- improve operational maturity awareness
- strengthen workload security monitoring

Defender for Cloud improves:
- Secure Score visibility
- governance analytics
- posture recommendations
- workload protection visibility
- remediation prioritization

---

# Why Azure Monitor Was Selected

Azure Monitor was selected to:
- centralize telemetry collection
- improve workload visibility
- improve operational analytics
- support monitoring continuity
- improve cloud observability

Azure Monitor improves visibility into:
- workload telemetry
- operational activity
- VM monitoring
- workload performance
- operational anomalies

---

# Why Log Analytics Workspace Was Selected

Log Analytics Workspace was selected to:
- centralize telemetry analytics
- support operational investigations
- improve telemetry correlation
- support KQL analytics
- improve monitoring consistency

The platform improves:
- telemetry visibility
- operational investigations
- SIEM analytics
- workload monitoring
- governance investigations

---

# Why Microsoft Entra ID Was Selected

Microsoft Entra ID was selected to:
- centralize identity visibility
- improve authentication monitoring
- support access governance
- improve sign-in investigations
- strengthen identity operational awareness

The implementation improves visibility into:
- failed sign-ins
- authentication anomalies
- identity risks
- suspicious authentication activity
- access investigations

---

# Why KQL Was Selected

KQL was selected to:
- improve operational investigations
- support telemetry analytics
- improve threat hunting capability
- improve SIEM investigations
- support telemetry correlation workflows

KQL improves investigations involving:
- authentication activity
- workload operations
- operational anomalies
- telemetry inconsistencies
- suspicious cloud activity

---

# Why Layered Monitoring Was Implemented

The architecture implements layered monitoring across:
- workload telemetry
- identity telemetry
- governance analytics
- SIEM investigations
- authentication visibility
- operational monitoring

Layered monitoring improves:
- operational awareness
- telemetry consistency
- governance visibility
- threat investigations
- cloud operational preparedness

---

# Why Governance Visibility Was Prioritized

Governance visibility was prioritized to improve:
- operational accountability
- remediation visibility
- posture management maturity
- operational awareness
- enterprise cloud resilience

The architecture integrates:
- Secure Score analytics
- governance dashboards
- posture recommendations
- remediation visibility
- workload governance monitoring

---

# Zero Trust Alignment

The architecture aligns conceptually with Zero Trust principles.

## Verify Explicitly
- identity telemetry monitoring
- Conditional Access visibility
- authentication analytics
- SIEM investigations

---

## Use Least Privilege Access
- segmented workloads
- controlled administrative access
- Bastion-based administration
- identity-centric governance

---

## Assume Breach
- centralized SIEM monitoring
- incident investigations
- telemetry analytics
- governance monitoring
- threat hunting workflows

---

# Enterprise Security Engineering Skills Demonstrated

This project demonstrates practical experience involving:
- SIEM engineering
- cloud-native monitoring
- telemetry analytics
- governance visibility
- detection engineering
- KQL investigations
- workload monitoring
- incident investigations
- operational cloud security workflows

---

# Real-World Enterprise Relevance

This implementation reflects realistic enterprise cloud operational workflows involving:
- SIEM deployments
- governance monitoring
- authentication investigations
- telemetry analytics
- workload visibility
- operational investigations
- threat hunting
- posture management

The architecture demonstrates practical cloud-native security engineering workflows commonly used within enterprise Azure environments.

---

# Operational Preparedness Focus

This project is positioned as:
- an enterprise cloud security engineering platform
- a practical operational monitoring environment
- a cloud-native SIEM implementation
- a governance visibility platform
- a telemetry analytics environment
- a cloud operational preparedness project

The implementation focuses on improving:
- operational readiness
- governance maturity
- cloud monitoring visibility
- incident investigation capability
- telemetry correlation
- enterprise cloud resilience

---

# Security Principles Demonstrated

## Visibility Improves Awareness

Centralized telemetry visibility improves operational investigations and workload awareness.

---

## Monitoring Improves Preparedness

Layered monitoring improves incident readiness and operational resilience.

---

## Telemetry Correlation Improves Detection

Centralized telemetry analytics improve threat visibility and operational investigations.

---

## Governance Improves Operational Maturity

Governance visibility improves accountability and remediation awareness.

---

## Segmentation Reduces Operational Risk

Subnet isolation and NSG boundaries reduce workload exposure and lateral movement risk.

---


# Final Architecture Decisions Statement

The Secure Azure Cloud Workloads architecture demonstrates how layered monitoring, telemetry analytics, governance visibility, segmentation, SIEM integration, and cloud-native operational investigations improve:
- workload visibility
- operational preparedness
- governance maturity
- incident investigation readiness
- threat visibility
- telemetry correlation capability
- enterprise cloud resilience

through practical implementation of Microsoft Sentinel, Microsoft Defender for Cloud, Azure Monitor, Log Analytics Workspace, Microsoft Entra ID, NSGs, Azure Bastion, Secure Score analytics, and KQL-based operational investigations within Azure cloud environments.

---