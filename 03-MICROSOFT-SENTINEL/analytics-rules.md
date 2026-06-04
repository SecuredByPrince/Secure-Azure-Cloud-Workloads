# Analytics Rules

## Secure Azure Cloud Workloads

This document explains the Microsoft Sentinel analytics rules implementation within the Secure Azure Cloud Workloads project.

The objective of this implementation is to improve:
- threat detection capability
- operational cloud visibility
- telemetry correlation
- operational investigations
- incident response readiness
- governance visibility
- operational monitoring maturity
- enterprise cloud resilience

through layered cloud-native detection engineering and practical operational cloud security engineering workflows within Azure environments.

---

# Analytics Rules Overview

Microsoft Sentinel analytics rules are used to:
- detect suspicious activity
- correlate operational telemetry
- generate security incidents
- improve operational awareness
- support investigations
- improve cloud monitoring visibility
- strengthen operational preparedness

The implementation demonstrates how detection engineering improves:
- cloud threat visibility
- operational investigations
- incident readiness
- workload protection awareness
- governance maturity
- operational cloud resilience

The project focuses heavily on operational visibility and realistic enterprise threat detection workflows.

---

# Analytics Rule Objectives

The analytics rules implementation was designed to:
- improve operational threat visibility
- improve cloud monitoring capability
- improve incident investigations
- improve telemetry correlation
- improve operational readiness
- improve governance visibility
- improve workload protection awareness
- strengthen enterprise cloud resilience

The implementation demonstrates how layered detection engineering improves operational cloud security maturity.

---

# Analytics Rule Architecture Flow

Telemetry Sources  
↓  
Log Analytics Workspace  
↓  
Microsoft Sentinel Analytics Rules  
↓  
Threat Detection Logic  
↓  
Alert Generation  
↓  
Incident Creation  
↓  
Operational Investigations & Response

---

# Analytics Rule Categories

The implementation includes analytics rules for:
- authentication monitoring
- operational activity monitoring
- workload anomaly visibility
- cloud activity investigations
- suspicious behaviour detection
- operational monitoring visibility
- governance-related monitoring
- threat visibility workflows

The project demonstrates how layered analytics improve operational cloud security capability.

---

# 1. Failed Sign-In Detection Rules

## Overview

Authentication monitoring is critical because compromised identities may lead to:
- unauthorized access
- privilege escalation
- workload compromise
- governance failures

The implementation includes analytics rules for:
- failed sign-ins
- brute force activity
- authentication anomalies
- suspicious login patterns

---

## Detection Objectives

Improve:
- authentication visibility
- operational investigations
- identity governance awareness
- cloud access monitoring

---

## Example Detection Logic

### Failed Sign-In Threshold Monitoring

The rule identifies:
- excessive failed authentication attempts
- repeated login failures
- suspicious authentication behaviour
- operational identity anomalies

---

## Example KQL Query

```kql
SigninLogs
| where ResultType != 0
| summarize FailedAttempts=count() by UserPrincipalName, IPAddress
| where FailedAttempts >= 5
| order by FailedAttempts desc
```

---

## Operational Benefits

Failed sign-in analytics improve:
- operational investigations
- cloud threat visibility
- operational preparedness
- identity awareness

---

# 2. Brute Force Detection Rules

## Overview

Brute force attacks are common internet-facing threats targeting:
- administrative accounts
- exposed workloads
- remote management services
- cloud authentication systems

The implementation demonstrates how Sentinel analytics improve brute force visibility.

---

## Detection Objectives

Improve:
- workload exposure awareness
- authentication threat visibility
- operational readiness
- cloud monitoring maturity

---

## Detection Logic

### Brute Force Indicators

- repeated failed logins
- multiple login attempts
- suspicious authentication activity
- repeated IP-based login failures

---

## Example KQL Query

```kql
SigninLogs
| summarize Attempts=count() by IPAddress
| where Attempts > 20
| order by Attempts desc
```

---

## Operational Benefits

Brute force visibility improves:
- cloud threat awareness
- operational investigations
- workload resilience
- incident readiness

