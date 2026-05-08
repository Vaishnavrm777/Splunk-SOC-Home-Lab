# Top Executed Processes

## Purpose
Displays the most frequently executed processes.

## SPL Query
```spl
index=sysmon_logs EventCode=1
| top Image limit=10
```