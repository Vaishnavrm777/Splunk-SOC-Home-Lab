# SOC SIEM Lab using Splunk and Sysmon

## Project Overview

This project demonstrates the implementation of a Security Operations Center (SOC) home lab using Splunk Enterprise, Sysmon, and Windows Event Logs.

## Project Highlights

* 14 Active Detections
* 2 Correlation-Based Detections
* MITRE ATT&CK Mapping
* Sysmon Event Monitoring
* Splunk Alerting
* Detection Coverage Tracking
* Threat Hunting Workflows
* Behavioral Detection Engineering

The environment collects Windows and Sysmon telemetry through Splunk Universal Forwarder and analyzes the data using SPL queries and SOC detections.


## Architecture Diagram

![SOC Architecture](Architecture/soc_architecture.png)


## Tools & Technologies

- Splunk Enterprise
- Splunk Universal Forwarder
- Sysmon
- Windows Event Logs
- SPL (Search Processing Language)
- MITRE ATT&CK Framework


## Data Sources

| Data Source | Description |
|---|---|
| Windows Security Logs | Authentication and login events |
| Windows System Logs | System-level events |
| Sysmon Event ID 1 | Process Creation |
| Sysmon Event ID 3 | Network Connections |


## Detection Rules

Implemented detections include:

- Encoded PowerShell Detection
- PowerShell Execution Monitoring
- Failed Login Detection
- Excessive Failed Login Detection
- Certutil LOLBin Detection
- Office Spawning PowerShell Detection
- Network Connection Monitoring

## Detection Coverage

Current Detection Library: 14 Detections

### Behavioral Detections

* CMD → PowerShell
* Explorer → PowerShell
* Office → PowerShell
* PowerShell Download Activity
* Suspicious User Directory Execution
* WMI Activity Detection

### Correlation Detections

* Failed Logins Followed by Success
* PowerShell + Network Activity

## MITRE ATT&CK Mapping

| Detection | Technique ID |
|---|---|
| Encoded PowerShell | T1059.001 |
| Failed Login Attempts | T1110 |
| Certutil Execution | T1218 |
| Network Connections | T1071 |


## SOC Dashboard Features

The Splunk dashboard includes:

- Failed login monitoring
- PowerShell activity visualization
- Top executed processes
- Outbound network connection tracking
- Security event distribution


## Key Learning Outcomes

Through this project I gained hands-on experience in:

- SIEM deployment and configuration
- Endpoint telemetry ingestion
- Detection engineering using SPL
- Sysmon configuration and monitoring
- Alert creation in Splunk
- Threat hunting workflows
- MITRE ATT&CK mapping
- Troubleshooting log ingestion and permission issues


## Future Improvements

Planned future enhancements include:

- Advanced threat simulations
- Additional Sysmon detections
- Sigma rule integration
- Threat intelligence enrichment
- Automated alert actions
- Multi-endpoint log collection


## Screenshots

## Dashboard Preview

![Dashboard](Screenshots/Dashboard/dashboard_overview.png)

## Detection Example

![Dashboard](Screenshots/Detections/encoded_powershell_alert.png)

## Sysmon Telemtery Example

![Dashboard](Screenshots/Sysmon/sysmon_operational_logs.png)
