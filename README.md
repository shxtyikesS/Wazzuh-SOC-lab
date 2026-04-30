# Wazzuh-SOC-lab🛡️
![Wazuh](https://img.shields.io/badge/Wazuh-4.8-blue?style=flat-square&logo=wazuh)
![Linux](https://img.shields.io/badge/OS-Ubuntu_Server-E95420?style=flat-square&logo=ubuntu)
![Cybersecurity](https://img.shields.io/badge/Domain-Defensive_Security-red?style=flat-square)

Enterprise-grade SIEM/XDR deployment using Wazuh 4.8. Focus on defensive security monitoring and threat detection.
---
## Technical Stack
* **Operating System:** Ubuntu Server
* **Platform:** Wazuh (Indexer, Server, and Dashboard)
* **Deployment Method:** Official Wazuh Installation Assistant
---
## Challenges & Troubleshooting🛠️
During the installation, I encountered several deployment hurdles:
* **Corrupted Script Downloads:** Resolved by performing a deep clean of `/etc/wazuh-*` directories and using the `--overwrite` flag.
* **Certificate Issues:** Fixed by utilizing the automated installation assistant to ensure proper cryptographic handshake between nodes
---
## Key Achievements✅
* Successful deployment of the "All-in-One" Wazuh stack.
* Configured system persistence to prevent VM suspension during heavy indexing tasks.
* Achieved a healthy status across all security modules.
---
## Lab Process💻
* Health Status:
  
**The image below showcases the active Wazuh Dashboard after a successful all-in-one deployment. The environment is currently monitoring system events and is ready for agent registration**.
  
<img width="2462" height="1194" alt="Wazuh Dashboard Overview" src="https://github.com/user-attachments/assets/03b8a27d-4fc2-4007-827c-495d1ff66900" />

---
* Deploying new agent to Wazzuh:
  
  **The image below showcases the command used provided by wazzuh to add a new agent to Wazzuh server**
  
  <img width="1103" height="618" alt="DEPLOY NEW AGENT" src="https://github.com/user-attachments/assets/09791966-fa0f-4f55-afd3-b2ef6a10a453" />

## Agent Configuration & Log Ingestion
After the initial installation, I manually configured the Wazuh agent to establish a secure handshake with the manager and define which event logs should be monitored.
* **Manager Connection**
I modified the ossec.conf file located in the agent's installation directory to point towards the Ubuntu Server's IP address. This ensures that the agent knows exactly where to send the collected security data.

* **Event Log Monitoring**
To enhance visibility, I verified and updated the <localfile> blocks. This allows the SIEM to ingest critical logs from the Windows environment, such as:

System Logs: To track hardware and driver events.

Security Logs: Crucial for detecting failed login attempts and privilege escalation.

Application Logs: To monitor software-related errors or suspicious activities.


* First logs registrated with the new user agent added:
  
**The image below showcases the File Integrity Monitoring (FIM) dashboard capturing real-time events from the "EDUARDO-PC" agent. It demonstrates the SIEM's ability to detect file modifications, additions, and deletions within monitored directories, providing a detailed audit trail for security analysis.**

<img width="2467" height="1230" alt="FIRST LOGS IMPLEMENTED" src="https://github.com/user-attachments/assets/32fd791a-1156-4242-ae56-d4f6b44dde9a" />




