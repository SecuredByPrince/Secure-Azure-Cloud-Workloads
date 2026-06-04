# MITRE ATT&CK Mapping

## Secure Azure Cloud Workloads

## Enterprise Cloud Security Engineering, Threat Visibility & Cloud-Native Security Operations Platform

---

# MITRE ATT&CK Mapping Overview

This document maps the Secure Azure Cloud Workloads project to the MITRE ATT&CK framework using:
- Microsoft Sentinel
- Microsoft Defender for Cloud
- Azure Monitor
- Log Analytics Workspace
- Microsoft Entra ID
- Azure Activity Logs
- Kusto Query Language (KQL)
- telemetry analytics
- workload monitoring
- cloud-native operational investigations

The objective of this document is to demonstrate how:
- telemetry analytics
- SIEM visibility
- operational investigations
- governance monitoring
- workload visibility
- cloud-native operational monitoring

align with enterprise threat detection and operational visibility workflows commonly mapped to the MITRE ATT&CK framework.

---

# MITRE ATT&CK Overview

The MITRE ATT&CK framework provides a globally recognized knowledge base of:
- adversary tactics
- attack techniques
- operational behaviours
- detection opportunities
- investigation visibility
- defensive monitoring strategies

The framework helps organizations:
- improve threat visibility
- strengthen detection maturity
- improve operational investigations
- improve telemetry analytics
- improve incident readiness
- strengthen enterprise cloud resilience

---

# Project Objectives

This implementation demonstrates how Azure-native telemetry analytics improve:
- operational visibility
- detection maturity
- telemetry correlation capability
- governance maturity
- workload operational awareness
- incident investigation readiness
- operational preparedness
- enterprise cloud resilience

---

# MITRE ATT&CK Mapping Scope

The implementation maps:
- authentication monitoring
- workload monitoring
- telemetry analytics
- governance visibility
- SIEM investigations
- operational investigations
- workload operational anomalies
- administrative activity monitoring

to MITRE ATT&CK tactics and operational visibility workflows.

---

# MITRE ATT&CK Tactics Covered

| MITRE ATT&CK Tactic | Project Coverage |
|---|---|
| Initial Access | Authentication visibility |
| Execution | Administrative activity visibility |
| Persistence | Governance monitoring |
| Privilege Escalation | Administrative telemetry |
| Defense Evasion | Telemetry visibility gaps |
| Credential Access | Failed sign-in analytics |
| Discovery | Workload operational analytics |
| Lateral Movement | Operational investigations |
| Collection | Telemetry analytics |
| Command and Control | Operational visibility |
| Exfiltration | Operational investigations |
| Impact | Monitoring disruption visibility |

---

# 1. Initial Access

## MITRE ATT&CK Tactic

```text
TA0001 — Initial Access
```

---

## Threat Overview

Threat actors commonly attempt to gain access through:
- exposed credentials
- authentication abuse
- unauthorized sign-in attempts
- identity visibility gaps
- remote administrative pathways

---

## Project Visibility Coverage

The implementation improves visibility into:
- failed sign-ins
- suspicious authentication activity
- authentication telemetry anomalies
- abnormal sign-in behaviour
- operational identity risks

---

## Microsoft Technologies Used

| Technology | Purpose |
|---|---|
| Microsoft Entra ID | Authentication visibility |
| Microsoft Sentinel | SIEM investigations |
| Log Analytics | Telemetry analytics |
| KQL | Authentication investigations |

---

## Example KQL Query

```kql
SigninLogs
| where ResultType != 0
| summarize FailedAttempts=count()
    by UserPrincipalName, IPAddress
```

---

## Operational Security Value

The implementation improves:
- authentication monitoring
- operational investigations
- telemetry visibility
- operational preparedness
- enterprise cloud resilience

---

# 2. Credential Access

## MITRE ATT&CK Tactic

```text
TA0006 — Credential Access
```

---

## Threat Overview

Threat actors frequently target:
- privileged accounts
- exposed credentials
- identity systems
- authentication visibility weaknesses
- operational blind spots

