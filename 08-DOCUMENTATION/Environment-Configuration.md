# Environment Configuration

## Secure Azure Cloud Workloads

This document explains the environment configuration for the Secure Azure Cloud Workloads project using Microsoft Defender for Cloud, Microsoft Sentinel, Azure Monitor, Log Analytics, Kusto Query Language (KQL), telemetry analytics, posture management workflows, and cloud-native operational monitoring within Azure environments.

The objective of this environment configuration is to:
- improve operational visibility
- improve governance maturity
- improve telemetry correlation capability
- improve workload protection awareness
- improve operational preparedness
- improve cloud monitoring maturity
- improve incident readiness
- strengthen enterprise cloud resilience

through practical cloud-native security engineering workflows and operational monitoring visibility.

---

# Environment Configuration Overview

The Secure Azure Cloud Workloads environment demonstrates a practical enterprise cloud operational monitoring architecture involving:
- cloud-native operational monitoring
- SIEM visibility
- telemetry analytics
- posture management
- governance monitoring
- incident investigations
- workload visibility
- operational preparedness

The implementation focuses heavily on:
- operational visibility
- governance maturity
- telemetry analytics
- workload monitoring
- operational resilience
- enterprise cloud readiness

rather than offensive exploitation activities.

---

# Environment Configuration Objectives

The environment configuration was designed to:
- improve governance visibility
- improve telemetry correlation capability
- improve cloud monitoring maturity
- improve workload visibility
- improve operational preparedness
- improve posture management visibility
- improve operational resilience
- strengthen enterprise cloud resilience

The implementation demonstrates realistic enterprise cloud operational workflows.

---

# Environment Architecture Overview

Azure Subscription  
↓  
Resource Group  
↓  
Log Analytics Workspace  
↓  
Microsoft Defender for Cloud  
↓  
Microsoft Sentinel  
↓  
Azure Monitor  
↓  
Virtual Machines & Workloads  
↓  
Telemetry Collection & Correlation

---

# Environment Components

| Component | Purpose |
|---|---|
| Azure Subscription | Cloud resource management |
| Resource Group | Resource organization |
| Log Analytics Workspace | Centralized telemetry analytics |
| Microsoft Sentinel | SIEM monitoring and investigations |
| Microsoft Defender for Cloud | Posture management visibility |
| Azure Monitor | Telemetry collection |
| Azure Virtual Machines | Workload monitoring |
| Microsoft Entra ID | Authentication visibility |

---

# 1. Azure Subscription Configuration

## Overview

The Azure subscription provides centralized cloud resource visibility and operational governance.

The implementation improves:
- governance visibility
- resource organization
- operational accountability
- telemetry management
- cloud operational consistency

---

## Recommended Subscription Configuration

### Subscription Naming Convention

```text
Secure-Cloud-Workloads-Subscription
```

---

## Recommended Configuration Areas

Configure:
- resource access governance
- operational visibility
- telemetry integration
- monitoring consistency
- workload operational awareness

---

## Operational Configuration Benefits

Subscription configuration improves:
- governance maturity
- operational organization
- monitoring consistency
- enterprise cloud resilience

---

# 2. Resource Group Configuration

## Overview

Resource groups improve:
- operational organization
- governance visibility
- monitoring consistency
- workload operational management

The implementation centralizes:
- monitoring resources
- Sentinel resources
- Defender visibility
- telemetry analytics
- governance monitoring

---

## Recommended Resource Group

### Resource Group Name

```text
rg-secure-cloud-workloads
```

---

## Azure Portal Navigation

Navigate to:

```text
Azure Portal
→ Resource Groups
→ Create
```

---

## Recommended Configuration

| Setting | Recommended Value |
|---|---|
| Resource Group | rg-secure-cloud-workloads |
| Region | Preferred Azure Region |
| Tags | Environment=SecurityLab |

---

## Operational Configuration Benefits

Resource group configuration improves:
- governance visibility
- operational consistency
- workload organization
- cloud operational maturity

---

# 3. Log Analytics Workspace Configuration

## Overview

Log Analytics provides centralized telemetry analytics and operational visibility.

The workspace improves:
- telemetry collection
- monitoring capability
- workload visibility
- incident investigations
- governance telemetry

---

## Recommended Workspace Configuration

