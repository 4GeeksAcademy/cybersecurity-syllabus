---
title: "Introduction to the ENS (National Security Framework)"
subtitle: "🛡️ Understanding the fundamentals of the National Security Framework, its importance in information security management, and the certification process."
tags: ["ENS", "cybersecurity"]
authors: ["alesanchezr"]

---

> 🇪🇸 If you are not going to work in 🇪🇸 Spain, this topic will be irrelevant to you and you can skip the entire module. Alternatives to ENS in other countries: NIST Cybersecurity Framework 🇺🇸, [ISO 27001](https://4geeks.com/es/lesson/introduccion-a-iso-27001) 🌎, IT-Grundschutz 🇩🇪, NERC CIP 🇺🇸, CERC 🇨🇦, NIS Directive 🇪🇺, CNSSI 1253 🇨🇳.

In some cases during our careers as cybersecurity analysts in 🇪🇸 Spain, we will have to audit a system of a public body governed by the ENS, so it is necessary to have knowledge about this.

Among the ENS topics we will cover are frameworks, protection measures, risk analysis, and certain tools that will help us implement the framework. Without further ado, let's get into the topic.

# Introduction to the ENS (National Security Framework) 🛡️🇪🇸

The National Security Framework (ENS) is a set of policies and guidelines carefully designed to anticipate, prevent, and respond to cybersecurity challenges. This regulatory framework was established by the Spanish government to **ensure the security of information systems used by public administrations**. The ENS is essential for protecting the information and services managed by government entities. 🏛️💻

## Regulation and Purpose of the ENS

The National Security Framework (ENS) is a regulatory framework established in Royal Decree 311/2022, aimed at ensuring the protection of information in the public sector and in private entities that manage technology services for public administrations. The ENS is **mandatory** for:

- All **Spanish Public Administrations**.
- **Private companies** that provide technology services or manage public systems under contract.

Compliance with the ENS is therefore essential in both governmental and public-private collaboration environments.

## ENS Objectives

The main objectives of the ENS are:

1. Create the necessary conditions for trust in the use of electronic means.
2. Promote continuous security management.
3. Provide a common language for interaction between administrations on security matters. 🗣️
4. Establish rules, measures, and minimum security requirements for public entities.

## Basic Principles 📊

The ENS is based on the following principles:

- **Comprehensive security:** Security must be addressed from a global perspective. It is not enough to protect only technological systems; it must cover: Physical infrastructure, internal processes, information in paper and digital formats, people (users, administrators, third parties), and external or subcontracted services.

    The comprehensive approach ensures that no part of the ecosystem is left unprotected or isolated from security policies.

- **Risk management:** All security decisions must be based on a systematic risk analysis. This involves: Identifying threats and vulnerabilities, assessing potential impact, estimating the likelihood of occurrence, and applying proportional measures to mitigate them.

    This principle promotes proactive and rational management, avoiding unnecessary investments or poorly founded reactive decisions.

- **Prevention, detection, response, and recovery:** Security must cover the entire incident lifecycle. Mechanisms must be implemented to prevent threats, detect anomalous activities, respond appropriately to incidents, and restore operations.

    This approach ensures system resilience and reduces the impact of attacks.

- **Periodic reassessment:** Security measures must be regularly reviewed to ensure their validity and effectiveness. This includes assessing technological, organizational, and regulatory changes that may affect the system.

    Periodic review allows protection to adapt to new circumstances and avoids obsolescence.

- **Differentiated function:** Security functions within the organization must be clearly separated. There must be a distinction between those responsible for information, service, security, and technical operation.

    This division of responsibilities avoids conflicts of interest and facilitates control and accountability.

- **Continuous improvement:** Security is not a static state but an evolving process. Organizations must learn from their mistakes, review procedures, and constantly adopt best practices.

    This principle reinforces the maturity and efficiency of the security management system.

- **Regulatory compliance:** All measures must align with current laws and regulations. This includes regulations such as the GDPR, sectoral legislation, and other applicable provisions.

    Regulatory compliance ensures the legality of actions and the protection of fundamental rights.

- **Responsibility and commitment:** Security is the responsibility of all members of the organization, not just technical staff. Senior management must lead institutional commitment, and users must be aware of their role in protecting information.

    This principle strengthens the organizational culture around security.

## Classification and Levels of Security Measures

Royal Decree 311/2022 establishes **73 security measures**, classified into:

- **Organizational framework**: 16 measures  
- **Operational framework**: 31 measures  
- **Protection measures**: 26 measures

Each measure has three levels of application:

- **BASE** (mandatory)  
- **Reinforced**  
- **High**

The levels allow security requirements to be adapted according to the system's category (low, medium, or high criticality), as established in Guide CCN-STIC 808.

## Compliance Profile

The **compliance profile** is a concept introduced by Royal Decree 311/2022 as a mechanism to **adapt ENS security measures to the reality of each organization**, allowing for a **proportional, effective, and sustainable** application. This approach recognizes that not all entities have the same capabilities or face the same risks. Therefore, the compliance profile considers the following factors:

- **System criticality:** That is, the importance of a particular system or service for operational continuity, protection of sensitive data, or provision of essential services. A critical system will require more demanding measures.

- **Cybersecurity maturity level:** Assesses the organizational and technical capacity to properly manage information security. More mature entities can address advanced measures, while others can scale up gradually.

- **Available resources:** Includes qualified personnel, budget, technological infrastructure, and available tools. The ENS recognizes the need to tailor compliance requirements to each organization's actual capacity.

The compliance profile is reflected in the **statement of applicability** and the **adaptation plan**, which determine how, when, and to what extent the required measures will be implemented. This mechanism seeks to avoid rigid and homogeneous application of controls, allowing for a more **realistic, flexible, and risk-oriented ENS**, without undermining security.

## Implementation and Compliance

To comply with ENS requirements, organizations must follow a **structured process** to ensure the effective and verifiable implementation of security measures. This process consists of the following phases:

1. **Risk analysis:** Identification and assessment of risks threatening the security of information and services. It is the basis for selecting appropriate measures and defining their level of requirement (BASE, Reinforced, or High).

2. **Statement of applicability:** A document identifying the ENS measures applicable to the organization, indicating their level of implementation according to the compliance profile. It must be properly justified.

3. **Adaptation plan:** A strategic document establishing the activities, resources, and deadlines needed to achieve compliance. It prioritizes actions based on risk and system criticality.

4. **Implementation of measures:** Execution of the adaptation plan, which may include the adoption of policies, technical configurations, procedures, staff training, and internal audits.

5. **Periodic audits:** Internal or external evaluations that verify the degree of compliance and the effectiveness of the measures. They are mandatory and allow deviations and improvement opportunities to be detected.

> 🕓 According to the transitional provision of Royal Decree 311/2022, entities had a **24-month period from April 2022** to adapt to the new ENS. This transition period ended in **April 2024**, so **full compliance is now required**.

## ENS Certification

**ENS certification** is a formal process by which an organization certifies that it complies with the security requirements established in Royal Decree 311/2022. This certification not only verifies legal compliance but is also a key tool to **improve institutional trust, facilitate transparency, and demonstrate cybersecurity maturity** to third parties.

### Who can be certified?

- **Public Administration bodies** (AGE, Autonomous Communities, Local Entities)
- **Private companies** providing technology services to Public Administrations
- **Technology providers** in public procurement processes that require ENS alignment

> The ENS allows certification of both entire organizations and specific information systems (for example, a critical application, a specific infrastructure, etc.).

The usual ENS certification process includes the following stages:

1. **Internal self-assessment:**  
   The organization conducts an internal review of its ENS compliance level. It identifies gaps, prepares the statement of applicability, and defines its compliance profile.

2. **Audit by an accredited entity:**  
   A certification company recognized by ENAC (National Accreditation Entity) evaluates the information system or organization. The audit verifies the implementation of the measures as declared.

3. **Conformity report:**  
   If the audit is satisfactory, a report is issued justifying that the system meets the ENS requirements at the corresponding level.

4. **Certificate issuance by the CCN:**  
   The National Cryptologic Center (CCN), as the competent authority, approves the report and issues the certificate of conformity.

### Certification Levels

Certification can be issued for one of the following levels, according to risk analysis and system impact:

- **Basic Level:** For systems without sensitive information and limited impact.
- **Medium Level:** For systems with appreciable impact on operations, services, or reputation.
- **High Level:** For critical systems affecting essential services, specially protected data, or strategic state functions.

> 🔐 The choice of certification level determines the number and stringency of measures to be implemented.

Certification is important because it demonstrates commitment to information security, is mandatory for certain public administration information systems, may be a requirement for participating in public tenders, and increases the confidence of citizens and other organizations.

### Validity and Renewal

ENS certification is **valid for 2 years** from the date of issue. Once this period has elapsed, the organization must: undergo another audit, update its statement of applicability, and demonstrate improvements or maintenance in its security system.

Renewal ensures that the system remains **effective, up-to-date, and compliant with current regulatory and technological requirements**.

## ENS vs ISO 27001 Comparison

| Feature                    | ENS                                       | ISO 27001                           |
|----------------------------|-------------------------------------------|-------------------------------------|
| Scope                      | Public sector in Spain                    | International                       |
| Mandatory                  | Yes, for public administrations and providers | No (voluntary)                      |
| Measures / Controls        | 73 specific measures                      | 114 controls in 14 domains          |
| Application levels         | Low, Medium, High                         | Not defined                         |
| Certification              | 2 years                                   | 3 years                             |
| Risk analysis              | Mandatory                                 | Mandatory                           |
| Compatibility              | Compatible with ISO 27001                 | Can be a basis for ENS              |

### Is ISO 27001 certification enough to comply with the ENS? 🤔

**ISO/IEC 27001** certification is an internationally recognized standard for information security management and can serve as a solid foundation for meeting many ENS requirements. However, **it is not sufficient by itself** to guarantee full compliance with the National Security Framework. Key differences are explained below:

1. **Additional specific requirements:**  
   The ENS establishes **73 security measures** distributed in three frameworks (organizational, operational, and protection), each with application levels (BASE, Reinforced, High). These requirements are specific and mandatory and are not detailed in ISO 27001.

2. **Legal framework and scope:**  
   The ENS is **mandatory** in Spain for all Public Administrations and companies providing public technology services. In contrast, ISO 27001 is a **voluntary** standard of general application.

3. **Distinct audit and certification processes:**  
   ENS certification is managed through entities accredited by ENAC, and the process includes **validation and issuance of the certificate by the National Cryptologic Center (CCN)**. ISO 27001 does not require this level of institutional control in its certification process.

4. **Partial compatibility between controls:**  
   ISO 27001 includes **114 controls grouped into 14 domains**, which do not match one-to-one with ENS measures. Although there is overlap, many specific aspects of the ENS (e.g., measures for classified systems, criticality levels, compliance profile) are not covered by ISO.

### How can ISO 27001 help you comply with the ENS?

Implementing ISO 27001 can facilitate ENS compliance in several ways:

- Establishes a solid security governance foundation.
- Fosters a culture of continuous improvement compatible with the ENS approach.
- Standardizes procedures such as risk analysis, documentation, and internal audit.

> 💡 If your organization is already ISO 27001 certified, it is recommended to conduct a **gap analysis** with respect to ENS requirements. This analysis will allow you to **reuse part of the work already done** and focus on the **additional specific requirements** of the Spanish framework.

## Conclusion 🏁

The ENS plays a crucial role in the cybersecurity of the Spanish public sector, providing a common framework for the protection of information and electronic services. Its effective implementation is essential to ensure trust in e-government and protect citizens' data. The ENS seeks to apply a cycle of continuous improvement, following the steps of planning, action, checking, and acting, thus ensuring the constant evolution and adaptation of security measures to the changing challenges of the digital environment. 🔐🇪🇸👥

