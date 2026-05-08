# Security Event Distribution

## Purpose
Shows frequency of Windows security events.

## SPL Query
```spl
index=security_logs
| stats count by EventCode
```