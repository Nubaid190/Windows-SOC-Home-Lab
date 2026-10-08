# Windows SOC home lab - Endpoint monitoring

## Project overview
This project demonstrates how windows security event logs can be used to monitor endpoint activity and investigate process execution

I created a windows 10 virtual machine using VMware workstation to gain hands-on experience with security monitoring techniques used by SOC analysts. 

## Tool and technologies
- Windows 10 pro
- VMware workstation pro
- Windows event viewer
- PowerShell
- Windows group policy

## Lab objectives 
- Configure windows security auditing
- Enable process creation monitoring
- Capture command-line activity
- Generate windows security event ID 4688
- Investigate process execution events

## Lab setup
1. Created a windows 10 pro virtual machine using VMware workstation
2. Configured the virtual machine with NAT networking
3. Enabled audit process creation through windows group policy
4. Enabled command-line logging for process creation events
5. Opened windows event viewer to monitor security logs

## Testing and investigating
Executed several test commands within windows PowerShell to generate process creation events, then investigated the resulting event ID 4688 logs using windows event viewer

- 'whoami'
- 'systeminfo'
- 'ipconfig'

## Key findings
- Event ID 4688 records windows process creation activity
- Command-line auditing provides additional context about executed commands
- Process creation logs can help SOC analysts investigate potentially suspicious activity
- Individual events should be assessed alongside other evidence before determining whether activity is malicious

## Skills demonstrated 
- Windows endpoint monitoring
- Security event log analysis
- Windows auditing configuration
- Process investigation
- Security investigation documentation

## Future improvements
- Simulate suspicious activity within the isolated lab
- Introduce a SIEM for centralised log monitoring
- Develop detection rules for suspicious process execution
