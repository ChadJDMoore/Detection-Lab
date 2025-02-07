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
- Ensure the networking of both virtual machines are properly configured before testing

## Steps
### 1. Turn off the firewalls on the Windows VM
   <img width="388" alt="image" src="https://github.com/user-attachments/assets/e29efdec-9743-4dae-8e71-773ffcb23759" />

### 2. Obtain the ip address of the Kali Linux VM
   <img width="388" alt="image" src="https://github.com/user-attachments/assets/f9e090e9-9003-4063-808a-ddfc9ebc5793" />

### 3. Use nmap on Kali Linux VM to target the Windows VM
   <img width="388" alt="image" src="https://github.com/user-attachments/assets/83017e8f-95b6-4a15-998f-3920bbf0cd0d" />

### 4. Create basic malware using msfvenom
   <img width="388" alt="image" src="https://github.com/user-attachments/assets/72bee508-918b-4dce-91c2-ec375a8ad8b5" />

### 5. Open up a handler to listen to the port that was configured in the malware
   <img width="388" alt="image" src="https://github.com/user-attachments/assets/b48173b1-fcaa-408a-9ff5-2aebaa332bfe" />

### 6. Set payload option in the handler to the exact payload use for the malware
   <img width="388" alt="image" src="https://github.com/user-attachments/assets/98d34d0b-5468-4559-a91f-0dc25478fd41" />
   <div>
   <img width="388" alt="image" src="https://github.com/user-attachments/assets/142e8a3d-75c2-4da4-8181-a4f0d079a084" />
   </div>

### 7. Set LHOST to the Kali Linux VM's ip address
   <img width="388" alt="image" src="https://github.com/user-attachments/assets/3573fbdf-affa-4bc3-9883-ef1673fce096" />
  
### 8. Start the handler to initiate exploiting
   <img width="388" alt="image" src="https://github.com/user-attachments/assets/2890d9ea-1c8e-474e-b88e-9e64fb1c8e78" />

### 9. Set up a HTTP Server on the Kali Linux VM
  <div>
  <img width="388" alt="image" src="https://github.com/user-attachments/assets/e25166ab-c7f6-4c95-92b3-b6da172943d0" />
  </div>
This is done so the test/Windows 10 VM can download the malware

### 10. 
### 11.
### 12.
### 13.
### 14.
### 15.
### 16.
### 17.
### 18.
### 19.
### 20.

