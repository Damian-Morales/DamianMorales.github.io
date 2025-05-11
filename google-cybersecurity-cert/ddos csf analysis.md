# DDoS Incident Report with NIST CSF Analysis

## Summary of the Security Event

A multimedia company that offers web and graphic design services experienced a Distributed Denial of Service (DDoS) attack targeting its internal network. The attack involved a flood of incoming ICMP packets that overwhelmed the company’s infrastructure and caused a complete network outage for approximately two hours. The organization’s network stopped responding to internal requests and could not access any services or resources.

The incident response team mitigated the attack by blocking ICMP traffic and shutting down all non-critical services. Once the traffic flow was stabilized, critical network services were gradually restored. The malicious actor exploited an unconfigured firewall rule, allowing unsolicited ICMP packets to enter the network.

## Identify: Type of Attack and Systems Affected

The attack was identified as a DDoS attack, specifically using a flood of ICMP ping requests to overwhelm the network. This attack exploited the network’s perimeter defenses, particularly a misconfigured firewall that failed to filter external ICMP traffic.

Affected systems included:

- Network routers and switches, which became overwhelmed by traffic
- Internal application servers that could not be reached
- User devices are unable to connect to internal or external services

The lack of source IP filtering and monitoring allowed the attacker to bypass the firewall protections and was able to successfully attack.

## Protect: Immediate Action Plan

Following the incident, the cybersecurity team implemented the following protections:

- Configured a new firewall rule to block incoming ICMP packets from external sources
- Enabled source IP address verification to help detect and prevent IP spoofing
- Deployed enhanced intrusion detection/prevention systems (IDS/IPS) to flag abnormal ICMP traffic
- Conducted a full audit of perimeter security controls.

These measures aim to reduce exposure to similar attacks and mitigate vulnerabilities.

## Detect: Monitoring Methods

To improve early detection of similar threats, the organization implemented continuous monitoring solutions, including:

- Network traffic analysis tools to flag spikes in ICMP or other protocol-specific traffic
- Alerting systems
- Periodic firewall and IDS/IPS log reviews to identify malicious patterns
- Enhanced system performance monitoring to catch traffic anomalies before systems become unresponsive

These tools help the organization quickly detect early signs of a DDoS or related attack.

## Respond: Response Strategy

In response to the event, the security team executed the following actions:

- Immediately blocked ICMP traffic at the firewall
- Took the network offline to prevent further damage and stabilize system behavior
- Communicated with stakeholders and issued an internal alert explaining the situation
- Reviewed and updated the incident response playbook to include steps for handling future ICMP-flood DDoS events

## Recover: Restoration and Post-Incident Steps

After the attack, the team:

- Restored normal traffic flow and re-enabled internal services in a phased manner
- Reviewed system logs and firewall changes to ensure the vulnerability was fully addressed
- Notified affected internal teams of system status and reinforced security awareness training
- Scheduled recurring reviews of firewall rules and IDS/IPS configurations to prevent future oversights

---

[← Back to Portfolio](./index.md)
