<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="logo-lockup.svg">
    <img src="logo-lockup-light.svg" alt="Prosentriq" width="300">
  </picture>
</p>

# PROSENTRIQ: Autonomous Cyber-Immunity Platform

PROSENTRIQ is a modern, multi-layered host protection system designed to provide adaptive immunity against network threats. It leverages the power of Linux eBPF for efficient, kernel-level monitoring and combines advanced detection techniques to identify and neutralize threats in real-time. PROSENTRIQ is not just another firewall; it is an autonomous, self-healing security platform designed for the modern era of cyberattacks.

Traditional firewalls are like security guards with a list of known criminals; they are excellent at stopping threats we already know about. PROSENTRIQ, however, is designed to solve a much harder problem: detecting and neutralizing novel and zero-day attacks—the threats that have never been seen before.

At its core, PROSENTRIQ operates less like a static wall and more like a biological immune system for a server. It doesn't rely on a list of pre-defined rules. Instead, it learns, adapts, and evolves its own defenses in real-time based on what it observes.

This intelligence is built on three pillars:

1. It Learns "Normal"

Before protecting a system, PROSENTRIQ enters a learning phase. Using its NetworkBaseline and BehavioralPolicy components, it builds a sophisticated model of the server's normal operations:

    Network Baseline: It learns which network ports are normally used and what kind of traffic is expected.

    Process Behavior: It learns which applications are supposed to be running and which other servers they are allowed to communicate with.

Anything that deviates from this learned baseline is immediately considered a potential threat. This allows it to detect a "scan" not because of a rule, but because it's a massive, abnormal deviation from the learned behavior.

2. It Correlates Suspicious Events Over Time

PROSENTRIQ has a long-term memory, powered by its ThreatHistorian module and an internal SQLite database. This is crucial for detecting patient attackers. PROSENTRIQ can identify a pattern of seemingly minor, unrelated events and understand that they are part of a larger, coordinated attack campaign. For example, it can correlate:

    Day 1: A suspicious DNS query from an attacker.

    Day 4: A probe of a single, non-standard network port.

    Day 9: A single failed login attempt.

Individually, these events are low-threat. The ThreatHistorian allows PROSENTRIQ to see the whole picture, recognize the pattern, and dramatically increase the attacker's threat score based on their history.

3. It Sees Beyond the Network

A zero-day exploit might be so new that it gets past the initial network defenses. PROSENTRIQ anticipates this with its File Integrity Monitor (FIM).

    It monitors critical system directories for suspicious file changes.

    If an exploit successfully drops a backdoor file (e.g., backdoor.php) into a web directory, the FIM detects this instantly.

    Crucially, the AI engine correlates the file creation with the "last active IP address" seen by the ReputationEngine, correctly blaming the attacker for the new file and triggering a high-severity alert.

The "Self-Healing" Response

When the combined evidence from these modules pushes an attacker's threat score past a critical threshold, PROSENTRIQ doesn't just send an alert; it takes autonomous action.

    Evolving Defenses: The GeneticAlgorithm engine analyzes the threat and evolves a brand new, custom firewall rule specifically designed to neutralize it.

    Adaptive Response: The response is proportional to the threat. Based on the rule's final "fitness" score, the block can be adaptive—a minor threat might be blocked for an hour, while a critical, multi-stage attack can be locked out for a full day.

    Cross-Fleet Immunity: PROSENTRIQ is designed to operate as a "hive mind." Using its ThreatHubClient, it can report the signature of a new, confirmed zero-day attack to a central hub. This new intelligence can then be shared with all other PROSENTRIQ instances, making the entire fleet immune to the new attack almost instantly.

In essence, PROSENTRIQ is designed to function as a digital immune system. It learns the "self," identifies the "non-self," and creates custom "antibodies" to neutralize threats, constantly evolving to stay ahead of attackers.

---

## Features

PROSENTRIQ ships as a single commercial edition — there is no separate free/Community
tier. Every deployment gets the full feature set below (subject to the usage-based
plan on your account, see Pricing further down):

