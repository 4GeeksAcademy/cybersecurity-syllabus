---
title: "Basic Network Security"
subtitle: "Fortifying Networks: The Crucial Role of Firewalls in Shielding Against Unauthorized Access and DDoS Attacks, Enhancing Security."
tags: ["networks"]
authors: ["blindma1den", "lorenagubaira"]

---

## The role of Firewalls in networks

The firewall is an essential tool in network security since its main function is to protect the entire computer network by controlling the data traffic entering and leaving it. It acts as a kind of barrier between the internal network and the outside world, filtering and blocking unauthorized and potentially dangerous access, One of its most important functions is intrusion prevention, i.e. it detects and blocks unauthorized access attempts to the network either from the outside or from compromised internal devices, and most importantly, a firewall can prevent denial of service (DDoS) attacks by limiting the traffic that can enter the network.

## **Firewall**

Since we know a little better the function of a firewall in the network, let's talk about what a firewall is...

A firewall is a network security system, which restricts internet traffic incoming, outgoing or within a private network, the term comes from the concept of physical walls that act as barriers to slow the spread of fire until the emergency services can extinguish it.

Firewalls can be software or a dedicated hardware and software unit that works by selectively blocking or allowing access to data packets.

A simpler explanation is to consider them as boundaries or gates that are to be delimited on a private network or host devices to manage the flow of activity that is allowed or prohibited on that network, we can say that they are intended to slow down the spread of threats on the network.

These barriers are usually found in two locations: On specific devices within the network and at other connection points (hosts).

### **How do firewalls work?**

The firewall decides which network traffic is allowed or considered dangerous, basically separating good traffic from bad, or safe traffic from untrusted traffic. Its main purpose is to protect private networks and the point-of-connection devices on them, known as network hosts. These hosts communicate with other hosts on the network, send and receive traffic between internal networks and may also receive traffic from external networks.

Computers and other point-of-attachment devices use networks to access the Internet and communicate with each other. However, the Internet itself is segmented into subnets for security and privacy reasons.

In a firewall, traffic filtering is achieved through preset or dynamically learned rules for allowing and denying connection attempts. These rules determine how the firewall regulates the flow of web traffic through the private network and private computing devices. Regardless of type, all firewalls can perform filtering using a combination of the following:

- **Source**: location from where the connection is attempted to be established.
- **Destination**: the place to which the connection is intended to be directed.
- **Content**: information that the connection is trying to send.

**Packet protocols**: the "language" used to transmit the message when attempting to establish the connection. Among the network protocols that hosts use to "communicate" with each other, TCP/IP protocols are primarily used to communicate over the Internet and between intranets or subnets.

**Application protocols:** common protocols include HTTP, Telnet, FTP, DNS and SSH.

### **Types of firewall**

Firewall types include various filtering methods and are distinguished according to their method in relation to the following.

- Connection tracking.
- Filtering rules.
- Audit logging.

Generally the most common firewalls on the market are:

- **Packet filtering firewall**

Its function is to filter packets based on network addresses, protocols or ports. The rules for filtering are set according to a manually created access control list. These rules are very rigid and it is difficult to correctly address unwanted traffic without compromising the usability of the network.

The inability to read application protocols means that the contents of a message sent within a packet cannot be read. Without reading the contents, firewalls with packet filtering have a limited quality of protection.

- **Gateway firewall**

These firewalls check for functional packets in the connection attempt and, if successful, allow a persistent open connection to be established between the two networks. After this, the firewall stops monitoring the connection.

Apart from its connection strategy, the circuit-level gateway can be similar to proxy firewalls.

- **Stateful inspection firewall**

Stateful inspection firewalls, also called dynamic packet filtering firewalls, are unique compared to static filtering because of their ability to monitor ongoing connections and remember previous connections. They started out acting at the transport layer, but today, these firewalls can monitor many layers, including the application layer.

Like the static filtering firewall, stateful inspection firewalls allow or block traffic based on technical properties, such as specific packet protocols, IP addresses or ports.

- **New generation firewall (NGFW)**

