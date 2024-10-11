---
title: "ENS Implementation and Security Measures"
subtitle: "🛡️ Understanding the key components of the implementation and security measures in Spain's National Security Scheme (ENS)"
tags: ["spain-national-security-framework", "cybersecurity"]
authors: ["alesanchezr"]

---

# ENS Implementation and Security Measures

> Before we start, we thoroughly cover ENS (Esquema Nacional de Seguridad) in several lessons. This lesson soly focused on the security measures and implementation.
> Read an [Introduction to ENS](https://4geeks.com/lesson/spain-national-security-scheme-esquema-nacional-de-seguridad) and learn more about the [ENS Organizational and operational framework](https://4geeks.com/lesson/ens-organizational-and-operational-framework).

In order to implement Spain's 🇪🇸 National Security Framework (ENS) we first need to name a committee that will be responsible for the implementation of the scheme.

![ENS Implementation](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/12-ens/esquema-nacional-de-seguridad.jpg?raw=true)

## Who is responsible for the implementation of the ENS inside an organization?

Since 2022 ENS is governed by [Real Decreto 311/2022](https://www.boe.es/buscar/act.php?id=BOE-A-2022-12345) and establishes 4 roles in 2 levels according to its article 11. These roles are also detailed in [the Guía 801 of the National Cryptographic Center](https://www.ccn-cert.cni.es/es/series-ccn-stic/800-guia-esquema-nacional-de-seguridad/501-ccn-stic-801-responsabilidades-y-funciones-en-el-ens/file?format=html).

### Committee composition

> 💡 While the ENS defines distinct roles with specific responsibilities, it's important to note that in practice, especially in smaller organizations or those with limited resources

This committee will be composed of a president who will have the role of moderator of the meetings and in case of a tie vote, he will have the casting vote, some members who will have voice and vote within the meetings and a secretary of the committee who is in charge of the convocations and reads the minutes of the last meetings:


### Information Officer 🧑‍💼📊

Determines the security requirements of the information treated according to the parameters of Annex I of the ENS. It can be a person or a collegiate body.

### Service Responsible 🛠️👨‍💼

- Helps determine the security requirements of the services being provided, identifying the security levels of these by evaluating the impact of incidents on them, and providing the necessary information for performing the respective risk analyses to establish the safeguards to be implemented.
- Counts on the help of the system responsible to perform its tasks

### Security Officer (CISO) 🕵️‍♂️🔒

- Develop Plans with Measures to manage detected risks.
- Supervise and develop security policies, regulations and procedures, their effectiveness... Conducting periodic controls.
- Prepare the document of Declaration of Applicability of security measures.
- Promote and train on the organization's "best practices" in cybersecurity matters.
- Submit notifications of incidents with adverse effects to the competent authority.
- Receive, interpret and supervise the application of instructions and guidelines from the competent authority.
- Collect and provide information or documentation to the competent authority.

### System Responsible 💻🛠️

- Develop, operate and maintain the system.
- Define the typology and policy of System Management.
- The connection/disconnection of equipment/users.
- Approve operational changes that affect the system.
- Decide on security measures to be applied by component suppliers.
- Implement, control and integrate specific security measures.
- The authorized configuration and approval of substantial modifications to hardware and software.
- Keep the Risk Analysis in the system updated.
- Determine the System Category (process in Annex I ENS) and the security measures that should be applied (Annex II ENS).
- Develop and approve system documentation and determine the responsibilities of those involved in the maintenance, exploitation, implementation and supervision of the system.
- Investigate Security Incidents and communicate them to whom it may concern if appropriate.
- Establish Contingency or Emergency Plans and carry out scheduled exercises.
- Agree on the use of certain information or service provision if there are serious vulnerabilities in the system, a decision agreed upon with the Security Officer beforehand.

## Implementation of the ENS

![ENS Implementation](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/12-ens/proceso-ens.png?raw=true)

To implement an Information Security Management System (ISMS) that complies with Spain’s **Esquema Nacional de Seguridad (ENS)**, you'll need to follow a structured approach that aligns with the regulatory framework. Below is a step-by-step implementation plan:

### 1. **Understand the ENS Requirements**

- **Classification of systems:** The ENS defines different levels of security (Basic, Intermediate, and High). Start by classifying your information systems based on the sensitivity and criticality of the data handled.
- **Security Measures:** Each level requires specific security measures (administrative, technical, and operational). Review Annex II and Annex III of the ENS for the detailed requirements.
- **Legal Review:** Current state of the organization compliance with related Spanish laws (e.g., GDPR, Spanish Data Protection Act).

### 2. **Gap Analysis**

- **Current State Assessment:** Conduct a comprehensive analysis of your current security posture. Evaluate existing security measures, policies, and procedures.
- **Gap Identification:** Compare your current security controls against the ENS requirements. Identify gaps in both technical (e.g., firewalls, encryption) and organizational (e.g., policies, risk management) aspects.

### 3. **Set Up a Security Governance Framework**

- **Appoint a Security Officer:** Designate a security officer responsible for ENS compliance and ensure they are appropriately trained.
- **Create a Security Committee:** Establish a committee with representatives from IT, legal, HR, and other relevant departments to oversee the security program.

### 4. **Develop the ISMS Framework**

- **Policy Development:** Create or update information security policies to reflect ENS requirements. Include policies on access control, incident management, and data classification.
- **Risk Management Process:** Implement a formal risk management process, including risk identification, assessment, and treatment. Ensure that the risk management strategy aligns with ENS guidelines.
- **Asset Management:** Identify and classify assets (hardware, software, data) according to their importance to your organization. Define appropriate protection measures for each asset.

### 5. **Technical Security Controls Implementation**

- **Encryption:** Use strong encryption for sensitive data in storage and transit.
- **Access Control:** Implement role-based access controls (RBAC) and two-factor authentication (2FA) for all critical systems.
- **Monitoring and Incident Detection:** Install monitoring tools (SIEM, IDS/IPS) to detect and respond to incidents. Align this with Spain's regulatory requirements for incident reporting.
- **Backup and Recovery:** Establish a reliable backup and disaster recovery system. Ensure that backups are encrypted and regularly tested.
- **Perimeter Security:** Harden perimeter defenses using firewalls, intrusion detection systems, and network segmentation.

### 6. **Administrative and Organizational Measures**

- **Awareness and Training Programs:** Develop and execute a security awareness program for all employees, covering topics like phishing, safe data handling, and reporting incidents.
- **Incident Response Plan:** Create an incident response plan that complies with ENS guidelines. Ensure it covers incident detection, response, recovery, and reporting.
- **Continuous Monitoring:** Set up a monitoring process for security threats, ensuring periodic audits and vulnerability assessments are conducted.

### 7. **Third-Party and Supplier Management**

- **Supplier Risk Assessment:** Evaluate the security measures of third-party service providers to ensure they comply with ENS requirements.
- **Contractual Obligations:** Incorporate ENS-related clauses into contracts with suppliers and partners, especially those handling sensitive information.

### 8. **Audit and Certification**

- **Internal Audit:** Perform regular internal audits to ensure ongoing compliance with ENS. Address any non-conformities identified during the audits.
- **ENS Certification:** Engage with accredited auditors to obtain ENS certification. This step is crucial for public administrations and suppliers working with the public sector.
- **External Audit:** Depending on your security level, you may need to undergo an external audit for official certification (particularly for Intermediate and High levels).

### 9. **Incident Management and Reporting**

- **Incident Handling Process:** Implement a formal process for incident reporting and response. Ensure that incidents are reported to the relevant authorities, following the ENS guidelines.
- **Continuous Improvement:** After incidents, conduct a post-mortem to update the ISMS and prevent similar incidents in the future.

### 10. **Documentation and Reporting**

- **Security Plan:** Document the security plan, which should include objectives, risk management approaches, and security measures in line with ENS.
- **Conformity Reports:** Produce regular conformity reports that demonstrate adherence to ENS requirements.
- **Communication with Authorities:** Ensure regular communication with regulatory authorities for incident reporting and certifications.

### 11. **Continuous Improvement**

- **Regular Review:** Periodically review and update your ISMS to align with evolving threats and ENS updates.
- **Penetration Testing:** Conduct annual penetration tests to assess the effectiveness of your security controls.
- **Employee Re-training:** Regularly refresh employees' security awareness through ongoing training programs.

## ENS Protective Measures

The following is a list of all the protective measures that we must implement to comply with the ENS.

### Protection of facilities 🔒🏢

The protection of facilities stands as a fundamental pillar in the National Security Scheme, playing a critical role in preserving the integrity and information of a public entity. This component, which ranges from strategic infrastructures to key buildings, becomes an essential link for secure and sustainable development.

The protection of facilities refers to the application of measures and strategies aimed at physically and strategically safeguarding places and structures considered crucial for the functioning and well-being of a society. These facilities can range from power plants and water treatment plants to government buildings and research centers.

Among its controls we have:

#### Separate areas with access control 🔒🚧

According to the ENS, the infrastructure of all systems must follow a distribution of separate zones according to their function and have access control for these zones

| Dimensions |  |  | Protection measures |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Operational Framework |
| Applies | = | = | mp.if.1 | Separate areas with access control |

#### Identification of people 🧑‍💼🚧

All entities must have access control to the premises and with entry and exit registration

| Dimensions |  |  | Protection measures |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Operational Framework |
| Applies | = | = | mp.if.2 | Identification of people |

#### Conditioning of premises 🌡️💧

All facilities must have favorable temperature and humidity conditions, and have protection against threats obtained from risk analysis

| Dimensions |  |  | Protection measures |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Operational Framework |
| Applies | = | = | mp.if.3 | Conditioning of premises |

#### Electrical power 🔌💡

According to the ENS, facilities must have power supply in case of electrical failure or at least guarantee the correct operation of emergency lights

| Dimensions |  |  | Protection measures |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Operational Framework |
| Applies | + | = | mp.if.4 | Electrical power |

#### Fire protection 🔥🚨

Facilities must have fire protection, as well as equipment to extinguish fire

| Dimensions |  |  | Protection measures |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Operational Framework |
| Applies | = | = | mp.if.5 | Fire protection |

#### Flood protection 🌊🚨

As with the previous point, there must be protection in case of floods, we can reference this protection according to the industrial regulations followed in the installation and adaptation of the building for fires and floods

In this case, controls must be applied in medium and high category entities.

| Dimensions |  |  | Protection measures |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Operational Framework |
| Does not apply | Applies | = | mp.if.6 | Flood protection |

#### Equipment entry and exit registry 📦🚧

All equipment that leaves and enters must be identified and documented, as well as who authorized it, the date of departure and the estimated time.

| Dimensions |  |  | Protection measures |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Operational Framework |
| Applies | = | = | mp.if.7 | Equipment entry and exit registry |

#### Alternative facilities 🚧🚨

Public entities with high category systems must have alternative facilities in case an incident takes the main facility out of operation, these alternative facilities must have the same security guarantees as the usual ones

| Dimensions |  |  | Protection measures |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Operational Framework |
| Does not apply | Does not apply | Applies | mp.if.1 | Alternative facilities |

### Protection of assets and personnel

The protection of assets and personnel involves the implementation of strategies and measures aimed at safeguarding both the critical resources of the country's public entities, as well as strategic information and the security of its citizens.

Within the ENS, personnel management and protection is mostly related to the function and obligations within their job position as well as training and awareness regarding security, its controls are:

#### Job characterization 🧑‍💼📄

In this control, documentation must be stipulated with the security responsibilities of each employee according to their job position, as well as the requirements that must be met to occupy the job position and in personnel selection.

| Dimensions |  |  | Protection measures |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Operational Framework |
| Does not apply | Applies | = | mp.if.1 | Job characterization |

#### Duties and obligations 🧑‍💼🔒

The duties and responsibilities regarding security in the job position must be explained. Disciplinary measures must also be taken in case of non-compliance with duties in the job position

| Dimensions |  |  | Protection measures |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Operational Framework |
| Applies | = | = | mp.per2 | Duties and obligations |

#### Awareness 🧑‍🏫🔒

The ENS explains that talks should be given periodically to staff to remind them of security regulations and incident management procedures

| Dimensions |  |  | Protection measures |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Operational Framework |
| Applies | = | = | mp.per3 | Awareness |

#### Training 🧑‍🏫🔒

This control involves correctly managing the institution's information and training staff so they know how to react to different types of incidents

| Dimensions |  |  | Protection measures |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Operational Framework |
| Applies | = | = | mp.per4 | Training |

#### Alternative Personnel 🧑‍💼🚨

There must be personnel who take charge of functions in case of any unavailability of regular personnel.

| Dimensions |  |  | Protection measures |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Operational Framework |
| Does not apply | Does not apply | Applies | mp.per5 | Alternative Personnel |

Regarding the protection of assets, the standard is more oriented towards workstations and their manipulation and protection

#### Clear desk 🧑‍💼🚧

This control establishes the policy that the work desk must be clean and only the activity that is being carried out at the moment should be performed, material that is not being used must be stored in a closed place

| Dimensions |  |  | Protection measures |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Operational Framework |
| Does not apply | Does not apply | Applies | mp.eq1 | Clear desk |

#### Workstation lock 🔒🧑‍💻

In medium category systems, workstations must have a lock after a period of inactivity and require authentication to be reactivated, mainly for the purpose of closing open sessions.

| Dimensions |  |  | Protection measures |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Operational Framework |
| Does not apply | Does not apply | Applies | mp.eq2 | Workstation lock |

#### Protection of portable equipment 📱🚧

This is the most rigorous control within the asset protection controls and it is that there must be an inventory of all portable equipment that leaves the facility along with the person responsible for it, and there must be documentation of all information procedures on any incident that may exist with said equipment

This equipment must also have limitation of accessible information and storage of sensitive information, it is advisable to handle information with a high level of encryption

| Dimensions |  |  | Protection measures |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Operational Framework |
| Does not apply | Does not apply | Applies | mp.eq3 | Protection of portable equipment |

#### Alternative means 🚧🚨

Alternative equipment must be available in case the usual equipment fails.

| Dimensions |  |  | Protection measures |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Operational Framework |
| Does not apply | Does not apply | Applies | mp.per4 | Alternative means |

### Protection of information and services

It is important to have protection of the information that can be handled within a public entity, as well as its services, which is why the ENS maintains controls regarding these areas which we will see below

#### Personal data 🧑‍💼📄

This control is based on systems with personal data, which must meet the requirements of the Organic Law on Data Protection and Guarantee of Digital Rights

| Dimensions |  |  | Information protection |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Operational Framework |
| Applies | = | = | mp.info1 | Personal data |

#### Information classification 🧑‍💼📄

This policy gives the information manager the responsibility to determine its classification and describe the criteria for labeling information according to its security level

| Dimensions |  |  | Information protection |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Operational Framework |
| Applies | + | = | mp.info2 | Information classification |

#### Encryption 🔒🔑

There must be high-level encryption for stored and transmitted information

| Dimensions |  |  | Information protection |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Operational Framework |
| Does not apply | Does not apply | Applies | mp.info3 | Encryption |

#### Electronic signature 🔑🖋️

The electronic signature must exist within systems and documents to verify their integrity and authenticity

| Dimensions |  |  | Information protection |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Operational Framework |
| Applies | + | ++ | mp.info4 | Electronic signature |

#### Time stamps 🕒🔑

Time stamps help analyze the integrity of information when it is required temporarily, generally oriented to data used as electronic evidence

| Dimensions |  |  | Information protection |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Operational Framework |
| Applies | = | = | mp.info5 | Time stamps |

#### Document cleaning 🧑‍💼📄

Information should be removed in hidden fields, metadata and special revisions especially when the document is made public

| Dimensions |  |  | Information protection |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Operational Framework |
| Applies | = | = | mp.info6 | Document cleaning |

#### Backups 💾📄

There must be backups that have the same level of security as the original data and must cover both work information and applications and keys

| Dimensions |  |  | Information protection |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Operational Framework |
| Applies | = | = | mp.info9 | Backups |

Within the protection of services, the following controls are established

#### Email protection 📧🔒

There must be security measures that will be used to prevent incidents such as SPAM or malware, in addition to documentation explaining the safe use of email

It is advisable to use a trusted email provider

| Dimensions |  |  | Service protection |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Operational Framework |
| Applies | = | = | mp.s.1 | Email protection |

#### Protection of services and applications 📧🧑‍💻

There must be security measures to prevent incidents such as URL and cookie manipulation, privilege escalation, among others. For high category systems, the use of qualified authentication certificates is recommended

| Dimensions |  |  | Service protection |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Operational Framework |
| Applies | = | + | mp.s.2 | Protection of web services and applications |

#### Protection against denial of service 🚨🧑‍💻

There must be protection against these types of attacks, such as request control and load balancers, as well as systems to detect the attack and procedures to react to the attack

| Dimensions |  |  | Service protection |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Operational Framework |
| Does not apply | Applies | + | mp.s.8 | Protection against denial of service |

#### Alternative means 🚨🧑‍💻

There must be availability of alternative means to provide the service of applications with the same guarantees as the usual means, this can be included in the business continuity plan

| Dimensions |  |  | Service protection |  |
| --- | --- | --- | --- | --- |
| L | M | H | Org | Operational Framework |
| Does not apply | Does not apply | Applies | mp.s.9 | Alternative means |