* **eBPF-Powered Monitoring**: High-speed packet and process monitoring.
* **Standard Heuristic Analysis**: Detects port scans, suspicious entropy, and protocol mismatches.
* **Public Threat Intelligence**: Ingests public threat feeds for baseline blocklisting.
* **Basic GeoIP Filtering**: Block traffic from known high-risk countries.
* **Web Dashboard**: Monitor system status and review detected events.
* **Manual Rule Management**: Manually create and manage custom firewall rules.
* **Honeypot**: Detects scans against decoy ports.

* 🎯 **Advanced Threat Intelligence**
    * **Collaborative Immunity**: All nodes share real-time threat data via the PROSENTRIQ Threat Hub, instantly protecting your entire fleet from an attack on a single node.
    * **Commercial Threat Feeds**: Integrates with premium feeds (e.g., Flashpoint, Recorded Future) for proactive defense.
    * **Real-time IOC Updates**: Pushes new indicators of compromise to all nodes every 15 minutes.

* 🤖 **AI-Powered Protection**
    * **Genetic Algorithm Rule Generation**: Automatically analyzes threats and evolves the most effective firewall rules, requiring no human intervention.
    * **Advanced Behavioral Profiling (UEBA)**: Learns normal application and user behavior to detect sophisticated anomalies and insider threats.
    * **Predictive Threat Modeling**: Identifies attack patterns *before* they result in a breach.
    * **Automated Incident Response**: Triggers playbooks to automatically isolate compromised hosts.

* 🏢 **Enterprise Management**
    * **Centralized Management Console**: Manage and monitor thousands of PROSENTRIQ nodes from a single pane of glass.
    * **Multi-Tenant Deployment**: Securely segment data and policies for different departments or customers.
    * **Role-Based Access Control (RBAC)**: Enforce granular permissions for security analysts and administrators.
    * **High Availability (HA)**: Deploys in a clustered configuration for mission-critical resilience.

* 📈 **Advanced Analytics & Reporting**
    * **Unlimited Data Retention**: Store forensic data indefinitely.
    * **Compliance Reporting**: Generate one-click reports for PCI DSS, HIPAA, and SOC2.
    * **Custom Dashboards & Widgets**: Build visualizations tailored to your team's needs.
    * **Forensic Timeline Analysis**: Visually investigate the full lifecycle of an attack.

* 🔌 **Enterprise Integrations**
    * **SIEM Integration**: Forward enriched event data to Splunk, Elastic, QRadar, and more.
    * **SOAR Platform Connectivity**: Integrate with Cortex XSOAR, Splunk SOAR, etc., for automated remediation.
    * **Alerting**: Send critical alerts to Slack, Microsoft Teams, and PagerDuty.
    * **Custom Webhook Support**: Connect PROSENTRIQ to any internal tool or API.

---

## Pricing

| Plan | Price (per node/month) | Key Features |
| :--- | :--- | :--- |
| **Trial** | **$0** | Full scoring & behavioral baselining, Structurally cannot block traffic, Upgrade to production anytime |
| **Production**| **$49/node/mo** | Everything in Trial, enforcement on, Genetic algorithm rule evolution, Threat Hub collective immunity, Compliance report generation |
| **Enterprise** | **Custom** | Volume pricing per node, Dedicated Threat Hub instance, On-prem / air-gapped install path, SLA & priority support |

*All plans include 24/7 support, managed threat intelligence updates, and regular security patches.*s

For detailed instructions on installation and usage, please see **[INSTALL.md](INSTALL.md)** and **[USAGE.md](USAGE.md)**.

---

## License

PROSENTRIQ is proprietary, commercially licensed software. There is no free/open-source
("Community") edition and no AGPL or other open-source license applies to any part
of this codebase — the entire product is a single commercial edition.

See [LICENSE](LICENSE) for the full commercial license terms. For licensing
inquiries, contact `sales@prosentriq.com`.
