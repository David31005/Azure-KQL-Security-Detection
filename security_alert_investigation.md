SOC Security Alert Investigation Report

Analyst: David Jeffries
Project: Azure KQL Security Detection
Date: November 2, 2026
Environment: Azure Data Explorer (KQL)
Investigation Type: Simulated Failed Login Detection

*1. Executive Summary*

This project demonstrates how a Security Operations Center (SOC) analyst can use Kusto Query Language (KQL) to identify suspicious authentication activity, classify alert severity, and prioritize potential security incidents.

The investigation uses simulated authentication data rather than actual production security logs.

*2. Security Events Analyzed*

Username	Source IP	Failed Logins	Severity
admin	203.0.113.45	8	Medium
jsmith	192.0.2.10	2	Low
guest	198.51.100.25	12	High

All IP addresses are reserved documentation addresses used for simulation.

*3. Detection Logic*

The KQL query classifies authentication activity using the following thresholds:

* High: 10 or more failed login attempts
* Medium: 5–9 failed login attempts
* Low: Fewer than 5 failed login attempts

The query filters out Low-severity records and sorts the remaining alerts by their assigned event times.

*4. Investigation Findings*

Alert 1 — Guest Account

* Source IP: 198.51.100.25
* Failed login attempts: 12
* Severity: High
* Simulated event time: 09:10 AM

The guest account exceeded the High-severity threshold. This pattern warrants further investigation for possible password guessing or brute-force activity.

Alert 2 — Administrator Account

* Source IP: 203.0.113.45
* Failed login attempts: 8
* Severity: Medium
* Simulated event time: 09:05 AM

The administrator account exceeded the Medium-severity threshold. Because this is a privileged account, the alert deserves careful review even though its count is below the High threshold.

*5. Recommended Incident Response*

1. Review supporting authentication logs and verify the event timestamps.
2. Determine whether the affected accounts experienced successful logins.
3. Check source IP reputation and related authentication activity.
4. Notify the security team and account owners as appropriate.
5. Apply account protection measures, such as multifactor authentication and rate limiting.
6. Escalate confirmed suspicious activity according to the organization’s incident response procedures.
7. Document investigation findings and outcomes.

*6. Limitations*

This exercise uses manually constructed data with aggregate failed-login counts and assigned timestamps. The alerts are not derived from live authentication events. The findings do not establish that an account was compromised or that a brute-force attack occurred.

*7. Skills Demonstrated*

* Kusto Query Language (KQL)
* Azure Data Explorer
* Security alert classification
* Failed login detection
* SOC alert triage
* Incident investigation documentation
* Security event timeline sorting

*8. Conclusion*

This simulation demonstrates foundational SOC analyst skills in writing KQL queries, filtering security events, prioritizing alerts, and documenting recommended investigation steps.
