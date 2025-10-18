# Home SOC: Wazuh SIEM + Sysmon Telemetry

This project demonstrates how to build a home-based Security Operations Center (SOC)
using the open-source Wazuh SIEM and Windows Sysmon for endpoint telemetry.

## Objectives
- Deploy Wazuh all-in-one with Docker on Ubuntu.
- Connect a Windows endpoint configured with Sysmon.
- Collect and visualize telemetry in Wazuh.
- Write custom detection rules (e.g., encoded PowerShell, user enumeration).
- Investigate alerts and document incidents.

## Folder Layout
home-soc-wazuh-sysmon/
├─ docs/
├─ wazuh/
├─ endpoint/
├─ rules/
└─ screenshots/

## Portfolio Page
The live project write-up will be available at:
[Home SOC Project Page](../home-soc-wazuh-sysmon.html)

## Architecture Overview
The Home SOC environment consists of:

- **Ubuntu VM (Wazuh Server):** Runs Wazuh Manager, Indexer, and Dashboard using Docker.
- **Windows Endpoint:** Runs the Wazuh Agent with Sysmon for telemetry collection.
- **Network:** The agent forwards security event logs to the Wazuh Manager via port 1514/udp and management channel 1515/tcp.
- **Dashboard:** Provides visualization, rule configuration, and alerting.

![Architecture Diagram](docs/architecture.png)
