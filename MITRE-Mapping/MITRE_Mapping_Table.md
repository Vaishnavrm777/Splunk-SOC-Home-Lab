# MITRE ATT&CK Mapping

| Detection Name | SPL Query Purpose | MITRE Technique | Description |
|---|---|---|---|
| Encoded PowerShell | Detect obfuscated PowerShell commands | T1059.001 | PowerShell execution with encoded commands |
| Failed Login Attempts | Detect brute-force activity | T1110 | Multiple failed authentication attempts |
| PowerShell Execution | Detect PowerShell process activity | T1059 | Command execution through PowerShell |
| Network Connections | Monitor outbound connections | T1071 | Application layer protocol communication |
| Certutil Execution | Detect LOLBin abuse | T1218 | Signed binary proxy execution |