---

# 3. Azure Activity Monitoring Rules

## Overview

Administrative visibility improves:
- governance maturity
- operational accountability
- cloud activity awareness
- operational investigations

The implementation includes analytics rules for:
- suspicious administrative activity
- resource modifications
- workload changes
- operational governance visibility

---

## Detection Objectives

Improve:
- operational accountability
- cloud activity awareness
- governance visibility
- investigation readiness

---

## Detection Logic

### Administrative Activity Visibility

The rules monitor:
- resource deletions
- configuration changes
- workload modifications
- administrative anomalies

---

## Example KQL Query

```kql
AzureActivity
| summarize ActivityCount=count() by Caller, OperationName
| order by ActivityCount desc
```

---

## Operational Benefits

Administrative visibility improves:
- governance maturity
- operational investigations
- cloud awareness
- operational resilience

---

# 4. Security Alert Correlation Rules

## Overview

Security alert correlation improves:
- operational visibility
- incident investigations
- cloud monitoring capability
- workload awareness
- threat detection maturity

The implementation correlates:
- Defender for Cloud alerts
- operational telemetry
- authentication activity
- workload anomalies

---

## Detection Objectives

Improve:
- telemetry correlation capability
- operational awareness
- investigation readiness
- threat visibility

---

## Detection Logic

### Alert Correlation Visibility

The rules correlate:
- multiple security alerts
- workload findings
- suspicious operational activity
- cloud monitoring anomalies

---

## Example KQL Query

```kql
SecurityAlert
| summarize AlertCount=count() by AlertName, Severity
| order by AlertCount desc
```

---

## Operational Benefits

Alert correlation improves:
- operational investigations
- cloud threat visibility
- governance awareness
- operational preparedness

---

# 5. Workload Monitoring Rules

## Overview

Workload visibility improves:
- workload resilience
- operational awareness
- governance visibility
- incident readiness

The implementation includes analytics rules for:
- workload anomalies
- VM activity visibility
- operational monitoring
- workload investigations

---

## Detection Objectives

Improve:
- workload protection awareness
- cloud visibility
- operational investigations
- workload resilience

---

## Detection Logic

### Workload Activity Monitoring

The rules monitor:
- abnormal workload activity
- operational telemetry
- workload behaviour anomalies
- operational monitoring visibility

---

## Example KQL Query

```kql
Heartbeat
| summarize LastHeartbeat=max(TimeGenerated) by Computer
```

---

## Operational Benefits

Workload monitoring improves:
- operational visibility
- cloud monitoring maturity
- workload awareness
- incident readiness

---

# 6. Threat Hunting Visibility Rules

## Overview

Threat hunting workflows improve:
- operational investigations
- cloud threat awareness
- telemetry analysis capability
- operational preparedness

The implementation demonstrates practical operational cloud threat hunting workflows.

---

## Detection Objectives

Improve:
- operational investigations
- telemetry analysis capability
- cloud visibility
- operational resilience

---

## Detection Logic

### Threat Hunting Visibility

The rules support:
- operational telemetry analysis
- suspicious activity reviews
- workload investigations
- cloud monitoring visibility

---

## Operational Benefits

Threat hunting visibility improves:
- operational awareness
- incident investigations
- governance visibility
- enterprise cloud resilience

---

# Analytics Rule Severity Levels

The implementation uses severity classifications involving:
- High Severity
- Medium Severity
- Low Severity
- Informational Visibility

Severity classification improves:
- operational prioritization
- incident management
- governance visibility
- response coordination

---

# Alert-to-Incident Workflow

Analytics rules generate:
- operational alerts
- incident visibility
- telemetry investigations
- operational response workflows

The workflow follows:

Suspicious Activity  
↓  
Analytics Rule Triggered  
↓  
Security Alert Generated  
↓  
Incident Created  
↓  
Operational Investigation Initiated  
↓  
Response Activities Performed

---

# Detection Engineering Visibility

