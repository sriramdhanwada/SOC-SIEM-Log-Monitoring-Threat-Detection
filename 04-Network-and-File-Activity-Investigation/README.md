# 04 Network and File Activity Investigation

## Overview
This section focuses on investigating network connections and file activity on a Windows endpoint using Microsoft Sysmon and Splunk.

The objective was to understand how endpoint network connections and file creation events can help SOC analysts identify unusual activity.

## Objectives
- Analyze Sysmon Event ID 3 (Network Connection).
- Analyze Sysmon Event ID 11 (File Creation).
- Identify external network connections.
- Investigate destination IP addresses and ports.
- Perform reverse DNS lookups.
- Use Splunk to investigate network and file activity.

## Tools Used
- Windows 11
- Microsoft Sysmon
- Splunk Enterprise
- Splunk Universal Forwarder
- PowerShell
- Command Prompt

## Activities Performed

### 1. Sysmon Configuration
Verified Sysmon configuration and confirmed that network connection and file creation events were being collected.

### 2. Network Connection Monitoring — Event ID 3
Investigated Sysmon network connection events and examined:
- Process image
- Source IP address
- Destination IP address
- Source port
- Destination port
- Protocol
- Connection timestamp

### 3. File Creation Monitoring — Event ID 11
Analyzed file creation events to identify which processes created files and where those files were created.

### 4. External Network Connection Investigation
Used Splunk to identify external network connections and examine associated processes, destination IP addresses, and ports.

### 5. Reverse DNS Investigation
Performed reverse DNS lookups to investigate destination IP addresses and understand the associated hostname information when available.

## Investigation Findings
- Successfully analyzed Sysmon Event ID 3 network connection events.
- Investigated Sysmon Event ID 11 file creation events.
- Identified external network connections.
- Examined destination IP addresses and ports.
- Practiced reverse DNS investigation.

Network connections were assessed using available endpoint telemetry. An external connection alone does not establish malicious activity.

## Skills Demonstrated
- Network Traffic Investigation
- Sysmon Event Analysis
- File Activity Monitoring
- External IP Investigation
- Reverse DNS Lookup
- Splunk SPL
- Endpoint Security Monitoring

## Conclusion
This exercise provided practical experience in investigating endpoint network connections and file activity. It demonstrated how Sysmon telemetry and Splunk can help SOC analysts investigate potentially suspicious endpoint behavior.
