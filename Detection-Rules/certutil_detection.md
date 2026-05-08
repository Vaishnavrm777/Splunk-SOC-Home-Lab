# Certutil Execution Detection

## Description
Detects execution of certutil.exe, commonly abused as a LOLBin.

## Detection Logic
Monitors Sysmon process creation events for certutil.exe.

## SPL Query
```spl
index=sysmon_logs EventCode=1 Image="*certutil.exe"
```

## MITRE ATT&CK Mapping
- Technique ID: T1218
- Technique Name: Signed Binary Proxy Execution
- Tactic: Defense Evasion

## Severity
High

## Data Source
- Sysmon Event ID 1

## Expected Behavior
Detects certutil process executions.

## Possible False Positives
- Certificate management operations
- Administrative tasks

## Investigation Steps
- Review command-line arguments
- Check downloaded files
- Identify destination URLs

## Simulation Notes

A test execution of certutil.exe was attempted to simulate LOLBin abuse. Microsoft Defender blocked the execution before full telemetry generation, demonstrating endpoint protection behavior against suspicious binary usage.