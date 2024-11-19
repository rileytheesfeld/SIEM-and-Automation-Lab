# SIEM-and-Automation-Lab
I'm wanting to learn more about threat detection and incident response. I wanted to teach myself how to build up a mock SoC, with EDR, SIEM,and SOAR implementation. 

## Goals
  1. Teach myself how to deploy and manage a small scale "simulated" threat detection and incident response engineering infrastructure.
  2. Deploy default detections, custom detections, maintain detection lifecycles while collecting data from threat feeds, custom honeypots, and a simulated threat environment.

At the end of this lab I would like to experience what a security engineer might deal with on an average day. The way I plan on building this is through utilization of different networking, virtualization, and open-source technologies. This is the beginning of a larger scale implementation I plan to create down the line with this as a foundation.

# The SIEM-and-Automation-Lab Topology
![Screenshot 2024-11-16 163934](https://github.com/user-attachments/assets/b8e2342c-e1d0-4bf6-8f1d-2901c2b2f49d)


## Project Breakdown / Key Technologies
Starting from my computer to splunk, here is an overview of the technologies utilized in the project.
  - **Proxmox:** Virtualization platform that was utilized for this lab, all built on my HPE DL380p server.
  - **Personal Computer:** My computer that is used to interface with the infrastructure. Login, configuration, and management are handled from this endpoint.
  - **Detection Generator:** Leveraging Red Canary's Atomic Red Team and MITRE's Caldera Automated Adversary Emulation Platform for pre-developed attacks. Utilizing the MITRE ATT&CK framework, deploys common "red team" attacks on a Windows 11 VM. Installed FlareVM for Malware Analysis and Reverse Engineering.
  - **Wazuh:** Open-source XDR and SIEM application used to ingest data from the endpoint. Used only to as ingress to then be forwarded to splunk enterprise.
  - **Splunk Enterprise:** Acts as the centralized SIEM system to monitor, query, and build alerts based on logs, also forwards logs to splunk soar for automation tasks.
  - **Splunk SOAR:** The security orchestration, automation, and response platform to detect and remediate any threats.

*Wazuh, and Splunk Enterprise were built on Ubuntu Server 22.04. Splunk SOAR was built on CentOS 8.


## Center on the SIEM capabilities
A central part of the goals I have set for this project is becoming proficient in SIEM parsing and alerting. I plan on starting with Splunk as it is the most popular SIEM system in the industry right now. I also want to learn to read and write playbooks using splunks SOAR solution. 


## Skills improved from this project
  - Data analysis and log analysis
  - Working knowledge and implementation of attack tactics, techniques and procedures. (TTPs)
  - Parsing necessary details when looking for TTPs

## Future plans for this lab
I plan on expanding this lab into the cloud with a wider surface area and more log ingestion. I plan on adding a honey-net, Metasploitable, and DVWP into the Cloud in Azure. Install the wuzah agent on all of these and forward these logs into Splunk. I will then take those logs and create automation tasks in SOAR to be able to automatically detect and defend against these attacks. I will be documenting these changes as they come in the future.
