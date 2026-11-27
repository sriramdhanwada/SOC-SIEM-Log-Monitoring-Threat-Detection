# Detection Engineering and SOC Dashboard

## Overview
This section focuses on developing basic security detection searches and building a SOC monitoring dashboard using Splunk.

The objective was to identify potentially suspicious activity, investigate security events, visualize monitoring results, and document investigation findings.

## Objectives
- Develop detection searches using Splunk SPL.
- Identify suspicious PowerShell execution.
- Detect repeated failed login attempts.
- Investigate unusual external network connections.
- Build a SOC monitoring dashboard.
- Prepare an incident investigation report.

## Tools Used
- Splunk Enterprise
- Splunk Universal Forwarder
- Microsoft Sysmon
- Windows Security Event Logs
- Windows 11

## Detection Use Cases

### 1. Suspicious PowerShell Execution
Created a detection search using Sysmon Event ID 1 to identify command-line indicators such as:
- EncodedCommand
- FromBase64String
- DownloadString
- Invoke-WebRequest
- Invoke-Expression

### 2. Multiple Failed Login Attempts
Developed a threshold-based search using Windows Security Event ID 4625 to identify repeated failed authentication attempts within a five-minute window.

### 3. Suspicious Network Connections
Used Sysmon Event ID 3 to investigate external network connections and examine associated processes, destination IP addresses, and ports.

## SOC Dashboard

Created a Splunk dashboard titled **SOC Security Monitoring Dashboard**.

The dashboard includes:
- Failed Login Attempts Over Time
- Suspicious PowerShell Execution
- External Network Connections

## Incident Investigation Report
Prepared an incident investigation report documenting:
- Lab environment and methodology
- Detection use cases
- Investigation evidence
- Findings and assessment
- Recommendations
- Conclusion

## Investigation Findings
- Implemented three basic detection use cases.
- Created a centralized SOC monitoring dashboard.
- Investigated controlled test activity.
- Documented findings and recommendations.

The examined evidence did not establish confirmed malicious activity. Detection alerts require contextual investigation before being classified as true positives.

## Skills Demonstrated
- Detection Engineering
- Splunk SPL
- Security Monitoring
- Alert Investigation
- Dashboard Development
- Incident Documentation
- SOC Analysis

## Conclusion
This exercise demonstrated how a SOC analyst can develop basic detection logic, monitor security events through dashboards, investigate potentially suspicious activity, and document findings in an incident investigation report.
