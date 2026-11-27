# 02 Windows Security Log Analysis

## Overview
This section focuses on analyzing Windows Security Event Logs using Splunk. The objective was to investigate authentication activity, identify failed login attempts, understand Windows logon types, and develop a basic detection approach for suspicious login behavior.

## Objectives
- Understand Windows Security Event Logs.
- Analyze successful and failed authentication events.
- Investigate Event ID 4624 and Event ID 4625.
- Understand Windows logon types.
- Identify repeated failed login attempts.
- Create a basic detection search in Splunk.

## Tools Used
- Windows 11
- Splunk Enterprise
- Splunk Universal Forwarder
- Windows Security Event Logs

## Activities Performed

### 1. Windows Security Log Ingestion
Configured log collection and verified that Windows Security events were available in Splunk.

### 2. Failed Login Investigation — Event ID 4625
Analyzed failed login events to identify:
- Target username
- Source IP address
- Failure information
- Logon type
- Event timestamp

### 3. Successful Login Investigation — Event ID 4624
Examined successful authentication events and compared them with failed login activity.

### 4. Windows Logon Types
Studied common Windows logon types:

- Type 2 — Interactive logon
- Type 3 — Network logon
- Type 5 — Service logon
- Type 7 — Workstation unlock
- Type 10 — Remote Interactive logon

### 5. Failed Login Detection
Created a Splunk search to identify repeated failed login attempts against the lab account `SOC-Test-User`.

The detection grouped failed login events into five-minute time windows and identified windows containing three or more failures.

## Investigation Findings
- Successfully identified Windows failed login events (4625).
- Examined successful login events (4624).
- Investigated authentication details and logon types.
- Generated controlled failed login activity using the lab account.
- Created a threshold-based search for repeated authentication failures.

The observed activity was generated in a controlled lab environment. Repeated failed logins alone do not establish malicious activity; further investigation and correlation are required.

## Skills Demonstrated
- Windows Event Log Analysis
- Authentication Monitoring
- Splunk Search Processing Language (SPL)
- Failed Login Detection
- Security Event Investigation
- Basic Detection Engineering

## Conclusion
This exercise provided practical experience in Windows authentication monitoring and security log investigation. It demonstrated how a SOC analyst can use Windows Security Event Logs and Splunk to identify and investigate suspicious authentication patterns.
