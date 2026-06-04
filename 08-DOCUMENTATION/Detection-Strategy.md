# Detection Strategy

## Secure Azure Cloud Workloads

This document explains the detection strategy implementation for the Secure Azure Cloud Workloads project using Microsoft Defender for Cloud, Microsoft Sentinel, Azure Monitor, Log Analytics, Kusto Query Language (KQL), telemetry analytics, posture management workflows, and cloud-native operational monitoring within Azure environments.

The objective of this detection strategy is to:
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

# Detection Strategy Overview

The Secure Azure Cloud Workloads detection strategy demonstrates a practical enterprise cloud detection architecture involving:
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

# Detection Strategy Objectives

The detection strategy was designed to:
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

# Detection Architecture Overview

Telemetry Sources  
↓  
Azure Monitor  
↓  
Log Analytics Workspace  
↓  
Microsoft Sentinel  
↓  
Analytics Rules & Correlation  
↓  
Security Alerts  
↓  
Incident Investigations  
↓  
Operational Response

---

# Detection Scope

The implementation detects:
- failed authentication attempts
- suspicious IP activity
- abnormal sign-in behaviour
- administrative anomalies
- workload operational risks
- posture management findings
- telemetry inconsistencies
- governance monitoring gaps

---

# Core Detection Components

| Service | Detection Purpose |
|---|---|
| Microsoft Sentinel | SIEM detections and investigations |
| Microsoft Defender for Cloud | Posture and workload findings |
| Azure Monitor | Telemetry collection |
| Log Analytics Workspace | Telemetry analytics |
| Microsoft Entra ID | Authentication detections |
| Azure Activity Logs | Administrative detections |
| Security Events | VM security visibility |
| KQL Analytics | Detection engineering |

---

# 1. Authentication Detection Strategy

## Overview

Identity systems are critical operational trust boundaries within cloud environments.

Threat actors frequently target:
- exposed identities
- administrative accounts
- authentication services
- remote access pathways

The detection strategy improves visibility into:
- failed sign-ins
- suspicious login attempts
- abnormal authentication behaviour
- identity anomalies
- authentication telemetry

---

## Authentication Detection Areas

### Failed Sign-In Detection

The implementation detects:
- repeated failed sign-ins
- authentication anomalies
- suspicious login behaviour
- abnormal authentication patterns
- operational authentication risks

---

### Suspicious Authentication Detection

The implementation detects:
- authentication anomalies
- unusual sign-in behaviour
- abnormal authentication locations
- repeated authentication failures
- operational authentication inconsistencies

---

## Detection Telemetry Sources

The detection strategy uses:
- Sign-In Logs
- Audit Logs
- Sentinel analytics
- Log Analytics telemetry
- Microsoft Entra ID visibility

---

## Example KQL Query

```kql
SigninLogs
| where ResultType != 0
| summarize FailedAttempts=count()
    by UserPrincipalName, IPAddress
| where FailedAttempts >= 5
```

---

## Operational Detection Benefits

Authentication detections improve:
- operational awareness
- governance maturity
- incident preparedness
- enterprise cloud resilience

---

# 2. Security Alert Detection Strategy

## Overview

Security alerts improve:
- operational investigations
- telemetry correlation
- governance visibility
- incident response readiness

The implementation improves visibility into:
- Defender alerts
- Sentinel incidents
- workload operational risks
- posture management findings
- suspicious operational activity

---

## Alert Detection Areas

### Alert Correlation

The implementation detects:
- correlated telemetry anomalies
- suspicious operational activity
- workload monitoring inconsistencies
- authentication anomalies
- governance visibility gaps

---

### Severity-Based Detection

The implementation categorizes:
- informational alerts
- low-severity alerts
- medium-severity alerts
- high-severity alerts
- operational risk visibility

---

## Detection Telemetry Sources

The detection strategy uses:
- Security Alerts
- Sentinel incidents
- Defender findings
- Azure Monitor telemetry
- Log Analytics analytics

---

## Example KQL Query

```kql
SecurityAlert
| summarize AlertCount=count()
    by Severity
```

---

## Operational Detection Benefits

Security alert detections improve:
- incident investigations
- telemetry analytics
- governance awareness
- enterprise cloud resilience

---

# 3. Administrative Activity Detection Strategy

## Overview

Operational accountability is essential for enterprise cloud resilience.

The implementation improves visibility into:
- administrative operations
- workload modifications
- governance inconsistencies
- operational telemetry
- monitoring visibility

---

## Administrative Detection Areas

### Administrative Operation Detection

The implementation detects:
- administrative anomalies
- workload modifications
- governance telemetry inconsistencies
- suspicious operational changes
- monitoring visibility gaps

---

### Correlation Visibility

