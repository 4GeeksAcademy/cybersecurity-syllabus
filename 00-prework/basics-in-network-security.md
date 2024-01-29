---
title: "Basics in Network security"
subtitle: "Learn how to enhance network security by configuring packet filtering rules in a firewall."
tags: ["networking", "cybersecurity"]
authors: ["blindma1den", "lorenagubaira"]

---

## Firewall and Packet Filtering

A firewall is a device or software used to protect a network from external threats. It works by monitoring and filtering incoming and outgoing network traffic, allowing only secure traffic.

**Packet filtering** is one of the main functions of firewalls. This process involves inspecting each data packet entering or leaving the network and comparing it to a set of pre-configured security rules. If a packet does not meet the rules, it is blocked, and its transmission is not allowed.

Packet filtering can be based on various criteria, such as IP address, port, MAC address, protocol, packet content, etc.

In addition to protecting the network from external attacks, firewalls can also be used to control user access to the Internet and limit internal network traffic, for example, by blocking access to unwanted websites.

Configuring packet filtering rules in a firewall involves specifying the conditions that must be met for a data packet to be allowed or blocked. These rules are based on criteria such as source and destination IP address, port, protocol, etc.

### Steps to Configure Packet Filtering Rules in a Firewall:

1. **Access the Firewall**: To access the firewall and configure packet filtering rules, access to an administration console or a web management interface is required.
2. **Define Filtering Rules**: Once inside the administration console, filtering rules can be defined by specifying criteria for each rule.
3. **Apply the Rules**: After defining the rules, it is necessary to apply them so that the firewall uses them to filter network traffic.
4. **Verify Operation**: Finally, it is essential to verify that the packet filtering rules are being applied correctly and that there are no errors or conflicts.

>🔥 **Exercise** - Research firewall rules and create 5 rules, explaining what type of traffic each rule would filter.

### Security Technologies for Networks and Communications

**Virtual Private Network (VPN)**

A **VPN** or **Virtual Private Network** creates a private network connection between devices over the Internet. VPNs are used to transmit data securely and anonymously over public networks. They work by hiding users' IP addresses and encrypting data so that only authorized recipients can read it.

A VPN connection redirects data packets from a machine to another remote server before transmitting them to third parties over the Internet.

The main features of VPN technology include:

- **Tunneling Protocol**

A virtual private network creates a secure data tunnel between your local machine and another VPN server located thousands of kilometers away. When connected, this VPN server becomes the origin of all your data. The Internet Service Provider (ISP) and other third parties can no longer see the content of your Internet traffic.

- **Encryption**

VPN protocols like IPSec encrypt your data before sending it through the data tunnel. IPSec is a set of protocols to secure Internet Protocol (IP) communications by authenticating and encrypting all IP packets in a data stream. The VPN service acts as a filter, making your data unreadable at one end and only decrypting it at the other, preventing misuse of personal data even if your network connection is compromised. Network traffic is no longer vulnerable to attacks, and your Internet connection is secure.

- **Protected Wi-Fi Access (WPA)**

Wi-Fi Protected Access (WPA) is a wireless security protocol launched in 2003 to address the growing vulnerabilities of its predecessor, WEP. The WPA Wi-Fi protocol is more secure than WEP because it uses a 256-bit key for encryption, a significant improvement over the 64 and 128-bit keys used by the WEP system.

WPA also uses the Temporal Key Integrity Protocol (TKIP), which dynamically generates a new key for each data packet or unit. TKIP is much more secure than the fixed key system used by WEP.

However, WPA is not without its flaws. TKIP, the main component of WPA, was designed to be implemented in systems with WEP through firmware updates. This meant that WPA continued to rely on easily exploitable elements.

- **Wi-Fi Protected Access 2 (WPA2)**

WPA2 (Wi-Fi Protected Access 2) is the second generation of the Wi-Fi Protected Access wireless security protocol. Like its predecessor, WPA2 was designed to secure and protect Wi-Fi networks. WPA2 ensures that data sent or received over the wireless network is encrypted and only accessible to those with the network password.

One of the advantages of the WPA2 system was the introduction of the Advanced Encryption Standard (AES) to replace the more vulnerable TKIP system used in the original WPA protocol. AES provides robust encryption and is used by the United States government to protect classified data.
