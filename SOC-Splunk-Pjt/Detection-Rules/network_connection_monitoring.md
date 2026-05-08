# Network Connection Monitoring

## Description
Monitors outbound network connections from processes on the endpoint.

## Detection Logic
Tracks Sysmon network connection events.

## SPL Query
```spl
index=sysmon_logs EventCode=3
```

## MITRE ATT&CK Mapping
- Technique ID: T1071
- Technique Name: Application Layer Protocol
- Tactic: Command and Control

## Severity
Medium

## Data Source
- Sysmon Event ID 3 (Network Connections)

## Expected Behavior
Displays processes making outbound connections.

## Possible False Positives
- Browsers
- Software updates
- Cloud applications

## Investigation Steps
- Review DestinationIp
- Review DestinationPort
- Identify suspicious processes