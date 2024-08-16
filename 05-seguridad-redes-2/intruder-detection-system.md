---
title: "Intrusion Detection Systems (IDS)"
subtitle: "Comprehensive Guide to Intrusion Detection Systems (IDS): Types, Functionality, and Best Practices for Network Security"
technologies: ["cybersecurity","networks"]
authors: ["blindma1den", "lorenagubaira", "alesanchezr"]

---

The Intrusion Detection System (IDS) consists of a set of methods and techniques to detect suspicious activity on a computer resource or resources. That is, events that suggest anomalous, incorrect, or inappropriate behavior on a system.

An intrusion detection system can be described as a process of detecting and monitoring events that occur on a network. This system listens to and analyzes all the information circulating on a network, helping to understand attacks, estimate the damage caused, and try to prevent other attacks. To detect intrusions in a system, IDSs use three types of information: a history of events, the current configuration of the system, and finally, active system processes or rules.

![intrusion detection system](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/1intrusion-detection-systen.png?raw=true)

## **What is an IDS and How Does It Work?**

Even though we have the firewall enabled, we generally have many open ports, such as 80 and 443 for web applications. Therefore, we must have an additional system to help us control these open doors. For greater control, we should use an IDS, which is an intrusion and vulnerability detection system. There are active IDSs and passive IDSs. The former generates log entries and alerts. The latter performs the same functions but also takes actions, such as blocking IP addresses or closing access to restricted ports.

From a software perspective, there are different types of tools: host-based intrusion detection systems (HIDS), network intrusion detection systems (NIDS), signature-based intrusion detection systems (SIDS), and anomaly-based intrusion detection systems.

![network intrusion detection](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/2network-intrusion-detection.png?raw=true)

IDSs use three methods to detect traffic: anomaly detection, protocol analysis, and signature analysis.

- **Anomaly Detection:** The aim is to detect abnormal behavior. An example would be an unusually high volume of ICMP traffic (used by ping), which would indicate that we are the target or the source of a DDoS (Denial of Service) attack.
- **Protocol Analysis:** This looks for application traffic that does not meet the standard protocol.
- **Signature Analysis:** This identifies known attacks or harmful behaviors by comparing them to a database of signatures. It is usually the most effective technique as it only detects attacks or intrusions that have previously been successful elsewhere, making them easy to identify.

It's important for an IDS to update its information regularly to keep its analysis techniques and signature databases current.

There are organizations, associations, and companies that keep us updated on the latest techniques in intrusion and attacks. The main ones are:

