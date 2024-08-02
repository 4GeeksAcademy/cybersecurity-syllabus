---

title: "IDS/IPS Tools"  
subtitle: "Exploring IDS/IPS Tools: Snort, Suricata, Quickdraw, Zeek, OSSEC, and Wazuh - Advanced Protection for Networks and Control Systems"  
tags: ["cybersecurity", "networks"]  
authors: ["blindma1den", "lorenagubaira", "alesanchezr"]  

---

Intrusion Detection Systems (IDS) and Intrusion Prevention Systems (IPS) are essential tools for protecting networks and control systems against unauthorized access and cyberattacks. This article will explore some of the most notable tools in this field, starting with Snort and Suricata.

## Snort

Snort is among the most popular and widely used IDS/IPS tools. Developed by Sourcefire, now part of Cisco, Snort is used for real-time intrusion detection by analyzing network traffic and comparing packets against predefined rules. Its features include anomaly detection, protocol analysis, and logging suspicious packets for further analysis.

Snort is known for its flexibility and robustness, allowing network administrators to customize and update rules to fit the specific needs of their environment. Additionally, Snort's active community provides a comprehensive rule database and continuous updates to address new threats.

## Suricata

Suricata is another powerful IDS/IPS tool that competes directly with Snort. Developed by the Open Information Security Foundation (OISF), Suricata offers high-performance intrusion detection capabilities thanks to its support for multi-threaded packet processing, allowing it to leverage modern hardware architectures.

One of Suricata's standout features is its ability to perform deep packet inspection (DPI) and its integration with network flows, providing additional context for threat detection. Suricata also offers excellent compatibility with Snort rules, making it easy to implement in existing environments that already use Snort.

## Other IDS/IPS Tool Options

### Quickdraw

Quickdraw is a set of Snort rules created by Digital Bond. It enhances existing IDS by developing signatures for controlling traffic of certain protocols used in control systems. It also includes rules for detecting devices and vulnerabilities.

Quickdraw signatures (rules in Snort's jargon) identify unauthorized requests, erroneous protocol requests and responses, dangerous commands, and other situations that are likely or possible attacks. Currently, they have signatures available for four control system protocols, a set of signatures to identify control system vulnerabilities attacks, and a group of signatures that identify security events.

### Zeek (formerly Bro)

Zeek is another tool that serves as an IDS/IPS due to its network analysis features, similar to Snort and Suricata. It is based on a powerful analysis engine that allows high-performance network monitoring, analyzing protocols and application-layer information in real time.

![intruder prevention system Bro](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/ips1-bro.png?raw=true)

#### Zeek Architecture

Like other tools, Zeek also uses the libpcap library for its operation and can function on multiple networks. In addition to the portability gained through the use of libpcap, Zeek can also be a passive network tool, meaning it can monitor a network without being a node with an assigned IP address. Zeek is conceptualized in two layers:

- **Event Engine**: Analyzes and stores network traffic to generate neutral events, based on transmission starts or stops, port and protocol detection.
- **Policy Script**: Analyzes events to create action policies.

Zeek logs events but can also be configured to take actions such as sending alerts, executing commands, updating, and calling other programs.

### OSSEC

OSSEC is a host-based IDS (HIDS). It performs log analysis, integrity checking, Windows registry monitoring, rootkit detection, time-based alerting, and active response. It provides intrusion detection for most operating systems, including Linux, OpenBSD, FreeBSD, OS X, Solaris, and Windows. OSSEC has a centralized and cross-platform architecture that allows multiple systems to be easily controlled and managed.

OSSEC is based on naming each host as a server or sensor, according to its characteristics. A sensor is needed in each zone where the network is to be inspected for threats and at least one server to read the data arriving from the sensors.

#### OSSEC Architecture

OSSEC consists of multiple components:

- **Server**: The server is the central piece of the OSSEC deployment. It stores the integrity of the file databases, log checks, events, and system audit entries. All rules, decoders, and main configuration options are stored centrally in the manager, making it easy to manage even with a large number of agents.
- **Agents/Sensors**: The agent is a small program or set of programs installed on the system that will be monitored. The agent will collect information and transmit it to the manager for analysis and information correlation. Part of the information is collected in real-time, and other data will be collected periodically. It has a small default memory and CPU usage, which does not affect system usage.

![intruder prevention system ossec](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/ips2-ossec.png?raw=true)

#### OSSEC in Industrial Networks

By implementing OSSEC in an industrial network, a whitelist can be included with the IP of each industrial device, routers, and switches that may be connected to the network, denying traffic injection to any other device not registered on this list.

This way, effective security is achieved in a free and simple way. Likewise, it can be created in other operating systems, in Linux as seen, or in Windows, which is presented below. By working well with low-performance equipment, it allows installation in industrial networks where older equipment is often found.

The inclusion of server integrity, rootkit detection, and active detection is an addition to the security of an industrial network, being an indispensable requirement to increase the defense of a company.

### Wazuh

Wazuh is an open-source security monitoring platform that has evolved from OSSEC. It extends OSSEC's capabilities with new features, such as integration with cloud platforms, centralized management, and a broader set of preconfigured rules.

#### Key Features of Wazuh

- **Integration with the ELK Stack**: Wazuh integrates seamlessly with Elasticsearch, Logstash, and Kibana, providing a powerful graphical interface for security data visualization and analysis.
- **Cloud Threat Detection**: It offers specific rules and decoders for cloud environments such as AWS, Azure, and Google Cloud, helping identify threats and misconfigurations in these environments.
- **Centralized Management**: Allows managing multiple agents and servers from a centralized console, facilitating the management of large deployments.

## Comparison between various IDS/IPS

Table 1 reflects a comparison of the features of some of the IDS/IPS systems discussed in this study.

| Features                         | Zeek | Snort | Suricata | OSSEC | Wazuh |
|----------------------------------|------|-------|----------|-------|-------|
| Multi-threading                  | No   | v3.0  | Yes      | No    | No    |
| IPv6 Support                     | Yes  | Yes   | Yes      | Yes   | Yes   |
| IP Reputation                    | Partial| No   | Yes      | No    | Yes   |
| Automatic Protocol Detection     | Yes  | v3.0  | Yes      | No    | No    |
| GPU Acceleration                 | No   | No    | Yes      | No    | No    |
| Global Variables/Flowbits        | Yes  | No    | Yes      | No    | No    |
| GeoIP                            | Yes  | No    | Yes      | No    | No    |
| Advanced HTTP Analysis           | Yes  | No    | Yes      | No    | No    |
| HTTP Access Logging              | Yes  | No    | Yes      | No    | No    |
| SMB Access Logging               | Yes  | No    | Yes      | No    | No    |
| Free                             | Yes  | Yes   | Yes      | Yes   | Yes   |
| Integration with ELK Stack       | No   | No    | Partial  | No    | Yes   |

---

### Conclusion

Choosing an appropriate IDS/IPS tool depends on the specific needs of each organization. Factors such as performance, ease of integration, and analysis capabilities should be considered when selecting the right solution. The tools presented in this article offer a wide range of functionalities that can be adapted to different network environments and security needs. Keeping rules and configurations up to date, as well as integrating these tools with other security management systems, is crucial for ensuring effective protection against cyber threats.
