---
title: "Intrusion Prevention Systems"
technologies: ['cybersecurity', "networks"]

---
# Intrusion Prevention Systems (IPS)

IPS are hardware or software devices that review network traffic to detect and respond to possible attacks or intrusions. The response consists of discarding or modifying packets from the attack to nullify its purpose. This behavior classifies them as proactive devices due to their automatic reaction to anomalous situations.

IPSs are similar in behavior to firewalls, as both make decisions about accepting packets in a system. However, firewalls base their decisions on incoming packet headers, network, and transport layers, while IPSs base their decisions on both the headers and the packet data content.

![intrusion prevention system](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/7intrucion-prevension-system.png?raw=true)

### Packet Header and Content Depending on Protocol

IPS technology provides a more comprehensive view of network operations, offering information about all types of malicious activities, bad connections, inappropriate content, and other functions with minimal oversight. The main characteristics of this technology are:

- Automatic Reaction Capability to Incidents
- Application of New Filters as Attacks Are Detected in Progress
- Automatic Blocking Against Attacks in Real-Time
- Reduction of False Alarms of Attacks on the Network
- Protection of Unpatched Systems
  *Optimization of Network Traffic Performance

## IPSs as an Evolution of IDSs

While IDS is limited to detecting and notifying the system administrator of the intrusion, and the administrator is responsible for receiving and responding to alerts; IPS detects the intrusion and stops it in a pre-defined way, verifying certain behaviors on the network previously configured as anomalous. Thanks to this, the level of alerts from an IPS is significantly lower than the level of alerts produced by an IDS. The main difference between active IDSs and IPSs is that the latter can disable the packets involved in the attack by modifying their content.

A disadvantage of IPSs arises from proactive reactions to intrusions. On the one hand, the reaction time to an attack is reduced, but it can also cause unexpected and inconvenient effects when it reacts to a false positive (FP), potentially leading to a denial of service or even isolating the machine. Therefore, the use of IPSs in industrial control systems must be well-studied, or a firewall with deep packet inspection should be used for more secure communications. Current architectures centralize the operation of the IPS, which facilitates its operation and administration but decreases system scalability and makes the IPS a critical point.

![advantages intrusion prevention system](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/8ventajas-intrusion-prevesion-system.png?raw=true)

> In the image above: advantages of IPS.

## Types of IPS

The different types of IPS are mainly distinguished by their location.

- **Host-Based IPS (HIPS):** This intrusion prevention application resides at the specific IP address of a single machine and prevents possible attacks on the host.
- **Network-Based IPS (NIPS):** Monitors the network for suspicious traffic.
- **Wireless Network-Based IPS (WIPS):** Monitors wireless networks, just as NIPS do with LAN networks.
- **Network Behavior Analysis-Based IPS (NBA):** Examines network traffic to identify threats that generate unusual traffic, such as DoS attacks or malware.

## Network-Based IPS (NIPS) vs. Host-Based IPS (HIPS

A HIPS can handle both encrypted and unencrypted traffic since it can analyze data after it has been decrypted on the host. On the other hand, a NIPS does not use the host's processor and memory, so it does not impact machine performance.

A NIPS can detect scattered events across the network and react easily, whereas with a HIPS, it would take too long to inform a central engine and then inform the other machines.

## The Evolution and Categories of IPS

Two historical generations of IPSs can be distinguished:

- **First-Generation IPSs:** Upon detecting an attack from a specific IP address, they would discard all packets from that address, whether or not they were involved in the attack.
- **Evolved IPSs:** These IPSs can discard only the packets related to the identified attack, allowing other packets from the attacker's IP to pass through as long as they are not related to the attack.

Five categories of IPS can be distinguished depending on their operation, capabilities, and location in the network architecture.

- **Inline IPS**

  These IPSs represent the evolution of signature-based NIDS and function as a Bridge at layer two, reviewing all packets passing through the network for signatures. If an anomaly is detected, it is automatically logged, or the passage of a packet is altered to frustrate an attack without the attacker noticing. This process is done through *Scrubbing*, which involves error detection via checksum verification or redundancy with data copies. They are commonly known as network IPS or NIPS.

- **Layer 7 Application Switches (OSI Model)**

  Switches typically work at layer 2 (link) but increasingly work at layer 7 or application due to high bandwidth demand. The main task of these switches is to balance the load of distributed applications across multiple servers, making routing or switching decisions based on the application layer data content. Until this point, there is no difference from a load balancer.

  Functioning as an IPS is similar to a signature-based NIPS, serving to block attacks. These devices are usually positioned in front of firewalls, protecting the entire network. Being similar to a NIPS, they can only stop known attacks, but they can block DoS or DDoS attacks that other IPSs cannot stop without affecting the rest of the network. They can be configured redundantly, in hot-standby mode, or as a load balancer (a feature that differentiates them from any other IPS).

- **Application Firewalls/IDS**

  Application firewalls/IDSs are installed on each host to be protected, considering the applications running on it, so they are also known as HIPS. Proper functioning requires a training phase, identifying normal operating patterns on the host. This training creates a profile of frequent relationships between applications and system components, such as the operating system, other applications, memory, and users.

  HIPS behave similarly to anomaly-detection-based IDSs when detecting intrusions, but they must identify all processes exhaustively; otherwise, a valid application may be blocked.

  Since they rely on anomaly detection rather than signature matching, they can prevent very recent intrusions for which there is no specific signature definition.

- **Hybrid Switches**

  Hybrid switches are a combination of HIPS and application layer switches. They are hardware devices like application layer switches but use policies similar to those used by HIPS.

  Hybrid switches rely on behavioral pattern analysis. Their strength lies in the detailed knowledge of the traffic that should be accepted.

- **Deceptive Applications**

  This type of technology analyzes all network traffic and each device in particular to know what is allowed and correct traffic, similar to how a HIPS creates patterns. In operation, when it detects traffic not allowed for the network (access to a disallowed port) or a specific server (access to an SSH port on a server that does not have it open), it sends a marked response to the attacker so that the IPS can detect other traffic from the same source and block it.