The implementation correlates:
- Azure Activity telemetry
- authentication activity
- workload operational changes
- governance telemetry
- incident investigations

---

## Detection Telemetry Sources

The detection strategy uses:
- Azure Activity Logs
- Azure Monitor
- Sentinel analytics
- Log Analytics telemetry
- governance monitoring visibility

---

## Example KQL Query

```kql
AzureActivity
| summarize ActivityCount=count()
    by Caller, OperationNameValue
```

---

## Operational Detection Benefits

Administrative detections improve:
- governance maturity
- operational preparedness
- monitoring capability
- enterprise cloud resilience

---

# 4. Workload Detection Strategy

## Overview

Workload visibility improves:
- operational awareness
- workload resilience
- governance maturity
- incident readiness

The implementation improves visibility into:
- workload telemetry
- VM operational activity
- workload anomalies
- monitoring failures
- workload exposure findings

---

## Workload Detection Areas

### VM Security Monitoring

The implementation detects:
- workload telemetry anomalies
- authentication failures
- workload monitoring inconsistencies
- disconnected workloads
- operational VM risks

---

### Security Event Visibility

The implementation reviews:
- VM authentication events
- workload operational telemetry
- heartbeat visibility
- security event anomalies
- operational monitoring inconsistencies

---

## Detection Telemetry Sources

The detection strategy uses:
- Azure Monitor Agent
- VM Insights
- Security Events
- Performance telemetry
- heartbeat telemetry

---

## Example KQL Query

```kql
Heartbeat
| summarize LastHeartbeat=max(TimeGenerated)
    by Computer
```

---

## Operational Detection Benefits

Workload detections improve:
- workload awareness
- operational preparedness
- governance visibility
- enterprise cloud resilience

---

# 5. Suspicious IP Detection Strategy

## Overview

Suspicious IP visibility improves:
- operational investigations
- telemetry correlation
- authentication monitoring
- governance awareness
- incident preparedness

The implementation improves visibility into:
- repeated authentication attempts
- abnormal IP behaviour
- suspicious operational activity
- authentication anomalies
- workload operational risks

---

## Suspicious IP Detection Areas

### Authentication Correlation

The implementation detects:
- repeated failed authentication attempts
- excessive sign-in activity
- shared IP operational anomalies
- authentication inconsistencies
- operational authentication risks

---

### IP Activity Visibility

The implementation reviews:
- authentication locations
- repeated IP activity
- operational anomalies
- governance telemetry inconsistencies
- workload authentication risks

---

## Detection Telemetry Sources

The detection strategy uses:
- Sign-In Logs
- Security Events
- Azure Activity Logs
- Sentinel analytics
- telemetry correlation visibility

---

## Example KQL Query

```kql
SigninLogs
| summarize SignInCount=count()
    by IPAddress
| where SignInCount >= 20
```

---

## Operational Detection Benefits

Suspicious IP detections improve:
- operational investigations
- governance visibility
- incident preparedness
- enterprise cloud resilience

---

# 6. Telemetry Correlation Detection Strategy

## Overview

Telemetry correlation improves:
- operational investigations
- cloud monitoring capability
- governance visibility
- incident readiness

The implementation correlates:
- Sentinel alerts
- Defender findings
- authentication telemetry
- workload operational data
- governance telemetry

---

## Correlation Detection Areas

### SIEM Correlation

The implementation improves:
- telemetry consistency
- operational visibility
- analytics correlation
- governance telemetry visibility
- monitoring maturity

---

### Multi-Source Correlation

The implementation correlates:
- Sign-In Logs
- Azure Activity
- Security Alerts
- VM telemetry
- Defender findings

---

## Detection Telemetry Sources

The detection strategy uses:
- Microsoft Sentinel
- Log Analytics
- Azure Monitor
- Defender for Cloud
- workload telemetry

---

## Example KQL Query

```kql
SecurityAlert
| summarize AlertCount=count()
    by ProviderName, Severity
```

---

## Operational Detection Benefits

Telemetry correlation improves:
- operational investigations
- governance awareness
- incident preparedness
- enterprise cloud resilience

---

# 7. Governance Detection Strategy

## Overview

Governance visibility improves:
- operational accountability
- posture management maturity
- workload awareness
- cloud monitoring capability

The implementation reviews:
- governance inconsistencies
- posture management gaps
- monitoring weaknesses
- operational blind spots

---

## Governance Detection Areas

### Governance Monitoring

The implementation detects:
- posture management anomalies
- governance telemetry inconsistencies
- monitoring gaps
- operational maturity weaknesses
- workload exposure findings

---

### Recommendation Visibility

The implementation reviews:
- Secure Score recommendations
- Defender findings
- governance telemetry
- operational maturity visibility
- workload exposure risks

---

## Detection Telemetry Sources