The constant evolution of threats requires more robust solutions. Next-generation firewalls overcome this problem by combining the functions of a traditional firewall with network intrusion prevention systems.

Next-generation firewalls are designed to examine and identify specific threats, such as advanced malware, at a more detailed level. This is the type of firewall most commonly used by enterprises and sophisticated networks, as it provides a comprehensive solution to filter out and discard any threats.

## **Wireless networks security**

A wireless network or a wifi network is a frequency signal by waves, which can connect computers to the internet without using cables, as this connection is by transmission instead of cables, it is possible that unauthorized users can access this network. This can reduce the speed of the connection or generate vulnerability in situations such as identity theft. Therefore it is necessary to take certain security measures to protect our information in WiFi such as:

- **Encryption**

Encryption of wireless networks is used to add security through an authentication protocol, which prompts for a password or network key when a user or device attempts to connect. If the Wifi network is not secured with some form of encryption, it is possible that an unauthorized user can access it and obtain personal information, as well as reducing the speed and performance of the network.

> 💡 Different types of encryption are available for wireless LANs (WIFI)

- **Wired Encryption Protocol (WEP)**

This protocol uses a secret key shared between an access point and a host, and all data sent and received can be encrypted using this shared key.

The 802.11 standard does not specify how the private key is established, but allows for a table that associates a unique key with each station. However, in general practice, the same key is shared among all stations and access points.

**WEP provides two types of authentication:**

1. An open system, where all users are allowed to access the WLAN.
2. A shared key authentication, which controls access to the WLAN and prevents unauthorized access to the network.

> 👉 From the two levels, shared key authentication is the secure mode, in which a private key is shared between all stations and access points to the WLAN system.

To protect the encoded text from unauthorized modification while in transit, WEP applies an integrity check algorithm (CRC-32) to the plaintext.

Shared key authentication works only if WEP encryption is enabled, otherwise the system will revert to open system mode by default.

According to the standard, WEP should provide confidentiality, authentication and access control in WLAN networks.

WEP uses the same symmetric and static key at the stations and the access point. The standard does not provide for any automatic key distribution mechanism, which means that the key must be written manually on each network element.

This generates several inconveniences, on one hand the key is stored in all the stations, increasing the chances of it being compromised.

On the other hand, the manual distribution of keys leads to increased maintenance by the network administrator, which means that the key is rarely or never changed.

- **WiFi Protected Access (WPA)**

This encryption system was developed to solve the security problems of the WEP system by using TKIP (Temporal Key Integrity Protocol). This protocol is used to manage dynamic keys and therefore solves many of the problems that WEP had, such as the length of the key.

In general terms, we can say that WPA works similarly to WEP, but using dynamic keys, and also uses the RC4 algorithm to generate a stream of bits that are used for encryption.

WPA adopts user authentication through the use of a server, where the credentials and passwords of users on the network are stored. In order not to force the use of such a server for network deployment, WPA allows authentication through a pre-shared key.

In a similar way to WEP, it requires the same key to be entered on all devices on the network, so with WPA, as the key is constantly changing, incursions into the wireless network are more difficult than with WEP.

PSK or Pre Shared Key, is based on the security of a shared password formed between 8 and 63 characters. It is easy to use and configure, so it is recommended in family or small business environments. Any computer that has the key will be able to connect to the network.

The main weakness of WPA-PSK is precisely the use of a shared key between stations, since when a system bases its security on a password, it is always susceptible to a brute force attack, although if the length of the password is adequate and it is well chosen it should not be a major problem.

- **WiFi Protected Access 2 (WPA2)**

WPA2 is a WiFi encryption protocol that was developed to solve the vulnerability problems detected in the first version (WPA).

WPA2 specifications are not public, so the amount of information available is really scarce. It is known that WPA2 includes the AES (Advanced Encryption Standard) encryption algorithm, developed by NIS.

As already mentioned, this is a WiFi block cipher algorithm with a 128-bit key.

Powerful hardware is required to perform WPA2 algorithms, which means that older devices without sufficient processing capabilities will not be able to incorporate WPA2.

