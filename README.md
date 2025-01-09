SOC Automation Project: Wazuh, Shuffle, and TheHive

Overview

This project demonstrates the creation of an automated Security Operations Center (SOC) workflow. Using tools like Wazuh, Shuffle, and TheHive, this project automates the detection, enrichment, and management of security events in a simulated honeynet environment hosted on Microsoft Azure.

Project Goals

- Build a mini honeynet to simulate real-world security events.
- Automate alert enrichment and incident creation using OSINT and workflows.
- Compare metrics before and after applying security controls to evaluate effectiveness.


Architecture

Components:

- Windows 10 Endpoint: Generates logs and sends them to Wazuh.
- Wazuh Manager: Collects and analyzes logs to generate alerts.
- Shuffle: Automates alert enrichment (e.g., IOC checks) and responsive actions.
- TheHive: Manages enriched alerts as cases for SOC analysts.
- Email Notifications: Sends alerts and updates to analysts for review.


Workflow

1. Log Collection:
- The Wazuh Agent installed on the Windows 10 machine sends logs to Wazuh Manager.
- Events include failed logins, suspicious IP traffic, and system errors.
  
2. Alert Processing:
- Wazuh Manager generates alerts for suspicious activities and forwards them to Shuffle.
- Shuffle enriches alerts with IOC data using OSINT (e.g., VirusTotal) and sends results to TheHive and email.
  
3. Incident Management:
- Enriched alerts are automatically created as cases in TheHive for further investigation and tracking.

4. Responsive Actions:
- Alerts trigger automated or manual responsive actions, such as blocking IPs or isolating endpoints.





Tools Used

- Wazuh: Log collection and alert generation.
- Shuffle: Automation of alert enrichment and incident workflows.
- TheHive: Incident case management.
- Microsoft Azure: Hosting the honeynet and virtual machines.
- Windows Event Logs & Syslog: Sources for security events.
- OSINT Tools (e.g., VirusTotal): Enriching IOCs for enhanced context.


Results
Significant reduction in security events and incidents after hardening the environment.
Improved SOC efficiency with automated workflows for alert enrichment and incident management.
Enhanced security posture by implementing private endpoints and strict NSGs.































