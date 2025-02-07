# Detection Lab

## Objective

The Detection Lab project aimed to establish a controlled environment for simulating and detecting cyber attacks. The primary focus was to ingest and analyze logs within a Security Information and Event Management (SIEM) system, generating test telemetry to mimic real-world attack scenarios. This hands-on experience was designed to deepen understanding of network security, attack patterns, and defensive strategies.

### Skills Learned

- Advanced understanding of SIEM concepts and practical application.
- Proficiency in analyzing and interpreting network logs.
- Ability to generate and recognize attack signatures and patterns.
- Enhanced knowledge of network protocols and security vulnerabilities.
- Development of critical thinking and problem-solving skills in cybersecurity.

### Tools Used
- Splunk for log ingestion and analysis.
- Windows 10 VM for log generation and monitoring.
- Sysmon for detailed system activity logging.
- Kali Linux VM for attack simulation and testing.
- VirtualBox for virtualization

### Prerequisites
- Must have Splunk installed and properly configured on the Windows VM
- Must have Sysmon installed and properly configured on the Windows VM
- Must have the virtual machines properly configured before testing

## Steps
### 1. Obtain the ip address of the Kali Linux machine via the terminal
### 2. Use Nmap to scan for open ports on the target machine (Windows 10 VM).
### 3. Create malware with Metasploit’s msfvenom for a reverse TCP shell.
### 4. Analyze generated telemetry using Splunk and Sysmon.
