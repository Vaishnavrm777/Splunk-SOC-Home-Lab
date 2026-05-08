# Encoded PowerShell Detection

## Description
Detects PowerShell commands executed with Base64 encoded arguments, commonly used for obfuscation and fileless attacks.

## Detection Logic
Monitors Sysmon Process Creation events for PowerShell executions containing the `-enc` argument.

## SPL Query
```spl
index=sysmon_logs EventCode=1 CommandLine="*-enc*"
```

## MITRE ATT&CK Mapping
- Technique ID: T1059.001
- Technique Name: PowerShell
- Tactic: Execution

## Severity
High

## Data Source
- Sysmon Event ID 1 (Process Creation)

## Expected Behavior
Triggers when encoded PowerShell commands are executed.

## Possible False Positives
- Administrative scripts
- Legitimate automation tools

## Investigation Steps
- Review CommandLine field
- Identify parent process
- Check executed user account
- Determine if external payloads were downloaded