---
title: "Organizational and Operational Framework of the ENS"
subtitle: "🏛️ Understanding the key components of the organizational and operational framework in Spain's National Security Scheme (ENS)"
tags: ["ENS", "cybersecurity"]
authors: ["alesanchezr"]

---

Before reading this article, we assume you already have some knowledge about the ENS and what it entails. If not, we recommend reading our [introduction to Spain's National Security Scheme (ENS)](https://4geeks.com/es/lesson/introduccion-al-ens-esquema-nacional-de-seguridad).

## Organizational Framework of the ENS

The Organizational Framework of the National Security Scheme (ENS), regulated by Royal Decree 311/2022, defines the functions, responsibilities, policies, and measures necessary to organize security within an entity. Its objective is to establish a clear structure that facilitates daily security management and incident response.

![Cybersecurity Framework](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/ens/cybersecurity-framework.jpg?raw=true)

### Security Policies (Org.1)

Security policies are the central axis of the organizational framework. They establish the general guidelines to protect information and assets against threats. These policies should include:

- Objectives and mission of the organization regarding security  
- Roles and responsibilities  
- Security committee and governance structure  
- Security documentation and access procedures  
- Periodic review of their effectiveness

| Level | Low | Medium | High |
|-------|-----|--------|------|
| Org.1 | ✓   | =      | =    |

> This measure applies at all levels. The `=` symbol indicates that there are no additional requirements for higher levels.

### Security Regulations and Procedures (Org.2 and Org.3)

Measures **Org.2** and **Org.3** are part of the set of fundamental organizational controls of the ENS. These measures establish the rules for using information systems, as well as detailed instructions for operating them securely.

#### Org.2 – Security Regulations

Security regulations are **internal normative documents** that set the acceptable use conditions for the organization's systems, services, and technological resources. Their purpose is to:

- Prevent improper behavior by staff.  
- Establish **rights and duties** of users.  
- Define the framework for **disciplinary responsibility** in case of non-compliance.  
- Standardize the secure use of assets throughout the entity.

These regulations must be known, understood, and accepted by all users with access to the systems. Compliance is mandatory.

#### Org.3 – Security Procedures

Security procedures detail **how specific tasks should be performed securely** within the system. They act as operational guides that:

- Describe step-by-step the required actions.  
- Identify which roles or profiles should execute them.  
- Include criteria to **detect anomalous behaviors** or security failures.  
- Promote operational continuity and traceability of actions.

These procedures must be updated periodically, easily accessible, and compatible with existing regulations and policies.

#### Applicability Table:

| Security Level | Low | Medium | High |
|----------------|-----|--------|------|
| Org.2 - Regulations | ✓ | +    | ++   |
| Org.3 - Procedures  | ✓ | +    | ++   |

> At **Low** level, at least one regulation and one basic procedure are required.  
> At **Medium and High**, greater granularity is required, segmentation by profiles, specific scenarios (such as emergency or remote administration), and formal auditing of their effectiveness.

### Authorization Processes (Org.4)

Measure **Org.4** regulates the mechanisms by which access is granted or denied to different system components. This measure covers both **people and equipment, software, or communication links**, and is key to preventing unauthorized access.

Authorization processes must:

- Be formally documented.  
- Include clear evaluation and approval criteria.  
- Ensure traceability of all granted or revoked authorizations.  
- Be applied consistently in regular and extraordinary situations (e.g., replacements, subcontracting, mobility).

#### Some typical elements that must be subject to prior authorization:

- **Physical facilities** (access to data centers, secure offices, restricted areas).  
- **Production equipment**, especially those containing sensitive data or critical functions.  
- **Applications and updates** incorporated into the active environment.  
- **External connections**, such as VPN tunnels or links with other systems.  
- **Storage media**, such as hard drives, USB drives, or cloud backups.  
- **Mobile devices**, such as laptops, tablets, or corporate smartphones.  
- **Third-party services**, especially if they handle classified data or perform sensitive tasks.

#### Applicability Table:

| Security Level | Low | Medium | High |
|----------------|-----|--------|------|
| Org.4 - Authorization Processes | ✓ | = | = |

> This measure applies uniformly at all levels, although the degree of control, automation, and traceability may increase depending on the criticality of the environment.

## Compliance Profile

ENS measures are not applied rigidly but are conditioned by the system's **compliance profile**, defined according to:

- Security level of the system (low, medium, or high)  
- Risk associated with the services and data processed  
- Organizational maturity and available resources

This approach allows **adjusting the application of measures proportionally and reasonably**, avoiding unnecessary burdens on low-impact systems.

## Operational Framework

The Operational Framework refers to a series of measures that must be taken to protect the functioning of the system as an integral set of components for a purpose. This framework plays an essential role in providing the necessary structure to effectively implement and manage security measures.

### Security Planning

Security planning within the operational framework is one of the most important components of the ENS. It involves a strategic process that guides organizations in identifying and managing risks, implementing security measures, and preparing to respond to incidents. Security planning consists of several stages:

#### Risk Analysis (op.pl.1)

Risk analysis is the process that allows the organization to **identify, assess, and prioritize threats and vulnerabilities** affecting information and systems. This analysis should include:

- Identification of assets (data, services, infrastructures).
- Assessment of threats (internal, external, accidental, or malicious).
- Evaluation of vulnerabilities and their exploitability.
- Estimation of **potential impact** and **likelihood of occurrence**.
- Identification of existing safeguards and **residual risks**.
- Recommendations for mitigation measures adapted to the system profile.

The depth of the analysis will depend on the security level assigned to the system:

| Security Level | Requirement |
|----------------|-------------|
| Low            | Simple, qualitative assessment based on key assets. |
| Medium         | Semi-formal analysis, with tabular representation and qualitative values. |
| High           | Formal analysis, with quantitative metrics and specialized tools. |

| Level | Low | Medium | High |
|-------|-----|--------|------|
| op.pl.1 | ✓ | +      | ++   |

---

#### Security Architecture (op.pl.2)

Security architecture defines the **technical, logical, and organizational structure** that protects the entity's systems against attacks or failures.

This measure covers:

- Design of a **secure network topology** (segmentation, demilitarized zones, firewalls).
- Robust **authentication and identification** mechanisms.
- Access and privilege control (principle of least privilege).
- Use of **defense lines** (defense in depth).
- Identity management and user lifecycle.
- Supervision and maintenance of secure configurations.

The complexity and depth of this architecture increase according to the security level:

| Security Level | Key Requirements |
|----------------|------------------|
| Low            | Basic system documentation, basic authentication. |
| Medium         | Organized management of configurations and updates. |
| High           | Integrated ISMS with internal controls and continuous improvement plans. |

| Level | Low | Medium | High |
|-------|-----|--------|------|
| op.pl.2 | ✓ | +      | ++   |

---

#### Acquisition of New Components (op.pl.3)

This measure requires that **every new technological element** (hardware, software, services) acquired or developed by the organization **complies with the security requirements established by the ENS** before being deployed.

Includes:

- Security validation at the **acquisition or contracting** stage.  
- Evaluation of the provider's regulatory compliance.  
- Review of **licenses, updates, and product lifecycle**.  
- Secure integration into the organization's environment (avoiding introducing vulnerabilities).  
- Registration and change control in the asset inventory.

| Level | Low | Medium | High |
|-------|-----|--------|------|
| op.pl.3 | ✓ | =      | =    |

> The "=" symbol indicates that the same set of requirements must be met at all security levels.

---

#### Capacity Management (op.pl.4)

This measure ensures that the organization has **sufficient human, technical, and operational capacities** to maintain the security of its systems and services.

Covers:

- Continuous training of staff in cybersecurity, awareness, and best practices.
- Adequate provision of **technical tools and resources**.
- Assignment of clear responsibilities and qualified profiles.
- Periodic evaluation of **internal and external capacities** to respond to incidents.
- Preparation for the evolution of threats and emerging technologies.

| Level | Low | Medium | High |
|-------|-----|--------|------|
| op.pl.4 | — | ✓      | =    |

> At **Low** level, this measure is not mandatory.  
> At **Medium and High**, it is required to implement training programs and organizational structures that effectively support security management.

### Other Operational Controls (reference to Annex II)

The ENS includes other key measures that must also be implemented according to the compliance profile. Some of them are:

- **Configuration management** (`op.ex.1`)  
- **Secure maintenance** (`op.ex.3`)  
- **Change management** (`op.ex.4`)  
- **Malware protection** (`op.pro.1`)  
- **Incident management** (`op.mon.6`)  
- **Activity logging and monitoring** (`op.mon.1`, `op.mon.4`)  
- **Cryptographic key management** (`op.pro.5`)  
- **External services control** (`op.ext.1`)

Each has different applicability depending on the system level.

By implementing these organizational and operational frameworks, public administrations can ensure a comprehensive approach to information security, aligning with the requirements of the National Security Scheme.

