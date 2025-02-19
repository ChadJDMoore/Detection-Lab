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
- Splunk as the SIEM for log ingestion and analysis.
- Windows 10 VM for log generation and monitoring.
- Sysmon for detailed system activity logging.
- Kali Linux VM for attack simulation and testing.
- VirtualBox for virtualization

### Prerequisites
- Must have Splunk installed and properly configured on the Windows VM
   - Ensure Splunk Add-on for Sysmon app is downloaded
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

### 10. On the Windows 10 VM, disable Defender
   <img width="388" alt="image" src="https://github.com/user-attachments/assets/47636745-9d73-42f5-80de-e82b99636138" />

### 11. Go on Web Browser and download the malware from Kali Linux VM's server
   <img width="388" alt="image" src="https://github.com/user-attachments/assets/0c37b5f1-6bcd-4471-9f7e-94c56f92e1ec" />
   <div>
   <img width="388" alt="image" src="https://github.com/user-attachments/assets/cf75dff6-b5ea-4152-a475-6500c53ec392" />
   </div>

### 12. Locate the Malware in File Explorer and run it
   <img width="388" alt="image" src="https://github.com/user-attachments/assets/6a5dd6f0-fb62-462b-8cef-d6a451f40e8a" />

### 13. Use the Command Prompt with administrative privileges to see an established connection with the Kali Linux VM
   <img width="388" alt="image" src="https://github.com/user-attachments/assets/bce61766-4168-43e8-99fa-0b3864f5c2fc" />
   <div>
   <img width="388" alt="image" src="https://github.com/user-attachments/assets/4091317a-108f-42c6-90b1-7bafec393a25" />
   </div>

### 14. On the Kali Machine VM, verify a connection in the handler
   <img width="388" alt="image" src="https://github.com/user-attachments/assets/bc1aaeec-74e4-4fd7-a691-bfd90729e3c1" />

### 15. Establish a shell on the Windows 10 VM, via the handler on the Kali Linux VM
   <img width="388" alt="image" src="https://github.com/user-attachments/assets/bba9dee7-bc0d-434e-9638-8b6f1797031d" />

### 16. Generate telemetry via the established shell using commands
   <img width="388" alt="image" src="https://github.com/user-attachments/assets/1a4b0f12-956e-41a8-b750-4392836d36d1" />

### 17. Configure Splunk to ingest Sysmon logs
   <div>
   <img width="388" alt="image" src="https://github.com/user-attachments/assets/0244b473-e940-4886-8c9f-a8e199f7be49" />
   </div>
   The configuration was done prior to testing via a downloaded file

### 18. Restart the Splunk services
   <img width="388" alt="image" src="https://github.com/user-attachments/assets/188d2d84-48d7-4ea0-94ae-4fb5543f0b21" />

### 19. Open Splunk and create and index called "endpoint"
   <div>
   <img width="388" alt="image" src="https://github.com/user-attachments/assets/55f8e85d-6877-4ed7-92a7-3c21230e903d" />
   </div>
   This is done because the configuration of the configuration file, it make Splunk look into Windows Sysmon operational, take all the events from there and feed it into "index = enpoint" 

### 20. Start querying on Splunk
### 21. All the data from endpoint
   <img width="388" alt="image" src="https://github.com/user-attachments/assets/8cd7a926-173d-4b9a-b6bf-3018e0247bbc" />

### 22. Query the Kali Linux VM ip address
   <img width="388" alt="image" src="https://github.com/user-attachments/assets/259a51ca-24ba-46fc-b831-d7b6d6d116b3" />
   <div>
   <img width="388" alt="image" src="https://github.com/user-attachments/assets/7eb343ce-a74d-4795-8091-f40fc5b236ca" />
   </div>
   Questions to ask:
   <div></div>
              1) Should this machine be attempting to connect with our 4444 port?
   <div>
              2) What Machine is this?
   </div>
              3) Who's machine does it belong to?
   <div></div>

### 23. Query the Malware 
   <img width="388" alt="image" src="https://github.com/user-attachments/assets/ea8eb752-0461-4c3c-ae24-98363d7eb986" />

### 24. Further analyse the data from the Malware query, inspecting it's event codes
   <img width="388" alt="image" src="https://github.com/user-attachments/assets/15311476-f887-409a-9aaa-026ff07b3dbf" />

### 25. Click and analyse EventCode 1
   <img width="388" alt="image" src="https://github.com/user-attachments/assets/561ed143-9a97-4207-b845-59f2dc9fc1be" />

### 26. Expand the event and analyse
   <img width="388" alt="image" src="https://github.com/user-attachments/assets/58fc0781-6a57-44f4-b459-b0f270766ed2" />
   <div>
   <img width="388" alt="image" src="https://github.com/user-attachments/assets/1c590baa-5321-4b89-8ee5-892ec7cc029c" />
   </div>


### 27. Use the process_id or process_guid to query and examine the data to see what the Command Prompt had done
   <img width="388" alt="image" src="https://github.com/user-attachments/assets/19f3fffd-0786-4b62-aaee-bbd3bb1d7584" />


## Recommendations 
Create detections to alert analysts, the next time a similar activity occurs 



