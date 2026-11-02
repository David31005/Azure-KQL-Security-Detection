Azure KQL Security Detection

SOC Analyst Cybersecurity Portfolio Project

Analyst: David Jeffries
Platform: Azure Data Explorer
Language: Kusto Query Language (KQL)

Project Overview

This project demonstrates how KQL can be used to analyze simulated authentication activity, identify excessive failed login attempts, classify security alert severity, and organize investigation results.

The project models common Security Operations Center (SOC) analyst responsibilities, including alert triage, security event analysis, and incident documentation.

Tools and Technologies

* Microsoft Azure Data Explorer
* Kusto Query Language (KQL)
* GitHub
* Simulated authentication data

Detection Rules

Failed Login Attempts	Alert Severity
10 or more	High
5–9	Medium
Fewer than 5	Low

Investigation Results

The KQL query identified two simulated alerts requiring review:

* High: Guest account — 12 failed login attempts
* Medium: Administrator account — 8 failed login attempts

The query excludes Low-severity events and sorts the remaining alerts chronologically.

Project Files

* KQL Failed Login Detection Query
* SOC Security Alert Investigation Report

Skills Demonstrated

* KQL query development
* Security event filtering
* Failed login detection
* Alert severity classification
* SOC investigation workflow
* Incident response recommendations
* Security documentation

Project Limitations

This is a training simulation using manually created authentication data. It does not represent a live production monitoring system or a confirmed cyberattack.

About the Analyst

David Jeffries
Cybersecurity Professional | Google Cybersecurity Professional Certificate

GitHub Profile

LinkedIn Profile
