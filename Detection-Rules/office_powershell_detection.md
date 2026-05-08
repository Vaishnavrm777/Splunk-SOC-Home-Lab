# Office Spawning PowerShell Detection

## Description
Detects Microsoft Word spawning PowerShell processes, commonly associated with malicious macro activity.

## Detection Logic
Monitors PowerShell executions launched from WINWORD.EXE.

## SPL Query
```spl
index=sysmon_logs EventCode=1 ParentImage="*WINWORD.EXE" Image="*powershell.exe"
```

## MITRE ATT&CK Mapping
- Technique ID: T1204
- Technique Name: User Execution
- Tactic: Execution

## Severity
High

## Data Source
- Sysmon Event ID 1

## Expected Behavior
Triggers when Word launches PowerShell.

## Possible False Positives
- Administrative macro usage
- Internal automation documents

## Investigation Steps
- Review parent-child process chain
- Inspect command-line activity
- Identify document source