### Workspace Name

```text
law-secure-cloud-workloads
```

---

### Pricing Tier

```text
Pay-As-You-Go
```

---

### Retention Period

```text
30 to 90 days
```

---

## Azure Portal Navigation

Navigate to:

```text
Azure Portal
→ Log Analytics Workspaces
→ Create
```

---

## Recommended Configuration Areas

Configure:
- telemetry ingestion
- retention policies
- monitoring visibility
- operational analytics
- governance telemetry

---

## Operational Configuration Benefits

Workspace configuration improves:
- telemetry analytics capability
- operational investigations
- governance visibility
- enterprise cloud resilience

---

# 4. Microsoft Sentinel Configuration

## Overview

Microsoft Sentinel improves:
- SIEM visibility
- telemetry correlation
- incident investigations
- governance awareness
- operational preparedness

The implementation demonstrates:
- centralized SIEM visibility
- telemetry analytics
- operational investigations
- governance monitoring

---

## Recommended Sentinel Configuration

### Sentinel Workspace

```text
sentinel-secure-cloud-workloads
```

---

## Azure Portal Navigation

Navigate to:

```text
Azure Portal
→ Microsoft Sentinel
→ Create
```

---

## Recommended Configuration Areas

Configure:
- analytics rules
- incident settings
- data connectors
- automation visibility
- telemetry correlation

---

## Operational Configuration Benefits

Sentinel configuration improves:
- incident investigations
- telemetry analytics
- governance visibility
- enterprise cloud resilience

---

# 5. Microsoft Defender for Cloud Configuration

## Overview

Defender for Cloud improves:
- posture management visibility
- Secure Score awareness
- workload exposure visibility
- governance maturity
- operational resilience

The implementation demonstrates:
- centralized posture visibility
- governance monitoring
- workload operational awareness
- cloud-native telemetry analytics

---

## Recommended Defender Configuration

### Defender Plans

Enable:
- Defender for Servers
- Defender CSPM
- Vulnerability Assessment
- Secure Score visibility
- Regulatory Compliance visibility

---

## Azure Portal Navigation

Navigate to:

```text
Azure Portal
→ Microsoft Defender for Cloud
→ Environment Settings
```

---

## Recommended Configuration Areas

Configure:
- posture management visibility
- Secure Score monitoring
- governance telemetry
- workload operational visibility
- cloud monitoring awareness

---

## Operational Configuration Benefits

Defender configuration improves:
- governance maturity
- workload awareness
- operational preparedness
- enterprise cloud resilience

---

# 6. Azure Monitor Configuration

## Overview

Azure Monitor improves:
- telemetry collection
- workload monitoring
- operational visibility
- governance telemetry
- monitoring continuity

The implementation demonstrates:
- centralized telemetry visibility
- monitoring consistency
- operational workload awareness
- telemetry analytics maturity

---

## Recommended Azure Monitor Configuration

### Monitoring Features

Enable:
- Activity Logs
- VM Insights
- Diagnostic Settings
- Log Collection
- Performance Metrics

---

## Azure Portal Navigation

Navigate to:

```text
Azure Portal
→ Monitor
```

---

## Recommended Configuration Areas

Configure:
- telemetry collection
- monitoring visibility
- workload operational awareness
- governance telemetry
- incident investigation visibility

---

## Operational Configuration Benefits

Azure Monitor configuration improves:
- workload visibility
- telemetry consistency
- monitoring capability
- operational preparedness

---

# 7. Virtual Machine Configuration

## Overview

Virtual machines provide workload telemetry visibility and operational monitoring capability.

The implementation demonstrates:
- workload monitoring
- heartbeat visibility
- operational telemetry
- authentication visibility
- governance awareness

---

## Recommended VM Configuration

### VM Naming Convention

```text
vm-monitoring-01
vm-monitoring-02
```

---

### Recommended VM Size

```text
Standard_B2s
```

---

### Recommended Monitoring Features

Enable:
- Azure Monitor Agent
- VM Insights
- Boot Diagnostics
- NSG visibility
- telemetry collection

---

## Azure Portal Navigation

Navigate to:

```text
Azure Portal
→ Virtual Machines
→ Create
```

---

## Operational Configuration Benefits

VM configuration improves:
- workload visibility
- telemetry analytics
- monitoring capability
- operational investigations