Personal Mode or Pre-Shared Key (PSK) works in the same way as WAP security, and is the easiest WiFi encryption protocol to install as it requires a simple password to be created. Although WPA2 provides strong encryption and security, and is "potentially uncrackable" by attackers if a long and strong password is used.

### **MAC filtering**

The purpose of MAC filtering is to restrict network access to a specific device or group of devices. For example, let's say we have a computer and we don't want it to connect to the home network. We would have to know what its MAC address is and create a filter on the router.

We could create a MAC filtering in the router so that certain devices cannot connect when we activate it. For example, if we are going to be away from home for a long time and we do not want the TV or any device to connect to the router and that could pose a security problem in case a vulnerability appears.

Therefore, MAC filtering has a twofold approach. If we are only interested in blocking a specific device or a few devices, it is best to create a blacklist and include them. On the other hand, if we want to block all connections and only allow devices we trust, we would have to create a whitelist and include them there.

What the router does is to identify each device according to its MAC address. If it finds that that address is on any list that we have created, then that is when it would act. That address is unique to each network card that a device has. For example a simple smart watch that has Wi-Fi, is going to have a unique MAC.

### **Hidden SSID**

The hidden wifi ssid is one of the security mechanisms implemented by Wifi networks by hiding its name, so that only if you know the SSID you can connect to it.

In order to connect to a network, the first thing we need to know is that it is available. This is possible because wifi technology (802.11) specifies that in order to make a network known, beacon packets (Management Beacon) must be sent continuously. In this way, nearby devices with WiFi capabilities receive these packets so that they know that the network is available.

In this way, when a device wants to display the list of available networks, those from which a packet of this type has been received will appear, keeping the list always updated, useful when we move or change location.

When we activate the filtering by hiding SSID, all the devices that receive the beaconing packets will receive the empty packet, so users who want to connect to the network will have to add the SSID manually. This does not mean that this method is 100% effective as there are some software that can capture all the packets on the network, analyze them and extract the network name to be displayed on the interface.

- **VPN (Virtual Private Network): concept and basic configuration.**

A VPN or virtual private network creates a private network connection between devices over the Internet. VPNs are used to transmit data securely and anonymously over public networks. They work by hiding users' IP addresses and encrypting data so that no one who is not authorized to receive it can read it.

Its three main functions are:

1. Privacy

VPNs use encryption to maintain the privacy of sensitive information, especially when connecting over public wifi networks.

2. Anonymity

A VPN connection hides your IP address so that you remain anonymous on the Internet.

3. Security

VPNs use cryptography to protect your Internet connection from unauthorized access.

### 💡Lab: Firewall Configuration

In the following lab we are going to learn how to configure a firewall with the help of cisco packet tracer, following these steps:

1. We open Cisco Packet Tracer and create a simulated environment with two computers connected to a Switch, the Switch will be connected to a router and the router to a web server as in the following image:

![Firewall Configuration](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/confirguracion-firewall.png?raw=true)

2. We configure PC0 and PC0 with static ip, clicking on each one and entering in the Desktop tab:

IP Address 192.168.1.2 / 192.168.1.3

Subnet Mask 255.255.255.0

Default gateway 192.168.1.10

We can ping each ip to verify that the connection between both PCs is established.

3. Configure the server IP:

IP Address 200.200.200.200

Subnet Mask 255.255.255.0

Default gateway 200.200.200.201

4. Configure the router in the FastEthernet0/0 and FastEthernet0/1 options.

The IP address will be the Default Gateway of the devices.

ip address 192.168.1.10 (For FastEthernet0/0) 200.200.200.201 (For FastEthernet0/1)

5. Ping from the client computers to the web server by pinging 200.200.200.200 to confirm that there is a connection between the two devices.

6. Log back in to the router and go to the cli tab where we enter the following commands

![Cli Tab](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/pestana-cli.png?raw=true)

7. We ping the server again from the client computers, all the packets sent will be lost, since from the router with the previous commands we programmed so that the ICMP protocol will be disabled and only the clients will be allowed to access the web service.

8. Finally from any client computer we will access the web service, entering the web browser option and entering 200.200.200.200 in the search engine. it will show us a page called index.html