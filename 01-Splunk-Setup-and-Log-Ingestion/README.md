# 01 – Splunk Setup and Log Ingestion

## Objective

The objective of this task was to set up a basic SIEM environment using Splunk and configure log collection from a Windows endpoint.

This exercise focused on understanding how security logs are collected, forwarded, indexed, and monitored in a SIEM platform.

## Lab Environment

| Component | Details |
|---|---|
| Host Operating System | Windows 11 |
| SIEM Platform | Splunk Enterprise |
| Log Forwarding Tool | Splunk Universal Forwarder |
| Endpoint Monitoring | Windows Event Logs and Sysmon |
| Virtualization | Oracle VirtualBox |
| Endpoint | Local Windows Machine |

## Tools Used

- Splunk Enterprise
- Splunk Universal Forwarder
- Windows Event Viewer
- Sysmon
- Windows PowerShell

## Tasks Performed

### 1. Splunk Installation and Setup
- Installed and configured Splunk Enterprise.
- Accessed the Splunk Web Interface.
- Explored the Search & Reporting application.
- Understood the basic SIEM workflow.

### 2. Splunk Universal Forwarder Installation
- Installed Splunk Universal Forwarder on the Windows machine.
- Configured the Universal Forwarder service.
- Verified that the SplunkForwarder service was running.
- Configured forwarding to the Splunk receiving port 9997.

### 3. Log Collection Configuration
- Configured Windows event log collection.
- Added Sysmon Operational event log monitoring.
- Configured the input settings using `inputs.conf`.
- Enabled XML event rendering for Sysmon logs.

### 4. Log Ingestion Verification
- Verified that Windows and Sysmon events were being forwarded to Splunk.
- Used Splunk Search & Reporting to search collected events.
- Confirmed successful communication between the Universal Forwarder and Splunk.

## Configuration Details

The Universal Forwarder was configured to forward events to:

`127.0.0.1:9997`

The Sysmon input configuration included:

```ini
[WinEventLog://Microsoft-Windows-Sysmon/Operational]
disabled = 0
index = main
renderXml = true
```

## Key Learning Outcomes

- Understanding the purpose of a SIEM platform.
- Understanding the role of Splunk Universal Forwarder.
- Learning how endpoint logs are collected and forwarded.
- Understanding log ingestion and indexing.
- Learning basic Splunk Search & Reporting operations.
- Understanding the importance of centralized security monitoring.

## Evidence

Screenshots documenting the installation, configuration, log forwarding, and successful event ingestion are available in the `Screenshots` folder.

## Conclusion

Successfully established a basic SIEM lab environment using Splunk Enterprise and Splunk Universal Forwarder.

Verified that Windows and Sysmon security events were successfully collected and made available for investigation in Splunk.

This setup provides the foundation for further SOC monitoring, threat detection, and security event investigation.
