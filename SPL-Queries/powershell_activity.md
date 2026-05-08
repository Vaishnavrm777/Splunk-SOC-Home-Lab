# PowerShell Activity

## Purpose
Monitors PowerShell execution events.

## SPL Query
```spl
index=sysmon_logs EventCode=1 Image="*powershell.exe"
```