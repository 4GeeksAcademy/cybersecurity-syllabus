---
title: "Fundamentals of Digital Forensics"
subtitle: "🕵️‍♂️ Modern techniques for investigating cybersecurity incidents and preserving digital evidence"
tags: ["cybersecurity", "digital forensics", "digital investigation"]
authors: ["alesanchezr"]
---

**Digital forensics** is a critical discipline within cybersecurity, focused on the identification, preservation, analysis, and presentation of digital evidence after a security incident. In a context where cyber threats are increasingly sophisticated and persistent, forensics not only helps clarify what happened but also improves the future defense of affected systems. Its main objectives are:

- Determine the scope and nature of a security incident.
- Identify exploited vulnerabilities and the attack vector.
- Preserve evidence in an intact and admissible manner for legal environments.
- Provide intelligence to improve defensive posture.

## Phases of Modern Digital Forensics

1. **Identification and Preparation:** This phase marks the start of the investigation. Forensics does not begin spontaneously; it is triggered by the detection of a potential security incident. Its objectives are:

    - Activate the Incident Response Plan (IRP).
    - Assess the initial situation (malware, unauthorized access, data leak).
    - Define the scope: endpoints, servers, or compromised networks.
    - Preserve the system state without alterations.

    #### Best practices:
    - Use SIEM tools ([Wazuh](https://4geeks.com/lesson/wazuh-siem-and-edr-for-cybersecurity), Splunk, ELK).
    - Avoid forced shutdowns or reboots.
    - Coordinate with IT to maintain the integrity of the affected system.


2. **Evidence Acquisition:** The goal is to faithfully copy relevant digital content without alteration. This is the most critical phase for the legal validity of the evidence. The objective is to **collect evidence**, such as:

    - Forensic image of the entire disk.
    - RAM memory capture.
    - Logs and temporary files.

    #### Best practices:

    - Preserve the integrity of the evidence. It is important to generate and record **cryptographic hashes** (MD5, SHA-256) before and after acquisition, compare hashes to verify the forensic image is identical to the original, and include hash values in the technical report.
    - Use read-only devices (write blockers). Prevents accidental writing to the original disk and ensures the source remains unaltered during the process.
    - Work on copies, never the original. Obtain a **full forensic image** (bit by bit) of the medium and protect the original in a controlled, disconnected, and secure environment.
    - Document the entire process (chain of custody). Record date, time, location, and device conditions, note the names of those responsible for acquisition, and include tools used, storage media, and digital signatures.
    - Choose recognized forensic tools. For disks: `dd`, FTK Imager, Guymager; for RAM: Volatility, Belkasoft RAM Capturer. Always use tools with legal and technical acceptance.
    - Avoid altering the system state. Do not reboot, format, or modify the device before acquisition.
    - Record the operational context. Was the system on? Were there active processes or sessions? Which users were connected? Were there active network connections?

3. **Evidence Preservation:** Ensures the evidence is valid and legally admissible. Focuses on maintaining an intact chain of custody. Key elements include: signed chain of custody, use of working copies (never analyze originals), and storage in encrypted containers (`E01, AFF`).

    #### Best practices:
    - Record every action taken on the evidence.
    - Do not use personal or shared devices.


4. **Analysis:** This phase seeks to reconstruct events based on the collected digital evidence. The goal is to identify attack vectors, responsible parties, techniques used, and the chronology of events. Work is done on forensic disk images, memory dumps, system logs, and other artifacts to obtain a detailed picture of the incident.

    The scope of analysis may include:

    - Files and file systems (deleted, hidden, or suspicious files).
    - System logs, firewall, DNS, and network events.
    - Malware artifacts (prefetch, registry, temp files).
    - RAM memory analysis.
    - Forensic timeline (chronological reconstruction of events).

    #### Best practices:
    - Always work on a verified copy of the forensic image, never the original.
    - Generate timelines with tools like **Plaso** or **Timesketch** to understand the sequence of actions.
    - Correlate multiple data sources: system logs, network traffic, authentication records, etc.
    - Analyze RAM with tools like **Volatility** to detect hidden processes, credentials in memory, or active connections.
    - Apply a recognized methodology such as [**SANS DFIR**](https://www.sans.org/cyber-security-courses/digital-forensics-incident-response/), [**NIJ (National Institute of Justice)**](https://nij.ojp.gov/library/publications/forensic-examinations-digital-evidence-guide-law-enforcement), or [**ISO/IEC 27037**](https://www.iso.org/standard/44381.html) to ensure traceability.
    - Document each finding precisely: location, timestamp, tool used, and file hash if applicable.
    - Use reliable tools such as **Autopsy**, **X-Ways Forensics**, **Volatility**, **Log2timeline**, among others.
    - Do not draw conclusions without validated evidence. Every finding must be reproducible and supported by technical proof.


5. **Presentation:** This phase turns technical findings into clear, understandable documents usable by different audiences: IT teams, management, legal, or even judicial authorities. Its purpose is to communicate precisely what happened, how it happened, and what impact it had.

    The generated products must be backed by the collected evidence, the methodology used, and the analysis results, all under criteria of objectivity and traceability.

    #### Typical outputs:
    - **Technical report**: Detailed and structured. Includes evidence, tools used, procedures, results, hashes, and examiner's observations.
    - **Executive report**: For decision-makers. Summarizes impact, scope, identified weaknesses, and recommendations.
    - **Judicial presentation**: Formal and structured format that may include annexes, screenshots, chain of custody, and sworn statements if required in a legal context.

    #### Best practices:
    - Maintain precise technical language without ambiguity.
    - Be completely **objective and verifiable**; do not make unsupported assumptions.
    - Include **hashes**, **screenshots**, and **digital signatures** from the examiner or forensic team.
    - Record all chain of custody documentation.
    - Validate the report with a second review before delivery or presentation.


## Frameworks and Methodologies in Digital Forensics

Digital forensics must follow standardized methodologies to ensure procedures are systematic, reproducible, technically valid, and legally acceptable. Below are the main internationally recognized frameworks and standards:


### 1. [SANS DFIR (Digital Forensics and Incident Response)](https://www.sans.org)

- Proposed by the SANS Institute, widely used in corporate environments and incident response teams (CSIRT, SOC).
- Phases: **Preparation → Identification → Containment → Eradication → Recovery → Lessons Learned**.
- Focused on information security incidents.
- Combines forensics with incident management.


### 2. NIJ (National Institute of Justice)

- Focused on judicial and law enforcement environments.
- Defines the phases: **Identification, Preservation, Collection, Examination, Analysis, Presentation**.
- Emphasizes the importance of chain of custody and evidence integrity.
- Widely used in legal procedures in the US and Latin America. [NIJ Guide (PDF)](https://www.ojp.gov/pdffiles1/nij/219941.pdf)


### 3. [ISO/IEC 27037](https://www.iso.org/standard/44381.html)

- International ISO standard for digital evidence management.
- Provides guidance for **identification, collection, acquisition, and preservation** of digital evidence.
- Accepted in both legal and corporate environments.


### 4. [DFRWS Framework (Digital Forensic Research Workshop)](https://www.dfrws.org)

- Technical and academic approach.
- Proposes the phases: **Identification → Preservation → Collection → Examination → Analysis → Presentation → Decision**.
- Promotes the use of validated tools and a scientific approach to analysis.


### 5. [NIST 800-86 PDF](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-86.pdf)

- Publication from the National Institute of Standards and Technology (NIST).
- Offers practical guidance for integrating forensics into incident response.
- Widely used in US government and private institutions.


### 6. [ACPO Guidelines (Association of Chief Police Officers - UK)](https://library.npia.police.uk/docs/acpo/digital-evidence-2008.pdf)

- Based on **four fundamental principles** of digital evidence handling.
- Requires that any intervention be documented and justifiable.
- Recommended for criminal investigations and legal compliance.


## Which methodology to choose?

- **For corporate or SOC environments**:
  - SANS DFIR
  - NIST SP 800-86
  - ISO/IEC 27037

- **For judicial, police, or legal environments**:
  - NIJ
  - ACPO Guidelines
  - DFRWS

> 💡 Using a recognized methodology not only improves the quality of the analysis but also strengthens the legal validity of the report and the confidence of those receiving the findings.


## Practical Case: Ransomware Attack on a Corporate Endpoint

To illustrate the practical application of digital forensics, here is a simulated scenario based on a common threat: ransomware. This simulation can be used as a case study or as the basis for a technical lab.

### Scenario

An organization detects anomalous behavior on one of its internal network computers: multiple files were encrypted and their names changed with the `.locked` extension. A ransom note (`READ_ME.txt`) appears on the user's desktop.


## Practical Application of Forensic Phases

### 1. **Identification and Preparation**
- The **Incident Response Plan (IRP)** is activated.
- The affected device is confirmed as `pc-finanzas-03`.
- The endpoint is immediately isolated from the network to prevent lateral movement.
- The corporate SIEM (Wazuh) is consulted to review alerts and unusual behavior patterns.

### 2. **Evidence Acquisition**
- A **full forensic disk image** is created with **FTK Imager**.
- A **RAM memory capture** is performed using **Belkasoft RAM Capturer** before shutting down the device.
- **MD5 and SHA-256 hashes** of the image are calculated and recorded.
- All evidence is stored on encrypted external media and documented under a **formal chain of custody**.

### 3. **Preservation**
- Analysis is performed on a working copy.
- The original image is stored in a secure environment and not manipulated.
- The `.E01` format is used to encapsulate the forensic image, maintaining its integrity.

### 4. **Analysis**
- A malicious binary (`svc.exe`) is found in `AppData\Roaming`.
- The malware execution is traced to the opening of a `.zip` file downloaded via email.
- Memory analysis with **Volatility** reveals persistent processes and active connections to a C2 server in Eastern Europe.
- Tools like **Plaso** and **Timesketch** are used to reconstruct a detailed **forensic timeline** of events.
- Windows event logs, network traffic, firewall, DNS, and residual attack artifacts are inspected.

### 5. **Presentation**
- A **technical report** is generated with:
  - Collected evidence.
  - Hashes and integrity records.
  - Indicators of Compromise (IOCs).
  - Technical description of the malware.
- An **executive report** is prepared for senior management with:
  - Impact and scope of the incident.
  - Immediate recommendations.
  - Exploited vulnerabilities and mitigation suggestions.
- A summary is presented to the legal and compliance area to assess regulatory implications.


### Post-Incident Measures

- The incident originated from opening a malicious file received by email.
- Lack of multi-factor authentication (MFA) and lax attachment filtering policies were identified.
- The organization decides to implement:
  - Stricter email security policies.
  - Network segmentation for critical users.
  - Automated offline backups.
  - End-user awareness training.
  - Integration of a SIEM with EDR capabilities.