---

# 8. Diagnostic Settings Configuration

## Overview

Diagnostic settings improve:
- telemetry collection
- operational visibility
- monitoring continuity
- governance telemetry
- incident investigations

The implementation improves visibility into:
- authentication telemetry
- workload monitoring
- operational changes
- governance visibility
- telemetry analytics

---

## Recommended Diagnostic Settings

### Recommended Logs

Enable:
- Audit Logs
- Sign-In Logs
- Activity Logs
- Security Logs
- Performance Logs

---

## Azure Portal Navigation

Navigate to:

```text
Resource
→ Diagnostic Settings
→ Add Diagnostic Setting
```

---

## Recommended Configuration Areas

Configure:
- telemetry forwarding
- workspace integration
- monitoring continuity
- operational analytics
- governance visibility

---

## Operational Configuration Benefits

Diagnostic settings improve:
- telemetry consistency
- governance visibility
- monitoring capability
- operational preparedness

---

# 9. Data Connector Configuration

## Overview

Data connectors improve:
- telemetry visibility
- incident investigations
- governance monitoring
- operational analytics
- workload awareness

The implementation improves visibility into:
- authentication telemetry
- workload operational visibility
- governance analytics
- operational investigations
- telemetry correlation

---

## Recommended Data Connectors

Enable:
- Microsoft Defender for Cloud
- Azure Activity
- Microsoft Entra ID
- Security Events
- Azure Monitor Agent
- Office 365 (optional)

---

## Azure Portal Navigation

Navigate to:

```text
Microsoft Sentinel
→ Data Connectors
```

---

## Recommended Configuration Areas

Configure:
- connector health visibility
- telemetry ingestion
- operational analytics
- monitoring continuity
- governance telemetry

---

## Operational Configuration Benefits

Data connectors improve:
- telemetry analytics
- governance awareness
- operational visibility
- incident readiness

---

# 10. Analytics Rule Configuration

## Overview

Analytics rules improve:
- alert visibility
- telemetry correlation
- incident investigations
- operational awareness
- governance maturity

The implementation improves visibility into:
- authentication anomalies
- suspicious operational activity
- workload monitoring gaps
- governance inconsistencies
- telemetry anomalies

---

## Recommended Analytics Rules

Create rules for:
- failed sign-ins
- suspicious IP activity
- administrative changes
- VM authentication anomalies
- workload monitoring gaps
- security alert correlation

---

## Azure Portal Navigation

Navigate to:

```text
Microsoft Sentinel
→ Analytics
```

---

## Recommended Configuration Areas

Configure:
- scheduled query rules
- incident generation
- severity visibility
- telemetry correlation
- operational investigations

---

## Operational Configuration Benefits

Analytics rules improve:
- detection visibility
- operational preparedness
- governance awareness
- enterprise cloud resilience

---

# 11. KQL Environment Configuration

## Overview

KQL analytics improve:
- operational investigations
- telemetry correlation
- governance visibility
- workload awareness

The implementation improves visibility into:
- authentication telemetry
- workload operational risks
- governance inconsistencies
- telemetry anomalies
- operational investigations

---

## Recommended KQL Queries

### Failed Sign-Ins

```kql
SigninLogs
| where ResultType != 0
```

---

### Security Alerts

```kql
SecurityAlert
```

---

### Azure Activity

```kql
AzureActivity
```

---

### VM Heartbeat Visibility

```kql
Heartbeat
```

---

## Operational Configuration Benefits

KQL visibility improves:
- telemetry analytics capability
- operational investigations
- governance awareness
- enterprise cloud resilience

---

# 12. Environment Validation

## Overview

Environment validation ensures:
- monitoring consistency
- operational visibility
- governance telemetry continuity
- workload visibility
- incident investigation readiness

---

## Validation Areas

Validate:
- Sentinel incident visibility
- Defender findings
- authentication telemetry
- workload heartbeat visibility
- Activity Log visibility
- Log Analytics ingestion

---

## Validation Queries

### Security Alerts

```kql
SecurityAlert
| summarize AlertCount=count() by Severity
```

---

### Authentication Visibility

```kql
SigninLogs
| summarize SignInCount=count()
    by UserPrincipalName
```

---

### Workload Visibility