---

## Project Visibility Coverage

The implementation improves visibility into:
- repeated failed sign-ins
- suspicious authentication activity
- operational identity anomalies
- abnormal authentication behaviour
- sign-in telemetry analytics

---

## Microsoft Technologies Used

| Technology | Purpose |
|---|---|
| Microsoft Entra ID | Identity telemetry |
| Microsoft Sentinel | Authentication investigations |
| Azure Monitor | Operational telemetry |
| KQL | Authentication analytics |

---

## Example KQL Query

```kql
SigninLogs
| where ResultType != 0
| summarize FailedAttempts=count()
    by UserPrincipalName, IPAddress
| order by FailedAttempts desc
```

---

## Operational Security Value

The implementation improves:
- authentication visibility
- governance awareness
- operational investigations
- monitoring maturity
- enterprise resilience

---

# 3. Execution

## MITRE ATT&CK Tactic

```text
TA0002 — Execution
```

---

## Threat Overview

Threat actors may attempt to:
- execute unauthorized actions
- perform administrative operations
- modify operational resources
- change workload configurations
- disrupt operational visibility

---

## Project Visibility Coverage

The implementation improves visibility into:
- administrative operations
- workload modifications
- operational telemetry
- governance inconsistencies
- operational anomalies

---

## Microsoft Technologies Used

| Technology | Purpose |
|---|---|
| Azure Activity Logs | Administrative visibility |
| Microsoft Sentinel | Operational investigations |
| Log Analytics | Telemetry analytics |
| KQL | Operational investigations |

---

## Example KQL Query

```kql
AzureActivity
| summarize ActivityCount=count()
    by Caller, OperationNameValue
```

---

## Operational Security Value

The implementation improves:
- operational visibility
- governance maturity
- investigation capability
- workload operational awareness
- operational preparedness

---

# 4. Persistence

## MITRE ATT&CK Tactic

```text
TA0003 — Persistence
```

---

## Threat Overview

Threat actors may attempt to maintain operational access through:
- unauthorized administrative changes
- governance inconsistencies
- monitoring weaknesses
- workload operational persistence
- operational visibility gaps

---

## Project Visibility Coverage

The implementation improves visibility into:
- governance telemetry
- operational modifications
- posture management visibility
- workload operational risks
- remediation visibility

---

## Microsoft Technologies Used

| Technology | Purpose |
|---|---|
| Microsoft Defender for Cloud | Governance visibility |
| Secure Score | Posture awareness |
| Microsoft Sentinel | SIEM investigations |
| KQL | Governance analytics |

---

## Example KQL Query

```kql
SecurityRecommendation
| summarize RecommendationCount=count()
    by RecommendationName
```

---

## Operational Security Value

The implementation improves:
- governance maturity
- posture management visibility
- remediation awareness
- operational preparedness
- enterprise resilience

---

# 5. Privilege Escalation

## MITRE ATT&CK Tactic

```text
TA0004 — Privilege Escalation
```

---

## Threat Overview

Threat actors may attempt to:
- abuse administrative permissions
- modify privileged configurations
- gain elevated operational access
- exploit governance weaknesses
- manipulate operational settings

---

## Project Visibility Coverage

The implementation improves visibility into:
- administrative operations
- privileged activity
- governance inconsistencies
- operational anomalies
- workload configuration changes

---

## Microsoft Technologies Used

| Technology | Purpose |
|---|---|
| Azure Activity Logs | Administrative visibility |
| Microsoft Sentinel | Privileged activity investigations |
| Log Analytics | Telemetry analytics |
| KQL | Operational analytics |

---

## Example KQL Query

```kql
AzureActivity
| summarize ActivityCount=count()
    by Caller, OperationNameValue
| order by ActivityCount desc
```

---

## Operational Security Value

The implementation improves:
- governance accountability
- operational awareness
- telemetry analytics capability
- monitoring maturity
- enterprise resilience

---

# 6. Defense Evasion

## MITRE ATT&CK Tactic

