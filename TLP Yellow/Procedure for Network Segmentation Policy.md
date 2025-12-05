---
draft: true
tags: ["TLP", "policies", "procedures"]
---

#

#

#

#

#

# Procedure for Network Segmentation Policy

Violet Figueroa

[Procedure Title    3](#procedure-title)

[TLP Classification    3](#tlp-classification)

[Purpose    3](#purpose)

[Steps    3](#steps)

[References and Citation    4](#references-and-citation)

#

# Procedure Title {#procedure-title}

Implementing and Maintaining Network Segmentation

# TLP Classification {#tlp-classification}

TLP: Yellow

# Purpose {#purpose}

To isolate IT systems from OT systems to prevent ransomware spread and protect critical operational technology, as outlined in the Network Segmentation Policy.

# Steps {#steps}

* **Configuring Network Segmentation**:
  * Use firewalls or VLANs to create isolated zones for IT and OT networks.
  * Ensure OT systems (e.g., navigation controls) have no direct internet access.
* **Restricting Access Between Networks**:
  * Grant access between IT and OT networks only to authorized personnel with a legitimate business need.
  * Require secure VPN connections with MFA for remote access to OT systems.
* **Monitoring Traffic Between Segments**:
  * Deploy Intrusion Detection Systems (IDS) or Intrusion Prevention Systems (IPS) to monitor traffic between network segments.
  * Investigate alerts triggered by anomalous traffic patterns immediately.
* **Auditing Network Segmentation**:
  * Conduct semi-annual audits of firewall rules, VLAN configurations, and segmentation policies.
  * Document findings in an audit report submitted to executive leadership.
* **Incident Response Activation**:
  * If ransomware is detected in any segment, isolate affected zones immediately following the Incident Response Playbook.

#

# References and Citation {#references-and-citation}

1. Network Segmentation Policy
2. Incident Response Playbook
