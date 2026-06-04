# KQL Queries

## Secure Azure Cloud Workloads

This document explains the Kusto Query Language (KQL) queries implemented within the Secure Azure Cloud Workloads project using Microsoft Sentinel, Microsoft Defender for Cloud, Azure Monitor, Log Analytics, telemetry analytics, and cloud-native operational monitoring workflows.

The objective of this implementation is to improve:
- operational threat visibility
- telemetry correlation capability
- operational investigations
- cloud monitoring maturity
- governance visibility
- workload awareness
- incident response readiness
- enterprise cloud resilience

through layered cloud-native telemetry analytics and practical operational cloud security engineering workflows within Azure environments.

---

# KQL Overview

Kusto Query Language (KQL) is used throughout the project for:
- telemetry analysis
- operational investigations
- threat hunting
- authentication monitoring
- workload visibility
- governance analysis
- incident investigations
- cloud operational monitoring

The implementation demonstrates how cloud-native telemetry analytics improve:
- operational awareness
- cloud threat visibility
- governance maturity
- workload monitoring capability
- operational preparedness
- enterprise cloud resilience

---

# KQL Objectives

The KQL implementation was designed to:
- improve operational visibility
- improve cloud investigations
- improve telemetry correlation
- improve workload monitoring capability
- improve governance awareness
- improve operational preparedness
- improve detection engineering capability
- strengthen enterprise cloud resilience

The implementation demonstrates how telemetry analytics improve operational cloud security capability.

---

# KQL Operational Workflow

Telemetry Sources  
↓  
Azure Monitor Collection  
↓  
Log Analytics Workspace  
↓  
KQL Query Execution  
↓  
Telemetry Analysis & Threat Visibility  
↓  
Operational Investigations  
↓  
Governance & Response Activities

---

# KQL Visibility Areas

The implementation improves visibility into:
- authentication anomalies
- brute force activity
- workload operational telemetry
- administrative activity
- operational monitoring gaps
- governance weaknesses
- cloud operational risks
- incident investigations

The project demonstrates how telemetry analysis improves enterprise cloud resilience.

---

# Authentication Monitoring Queries

## Failed Sign-In Visibility

Authentication visibility is critical because compromised identities may lead to:
- unauthorized access
- workload compromise
- privilege escalation
- governance failures

This query identifies failed authentication activity.

---

## Failed Authentication Query

```kql
SigninLogs
| where ResultType != 0
| summarize FailedAttempts=count() by UserPrincipalName, IPAddress
| order by FailedAttempts desc
```

---

## Query Purpose

This query improves visibility into:
- failed sign-ins
- suspicious authentication attempts
- identity anomalies
- operational identity monitoring

---

## Operational Security Benefits

This visibility improves:
- operational investigations
- authentication monitoring
- governance awareness
- incident readiness

---

# Brute Force Monitoring Queries

## Brute Force Visibility

Internet-facing authentication services are common cloud attack surfaces.

This query identifies excessive authentication attempts from source IP addresses.

---

## Brute Force Query

```kql
SigninLogs
| summarize AttemptCount=count() by IPAddress
| where AttemptCount > 20
| order by AttemptCount desc
```

---

## Query Purpose

This query improves visibility into:
- repeated login attempts
- authentication spikes
- suspicious IP activity
- brute force behaviour

---

## Operational Security Benefits

This visibility improves:
- cloud monitoring maturity
- operational preparedness
- workload awareness
- operational resilience

---

# Administrative Activity Queries

## Azure Activity Visibility

Administrative operations represent critical operational trust boundaries.

This query improves visibility into:
- resource modifications
- operational changes
- administrative activity
- governance-related telemetry

---

## Azure Activity Query

```kql
AzureActivity
| summarize ActivityCount=count() by Caller, OperationName
| order by ActivityCount desc
```

---

## Query Purpose

This query improves visibility into:
- administrative anomalies
- resource modifications
- workload operational activity
- governance visibility

---

## Operational Security Benefits

This visibility improves:
- governance maturity
- operational accountability
- operational awareness
- cloud resilience

---

# Workload Monitoring Queries

## Workload Visibility

Operational monitoring visibility improves:
- workload awareness
- cloud resilience
- governance maturity
- operational preparedness

This query monitors workload heartbeat visibility.

---

## Workload Heartbeat Query

```kql
Heartbeat
| summarize LastHeartbeat=max(TimeGenerated) by Computer
```

---

## Query Purpose

This query improves visibility into:
- disconnected workloads
- monitoring failures
- workload telemetry gaps
- operational monitoring anomalies

---

## Operational Security Benefits

This visibility improves:
- workload awareness
- monitoring maturity
- operational preparedness
- governance visibility

---

# Security Alert Queries

## Security Alert Visibility

Operational investigations require centralized alert visibility.

This query improves visibility into:
- security alerts
- operational anomalies
- incident findings
- telemetry correlation visibility

---

## Security Alert Query

```kql
SecurityAlert
| summarize AlertCount=count() by Severity
```

---

## Query Purpose

This query improves visibility into:
- operational threat findings
- workload exposure
- cloud monitoring anomalies
- governance-related security findings