```text
TA0005 — Defense Evasion
```

---

## Threat Overview

Threat actors may attempt to:
- disrupt telemetry visibility
- exploit monitoring blind spots
- bypass operational analytics
- avoid detection visibility
- create telemetry fragmentation

---

## Project Visibility Coverage

The implementation improves visibility into:
- telemetry ingestion
- monitoring inconsistencies
- workload operational anomalies
- operational blind spots
- SIEM telemetry analytics

---

## Microsoft Technologies Used

| Technology | Purpose |
|---|---|
| Azure Monitor | Telemetry collection |
| Log Analytics | Telemetry analytics |
| Microsoft Sentinel | SIEM correlation |
| KQL | Operational investigations |

---

## Example KQL Query

```kql
SecurityAlert
| summarize AlertCount=count()
    by ProviderName, Severity
```

---

## Operational Security Value

The implementation improves:
- telemetry analytics capability
- operational investigations
- monitoring consistency
- governance visibility
- operational preparedness

---

# 7. Discovery

## MITRE ATT&CK Tactic

```text
TA0007 — Discovery
```

---

## Threat Overview

Threat actors commonly attempt to:
- identify workloads
- discover operational resources
- analyze monitoring visibility
- identify governance weaknesses
- locate operational blind spots

---

## Project Visibility Coverage

The implementation improves visibility into:
- workload operational activity
- VM telemetry
- workload operational anomalies
- monitoring inconsistencies
- workload operational visibility

---

## Microsoft Technologies Used

| Technology | Purpose |
|---|---|
| Azure Monitor | Workload telemetry |
| VM Insights | Workload analytics |
| Microsoft Sentinel | SIEM visibility |
| KQL | Operational investigations |

---

## Example KQL Query

```kql
Heartbeat
| summarize LastHeartbeat=max(TimeGenerated)
    by Computer
```

---

## Operational Security Value

The implementation improves:
- workload operational awareness
- telemetry visibility
- governance maturity
- operational preparedness
- enterprise resilience

---

# 8. Lateral Movement

## MITRE ATT&CK Tactic

```text
TA0008 — Lateral Movement
```

---

## Threat Overview

Threat actors may attempt to:
- move between workloads
- exploit operational visibility gaps
- abuse administrative pathways
- exploit governance weaknesses
- expand operational access

---

## Project Visibility Coverage

The implementation improves visibility into:
- authentication telemetry
- workload operational activity
- administrative operations
- operational anomalies
- telemetry correlation visibility

---

## Microsoft Technologies Used

| Technology | Purpose |
|---|---|
| Microsoft Sentinel | Correlation investigations |
| Azure Monitor | Workload telemetry |
| Log Analytics | Telemetry analytics |
| KQL | Operational investigations |

---

## Example KQL Query

```kql
SigninLogs
| summarize SignInCount=count()
    by UserPrincipalName, IPAddress
```

---

## Operational Security Value

The implementation improves:
- telemetry correlation capability
- operational investigations
- monitoring maturity
- governance visibility
- enterprise resilience

---

# 9. Collection

## MITRE ATT&CK Tactic

```text
TA0009 — Collection
```

---

## Threat Overview

Threat actors may attempt to:
- gather operational telemetry
- identify workload visibility gaps
- exploit monitoring weaknesses
- collect operational information
- analyze cloud operational activity

---

## Project Visibility Coverage

The implementation improves visibility into:
- telemetry analytics
- operational visibility
- workload operational activity
- governance telemetry
- monitoring consistency

---

## Microsoft Technologies Used

| Technology | Purpose |
|---|---|
| Log Analytics | Telemetry analytics |
| Azure Monitor | Operational telemetry |
| Microsoft Sentinel | SIEM investigations |
| KQL | Operational analytics |

---

## Example KQL Query

```kql
SecurityAlert
| summarize AlertCount=count()
    by Severity
```

---

## Operational Security Value

The implementation improves:
- telemetry analytics capability
- operational investigations
- governance awareness
- operational preparedness
- enterprise resilience

