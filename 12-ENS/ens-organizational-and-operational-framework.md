---
title: "ENS Organizational and Operational Framework"
subtitle: "🏛️ Understanding the key components of the organizational and operational framework in Spain's National Security Scheme (ENS)"
tags: ["ENS", "cybersecurity"]
authors: ["alesanchezr"]

---



## Organizational Framework

The Organizational Framework of the National Security Scheme (ENS) is a set of documents, guidelines, and measures related to the organization of the entity's security. This framework defines the functions, responsibilities, and policies that allow for daily management and incident resolution.

![Cybersecurity Framework](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/ens/cybersecurity-framework.jpg?raw=true)

### Security Policies

Security policies are a key component of the Organizational Framework. They are documents that establish guidelines, norms, and procedures to be followed to ensure the protection of information, systems, assets, and resources against security threats and risks.

According to Article 11 of Royal Decree 3/2010, all higher bodies of the Public Administration must have a security policy that clearly and precisely includes:

- Objectives and mission of the organization
- Security roles and functions, defining the duties and responsibilities of positions, as well as assignment and renewal procedures
- Legal and regulatory framework in which activities will be developed
- Structure of the security management and coordination committee, detailing responsibilities
- Guidelines for structuring the system's security documentation, its management and access

It is also recommended to establish plans for staff awareness and training on security actions, have a risk management plan, and know how to handle potential security incidents. These policies should undergo periodic review to improve their effectiveness.

The ENS establishes that security policies should be applied at low, medium, and high levels:

| Dimensions |  |  | Security Measures |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Organizational Framework |
| Applies | = | = | Org.1 | Security Policies |

**Explanation of Org.1 Security Policies:**

This measure requires that security policies must be implemented at all security levels (Low, Medium, and High). The "Applies" in the Low (L) column and the "=" signs in the Medium (M) and High (H) columns indicate that the same basic requirements apply across all levels, without additional requirements for higher levels.

In simpler terms:
- Every organization, regardless of its security level, must have clearly defined security policies.
- These policies should outline the organization's security objectives, roles, responsibilities, and guidelines.
- The policies should be appropriate for the organization's size and complexity, but the core requirement to have them exists for all security levels.

### Security Regulations and Procedures

Security regulations are another crucial control within the organizational framework. They establish the correct use of information systems and assets, as well as staff responsibilities regarding compliance or violation of these established norms.

The ENS establishes that security regulations should address:

1. Correct use of equipment, services, and facilities
2. What is considered improper use
3. Staff responsibility regarding compliance or violation of these norms: rights, duties, and disciplinary measures in accordance with current legislation

Security procedures are documents that describe step-by-step how to perform certain activities. The ENS establishes that these documents should include:

1. How to carry out routine tasks
2. Who should perform each task
3. How to identify and report anomalous behaviors

Both security regulations and procedures should be applied at all levels:

| Dimensions |  |  | Security Measures |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Organizational Framework |
| Applies | = | = | Org.2 | Security Regulations |
| Applies | = | = | Org.3 | Security Procedures |

In summary:
- Org.1 (Policies) applies to all levels and sets the overall security direction.
- Org.2 (Regulations) adds more detailed rules for Medium and High levels.
- Org.3 (Procedures) provides the most detailed security instructions, required only for High-level security environments.

### Authorization Processes

The last control established within the organizational framework is the authorization processes. These aim to establish how the process will be for authorizing a user or component to enter and be part of the entity's system.

According to the ENS, these processes should cover:

1. Use of facilities, both regular and alternative
2. Entry of equipment into production, particularly equipment involving cryptography
3. Entry of applications into production
4. Establishment of communication links with other systems
5. Use of communication media, both regular and alternative
6. Use of information supports
7. Use of mobile equipment (laptops, PDAs, etc.)
8. Use of third-party services, under contract or agreement

Authorization processes should be applied at all levels:

| Dimensions |  |  | Security Measures |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Organizational Framework |
| Applies | = | = | Org.4 | Authorization Processes |

## Operational Framework

The Operational Framework refers to a series of measures that must be taken to protect the operation of the system as an integral set of components for a purpose. This framework plays an essential role in providing the necessary structure to effectively implement and manage security measures.

### Security Planning

Security planning within the operational framework is one of the most important components of the ENS. It involves a strategic process that guides organizations in identifying and managing risks, implementing security measures, and preparing to respond to incidents.

Security planning consists of several stages:

#### Risk Analysis

This involves a comprehensive assessment of the risks faced by information and systems. The analysis identifies potential threats, assesses their impact, and determines the likelihood of occurrence.

The ENS establishes different requirements for risk analysis based on the system category:

- Basic Category Systems: A simple analysis showing the most valuable assets, most likely threats, safeguards protecting against these threats, and main residual risks.
- Medium Category Systems: A semi-formal analysis with a tabular presentation describing and qualitatively valuing assets, quantifying threats, valuing safeguards, and assessing residual risk.
- High Category Systems: A formal analysis with mathematical calculations covering asset valuation, possible threats, enabling vulnerabilities, adequate safeguards, and residual risk assessment.

| Dimensions |  |  | Security Measures |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Operational Framework |
| Applies | + | ++ | op.pl.1 | Risk Analysis |

#### Security Architecture

This is the fundamental structure that supports the safeguarding of sensitive information in public administrations. It's designed to establish a secure environment, ensuring the confidentiality, integrity, and availability of systems and data in a constantly evolving digital context.

The ENS establishes different requirements for security architecture based on the system category:

- Basic Category Systems: Documentation of facilities, system documentation, defense line scheme, and user identification and authentication system.
- Medium Category Systems: Management system related to planning, organization, and control of information security resources.
- High Category Systems: Information security management system with periodic updating and approval, and internal technical controls.

| Dimensions |  |  | Security Measures |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Operational Framework |
| Applies | + | ++ | op.pl.2 | Security Architecture |

#### Acquisition of New Components

This process is done with the aim of strengthening the security infrastructure within the public administration. These components must comply with ENS standards and must be able to integrate into the existing system.

| Dimensions |  |  | Security Measures |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Operational Framework |
| Applies | = | = | op.pl.3 | Acquisition of New Components |

#### Capacity Management

This focuses on identifying, acquiring, and developing the necessary capabilities to ensure the integrity, confidentiality, and availability of information, thus facing the changing challenges of the cyber environment.

| Dimensions |  |  | Security Measures |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Operational Framework |
| N/A | Applies | = | op.pl.4 | Capacity Management |

### Other Operational Controls

The ENS also establishes other operational controls such as:

- Configuration Management
- Maintenance
- Change Management
- Protection against Malicious Code
- Incident Management
- User Activity Logging
- Protection of Activity Logs
- Cryptographic Key Protection
- External Services Management

Each of these controls has specific requirements and applicability based on the system category (Low, Medium, High).

By implementing these organizational and operational frameworks, public administrations can ensure a comprehensive approach to information security, aligning with the requirements of the National Security Scheme.
