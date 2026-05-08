# Failed Login Detection

## Description
Detects failed authentication attempts on Windows systems.

## Detection Logic
Monitors Windows Security Event ID 4625.

## SPL Query
```spl
index=security_logs EventCode=4625
```

## MITRE ATT&CK Mapping
- Technique ID: T1110
- Technique Name: Brute Force
- Tactic: Credential Access

## Severity
Medium

## Data Source
- Windows Security Logs

## Expected Behavior
Displays failed login attempts.

## Possible False Positives
- User typing incorrect passwords
- Expired credentials

## Investigation Steps
- Review Account_Name
- Review Source_Network_Address
- Identify repeated failures