# Centralized Log Monitoring and Threat Detection System using ELK Stack

## Overview
This project implements a centralized log monitoring and threat-detection environment using Elasticsearch, Logstash and Kibana (ELK). The project brief specifies Ubuntu as the ELK server, Windows as an endpoint using Winlogbeat, and Linux/Kali as an endpoint using Filebeat.

## Objectives
- Understand centralized logging and SIEM concepts.
- Deploy and configure ELK.
- Collect Windows and Linux logs using Beats.
- Analyze logs using KQL.
- Implement security monitoring use-cases.
- Create dashboards/visualizations.

## Architecture
Windows 10 -> Winlogbeat -> Ubuntu ELK Server -> Elasticsearch -> Kibana
Kali Linux -> Filebeat(planned) -> Ubuntu ELK Server -> Elasticsearch -> Kibana

## Components
- Ubuntu Server: ELK Server
- Windows 10: Windows Endpoint
- Kali Linux: Linux Endpoint / Attacker
- Winlogbeat: Windows Event Logs
- Filebeat: Linux auth.log and syslog
- Elasticsearch: Storage and search
- Logstash: Log processing
- Kibana: Visualization and KQL

## Security Use-Cases
1. Windows Failed Login Detection — Event ID 4625
2. Suspicious Successful Login — Event ID 4624 following failures
3. Linux SSH Login Monitoring
4. Linux File Integrity Monitoring

## Demonstrated Work
- VMs configured and running.
- Kali lab-network connectivity tested.
- Kibana Discover accessed.
- `winlogbeat-*` data view used.
- Windows Event ID 4624 successfully queried and inspected.
- KQL filtering demonstrated.
- Filebeat installation was attempted but Kali package installation was blocked by a network/DNS repository problem.

## Useful KQL
```text
event.code:4624
event.code:4625
event.code:(4624 or 4625)
```

## Repository Structure
ELK-Cybersecurity-Project/
├── README.md
├── Report/
   └── MAJOR PROJECT – NAVISHTHA.docx (including screenshots)