```kql
Heartbeat
| summarize LastHeartbeat=max(TimeGenerated)
    by Computer
```

---

## Operational Configuration Benefits

Environment validation improves:
- telemetry consistency
- governance maturity
- monitoring capability
- operational preparedness

---

# Environment Validation Checklist

## Validate the Following

| Validation Area | Status |
|---|---|
| Resource Group Created | ☐ |
| Log Analytics Workspace Operational | ☐ |
| Microsoft Sentinel Enabled | ☐ |
| Defender for Cloud Enabled | ☐ |
| Azure Monitor Configured | ☐ |
| Diagnostic Settings Enabled | ☐ |
| Data Connectors Connected | ☐ |
| VM Monitoring Active | ☐ |
| Security Alerts Visible | ☐ |
| KQL Queries Functional | ☐ |

---

# Operational Configuration Benefits

The environment configuration improves:
- operational cloud visibility
- telemetry analytics capability
- governance maturity
- monitoring capability
- incident response readiness
- operational preparedness
- operational investigations
- enterprise cloud resilience

---

# Real-World Relevance

This environment configuration reflects common real-world enterprise cloud security operations involving:
- SIEM deployments
- telemetry analytics
- authentication monitoring
- workload visibility
- posture management visibility
- governance monitoring
- operational cloud investigations

The implementation demonstrates realistic operational cloud security engineering workflows commonly used within enterprise Azure environments.

---

# Operational Preparedness Focus

This project is positioned primarily as:
- an enterprise cloud security preparedness project
- a practical cloud security engineering environment
- a cloud-native telemetry analytics implementation
- an operational visibility platform
- a governance monitoring project

The focus is on improving:
- operational readiness
- cloud monitoring maturity
- governance visibility
- telemetry correlation capability
- operational investigations
- enterprise cloud resilience

---

# Security Principles Demonstrated

## Visibility Improves Awareness

Telemetry visibility improves operational investigations and cloud awareness.

---

## Monitoring Improves Preparedness

Operational monitoring improves incident readiness and operational resilience.

---

## Telemetry Correlation Improves Detection

Telemetry correlation improves operational cloud investigations and threat visibility.

---

## Governance Improves Operational Maturity

Operational visibility improves governance maturity and accountability.

---

## Layered Monitoring Improves Cloud Resilience

Layered telemetry analytics and operational visibility strengthen enterprise cloud resilience.

---

# Screenshots to Capture

## Recommended Evidence Screenshots

Capture screenshots for:
- resource group overview
- Log Analytics workspace
- Sentinel deployment
- Defender for Cloud overview
- VM monitoring dashboards
- analytics rule visibility
- telemetry ingestion dashboards
- Secure Score visibility
- governance monitoring dashboards
- operational environment overview

Store screenshots inside:

```text
08-DOCUMENTATION/Screenshots/
```

---

# Suggested Screenshot Names

```text
resource-group-overview.png
log-analytics-workspace.png
sentinel-deployment.png
defender-for-cloud-overview.png
vm-monitoring-dashboard.png
analytics-rule-visibility.png
telemetry-ingestion-dashboard.png
secure-score-visibility.png
governance-monitoring-dashboard.png
operational-environment-overview.png
```

---

# Continuous Improvement

The environment configuration continuously evolves as:
- cloud threats evolve
- Azure security capabilities expand
- governance requirements mature
- operational monitoring practices improve
- cloud-native attack surfaces grow
- detection engineering workflows improve
- enterprise cloud security knowledge expands

The objective is to continuously improve:
- operational cloud visibility
- telemetry analytics capability
- governance maturity
- operational investigations
- monitoring capability
- enterprise cloud resilience

---

# Final Environment Configuration Statement

The ultimate objective of this environment configuration is to demonstrate how layered telemetry analytics, posture management visibility, SIEM integration, governance visibility, and cloud-native operational monitoring improve:
- operational visibility
- telemetry analytics capability
- governance maturity
- operational preparedness
- telemetry correlation visibility
- incident response readiness
- enterprise cloud resilience

through practical operational cloud security engineering workflows using Microsoft Sentinel, Microsoft Defender for Cloud, Azure Monitor, Log Analytics, Secure Score visibility, governance telemetry analytics, and KQL-based operational monitoring within Azure environments.