---

## Operational Security Benefits

This visibility improves:
- incident readiness
- governance awareness
- operational investigations
- enterprise cloud resilience

---

# Incident Investigation Queries

## Incident Visibility

Operational investigations require centralized incident visibility.

This query improves visibility into:
- incident severity
- operational findings
- incident trends
- threat visibility

---

## Incident Query

```kql
SecurityIncident
| summarize IncidentCount=count() by Severity
```

---

## Query Purpose

This query improves visibility into:
- operational investigations
- incident trends
- workload operational risks
- governance visibility

---

## Operational Security Benefits

This visibility improves:
- operational preparedness
- cloud awareness
- investigation readiness
- enterprise cloud resilience

---

# Governance Visibility Queries

## Secure Score Visibility

Governance maturity requires visibility into posture management and workload exposure findings.

This query improves governance-related telemetry analysis.

---

## Governance Query

```kql
SecurityRecommendation
| summarize RecommendationCount=count() by RecommendationName
```

---

## Query Purpose

This query improves visibility into:
- posture management findings
- governance weaknesses
- workload exposure visibility
- operational monitoring maturity

---

## Operational Security Benefits

This visibility improves:
- governance maturity
- operational preparedness
- cloud posture awareness
- enterprise cloud resilience

---

# Threat Hunting Queries

## Threat Hunting Visibility

Threat hunting improves:
- operational awareness
- telemetry analysis capability
- cloud monitoring maturity
- incident readiness

This query improves visibility into suspicious operational behaviour.

---

## Threat Hunting Query

```kql
SigninLogs
| where ResultType != 0
| summarize FailedAttempts=count() by IPAddress, UserPrincipalName
| where FailedAttempts > 10
```

---

## Query Purpose

This query improves visibility into:
- suspicious authentication behaviour
- abnormal operational activity
- telemetry anomalies
- operational cloud risks

---

## Operational Security Benefits

This visibility improves:
- operational investigations
- threat visibility
- governance awareness
- cloud resilience

---

# Telemetry Correlation Queries

## Correlation Visibility

Telemetry correlation improves:
- operational investigations
- cloud monitoring capability
- governance visibility
- incident readiness

This query correlates telemetry visibility across cloud operational sources.

---

## Telemetry Correlation Query

```kql
SecurityAlert
| summarize AlertCount=count() by ProviderName, Severity
```

---

## Query Purpose

This query improves visibility into:
- correlated security findings
- operational cloud risks
- monitoring anomalies
- governance-related telemetry

---

## Operational Security Benefits

This visibility improves:
- operational preparedness
- governance maturity
- telemetry awareness
- enterprise cloud resilience

---

# KQL Detection Engineering Support

The implementation uses KQL for:
- analytics rule development
- operational investigations
- cloud monitoring visibility
- anomaly detection
- telemetry correlation
- threat hunting
- governance analysis

The project demonstrates practical enterprise cloud telemetry analytics workflows.

---

# Operational Monitoring Visibility

The KQL implementation improves visibility into:
- authentication anomalies
- workload telemetry
- operational monitoring gaps
- cloud operational risks
- governance weaknesses
- posture inconsistencies
- operational cloud threats

The implementation demonstrates how telemetry analysis improves enterprise cloud resilience.

---

# Governance Visibility

The implementation improves governance through:
- operational accountability
- telemetry visibility
- workload awareness
- posture management visibility
- operational monitoring maturity
- incident investigation readiness

The project demonstrates how operational visibility improves governance maturity.

---

# Operational Security Benefits

The KQL implementation improves:
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

This KQL implementation reflects common real-world enterprise cloud security operations involving:
- SIEM telemetry analysis
- operational investigations
- authentication monitoring
- workload visibility
- governance monitoring
- cloud-native threat hunting
- operational cloud monitoring

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
- KQL query execution
- failed sign-in investigations
- brute force visibility
- Azure Activity telemetry
- workload heartbeat visibility
- security alert analysis
- incident trend visibility
- governance telemetry dashboards
- threat hunting investigations
- operational monitoring overview

Store screenshots inside:

```text
04-THREAT-DETECTION/Screenshots/
```

---

# Suggested Screenshot Names

```text
kql-query-execution.png
failed-signin-investigations.png
brute-force-visibility.png
azure-activity-telemetry.png
workload-heartbeat-visibility.png
security-alert-analysis.png
incident-trend-visibility.png
governance-telemetry-dashboard.png
threat-hunting-investigations.png
operational-monitoring-overview.png
```

---

# Continuous Improvement

The KQL implementation continuously evolves as:
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

# Final KQL Queries Statement

The ultimate objective of this KQL implementation is to demonstrate how layered telemetry analytics and cloud-native operational monitoring improve:
- operational visibility
- telemetry analytics capability
- governance maturity
- operational preparedness
- telemetry correlation visibility
- incident response readiness
- enterprise cloud resilience

through practical operational cloud security engineering workflows using Microsoft Sentinel, Microsoft Defender for Cloud, Azure Monitor, Log Analytics, and KQL-based telemetry analytics within Azure environments.