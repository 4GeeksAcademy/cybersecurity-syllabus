---
title: "Security Architectures for Control Systems"  
subtitle: "Security Implementations in Control Networks: IDS, IPS, SIEM - An In-Depth Look at Architectures and Benefits"  
tags: ["networks"]  
authors: ["blindma1den", "lorenagubaira"]

---

## Security architecture with IDS

The first architecture, presented in the Figure, describes the placement of IDS-type devices to monitor traffic within the control network. For this purpose, all traffic passing through the routers/switches is brought to the IDS sensor through mirror ports (*mirror/SPAN*). A probe is also added to receive information from the firewall and thus control the traffic exchanged with the network corresponding to the enterprise zone. The IDSs must have the appropriate rules to generate the proper alerts that will be displayed to the corresponding operator or security administrator through the console.

![Security Architecture with IDS](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/04-seguridad-redes/security-architecture/aquitectura-2.us.png)

## Security architecture with IPS

The evolution of a security architecture with IDS involves blocking traffic. This requires the sensors to be in the middle of the traffic, instead of listening to the traffic through the mirror ports (*mirror/SPAN*), as shown in the Figure. The rule configuration must be appropriate so that the usual control traffic flow is not interrupted and only intrusions and security breaches are blocked. The situation of the IPS sensors is similar to that of the IDS sensors, and the operation will be the same, generating alerts that will be displayed on the IDS console.

![Security architecture with IPS](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/04-seguridad-redes/security-architecture/arquitectura3.us.png)

## Security architecture with SIEM

The Figure represents the installation of a SIEM within the control systems. It should be noted that the SIEM is dedicated to collecting and managing log events so that the data sources will come from all devices. In this case, care must be taken with communications, since all devices must be able to send their event logs to the SIEM, which may imply a network traffic overload. The best way to solve this overload is to have an exclusive network for sending these messages.

![Security architecture with SIEM](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/04-seguridad-redes/security-architecture/arquitectura4.us.png)

## Unified architecture with IDS, IPS and SIEM

The final representation (see Figure) shows how the three technologies are put together in a control system network architecture. The IPS would be for the upper levels, controlling the traffic exchanged between the control part and the corporate or business part; the IDS would manage the traffic between the control network and the field ones, reporting possible anomalies in the traffic; and the SIEM would collect the information from the largest possible number of devices, including process devices and network elements, as well as the alert information from both the IDS and the IPS.

The red lines shown in the figures indicate the points where both IDS sensors and IPS sensors connect to collect traffic and constitute a network connection. The monitoring network is used as a link between the IDS/IPS sensors and the central management core, and for this reason, no access to the network is required from any other part of the architecture. The green marked lines ending the SIEM show where information is obtained from and not actual network connections. The information will be sent through the existing connections by enabling the corresponding rules in the firewall (and if applicable in the IDS/IPS).

![Arquitectura de seguridad con SIEM](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/04-seguridad-redes/security-architecture/arquitectura5.us.png)

## CONCLUSIONS

Intrusion detection and prevention systems and event and incident processing and management systems provide a level of security to control systems as long as they are correctly configured and monitored. The configuration of a prevention system can involve many problems on a control system in production, so all the implications must be properly assessed and all possible tests must be carried out beforehand, including keeping the system only in detection mode until it is certain that critical traffic for the system will not be blocked and progressively fine-tuning the system so that it only detects or reports important events.

SIEMs provide system status information to security operators but are only useful if the information collected is properly analyzed. Centralizing all events in a single piece of equipment has the advantage that all actions occurring will be controlled in the minimum time and will not be lost by having to review multiple applications. The inclusion of these tools in the architecture of control systems can be complex depending on the system to be controlled, but the benefits will compensate for all the effort invested in the deployment, gaining control over the network, and ensuring the correct operation of the system without intrusions.