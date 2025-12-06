
#

#

#

#

#

# Procedure for Log Retention Policy

Violet Figueroa

[Procedure Title    3](#procedure-title)

[TLP Classification    3](#tlp-classification)

[Purpose    3](#purpose)

[Steps    3](#steps)

[References and Citation    4](#references-and-citation)

#

# Procedure Title {#procedure-title}

Log Collection, Retention, and Review

# TLP Classification {#tlp-classification}

TLP: Yellow

# Purpose {#purpose}

To securely retain system logs required for incident analysis, regulatory reporting, and operational monitoring, as outlined in the Log Retention Policy.

# Steps {#steps}

* **Collecting Logs**:
  * Configure all critical systems (e.g., servers, firewalls) to send logs to a centralized logging solution in real time.
  * Ensure logs include key details such as timestamps, user actions, and system changes.
* **Storing Logs Securely**:
  * Encrypt logs at rest within a centralized logging solution.
  * Restrict log access to authorized personnel only (e.g., Security Analysts).
* **Reviewing Logs Regularly**:
  * Use automated tools like Security Information and Event Management (SIEM) systems to review logs daily.
  * Investigate flagged anomalies immediately following Incident Response Playbook procedures.
* **Retaining Logs**:
  * Retain security-related logs for one year; general system logs are retained for six months unless otherwise specified by regulatory requirements.
* **Archiving or Deleting Logs**:
  * Archive older logs securely if still needed; delete expired logs using approved methods such as file overwriting or degaussing storage devices.
* **Incident Response Activation**:
  * Preserve relevant logs during incidents until investigations are complete per Incident Response Playbook guidelines.

#

# References and Citation {#references-and-citation}

1. Log Retention Policy
2. Incident Response Playbook
