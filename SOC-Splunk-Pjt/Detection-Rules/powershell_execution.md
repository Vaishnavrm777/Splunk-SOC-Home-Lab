# PowerShell Execution Detection

## Description
Detects execution of PowerShell processes on the endpoint.

## Detection Logic
Monitors Sysmon process creation events for `powershell.exe`.

## SPL Query
```spl
index=sysmon_logs EventCode=1 Image="*powershell.exe"
```

## MITRE ATT&CK Mapping
- Technique ID: T1059
- Technique Name: Command and Scripting Interpreter
- Tactic: Execution

## Severity
Medium

## Data Source
- Sysmon Event ID 1

## Expected Behavior
Displays PowerShell process executions.

## Possible False Positives
- System administration activity
- Automation scripts

## Investigation Steps
- Inspect command-line arguments
- Identify parent process
- Verify user context