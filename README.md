# Azure KQL Security Detection

SOC Analyst Cybersecurity Portfolio Project

Analyst: David Jeffries
Platform: Microsoft Azure Data Explorer
Language: Kusto Query Language (KQL)
Project Type: Security Monitoring and Threat Detection

⸻

## Project Overview

This project demonstrates how Kusto Query Language (KQL) can be used to analyze simulated authentication activity, identify excessive failed login attempts, classify security alert severity, and organize investigation results.

The project models common Security Operations Center (SOC) responsibilities, including security monitoring, alert triage, threat detection, and incident investigation.

## Tools and Technologies

* Microsoft Azure Data Explorer — Executing and testing KQL queries
* Kusto Query Language (KQL) — Analyzing and filtering security data
* GitHub — Storing and documenting the project
* Simulated Authentication Data — Testing failed-login detection rules

## Detection Rules

Failed Login Attempts	Severity
10 or more	High
5–9	Medium
Fewer than 5	Low

## Investigation Results

The KQL query identified two simulated alerts requiring investigation:

Alert 1 — High Severity

* Username: guest
* Source IP: 198.51.100.25
* Failed Login Attempts: 12
* Severity: High
* Event Time: 09:10 AM

Alert 2 — Medium Severity

* Username: admin
* Source IP: 203.0.113.45
* Failed Login Attempts: 8
* Severity: Medium
* Event Time: 09:05 AM

The query filters out Low-severity records and sorts the remaining alerts chronologically.

## Project Files

* View KQL Failed Login Detection Query
* View SOC Security Alert Investigation Report

## Skills Demonstrated

* KQL Query Development
* Security Event Analysis
* Failed Login Detection
* Security Alert Classification
* SOC Alert Triage
* Incident Investigation
* Security Documentation
* Incident Response Recommendations

## Recommended Security Response

1. Investigate accounts with repeated failed login attempts.
2. Review additional authentication logs for suspicious activity.
3. Verify whether unauthorized successful logins occurred.
4. Evaluate source IP addresses and associated activity.
5. Apply appropriate account protection measures.
6. Escalate confirmed threats according to incident response procedures.

## Project Limitations

This project uses simulated authentication data and reserved documentation IP addresses. It is a training exercise, not a live production security monitoring system or evidence of a confirmed attack.