The detection strategy uses:
- Defender for Cloud
- Secure Score
- Sentinel dashboards
- Log Analytics telemetry
- Azure Monitor visibility

---

## Example KQL Query

```kql
SecurityRecommendation
| summarize RecommendationCount=count()
    by RecommendationName
```

---

## Operational Detection Benefits

Governance detections improve:
- governance maturity
- operational preparedness
- cloud resilience
- operational accountability

---

# 8. Incident Investigation Detection Strategy

## Overview

Incident investigations improve:
- operational preparedness
- cloud resilience
- governance maturity
- monitoring visibility

The implementation improves:
- incident visibility
- telemetry analytics
- operational coordination
- governance accountability
- monitoring maturity

---

## Investigation Detection Areas

### Security Investigations

The implementation investigates:
- Sentinel incidents
- telemetry analytics
- workload visibility
- governance monitoring
- operational cloud risks

---

### Investigation Correlation

The implementation correlates:
- Security Alerts
- Sign-In Logs
- Azure Activity Logs
- VM telemetry
- governance telemetry

---

## Detection Telemetry Sources

The detection strategy uses:
- Sentinel incidents
- Security Alerts
- Log Analytics
- Azure Monitor
- Defender telemetry

---

## Example KQL Query

```kql
SecurityIncident
| summarize IncidentCount=count()
    by Severity
```

---

## Operational Detection Benefits

Incident investigations improve:
- governance maturity
- operational preparedness
- cloud resilience
- operational accountability

---

# 9. Continuous Detection Improvement Strategy

## Overview

Enterprise cloud governance is not static.

The implementation demonstrated that:
- cloud threats evolve
- governance requirements mature
- operational risks change
- monitoring practices improve
- telemetry analytics evolve

As a result, detection maturity requires:
- continuous monitoring
- ongoing posture improvements
- operational refinement
- telemetry visibility enhancements
- governance optimization

---

## Continuous Improvement Areas

### Detection Optimization

The implementation improves:
- telemetry visibility
- governance maturity
- workload monitoring
- incident investigations
- operational preparedness

---

### Detection Engineering Improvements

The implementation continuously reviews:
- analytics rules
- telemetry ingestion
- detection coverage
- governance visibility
- workload operational telemetry

---

## Operational Detection Benefits

Continuous detection improvements strengthen:
- operational preparedness
- governance maturity
- monitoring capability
- enterprise cloud resilience

---

# Detection Validation Checklist

## Validate the Following

| Validation Area | Status |
|---|---|
| Authentication Detections Operational | ☐ |
| Security Alerts Visible | ☐ |
| Administrative Activity Monitoring Operational | ☐ |
| VM Monitoring Active | ☐ |
| Sentinel Correlation Functional | ☐ |
| Defender Findings Visible | ☐ |
| Governance Monitoring Operational | ☐ |
| Telemetry Ingestion Functional | ☐ |
| Incident Visibility Operational | ☐ |
| KQL Queries Functional | ☐ |

---

# Example Validation Queries

## Failed Sign-Ins

```kql
SigninLogs
| where ResultType != 0
```

---

## Security Alerts

```kql
SecurityAlert
```

---

## Azure Activity

```kql
AzureActivity
```

---

## VM Heartbeat Visibility

```kql
Heartbeat
```

---

# Operational Detection Benefits

The detection strategy improves:
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

This detection strategy reflects common real-world enterprise cloud security operations involving:
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
- Sentinel detection dashboards
- Defender for Cloud findings
- analytics rules
- authentication monitoring dashboards
- telemetry correlation visibility
- workload monitoring dashboards
- governance monitoring visibility
- incident investigations
- detection analytics
- operational monitoring overview

Store screenshots inside:

```text
08-DOCUMENTATION/Screenshots/
```

---

# Suggested Screenshot Names

```text
sentinel-detection-dashboard.png
defender-findings.png
analytics-rules.png
authentication-monitoring-dashboard.png
telemetry-correlation-visibility.png
workload-monitoring-dashboard.png
governance-monitoring-visibility.png
incident-investigations.png
detection-analytics.png
operational-monitoring-overview.png
```

---

# Continuous Improvement

The detection strategy continuously evolves as:
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

# Final Detection Strategy Statement

The ultimate objective of this detection strategy is to demonstrate how layered telemetry analytics, posture management visibility, SIEM integration, and cloud-native operational monitoring improve:
- operational visibility
- telemetry analytics capability
- governance maturity
- operational preparedness
- telemetry correlation visibility
- incident response readiness
- enterprise cloud resilience

through practical operational cloud security engineering workflows using Microsoft Sentinel, Microsoft Defender for Cloud, Azure Monitor, Log Analytics, Secure Score visibility, governance telemetry analytics, and KQL-based operational monitoring within Azure environments.