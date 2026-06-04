# Data Connectors

## Secure Azure Cloud Workloads

This document explains the Microsoft Sentinel data connector configuration implemented within the Secure Azure Cloud Workloads project.

The objective of this implementation is to improve:
- centralized telemetry visibility
- operational cloud monitoring
- threat detection capability
- operational investigations
- telemetry correlation
- governance visibility
- incident response readiness
- enterprise cloud resilience

through layered cloud-native SIEM integrations and practical operational cloud security engineering workflows within Azure environments.

---

# Data Connectors Overview

Microsoft Sentinel data connectors are used to ingest telemetry from multiple Azure and security sources into the SIEM environment.

The implementation demonstrates how telemetry ingestion improves:
- operational visibility
- cloud monitoring maturity
- threat detection capability
- operational investigations
- governance awareness
- incident readiness
- telemetry correlation capability

The project focuses heavily on operational cloud monitoring and centralized security visibility.

---

# Data Connector Objectives

The data connector implementation was designed to:
- centralize operational telemetry
- improve cloud activity visibility
- improve threat investigations
- improve workload monitoring awareness
- improve governance visibility
- improve operational preparedness
- improve telemetry correlation capability
- strengthen enterprise cloud resilience

The implementation demonstrates how centralized telemetry collection improves operational cloud security capability.

---

# Data Connector Architecture Flow

Azure Workloads  
↓  
Azure Monitor & Native Services  
↓  
Data Connectors  
↓  
Log Analytics Workspace  
↓  
Microsoft Sentinel Correlation  
↓  
Threat Detection & Analytics  
↓  
Incident Investigations & Response

---

# Primary Data Connectors Enabled

The following Microsoft Sentinel data connectors are enabled within the environment:
- Azure Activity
- Microsoft Defender for Cloud
- Microsoft Entra ID
- Azure Monitor Agent
- Log Analytics Workspace
- Security Events
- Microsoft Defender telemetry

These connectors create layered operational visibility across the Azure environment.

---

# 1. Azure Activity Connector

## Overview

The Azure Activity connector ingests:
- Azure administrative actions
- resource modifications
- subscription activities
- governance events
- operational changes

This connector improves visibility into operational cloud activity across the Azure environment.

---

## Telemetry Visibility Areas

### Activity Monitoring

- resource creation
- resource deletion
- administrative changes
- operational modifications
- governance visibility

---

## Operational Benefits

Azure Activity visibility improves:
- operational accountability
- governance maturity
- operational investigations
- cloud activity awareness

---

# 2. Microsoft Defender for Cloud Connector

## Overview

The Defender for Cloud connector ingests:
- security recommendations
- posture assessments
- workload findings
- security alerts
- operational cloud risks

This improves visibility into:
- workload protection
- posture management
- operational cloud security awareness

---

## Telemetry Visibility Areas

### Defender Visibility

- workload exposure findings
- posture recommendations
- vulnerability visibility
- governance findings
- workload monitoring visibility

---

## Operational Benefits

Defender telemetry improves:
- workload awareness
- governance visibility
- posture management capability
- cloud resilience

---

# 3. Microsoft Entra ID Connector

## Overview

The Microsoft Entra ID connector ingests:
- sign-in logs
- authentication telemetry
- identity events
- operational identity visibility
- authentication failures

Identity visibility is critical because compromised identities may lead to:
- unauthorized access
- privilege escalation
- workload compromise
- governance failures

---

## Telemetry Visibility Areas

### Authentication Monitoring

- failed sign-ins
- suspicious authentication attempts
- identity anomalies
- sign-in locations
- operational identity activity

---

## Operational Benefits

Identity telemetry improves:
- authentication visibility
- operational investigations
- governance maturity
- cloud access awareness

---

# 4. Azure Monitor Agent Connector

## Overview

The Azure Monitor Agent connector collects:
- VM telemetry
- operational monitoring data
- workload activity
- cloud monitoring telemetry
- operational system logs

This connector improves workload visibility across the Azure environment.

---

## Telemetry Visibility Areas

### Workload Monitoring

- VM operational activity
- workload telemetry
- performance visibility
- operational monitoring
- workload investigations

---

## Operational Benefits

Azure Monitor telemetry improves:
- workload awareness
- operational visibility
- cloud monitoring maturity
- investigation readiness

---

# 5. Log Analytics Workspace Connector

## Overview

The Log Analytics Workspace acts as the centralized telemetry repository for:
- operational monitoring
- telemetry correlation
- cloud investigations
- workload visibility
- SIEM operations

This connector supports:
- centralized investigations
- telemetry analysis
- operational visibility

---

## Telemetry Visibility Areas

### Workspace Visibility

- telemetry ingestion
- operational logs
- cloud monitoring visibility
- investigation telemetry
- workload monitoring

---

## Operational Benefits

Log Analytics improves:
- centralized monitoring
- telemetry correlation
- operational investigations
- cloud resilience

---

# 6. Security Events Connector

## Overview

The Security Events connector ingests:
- Windows security events
- workload activity
- authentication events
- operational telemetry
- security-related logs

This improves workload-level operational visibility.

---

## Telemetry Visibility Areas

### Security Monitoring

- login activity
- workload authentication events
- operational activity
- suspicious events
- workload investigations