---

# 10. Impact

## MITRE ATT&CK Tactic

```text
TA0040 — Impact
```

---

## Threat Overview

Threat actors may attempt to:
- disrupt operational visibility
- impact workload availability
- weaken monitoring continuity
- exploit governance weaknesses
- reduce operational awareness

---

## Project Visibility Coverage

The implementation improves visibility into:
- workload operational telemetry
- monitoring continuity
- governance inconsistencies
- telemetry fragmentation
- operational anomalies

---

## Microsoft Technologies Used

| Technology | Purpose |
|---|---|
| Azure Monitor | Monitoring continuity |
| Microsoft Sentinel | Operational investigations |
| Defender for Cloud | Governance visibility |
| KQL | Operational analytics |

---

## Example KQL Query

```kql
Heartbeat
| summarize LastHeartbeat=max(TimeGenerated)
    by Computer
```

---

## Operational Security Value

The implementation improves:
- operational preparedness
- monitoring maturity
- governance visibility
- workload operational awareness
- enterprise resilience

---

# Detection Engineering Mapping

The implementation demonstrates practical detection engineering involving:
- telemetry analytics
- SIEM investigations
- authentication monitoring
- workload monitoring
- governance visibility
- telemetry correlation
- operational investigations
- KQL analytics

---

# Enterprise Security Engineering Skills Demonstrated

This project demonstrates practical experience involving:
- SIEM engineering
- telemetry analytics
- operational investigations
- governance visibility
- workload monitoring
- posture management visibility
- KQL analytics
- cloud operational investigations

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

# Real-World Enterprise Relevance

This project reflects realistic enterprise cloud operational workflows involving:
- SIEM deployments
- telemetry analytics
- authentication monitoring
- workload visibility
- posture management visibility
- governance monitoring
- operational investigations
- cloud operational analytics

The implementation demonstrates realistic operational cloud security engineering workflows commonly used within enterprise Azure environments.

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

# MITRE ATT&CK Coverage Summary

| MITRE ATT&CK Area | Visibility Capability |
|---|---|
| Initial Access | Authentication monitoring |
| Credential Access | Failed sign-in analytics |
| Execution | Administrative telemetry |
| Persistence | Governance visibility |
| Privilege Escalation | Administrative monitoring |
| Defense Evasion | Telemetry analytics |
| Discovery | Workload monitoring |
| Lateral Movement | Telemetry correlation |
| Collection | Operational analytics |
| Impact | Monitoring continuity |

---

# Screenshots to Capture

## Recommended Evidence Screenshots

Capture screenshots for:
- Sentinel dashboards
- Secure Score visibility
- Defender for Cloud overview
- authentication monitoring dashboards
- telemetry correlation visibility
- workload monitoring dashboards
- governance monitoring visibility
- incident investigations
- operational analytics
- operational monitoring overview

Store screenshots inside:

```text
04-THREAT-DETECTION/Screenshots/
```

---

# Suggested Screenshot Names

```text
sentinel-dashboard.png
secure-score-visibility.png
defender-for-cloud-overview.png
authentication-monitoring-dashboard.png
telemetry-correlation-visibility.png
workload-monitoring-dashboard.png
governance-monitoring-visibility.png
incident-investigations.png
operational-analytics.png
operational-monitoring-overview.png
```

---

# Final MITRE ATT&CK Mapping Statement

The Secure Azure Cloud Workloads implementation demonstrates how layered telemetry analytics, posture management visibility, SIEM integration, governance visibility, and cloud-native operational monitoring align with MITRE ATT&CK operational visibility and detection workflows by improving:
- operational visibility
- telemetry analytics capability
- governance maturity
- operational preparedness
- telemetry correlation visibility
- incident response readiness
- enterprise cloud resilience

through practical operational cloud security engineering workflows using Microsoft Sentinel, Microsoft Defender for Cloud, Azure Monitor, Log Analytics, Secure Score visibility, governance telemetry analytics, and KQL-based operational monitoring within Azure environments.