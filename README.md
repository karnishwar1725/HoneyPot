# Honeypot Deployment and SIEM Analysis

## Overview
This project demonstrates the deployment of an SSH-based honeypot integrated with the Elastic Stack SIEM. The aim is to simulate real-world attacks and analyse attacker behaviour using log data.

## Architecture
The system consists of:
- Attacker VM (Windows)
- Honeypot VM (Ubuntu with OpenSSH)
- SIEM (Elastic Stack - Elasticsearch + Kibana)

## Features
- SSH brute-force attack simulation
- Log collection using journald
- SIEM ingestion and analysis
- Detection rules for:
  - Failed logins
  - Successful logins
  - Privilege escalation
- AI-assisted log analysis (MITRE ATT&CK mapping)

## Logs
Logs are collected using:

journalctl -u ssh
journalctl -t sudo


## SIEM
Logs are uploaded into Kibana and analysed using filters and dashboards.

## AI Enrichment
AI was used to:
- Summarise logs
- Identify threats
- Map to MITRE ATT&CK
- Extract IOCs

## Limitations
- Low-interaction honeypot
- Manual log ingestion
- No alert actions (Elastic paid feature)

## Future Improvements
- Use Cowrie honeypot
- Automate ingestion (Filebeat)
- Behaviour-based detection


## Author
Karnishwar Ravikrishna
