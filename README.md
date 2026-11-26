# SOC Project 1 – SIEM Log Monitoring & Threat Detection

## Project Overview

This project demonstrates a practical Security Operations Center (SOC) workflow using Splunk, Sysmon, Windows Event Logs, and security monitoring techniques.

The objective was to build a hands-on SOC lab to collect, monitor, investigate, and analyse security events, create detection rules, and develop a security monitoring dashboard.

## Lab Environment

| Component | Details |
|---|---|
| Host Operating System | Windows 11 |
| Virtualization | Oracle VirtualBox |
| SIEM Platform | Splunk |
| Endpoint Monitoring | Sysmon |
| Log Collection | Splunk Universal Forwarder |
| Investigation | Splunk Search Processing Language (SPL) |

## Project Activities

### 1. Splunk Setup and Log Ingestion
- Installed and configured Splunk.
- Installed Splunk Universal Forwarder.
- Configured Windows event log collection.
- Forwarded endpoint logs to Splunk.
- Verified successful log ingestion.

### 2. Windows Security Log Analysis
- Investigated Windows Security Event Logs.
- Analysed successful and failed login events.
- Studied Event ID 4624 and Event ID 4625.
- Investigated logon types and authentication activity.
- Created a failed-login detection search.

### 3. Sysmon and Process Monitoring
- Installed and configured Sysmon.
- Monitored process creation events.
- Investigated PowerShell execution.
- Analysed parent-child process relationships.
- Examined process command-line activity.

### 4. Network and File Activity Investigation
- Analysed Sysmon Event ID 3 (Network Connection).
- Investigated Sysmon Event ID 11 (File Creation).
- Monitored external network connections.
- Performed reverse DNS investigations.
- Examined application network activity.

### 5. Detection Engineering and SOC Dashboard
Created detection searches for:

1. Suspicious PowerShell execution.
2. Multiple failed login attempts.
3. Potentially suspicious external network connections.

Also:
- Built a SOC Security Monitoring Dashboard.
- Created visualizations for failed logins.
- Added a suspicious PowerShell monitoring panel.
- Added an external network connections panel.
- Prepared an incident investigation report.

## Detection Use Cases

| Detection | Data Source | Purpose |
|---|---|---|
| Suspicious PowerShell Execution | Sysmon Event ID 1 | Identify potentially suspicious PowerShell commands |
| Multiple Failed Login Attempts | Windows Event ID 4625 | Identify repeated authentication failures |
| Suspicious Network Connections | Sysmon Event ID 3 | Investigate potentially unusual external connections |

## SOC Dashboard

The dashboard includes:

- Failed Login Attempts Over Time
- Suspicious PowerShell Execution
- External Network Connections

## Investigation Findings

The lab generated controlled security events to test the detection searches.

The investigation identified repeated failed-login patterns, PowerShell commands matching selected indicators, and external network connections.

The examined activity was consistent with the controlled lab tests and ordinary application traffic. No confirmed malicious activity was established from the evidence analysed.

## Project Deliverables

- Splunk configuration and log ingestion.
- Windows Security Event Log investigation.
- Sysmon process monitoring.
- Network and file activity analysis.
- Three detection searches.
- SOC Security Monitoring Dashboard.
- Incident Investigation Report.
- Screenshots documenting the practical work.

## Skills Demonstrated

- SIEM Monitoring
- Splunk
- SPL
- Windows Event Log Analysis
- Sysmon
- Authentication Event Investigation
- PowerShell Monitoring
- Network Connection Analysis
- Security Detection Engineering
- SOC Alert Investigation
- Incident Documentation

## Conclusion

This project provided hands-on experience with SIEM-based security monitoring, endpoint telemetry, Windows authentication analysis, detection engineering, and SOC dashboard development.

It demonstrates practical foundational skills relevant to a SOC Analyst Level 1 role.