---
title: "Principles of the NIST Cybersecurity Framework"
subtitle: "🛡️ Understanding the key components and functions of the NIST Cybersecurity Framework for effective information security management"
tags: ["NIST", "cybersecurity"]
authors: ["alesanchezr"]

---

The **Cybersecurity Framework** or **NIST Framework** is a guide developed to provide a structured approach for managing and improving an organization's cybersecurity. This framework consists of three main components: the Core, Profiles, and Implementation Tiers.

The core of the [NIST Cybersecurity Framework 2.0](https://www.nist.gov/cyberframework) (also known as the Core) is a structured set of desired outcomes and best practices for managing cybersecurity risks. It is organized into six key functions: Govern, Identify, Protect, Detect, Respond, and Recover. These functions are further divided into **categories** and **subcategories** that help set priorities, measure capabilities, and define improvement plans.

The core is divided into six main functions:

- Govern
- Identify
- Protect
- Detect
- Respond
- Recover

![NIST Cybersecurity Framework](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/marco-de-ciberseguridad-de-nist.png)

Each function of the Core contains **categories** and **subcategories** that detail specific actions and security objectives, offering a flexible yet clear structure for practical application.

## Functions of the NIST Cybersecurity Framework 2.0

**CSF 2.0** introduces an updated structure with **six key functions** representing the complete cycle of cyber risk management. Each function is composed of **categories** (thematic groups) and **subcategories** (specific desired outcomes). This organization allows any organization, public or private, to adapt it according to its reality and maturity.

### 1. Govern – Cybersecurity Governance

| Category | Description | Subcategories (examples) |
|----------|-------------|--------------------------|
| GV.RM - Risk Management Strategy | Formalized and communicated strategy | GV.RM-1: The risk strategy is documented and aligned with organizational objectives |
| GV.OV - Organizational Context | Understanding mission, environment, and legal obligations | GV.OV-1: Responsibilities and regulatory boundaries are identified |
| GV.PO - Policies and Procedures | Established policies and procedures | GV.PO-1: Policies are documented and regularly reviewed |
| GV.SU - Supply Chain Risk Management | Third-party risks are effectively managed | GV.SU-1: Security agreements and monitoring with suppliers exist |

### 2. Identify – Understanding the Context

| Category | Description | Subcategories (examples) |
|----------|-------------|--------------------------|
| ID.AM - Asset Management | Complete inventory of physical and digital assets | ID.AM-1: Physical devices are identified<br>ID.AM-2: Software assets are identified |
| ID.BE - Business Environment | Identification of critical functions and dependencies | ID.BE-1: Critical functions are understood<br>ID.BE-2: Internal and external dependencies are documented |
| ID.RA - Risk Assessment | Ongoing assessment of threats and vulnerabilities | ID.RA-1: Relevant threats are identified<br>ID.RA-2: Existing vulnerabilities are assessed |
| ID.RM - Risk Management | Risk prioritization | ID.RM-1: Acceptable risk levels are determined<br>ID.RM-2: Responses to prioritized risks are documented |

### 3. Protect – Implementation of Safeguards

| Category | Description | Subcategories (examples) |
|----------|-------------|--------------------------|
| PR.AC - Access Control | Identity management and access control | PR.AC-1: Only authorized users can access systems |
| PR.AT - Awareness and Training | Ongoing staff training | PR.AT-1: Regular cybersecurity training is provided |
| PR.DS - Data Security | Protection of data in transit and at rest | PR.DS-1: Information is encrypted and protected |
| PR.IP - Information Protection Processes | Defined procedures to protect assets | PR.IP-1: Secure configurations and change management are applied |
| PR.MA - Maintenance | Secure and documented maintenance | PR.MA-1: Maintenance is performed with access control |
| PR.PT - Protective Technology | Protective technologies implemented | PR.PT-1: Firewalls, antivirus, IDS/IPS, and execution control are used |

### 4. Detect – Detection of Anomalies

| Category | Description | Subcategories (examples) |
|----------|-------------|--------------------------|
| DE.AE - Anomalies and Events | Detection of anomalous activities | DE.AE-1: Expected behaviors are defined<br>DE.AE-2: Deviations are detected |
| DE.CM - Continuous Monitoring | Ongoing monitoring of networks and systems | DE.CM-1: Security events are monitored<br>DE.CM-2: Logs are collected and analyzed |
| DE.DP - Detection Processes | Evaluation of detection effectiveness | DE.DP-1: Detection processes are periodically reviewed |

### 5. Respond – Incident Response

| Category | Description | Subcategories (examples) |
|----------|-------------|--------------------------|
| RS.RP - Response Planning | Preparedness to respond to incidents | RS.RP-1: A documented and approved response plan exists |
| RS.CO - Communications | Internal and external communication during incidents | RS.CO-1: Contacts are established for incident reporting<br>RS.CO-2: Stakeholders are informed |
| RS.AN - Analysis | Analysis of incident impact | RS.AN-1: The incident is analyzed to determine scope and cause |
| RS.MI - Mitigation | Impact reduction | RS.MI-1: Incident effects are mitigated |
| RS.IM - Improvements | Lessons learned | RS.IM-1: Plans and procedures are updated post-incident |

### 6. Recover – Restoration of Capabilities

| Category | Description | Subcategories (examples) |
|----------|-------------|--------------------------|
| RC.RP - Recovery Planning | Formal plans for service restoration | RC.RP-1: Recovery plans are documented and tested |
| RC.IM - Improvements | Continuous improvement after incidents | RC.IM-1: Lessons learned are applied to future plans |
| RC.CO - Communications | Effective communication during recovery | RC.CO-1: Recovery status is communicated to stakeholders |

> 💡 This updated structure allows organizations to perform more accurate diagnostics, build customized profiles, and use the Framework as a realistic roadmap to improve their cybersecurity posture.

In addition to the functions, the NIST Framework defines four implementation or organizational maturity levels, called **Tiers**, which help understand how deeply an organization has integrated risk management into its culture and operations.

## Tiers or Risk Maturity Levels

*Tiers* help an organization assess the extent to which its cyber risk management is formalized, integrated, and adaptive. They are not mandatory maturity levels, but reference points to guide improvements.

- **Tier 1 – Partial**
    - Risk management is improvised and unplanned: action is only taken when a problem occurs, with no established preventive measures.
    - The organization lacks formalized processes.
    - There is no integration between cybersecurity objectives and business objectives.
    - Senior management is rarely involved.

- **Tier 2 – Risk Informed**
    - Risk management processes exist but are not implemented uniformly.
    - Some functions are informed about cyber risks.
    - Cybersecurity decisions are partially based on risk knowledge.
    - There is a lack of clear alignment across all organizational areas.

- **Tier 3 – Repeatable**
    - The organization has developed formal policies and procedures.
    - Cybersecurity practices are documented, reviewed, and maintained.
    - There is integration with strategic objectives.
    - Response and recovery plans are reviewed and updated.

- **Tier 4 – Adaptive**
    - The organization has a culture of continuous improvement.
    - It dynamically adapts to changes in the environment and new threats.
    - Threat intelligence is used to anticipate incidents.
    - Cybersecurity is a priority at all decision-making levels.

> These levels are not a quality scale, but a tool to help each organization understand its starting point and plan improvements.

## What is a Profile in the NIST Cybersecurity Framework?

A **profile** in the context of the NIST CSF is a customized representation of the Framework **Core**, tailored to the specific reality of an organization. Not all organizations face the same risks or have the same resources, so the profile allows cybersecurity objectives to be aligned with operational priorities.

For example, a profile could reflect the following:

- **Business priorities**: e.g., if service continuity is more critical than data confidentiality.
- **Operating environment**: including sector, size, applicable regulations, and technological complexity.
- **Risk tolerance**: how much risk the organization is willing to accept based on its appetite and capabilities.
- **Available resources**: both human and technical, as well as budgetary.

#### Types of Profiles

- **Current Profile**: Describes the organization's actual state for each Core subcategory. It is based on evidence, existing practices, and internal or external assessments.
- **Target Profile**: Represents the ideal situation the organization wants to achieve. It is based on its strategy, policies, and risk management objectives.

### Why Compare Profiles?

Comparing the current profile and the target profile allows you to:

- Identify gaps and vulnerabilities.
- Prioritize improvement actions according to impact and effort.
- Justify budgets and implementation strategies.
- Measure progress over time.

> 💡 The profile is a **dynamic tool** that should be updated regularly as threats, resources, or business objectives change.

## Why Adopt the NIST CSF?

- Provides a common language between technical and executive teams.
- Is adaptable to any organizational size or sector.
- Allows prioritization of cybersecurity investments based on risk.
- Facilitates audits and alignment with other standards such as ISO/IEC 27001.
- Improves organizational resilience and incident response.

Furthermore, understanding and applying these principles will enable cybersecurity professionals to implement a solid, measurable, and evolving posture within any organization. Even in environments where no previous controls exist, the [NIST CSF 2.0](https://www.nist.gov/cyberframework/quick-start-guides) acts as a clear and effective roadmap to start from scratch or continuously improve.