The implementation demonstrates practical detection engineering involving:
- KQL-based detections
- telemetry correlation
- operational monitoring
- incident generation
- cloud activity investigations
- workload visibility

The project demonstrates realistic enterprise detection engineering workflows.

---

# Operational Monitoring Visibility

The analytics rules improve visibility into:
- authentication anomalies
- operational telemetry
- administrative changes
- workload monitoring
- suspicious activity
- cloud monitoring gaps
- governance visibility

The implementation demonstrates how analytics visibility improves operational cloud resilience.

---

# Governance Visibility

The analytics rule framework improves governance through:
- operational monitoring visibility
- telemetry accountability
- workload awareness
- cloud activity visibility
- incident investigations
- operational maturity tracking

The implementation demonstrates how centralized detection engineering improves enterprise cloud resilience.

---

# Operational Security Benefits

The analytics rule implementation improves:
- operational cloud visibility
- threat detection capability
- telemetry correlation visibility
- operational investigations
- governance maturity
- monitoring capability
- incident response readiness
- enterprise cloud resilience

---

# Real-World Relevance

This analytics rule implementation reflects common real-world enterprise cloud security operations involving:
- SIEM detections
- telemetry correlation
- operational investigations
- authentication monitoring
- cloud activity monitoring
- workload visibility
- operational threat detection

The implementation demonstrates realistic operational cloud security engineering workflows commonly used within enterprise Azure environments.

---

# Operational Preparedness Focus

This project is positioned primarily as:
- an enterprise cloud security preparedness project
- a practical cloud security engineering environment
- a cloud-native SIEM implementation
- an operational monitoring platform
- a detection engineering project

The focus is on improving:
- operational readiness
- cloud monitoring maturity
- governance visibility
- telemetry correlation capability
- operational investigations
- enterprise cloud resilience

---

# Security Principles Demonstrated

## Detection Visibility Matters

Threat detection visibility improves operational investigations and cloud awareness.

---

## Monitoring Improves Preparedness

Operational monitoring improves incident readiness and enterprise resilience.

---

## Telemetry Correlation Improves Detection

Telemetry correlation improves operational cloud threat visibility.

---

## Governance Improves Operational Maturity

Operational visibility improves governance maturity and accountability.

---

## Layered Detection Engineering Improves Cloud Resilience

Layered analytics and operational monitoring strengthen enterprise cloud resilience.

---

# Screenshots to Capture

## Recommended Evidence Screenshots

Capture screenshots for:
- analytics rules overview
- failed sign-in detection rule
- brute force detection rule
- Azure Activity monitoring rule
- security alert correlation rule
- workload monitoring rule
- analytics rule severity settings
- alert generation visibility
- incident creation workflow
- KQL analytics query visibility

Store screenshots inside:

```text
03-MICROSOFT-SENTINEL/Screenshots/
```

---

# Suggested Screenshot Names

```text
analytics-rules-overview.png
failed-signin-detection-rule.png
brute-force-detection-rule.png
azure-activity-monitoring-rule.png
security-alert-correlation-rule.png
workload-monitoring-rule.png
analytics-rule-severity-settings.png
alert-generation-visibility.png
incident-creation-workflow.png
kql-analytics-query-visibility.png
```

---

# Continuous Improvement

The analytics rule implementation continuously evolves as:
- cloud threats evolve
- Azure capabilities expand
- governance requirements mature
- operational monitoring practices improve
- cloud-native attack surfaces grow
- detection engineering workflows improve
- enterprise cloud security knowledge expands

The objective is to continuously improve:
- operational cloud visibility
- threat detection capability
- governance maturity
- operational investigations
- monitoring visibility
- enterprise cloud resilience

---

# Final Analytics Rules Statement

The ultimate objective of this analytics rule implementation is to demonstrate how layered detection engineering and cloud-native SIEM monitoring improve:
- operational visibility
- threat detection capability
- governance maturity
- operational investigations
- incident response readiness
- operational preparedness
- enterprise cloud resilience

through practical operational cloud security engineering workflows using Microsoft Sentinel within Azure environments.