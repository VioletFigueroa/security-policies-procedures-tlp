---
draft: true
tags: ["TLP", "policies", "procedures"]
---

#

#

#

#

#

# Procedure for Backup Policy

Violet Figueroa

[Procedure Title    3](#procedure-title)

[TLP Classification    3](#tlp-classification)

[Purpose    3](#purpose)

[Steps    3](#steps)

[References and Citation    4](#references-and-citation)

#

# Procedure Title {#procedure-title}

Backup Creation, Storage, and Restoration

# TLP Classification {#tlp-classification}

TLP: Yellow

# Purpose {#purpose}

To ensure regular backups of critical systems are securely stored and can be restored promptly in case of ransomware attacks or other disruptions, as outlined in the Backup Policy.

# Steps {#steps}

* **Creating Backups**:
  * Schedule nightly backups for critical systems using backup software.
  * Perform full backups weekly and incremental backups daily.
* **Storing Backups**:
  * Store one encrypted copy onsite in a secure server room with restricted access.
  * Store one encrypted offsite backup in a cloud-based solution with offline storage capabilities.
* **Testing Backups**:
  * Conduct quarterly restoration tests on random backup files to verify data integrity and recovery processes.
  * Document test results in backup logs for audit purposes.
* **Restoring Backups**:
  * Identify affected systems during an incident and isolate them from the network.
  * Restore data from clean backups following Incident Response Playbook procedures.
  * Test restored systems before reconnecting them to production environments.
* **Updating Backup Configurations**:
  * Review backup configurations annually or after major system changes to ensure they meet business needs.

#

# References and Citation {#references-and-citation}

1. Backup Policy
2. Incident Response Playbook
