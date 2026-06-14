# MITRE ATT&CK Mapping

| Detection Name | SPL Query Purpose | MITRE Technique | Description |
|---|---|---|---|
| Encoded PowerShell | Detect obfuscated PowerShell commands | T1059.001 | PowerShell execution with encoded commands |
| Failed Login Attempts | Detect brute-force activity | T1110 | Multiple failed authentication attempts |
| PowerShell Execution | Detect PowerShell process activity | T1059 | Command execution through PowerShell |
| Network Connections | Monitor outbound connections | T1071 | Application layer protocol communication |
| Certutil Execution | Detect LOLBin abuse | T1218 | Signed binary proxy execution |
| CMD Spawning PowerShell | Detects cmd launching powershell | T1059 | Command and Scripting Interpreter |
| PowerShell Download Activity | Detects Ingress Tool Transfer | T1105 | PowerShell download activity - Invoke-WebRequest |
| Failed Logins Followed by Success | Detects Brute forcing | T1110 | Multiple Failed Logins Followed by Success login |
| PowerShell Network Activity | Detects PowerShell processes establishing network connections | T1059.001 | Correlates Sysmon Process Creation events |
| Suspicious Directory Execution | Detects executable files from user directories | T1204 | Monitors Sysmon Process Creation events |
| WMI Activity Detection | Detects Windows Management Instrumentation execution in cmd | T1047 | Monitors Sysmon execution of wmic.exe |
| Explorer to powershell | Detects Windows Explorer launching PowerShell | T1059.001 | Monitors Sysmon Process Creation events |
