
#

#

#

#

#

# Ransomware Attack Incident Response Playbook

Violet Figueroa

[TLP Classification    3](#tlp-classification)

[Incident Overview    3](#incident-overview)

[Confidentiality, Integrity, Availability (C-I-A) Effect    3](#confidentiality,-integrity,-availability-\(c-i-a\)-effect)

[Team Members    3](#team-members)

[Cybersecurity Incident Response Team (CSIRT) Roles and Responsibilities    4](#cybersecurity-incident-response-team-\(csirt\)-roles-and-responsibilities)

[Team Collaboration    5](#team-collaboration)

[Escalation Triggers    6](#escalation-triggers)

[Internal and External Stakeholders    7](#internal-and-external-stakeholders)

[Internal Stakeholders    7](#internal-stakeholders)

[External Stakeholders    8](#external-stakeholders)

[Communication Guidelines    10](#communication-guidelines)

[Asset Classifications and Prioritizations    11](#asset-classifications-and-prioritizations)

[Company Data Classifications    11](#company-data-classifications)

[Categories of Assets/Devices That May Be Compromised    11](#categories-of-assets/devices-that-may-be-compromised)

[Prioritization of Assets    12](#prioritization-of-assets)

[Rationale for Prioritization    12](#rationale-for-prioritization)

[Protection Measures    13](#protection-measures)

[References and Citation    14](#references-and-citation)

#

# TLP Classification {#tlp-classification}

TLP: Red

# Incident Overview {#incident-overview}

Ransomware Attack on Ticketing System
Type: Ransomware

## Confidentiality, Integrity, Availability (C-I-A) Effect {#confidentiality,-integrity,-availability-(c-i-a)-effect}

* Confidentiality (C):
  * Customer Personally Identifiable Information (PII), such as names, addresses, and payment details, stored in ticketing systems may be accessed or exfiltrated by attackers.
  * Risk of exposure could lead to regulatory violations under PIPEDA and reputational damage.

* Integrity (I):
  * Unauthorized encryption of ticketing databases compromises data integrity, making it impossible to trust the accuracy of restored data without verification.

* Availability (A):
  * Ticketing systems are rendered unavailable due to ransomware encryption, causing disruptions to ferry operations, delays in customer bookings, and potential financial losses.

The C-I-A triad is a foundational concept in cybersecurity used to evaluate the impact of incidents on data and systems (Whitman & Mattord, 2017).

# Team Members {#team-members}

## Cybersecurity Incident Response Team (CSIRT) Roles and Responsibilities {#cybersecurity-incident-response-team-(csirt)-roles-and-responsibilities}

* Incident Response Manager (IRM)
  * Role:
    * Oversees the entire incident response process and ensures all team members are coordinated effectively. Acts as the primary decision-maker when escalations are required.
  * Responsibilities:
    * Activate the Incident Response Plan (IRP) upon detection of a ransomware attack.
    * Assign tasks to team members based on their expertise.
      Monitor progress during each phase of the incident response lifecycle (NIST SP 800-61).
    * Ensure timely communication with internal and external stakeholders, including executive leadership and regulatory authorities.
      Document all decisions made during the incident for post-incident review.
* Security Analysts
  * Role:
    * Investigate the ransomware attack, identify affected systems, and analyze Indicators of Compromise (IOCs).
  * Responsibilities:
    * Conduct forensic analysis to determine how the ransomware entered the network (e.g., phishing email, unpatched vulnerability).
      Identify the scope of the attack, including which systems and data have been encrypted or exfiltrated.
    * Collaborate with IT Specialists to isolate infected systems from the network.
      Provide technical recommendations for containment and eradication strategies.
* IT Specialists
  * Role:
    * Execute technical measures to contain, eradicate, and recover from the ransomware attack.
  * Responsibilities:
    * Isolate affected systems by disconnecting them from the network to prevent further spread of ransomware.
    * Restore encrypted systems using clean backups stored in secure locations.
    * Patch vulnerabilities exploited during the attack to prevent recurrence.
      Test restored systems to ensure they are secure and functional before reconnecting them to production environments.
* Legal Counsel
  * Role:
    * Ensure compliance with regulatory requirements and manage legal risks associated with the ransomware attack.
  * Responsibilities:
    * Review PIPEDA breach notification requirements and determine whether customer Personally Identifiable Information (PII) has been compromised. If so, notify the Office of the Privacy Commissioner of Canada within 72 hours (PIPEDA, 2000).
    * Advise on contractual obligations with third-party vendors or partners that may be impacted by the incident.
      Approve external communications to customers or media to minimize legal risks.
* Communications Lead
  * Role:
    * Manage internal updates for employees and external communications with customers, regulators, and media outlets during the incident response process.
  * Responsibilities:
    * Draft clear and concise messages for internal stakeholders outlining next steps (e.g., temporary system outages or operational changes).
    * Notify customers about potential impacts on their data or services in compliance with PIPEDA regulations.

    * Coordinate with Transport Canada to report any operational disruptions under Domestic Ferries Security Regulations (DFSR).

## Team Collaboration {#team-collaboration}

* The CSIRT operates as a cohesive unit under the direction of the IRM, ensuring that all phases of the incident response lifecycle are executed efficiently.
* Regular briefings are conducted throughout the response process to keep all team members aligned on progress and next steps.
* Escalations are handled promptly by involving executive leadership or external partners when necessary.

## Escalation Triggers {#escalation-triggers}

The following scenarios may trigger escalations:

* Detection of ransomware spreading beyond isolated systems.
* Identification of compromised customer PII requiring regulatory reporting.
* Inability to restore critical systems within defined Recovery Time Objectives (RTOs).
* Media inquiries regarding service disruptions or data breaches.
* Discovery of vulnerabilities affecting third-party vendors or partners.

Escalations are directed to executive leadership, Transport Canada, or external cybersecurity consultants based on severity.

# Internal and External Stakeholders {#internal-and-external-stakeholders}

## Internal Stakeholders {#internal-stakeholders}

Internal stakeholders are individuals or teams within BC Ferries who play a critical role in responding to and managing the ransomware incident. Their responsibilities are tied to ensuring operational continuity, compliance, and effective communication.

* Executive Leadership
  * Role:
    * Strategic oversight and decision-making.
  * Responsibilities:
    * Approve resource allocation for incident response efforts.
    * Make high-level decisions regarding service disruptions, public disclosures, or legal actions.
    * Ensure alignment between incident response efforts and organizational goals.
  * Communication Needs:
    * Receive regular updates from the Incident Response Manager (IRM) on the status of the incident.
    * Be informed of potential financial, legal, or reputational impacts.
* Incident Response Team (IRT)
  * Role:
    * Lead the technical response to contain, eradicate, and recover from the ransomware attack.
  * Responsibilities:
    * Investigate how the ransomware entered BC Ferries’ systems.
    * Execute containment measures to isolate affected systems.
    * Restore encrypted systems from clean backups.
  * Communication Needs:
    * Coordinate with IT Specialists to implement technical fixes.
    * Provide detailed reports to executive leadership on progress and challenges.
* Operations Team
  * Role:
    * Maintain ferry schedules and customer services during system outages caused by ransomware.
  * Responsibilities:
    * Implement manual processes for ticketing if digital systems are unavailable.
    * Minimize disruptions to ferry operations by coordinating with other teams.
  * Communication Needs:
    * Receive updates on system restoration timelines from the IRT.
    * Notify terminal staff and crew members about operational changes.
* Legal Counsel
  * Role:
    * Ensure compliance with regulatory requirements (e.g., PIPEDA) and manage legal risks.
  * Responsibilities:
    * Determine whether customer Personally Identifiable Information (PII) has been compromised.
    * Notify regulatory authorities (e.g., Office of the Privacy Commissioner of Canada) within 72 hours if required by PIPEDA (PIPEDA, 2000).
    * Review external communications to ensure they minimize legal exposure.
  * Communication Needs:
    * Regular updates on whether PII or sensitive data has been accessed by attackers.
* Human Resources
  * Role:
    * Manage employee communication and training related to ransomware prevention and response.
  * Responsibilities:
    * Distribute internal notices about phishing risks or new security protocols post-incident.
    * Coordinate employee training on recognizing ransomware threats.
  * Communication Needs:
    * Receive updates from the IRT on how employees may have contributed to the incident (e.g., clicking on phishing emails).

## External Stakeholders {#external-stakeholders}

External stakeholders include regulatory bodies, customers, vendors, and other third parties who must be informed or involved in responding to the ransomware incident.

* Transport Canada
  * Role:
    * Regulatory authority overseeing ferry operations under Domestic Ferries Security Regulations (DFSR).
  * Responsibilities:
    * Monitor BC Ferries’ compliance with reporting requirements for operational disruptions caused by cybersecurity incidents.
  * Communication Needs:
    * Immediate notification of any service disruptions affecting ferry routes classified as most vulnerable (e.g., Horseshoe Bay–Departure Bay).
* Office of the Privacy Commissioner of Canada (PIPEDA)
  * Role:
    * Regulatory body overseeing data privacy compliance in Canada.
  * Responsibilities:
    * Investigate breaches involving customer PII if reported by BC Ferries.
  * Communication Needs:
    * Detailed breach notification report submitted within 72 hours if customer data is compromised.
* Customers
  * Role:
    * End users affected by service disruptions or potential data breaches caused by the ransomware attack.
  * Responsibilities:
    * Protect their personal information if notified of a breach (e.g., resetting passwords).
  * Communication Needs:
    * Clear updates on service disruptions (e.g., ticketing system downtime).
    * Detailed instructions on mitigating risks if their data is compromised.
* Third-Party Vendors
  * Role:
    * Provide technical support for forensic analysis or assist in patching vulnerabilities exploited by ransomware attackers.
  * Responsibilities:
    * Collaborate with BC Ferries’ IRT to identify vulnerabilities in software or hardware used in ticketing systems.
  * Communication Needs:
    * Timely updates on system restoration progress and security patches required.
* Media Outlets
  * Role:
    * Inform the public about service disruptions or data breaches affecting BC Ferries customers.
  * Responsibilities:
    * Share accurate information provided by BC Ferries’ Communications Lead to avoid misinformation or panic.
  * Communication Needs:
    * Receive approved press releases outlining the nature of the incident, its impact, and steps being taken to resolve it.

## Communication Guidelines {#communication-guidelines}

To ensure effective communication with both internal and external stakeholders:

* Use secure channels for sensitive information (e.g., encrypted email for regulatory notifications).
* Follow predefined escalation protocols for high-severity incidents requiring immediate attention from executive leadership or regulators.
* Avoid sharing unnecessary technical details with non-technical stakeholders to prevent confusion.

# Asset Classifications and Prioritizations {#asset-classifications-and-prioritizations}

## Company Data Classifications {#company-data-classifications}

BC Ferries uses a data classification framework to categorize its information assets based on sensitivity and regulatory requirements. The classifications are as follows:

* Restricted Data:
  * Data that, if exposed, could cause severe harm to BC Ferries or its stakeholders.
  * Customer Personally Identifiable Information (PII) such as names, addresses, payment details, and reservation histories.
  * Employee payroll information, including banking details and Social Insurance Numbers (SINs).
  * Operational Technology (OT) system configurations for navigation and safety controls.
* Confidential Data:
  * Data that is critical to operations but less sensitive than restricted data.
  * Ferry schedules and route plans.
  * Internal operational reports related to fleet management.
  * Vendor contracts and service agreements.
* Public Data:
  * Information intended for public access with no confidentiality concerns.
  * Public ferry schedules available on the BC Ferries website.
  * Press releases and marketing materials.

Note: Proper classification ensures compliance with regulations like PIPEDA for protecting PII (Office of the Privacy Commissioner of Canada, 2000).

## Categories of Assets/Devices That May Be Compromised {#categories-of-assets/devices-that-may-be-compromised}

The following categories represent assets critical to BC Ferries’ operations that could be targeted during a ransomware attack:

* IT Systems:
  * Ticketing platforms used for customer bookings and payments.
  * Customer databases storing PII and financial information.
  * Internal communication tools used by employees.
* Operational Technology (OT) Systems:
  * Navigation systems ensure safe ferry operations.
  * Safety control systems onboard vessels (e.g., fire suppression systems).
  * Terminal management systems for vehicle traffic and boarding processes.
* Endpoints:
  * Employee workstations used for administrative tasks.
  * Mobile devices used by terminal staff for real-time communication.
* Network Infrastructure:
  * Core routers, switches, and firewalls supporting ferry operations.
  * Virtual Private Network (VPN) gateways enabling secure remote access.
* Backup Systems:
  * On-premises and cloud-based backup solutions storing critical data for recovery purposes.

## Prioritization of Assets {#prioritization-of-assets}

Assets are prioritized based on their criticality to operations, the potential impact of compromise, and regulatory requirements:

| Priority Level | Asset Category | Examples | Justification |
| ----- | ----- | ----- | ----- |
| High | IT Systems | Ticketing platforms, customer databases | Essential for revenue generation and customer service; contains sensitive PII. |
| High | OT Systems | Navigation controls, safety systems | Directly impacts passenger safety and operational continuity. |
| Medium | Network Infrastructure | Core routers, VPN gateways | Supports secure communication across terminals and vessels. |
| Medium | Endpoints | Employee workstations | Used for administrative tasks but less critical than core systems. |
| Low | Public-Facing Systems | Marketing websites | Minimal impact on operations if compromised; contains no sensitive data. |

## Rationale for Prioritization {#rationale-for-prioritization}

* High-Priority Assets:
  * These assets are essential to maintaining ferry operations, protecting customer trust, and ensuring compliance with regulations like Transport Canada’s Domestic Ferries Security Regulations (DFSR). For example, ticketing platforms directly impact revenue generation and customer satisfaction.
* Medium-Priority Assets:
  * While important for supporting operations, these assets have a lesser immediate impact compared to high-priority systems.
* Low-Priority Assets:
  * Public-facing systems are less critical as they do not store sensitive data or directly affect operational continuity.

## Protection Measures {#protection-measures}

To safeguard classified assets during a ransomware attack:

* Implement network segmentation to isolate IT systems from OT systems.
* Encrypt all restricted data both in transit and at rest to prevent unauthorized access.
* Regularly test backup solutions to ensure they can restore high-priority assets quickly in case of an incident.

#

# References and Citation {#references-and-citation}

1. National Institute of Standards and Technology. (2012). Computer Security Incident Handling Guide (SP800–61 Rev.2). [https://doi.org/10.6028/NIST.SP.800-61r2](https://doi.org/10.6028/NIST.SP.800-61r2)
2. Transport Canada. (2021). Domestic Ferries Security Regulations. Retrieved February 19, 2025, from [https://tc.canada.ca/en/marine-security/domestic-ferries-security-regulations](https://tc.canada.ca/en/marine-security/domestic-ferries-security-regulations)
3. Office of the Privacy Commissioner of Canada (PIPEDA). (2000). Personal Information Protection and Electronic Documents Act. Retrieved February 19, 2025, from [https://www.priv.gc.ca/en/](https://www.priv.gc.ca/en/)
4. Whitman, M., & Mattord, H. (2017). Principles of information security (6th ed.). CENGAGE Learning Custom Publishing.
5. Cybersecurity and Infrastructure Security Agency (CISA). (2021). Incident and Vulnerability Response Playbooks. Retrieved February 19, 2025, from [https://www.cisa.gov/publication/cybersecurity-playbooks](https://www.cisa.gov/publication/cybersecurity-playbooks)
6. Cynet. (n.d.). Incident Response Plan Template. Retrieved February 19, 2025, from [https://www.cynet.com/resources/incident-response-plan-template/](https://www.cynet.com/resources/incident-response-plan-template/)
7. Dilmegani, C. (2025). 50 Examples of Data Classification for Business Security. AIMultiple Research Report.