---

## Operational Benefits

Security event visibility improves:
- workload monitoring
- threat investigations
- cloud awareness
- incident readiness

---

# Data Ingestion Validation

The implementation validates:
- telemetry ingestion
- connector health
- operational visibility
- log collection
- investigation readiness
- cloud monitoring visibility

The project demonstrates how telemetry validation improves operational cloud resilience.

---

# Operational Monitoring Visibility

The connector implementation improves visibility into:
- authentication activity
- operational telemetry
- workload monitoring
- governance visibility
- administrative changes
- security alerts
- operational investigations

The implementation demonstrates how centralized telemetry improves operational cloud security capability.

---

# Threat Detection Support

The data connectors support operational threat visibility involving:
- suspicious authentication activity
- workload anomalies
- administrative modifications
- operational monitoring gaps
- cloud telemetry analysis
- incident investigations

The implementation demonstrates how telemetry centralization improves cloud threat detection capability.

---

# KQL Visibility & Telemetry Analysis

The ingested telemetry supports:
- KQL investigations
- threat hunting workflows
- cloud monitoring dashboards
- operational telemetry analysis
- incident investigations
- operational cloud visibility

The project demonstrates practical detection engineering workflows within enterprise cloud environments.

---

# Example Operational KQL Queries

## Failed Authentication Monitoring

```kql
SigninLogs
| where ResultType != 0
| summarize FailedAttempts=count() by UserPrincipalName
| order by FailedAttempts desc
```

---

## Administrative Activity Visibility

```kql
AzureActivity
| summarize ActivityCount=count() by Caller
| order by ActivityCount desc
```

---

## Security Alert Visibility

```kql
SecurityAlert
| project AlertName, Severity, TimeGenerated
```

---

# Governance Visibility

The connector implementation improves governance through:
- telemetry accountability
- operational monitoring visibility
- workload activity awareness
- cloud posture visibility
- operational investigations
- governance maturity tracking

The implementation demonstrates how centralized telemetry improves enterprise cloud resilience.

---

# Operational Security Benefits

The data connector implementation improves:
- operational cloud visibility
- telemetry correlation capability
- threat detection awareness
- operational investigations
- governance maturity
- monitoring visibility
- incident response readiness
- enterprise cloud resilience

---

# Real-World Relevance

This data connector implementation reflects common real-world enterprise cloud security operations involving:
- centralized telemetry collection
- SIEM integrations
- operational cloud monitoring
- threat investigations
- workload visibility
- governance monitoring
- cloud-native telemetry analysis

The implementation demonstrates realistic operational cloud security engineering workflows commonly used within enterprise Azure environments.

---

# Operational Preparedness Focus

This project is positioned primarily as:
- an enterprise cloud security preparedness project
- a practical cloud security engineering environment
- a cloud-native SIEM implementation
- an operational monitoring platform
- a governance visibility project

The focus is on improving:
- operational readiness
- cloud monitoring maturity
- governance visibility
- telemetry correlation capability
- operational investigations
- enterprise cloud resilience

---

# Security Principles Demonstrated

## Centralized Visibility Matters

Centralized telemetry visibility improves investigations and operational cloud awareness.

---

## Monitoring Improves Preparedness

Operational monitoring improves incident readiness and cloud resilience.

---

## Telemetry Correlation Improves Detection

Telemetry correlation improves operational investigations and threat visibility.

---

## Governance Improves Operational Maturity

Operational visibility improves governance maturity and accountability.

---

## Layered Monitoring Improves Cloud Resilience

Layered telemetry collection and operational visibility strengthen enterprise cloud resilience.

---

# Screenshots to Capture

## Recommended Evidence Screenshots

Capture screenshots for:
- data connectors overview
- Azure Activity connector
- Defender for Cloud connector
- Microsoft Entra ID connector
- Azure Monitor Agent connector
- Log Analytics integration
- connector health visibility
- telemetry ingestion visibility
- connected data sources
- operational monitoring dashboards

Store screenshots inside:

```text
03-MICROSOFT-SENTINEL/Screenshots/
```

---

# Suggested Screenshot Names

```text
data-connectors-overview.png
azure-activity-connector.png
defender-for-cloud-connector.png
entra-id-connector.png
azure-monitor-agent-connector.png
log-analytics-integration.png
connector-health-visibility.png
telemetry-ingestion-visibility.png
connected-data-sources.png
operational-monitoring-dashboard.png
```

---

# Continuous Improvement

The data connector implementation continuously evolves as:
- cloud threats evolve
- Azure capabilities expand
- governance requirements mature
- operational monitoring practices improve
- cloud-native attack surfaces grow
- detection engineering workflows improve
- enterprise cloud security knowledge expands

The objective is to continuously improve:
- operational cloud visibility
- telemetry correlation capability
- governance maturity
- operational investigations
- monitoring visibility
- enterprise cloud resilience

---

# Final Data Connectors Statement

The ultimate objective of this data connector implementation is to demonstrate how centralized telemetry ingestion and layered cloud-native monitoring improve:
- operational visibility
- threat detection capability
- governance maturity
- operational investigations
- incident response readiness
- operational preparedness
- enterprise cloud resilience

through practical operational cloud security engineering workflows using Microsoft Sentinel within Azure environments.