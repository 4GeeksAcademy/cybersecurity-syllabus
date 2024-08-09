---
title: "Security Incident Management Process and Techniques"  
subtitle: "Optimizing Security Incident Resolution: Strategies, Processes, and Tools for Efficient Management | ISO 27001 Standards"  
tags: ["networks"]  
authors: ["blindma1den", "lorenagubaira"]

---

Incidents in information security seem inevitable nowadays, so we have no choice but to consider how we are going to manage such incidents in the most agile and efficient way for the organization.

That is why the standard **[ISO 27001](https://normaiso27001.es/)** devotes a chapter to establishing controls for managing information security incidents, and has even dedicated a specific document with the principles for managing information security incidents.

### Objective 1: Incident management and information security improvements

Ensure a consistent and effective approach to information security incident management, including reporting security events and weaknesses.

As we have mentioned, a risk analysis cannot conclude with the total elimination of vulnerabilities as this would not even be practical or feasible yet, so residual vulnerabilities always exist. We are sure to have information security incidents, as well as threats and vulnerabilities not identified so far.

It is for that reason that we must implement a tool for the management of the incidents of the security of the information with the following general aims

- **Detect**, report, and evaluate information security incidents
- **Respond** to incidents
- **To report** vulnerabilities
- **Learning** from Information Security incidents

## Incident resolution steps

Security incident management is based on different steps, which include:

![Incident Management](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/04-seguridad-redes/incident-management/incident-management1.us.png)

> *NOTE: These steps could be different states than an incident so it is also important to inform the user of any changes in the incident status.*

- **1. Incident notification:** A person detects an event that may damage the organization's operation, so they must communicate the incident according to the organization's communication procedures (usually an email, phone call, software tool, etc.).
- **2. Classification of the incident:** A person receives notification of the incident and, according to the various parameters, it is classified. The person who detects the incident can also make a classification, but it is a technical expert who classifies it appropriately.
- **3. Incident handling:** Once the incident is classified and the severity and agreed time for resolution is known, a technical expert must decide on the actions required to resolve the incident.
- **4. Close the incident:** Once the incident is resolved, all information generated during the handling is recorded and finally the person who first sent the notification of the incident that was closed is notified.
- **5. Knowledge base:** All information generated during incident handling is critical for possible similar incidents in the future, as well as for gathering evidence. Imagine that a user updates a system and after this, the system shuts down (unintentionally). The user then opens an incident and the incident is resolved and closed. The information generated to resolve the incident is recorded, so if the problem occurs again in the future, they can simply refer to the knowledge base; they will have the perfect solution without wasting time.

> 👉 In this sense the standard establishes a series of controls starting with the organization that we must carry out to undertake this task.

## Controls for the management of information security incidents

### Responsible and procedures

Firstly, we must have implemented and documented procedures to guide us in the process of information security incident management.

These processes must take into account:

- **Responsibilities**.
    - Define a person or persons responsible for incident management who must ensure that the appropriate procedures are developed so that all the tasks or processes necessary to manage incidents are carried out.
    - Define the responsibilities of each employee in both the collaboration for the response and the need for communication of information security incidents.
- **Processes or procedures**
    - Have procedures in place for the detection, analysis and reporting of information security incidents.
    - Develop procedures for incident reporting.
    - That these procedures are known (That each employee is aware of the incident reporting procedures and their responsibilities).
    - Adequate communication channels are in place (ensure that information collection points for information security incidents and events are defined).
- **Training**
    - Ensure the competence of incident handling and resolution personnel. Maintain a training plan for those dealing with information security incidents.

## Information security event reporting

This control asks us to establish communication channels for all events or incidents. These channels must naturally be established with those responsible for incident management.

All users must be informed and familiar with the notification mechanisms. By users, we mean both internal and external users.

First, let us distinguish between two more or less similar concepts that we must separate for a correct analysis of incidents in Information Security

### Information security event

Any occurrence identified in an information system, service or network state that indicates a possible information security breach, policy or control failure, or a previously unknown situation that may be relevant to security.

### Information security incident

When the event can be classified as undesirable or unexpected within information security events and also have a significant likelihood of compromising business operations and pose a serious threat to information security.

An information security event does not necessarily mean an implication on confidentiality, integrity, or availability, sometimes we even want it, we can learn from it and tighten security.

- The incident is always undesired

### Clarifying concepts: threat, vulnerability, event and incident

![Incident Management - Threat, Vulnerability, Event and Incident](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/04-seguridad-redes/incident-management/incident-management2.us.png)

## Threats to Information Security

> *A threat refers to anything that has the potential to cause serious damage to an information system or asset. A threat is something that may or may not happen, but has the potential to cause serious harm.*
>
> *Threats can result in attacks on computer systems, networks and more.*

### Vulnerability in Information Security

Refers to a weakness or flaw in a system or information asset that can leave it exposed to a threat or attack. A vulnerability can also refer to any type of weakness in an information system itself, in a set of procedures, or in anything that leaves information security exposed to a threat.

### Information Security Event

An information security event is a change in the day-to-day operations of an information technology network or service that indicates that a security policy may have been violated or a security protection may have failed.

### Information Security Incident

A single or series of unwanted or unexpected information security events that have a significant likelihood of compromising business operations and threatening information security. For example, an anomalous behavior on a system is an event, however, if evidence of the virus is found on the system, it can be considered a security incident.

### Reporting of information security weaknesses

Incident reporting should be accompanied by a report of possible system weaknesses that are detected at any time. This should be supported by:

- Communication to users of the requirement to observe and report any information security weaknesses seen or suspected in systems or services.

> 💡 It is advised to warn that users who test the strength or weakness of systems to see if they find a vulnerability will be considered by the company as misuse of the system.

### Evaluation and decision on information security events

As we have already seen in the previous points, information security events can be classified as simple events, or they can become Information Security Indecent.

For this purpose, it establishes:

- An incident prioritization criterion depending on the system or service affected, the user, etc.
- Incident evaluation must be performed by both the user and the management team who must review the priority.
- Keep a record of the evaluation of incidents to be able to analyze the quality parameters, both in their resolution and their classification.

There are many ways to classify incidents, but the usual way is to consider two parameters:

- **Impact:** Damage caused to the business (in economic terms, image, etc.).
- **Urgency:** The speed with which the organization needs to correct the incident.

The combination of these parameters will allow us to determine the priority of each incident, so in this way, you can establish, for example, the following table of values:

![Incident Management - Threat Level](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/04-seguridad-redes/incident-management/incident-management3.us.png)

Thus we could classify the incidents into:

- **CRITICAL LEVEL (5 to 6)**
- **SERIOUS LEVEL (4)**
- **MILD LEVEL (1 to 2)**

### Security Incident Response

It is about controlling the process of information security incident resolution.

The controls to be established would be.

- Evaluate whether the organization can resolve the incident by itself or needs help from third parties.
- Keep a record of the evidence of the incidents.
- Establish the necessary communications system between users and the incident management team or whoever should be informed of the actions and status of the incident resolution process.
- Record the actions taken and the results of these actions.
- Formally close the issue when it has been resolved.
- Perform an analysis to determine the causes of each incident.

### Learning from Information Security Incidents

As we have already mentioned, incidents are not only a problem to solve, but also a source of information for the resolution of future incidents or the improvement of information security.

The standard's controls for maintaining a knowledge base on information security incidents are:

- Creation of a log that considers
- Volume of incidents that have occurred
- Type of incidents produced
- Cost of incident resolution
- Impact of the incident
- Solution applied

The information on the incidents can help us to:

- Identify the most recurrent and high impact incidents.
- Improve our management system with new controls and risk assessment criteria.
- Conduct training for users to avoid incidents and for incident managers to improve incident resolution.

> 👉 For this last point it is recommended to use Non-real data for training.

### Evidence collection

Information security incidents may require subsequent actions such as sanctions or legal action. Recovering evidence for later use can become a headache if we have not foreseen some mechanism to save it.

In this chapter, the standard requires us to keep information about incidents in a form that we can retrieve:

- Logins and logouts
- The identifications
- The status of devices and networks
- Evidence of briefings, documentation of responsibilities and security roles of personnel

***You should not overlook...***

Sometimes a forensic investigation of computer evidence may be necessary. Consideration should be given to maintaining secure access rights to information to enable a forensic investigation to be carried out.

To do so, be aware of the various requirements of the relevant jurisdictions and be prepared by prior communication to personnel or by signing contractual clauses.

- **Another issue is the preservation of evidence...**

Incidents we do not usually know how they will end and whether they will require further legal or disciplinary action. Certain incidents may lead to the deletion of evidence to hide the person responsible for them, which is why it is recommended to establish systems for copying and preservation of records so that certain evidence cannot be so easily deleted.

- **Security of the evidence...**

Finally, if possible or if it is identified as necessary, evidence collection systems can be certified or independent (approved and legal) means of surveillance and control can be maintained to strengthen the evidence for legal action.

## Security incident management tools

We would like to emphasize that incident management is not only done with a tool but with the right selection of tools, best practices, and DevOps team. Let's talk about our favorite incident management tools that we believe make a difference in the incident management process:

- [BigPanda](https://www.bigpanda.io/)
- [OnPage](https://www.onpage.com/)
- [NinjaRMM](https://www.ninjarmm.com/)
- [Rundeck](https://www.rundeck.com/open-source)
- [ServiceNow](https://www.servicenow.com/)
- [Issuetrak](https://www.issuetrak.com/)
- [AlertOps](https://alertops.com/)
- [Atlassian](https://www.atlassian.com/software/jira/service-management/features/service-desk)

Other great tools help track incidents, each incident can be tracked and documented, so trends can be identified and comparisons made over time. Some chat rooms allow real-time text communication to diagnose and resolve the incident as a team and provide a rich set of data for response analysis later. Additionally, video chat complements text chat for many incidents; team video chat can help discuss findings and map out a response strategy. The extremely important alert system integrates with your supervisory system and manages on-call rotations and escalations. Documentation tools, such as Confluence, can capture incident status documents and postmortems.