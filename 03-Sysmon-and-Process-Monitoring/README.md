# 03 Sysmon and Process Monitoring

## Overview
This section focuses on monitoring Windows process activity using Microsoft Sysmon and investigating process execution events through Splunk.

The objective was to understand how processes are created, how parent and child processes interact, and how suspicious command-line activity can be investigated by a SOC analyst.

## Objectives
- Understand Sysmon and its role in endpoint monitoring.
- Analyze Sysmon Event ID 1 (Process Creation).
- Analyze Windows Security Event ID 4688 (Process Creation).
- Investigate process names and executable paths.
- Examine parent-child process relationships.
- Analyze PowerShell execution activity.
- Use Splunk to investigate endpoint events.

## Tools Used
- Windows 11
- Microsoft Sysmon
- Splunk Enterprise
- Splunk Universal Forwarder
- Windows Event Viewer
- PowerShell

## Activities Performed

### 1. Sysmon Configuration
Configured Sysmon and verified that its operational events were being generated and collected.

### 2. Process Creation Monitoring
Analyzed Sysmon Event ID 1 to investigate:
- Process image
- Process ID
- Parent process
- Parent process ID
- Command line
- User account
- Process creation timestamp

### 3. Windows Security Process Creation Monitoring
Analyzed Windows Security Event ID 4688 to investigate process creation activity, including the newly created process and its parent process.

### 4. PowerShell Investigation
Examined PowerShell execution events and reviewed command-line information to understand process behavior.

### 5. Parent-Child Process Analysis
Investigated relationships between parent and child processes to understand process execution chains and identify activity requiring further investigation.

### 6. Process Activity Analysis in Splunk
Used Splunk searches to filter, examine, and correlate Sysmon process creation events.

## Investigation Findings
- Successfully collected Sysmon process creation events.
- Identified process names and executable paths.
- Examined parent-child process relationships.
- Investigated PowerShell command-line activity.
- Practiced identifying process behavior that may require additional investigation.
- Analyzed Windows Security Event ID 4688 for process creation activity.

## Skills Demonstrated
- Endpoint Monitoring
- Sysmon Event Analysis
- Process Investigation
- PowerShell Activity Analysis
- Parent-Child Process Analysis
- Splunk SPL
- Security Event Investigation
- Windows Security Event Log Analysis

## Conclusion
This exercise provided practical experience in Windows endpoint monitoring using Sysmon. It demonstrated how process creation events and command-line information can help SOC analysts investigate suspicious endpoint activity.