- **Bugtraq:** A mailing list dedicated to the publication of vulnerabilities, their use, and fixes. ([Security Focus](https://www.securityfocus.com/))
- **CERT:** *Computer Emergency Response Team.* An organization that studies vulnerabilities, researches network and security assessments, and offers security-related services. ([Wikipedia Entry](https://es.wikipedia.org/wiki/Equipo_de_Respuesta_ante_Emergencias_Inform%C3%A1ticas))
- **CIAC:** *Computer Incident Advisory Capability.* An alert and research organization managed by the U.S. Department of Energy. ([Energy Department](https://www.energy.gov/cio/about-our-services/integrated-joint-cybersecurity-coordination-center))

### **Tasks of an IDS**

An IDS performs two fundamental tasks:

- **Prevention:** This is done using tools called sensors that listen to network or computer traffic and identify attacks by applying rules, pattern recognition, or intelligent techniques.
- **Reaction:** This involves detecting intrusion patterns in network service traces or system behavior.

There are statistical indicators of sensitivity, specificity, and precision that help verify the effectiveness of an IDS, based on the following concepts:

- **True Positives (TP):** An existing intrusion correctly detected.
- **False Positives (FP):** A non-existent intrusion incorrectly detected.
- **False Negatives (FN):** An existing intrusion not detected.
- **True Negatives (TN):** A non-existent intrusion not detected.

### **Types of IDS**

There are different classifications of IDSs based on their approach, data source, structure, and behavior.

![intrusion detection system classification](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/3intrusion-detection-system-clasification.us.png?raw=true)

## **Based on Approach**

Two groups are presented: misuse detection systems, which compare signatures with collected information, and anomaly detection systems, which use statistical techniques to distinguish normal from abnormal behavior.

- **Anomaly Detection:** It is necessary to define what is considered normal system behavior through activity learning to classify deviating behaviors as suspicious. These systems are prone to false positives, which are triggered when normal activity sets off an alert. They depend on the quality of the learning process. There are three different techniques for anomaly detection in a system:
  
  - **Knowledge-Based Systems:** Represent the initial stage of IDSs and rely on security breaches detected using rules. They are more reliable and provide better performance against known attacks, with the drawback of limited ability to detect new attacks not included in the signature database.
  - **Statistical Method-Based Systems:** Based on activity profiles defined by user behavior regarding files, programs, logs, etc. This is done by establishing metrics and statistical models.
  - **Machine Learning-Based Systems:** These are the most developed for modeling normal behaviors and aim to improve detection results, reduce false positives, and decrease computation time. One advantage is the ability to capture attack characteristics and add them to a database as new signatures, allowing the signature base to be updated quickly.
  
- **Misuse Detection (Signature/Rule-Based Detection):** Misuse detection systems monitor activities occurring in a system and compare them with a database of attack signatures. When an activity matches one of these signatures, an alert is generated. These systems are easy to adapt since updating the database is as simple as writing a new rule or obtaining it from a third party.

  - **Expert Systems:** Knowledge encoded through implication rules (condition-action). If all conditions are met, the action or rule is applied. The disadvantage is that the rules are not sequential, making it difficult to isolate intrusion steps over time.
  - **Signature Detection:** Compares events occurring in the system with stored signatures in the database to find similarities.
  - **State Transition Analysis:** Attacks are represented as a sequence of transitions (finite state machine). When a state considered an intrusion is reached, an alarm is triggered.
  
- **Hybrids:** Signature-based IDSs are more reliable and provide better performance against known attacks, but they are deficient against new attacks. Anomaly-based IDSs can detect unknown attacks but have inferior performance. Hybrid systems are a combination of both, and therefore, they can be adjusted to operate as both types of detectors, improving functionality, attack detection, and performance.

## **Based on Data Origin**

Three types of IDSs are found based on the sources of information used:

- **HIDS (*Host-based Intrusion Detection Systems*):** Host-based IDSs only process information from user activities and services on a specific machine. They allow monitoring of data generated by a user using *syslog1* and identifying threats and intrusions at the host level. A disadvantage is the need for trust in the system, which may be infected before installation, making it vulnerable to direct attacks.
  
- **NIDS (*Network Intrusion Detection Systems*):** NIDS are installed on a device in promiscuous mode, performing passive listening on the network without interfering with its use, analyzing traffic in real time, but they are ineffective against local attacks. New systems based on intelligent agents allow detection of new attacks using the concept of sentinels, which monitor the system to collect all necessary information for detection.

![network intrusion detection systems](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/4network-intrusion-detection-systems.png?raw=true)

- **Hybrid IDSs:** Hybrid systems take the best of both HIDS and NIDS. They allow local detection of systems, and a sensor on each network segment is responsible for monitoring. This way, HIDS needs are combined with NIDS, allowing the advantages of both architectures to be leveraged.

## **Based on Structure**

Classification based on control strategies:

- **Distributed Intrusion Detection System (DIDS):** Based on installation in a distributed system, with sensors located on several network devices. These sensors communicate with a central node where all information is received and cross-referenced, allowing for reliable detection of attacks and a global view that improves incident detection.

![distributed intrusion detection systems](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/5distributed-intrusion-detection-systems.png?raw=true)

- **Centralized Intrusion Detection System:** Employs sensors that transmit information to a central system for control, reducing equipment costs.

![centralized intrusion detection system](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/6centralized-instrusion-detection-system.us.png?raw=true)

## **Based on Behavior**

There are two types of IDSs depending on whether they perform prevention by listening to traffic or develop a defensive response when an attack is detected.

- **Passive IDS:** Only notifies the network administrator but does not act on the attack.

 It merely processes the information to detect intrusions, and once detected, it generates an alert.

- **Active IDS:** A type of IDS known as an Intrusion Prevention System (IPS). Unlike IDS, this technology does not just listen to network traffic and send alerts; it allows rules, as done in firewalls, to stop intrusions.
