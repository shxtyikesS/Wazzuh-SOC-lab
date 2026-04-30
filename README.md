# Wazzuh-SOC-lab
Enterprise-grade SIEM/XDR deployment using Wazuh 4.8. Focus on defensive security monitoring and threat detection.
## Technical Stack
- **Operating System:** Ubuntu Server
- **Platform:** Wazuh (Indexer, Server, and Dashboard)
- **Deployment Method:** Official Wazuh Installation Assistant
  
- ## Challenges & Troubleshooting
During the installation, I encountered several deployment hurdles:
- **Corrupted Script Downloads:** Resolved by performing a deep clean of `/etc/wazuh-*` directories and using the `--overwrite` flag.
- **Certificate Issues:** Fixed by utilizing the automated installation assistant to ensure proper cryptographic handshake between nodes

  

- ## 🛠️ Key Achievements
- Successful deployment of the "All-in-One" Wazuh stack.
- Configured system persistence to prevent VM suspension during heavy indexing tasks.
- Achieved a healthy status across all security modules.
