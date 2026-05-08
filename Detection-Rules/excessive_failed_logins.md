# Excessive Failed Login Detection

## Description
Detects potential brute-force attempts through repeated failed logins.

## Detection Logic
Counts failed login attempts grouped by account and source IP.

## SPL Query
```spl
index=security_logs EventCode=4625
| stats count by Account_Name Source_Network_Address
| where count > 5
```

## MITRE ATT&CK Mapping
- Technique ID: T1110
- Technique Name: Brute Force
- Tactic: Credential Access

## Severity
High

## Data Source
- Windows Security Logs

## Expected Behavior
Triggers when multiple failed logins exceed threshold.

## Possible False Positives
- Users forgetting passwords
- Misconfigured applications

## Investigation Steps
- Identify targeted accounts
- Review source IP addresses
- Check for successful follow-up logins