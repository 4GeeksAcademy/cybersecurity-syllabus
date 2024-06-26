## What is a Firewall

A firewall is a network security system that restricts incoming, outgoing, or internal internet traffic within a private network. The term comes from the concept of physical walls that act as barriers to slow the spread of fire until emergency services can extinguish it.

Firewalls can be software or a dedicated hardware and software unit that works by selectively blocking or allowing access to data packets.

A simpler explanation is to consider them as boundaries or gates on a private network or host devices to manage the flow of activity that is allowed or prohibited on that network. We can say they are intended to slow the spread of threats on the network.

These barriers are usually found in two locations: on specific devices within the network and at other connection points (hosts).

## The Role of Firewalls in Networks

A firewall is an essential tool in network security, with its main function being to protect the entire computer network by controlling the data traffic entering and leaving it. It acts as a barrier between the internal network and the outside world, filtering and blocking unauthorized and potentially dangerous access. One of its most important functions is intrusion prevention, detecting and blocking unauthorized access attempts to the network from the outside or from compromised internal devices. Most importantly, a firewall can prevent denial of service (DDoS) attacks by limiting the traffic that can enter the network.

## How Do Firewalls Work?

A firewall decides which network traffic is allowed or considered dangerous, essentially separating good traffic from bad or safe traffic from untrusted traffic. Its main purpose is to protect private networks and the point-of-connection devices on them, known as network hosts. These hosts communicate with other hosts on the network, send and receive traffic between internal networks, and may also receive traffic from external networks.

Computers and other point-of-attachment devices use networks to access the Internet and communicate with each other. However, the Internet itself is segmented into subnets for security and privacy reasons.

In a firewall, traffic filtering is achieved through preset or dynamically learned rules for allowing and denying connection attempts. These rules determine how the firewall regulates the flow of web traffic through the private network and private computing devices. Regardless of type, all firewalls can perform filtering using a combination of the following:

- **Source**: The location from where the connection attempt is made.
- **Destination**: The location to which the connection is directed.
- **Content**: The information that the connection is trying to send.

**Packet Protocols**: The "language" used to transmit the message when attempting to establish the connection. Among the network protocols that hosts use to "communicate" with each other, TCP/IP protocols are primarily used to communicate over the Internet and between intranets or subnets.

**Application Protocols**: Common protocols include HTTP, Telnet, FTP, DNS, and SSH.

## Types of Firewalls

Firewall types include various filtering methods and are distinguished according to their method in relation to the following:

- Connection tracking
- Filtering rules
- Audit logging

Generally, the most common firewalls on the market are:

### Packet Filtering Firewall

Its function is to filter packets based on network addresses, protocols, or ports. The rules for filtering are set according to a manually created access control list. These rules are very rigid, and it is difficult to correctly address unwanted traffic without compromising the usability of the network.

The inability to read application protocols means that the contents of a message sent within a packet cannot be read. Without reading the contents, packet filtering firewalls have limited protection quality.

### Gateway Firewall

These firewalls check for functional packets in the connection attempt and, if successful, allow a persistent open connection to be established between the two networks. After this, the firewall stops monitoring the connection.

Apart from its connection strategy, the circuit-level gateway can be similar to proxy firewalls.

### Stateful Inspection Firewall

Stateful inspection firewalls, also called dynamic packet filtering firewalls, are unique compared to static filtering due to their ability to monitor ongoing connections and remember previous connections. They started out acting at the transport layer, but today, these firewalls can monitor many layers, including the application layer.

Like the static filtering firewall, stateful inspection firewalls allow or block traffic based on technical properties, such as specific packet protocols, IP addresses, or ports.

### Next-Generation Firewall (NGFW)

The constant evolution of threats requires more robust solutions. Next-generation firewalls overcome this problem by combining the functions of a traditional firewall with network intrusion prevention systems.

Next-generation firewalls are designed to examine and identify specific threats, such as advanced malware, at a more detailed level. This is the type of firewall most commonly used by enterprises and sophisticated networks, as it provides a comprehensive solution to filter out and discard any threats.

## Wireless Network Security

A wireless network or wifi network is a frequency signal by waves, which can connect computers to the internet without using cables. As this connection is by transmission instead of cables, unauthorized users can access this network. This can reduce the speed of the connection or create vulnerability in situations such as identity theft. Therefore, it is necessary to take certain security measures to protect our information in WiFi, such as:

### Encryption

Encryption of wireless networks is used to add security through an authentication protocol, which prompts for a password or network key when a user or device attempts to connect. If the WiFi network is not secured with some form of encryption, it is possible that an unauthorized user can access it and obtain personal information, as well as reduce the speed and performance of the network.

> 💡 Different types of encryption are available for wireless LANs (WiFi).

- **Wired Encryption Protocol (WEP)**

This protocol uses a secret key shared between an access point and a host, and all data sent and received can be encrypted using this shared key.

The 802.11 standard does not specify how the private key is established, but allows for a table that associates a unique key with each station. However, in general practice, the same key is shared among all stations and access points.

**WEP provides two types of authentication:**

1. An open system, where all users are allowed to access the WLAN.
2. Shared key authentication, which controls access to the WLAN and prevents unauthorized access to the network.

> 👉 Of the two levels, shared key authentication is the secure mode, in which a private key is shared between all stations and access points to the WLAN system.

To protect the encoded text from unauthorized modification while in transit, WEP applies an integrity check algorithm (CRC-32) to the plaintext.

Shared key authentication works only if WEP encryption is enabled; otherwise, the system will revert to open system mode by default.

According to the standard, WEP should provide confidentiality, authentication, and access control in WLAN networks.

WEP uses the same symmetric and static key at the stations and the access point. The standard does not provide for any automatic key distribution mechanism, which means that the key must be written manually on each network element.

This generates several inconveniences. On one hand, the key is stored in all the stations, increasing the chances of it being compromised.

On the other hand, the manual distribution of keys leads to increased maintenance by the network administrator, which means that the key is rarely or never changed.

### WiFi Protected Access (WPA)

This encryption system was developed to solve the security problems of the WEP system by using TKIP (Temporal Key Integrity Protocol). This protocol is used to manage dynamic keys and therefore solves many of the problems that WEP had, such as the length of the key.

In general terms, we can say that WPA works similarly to WEP, but using dynamic keys, and also uses the RC4 algorithm to generate a stream of bits that are used for encryption.

WPA adopts user authentication through the use of a server, where the credentials and passwords of users on the network are stored. In order not to force the use of such a server for network deployment, WPA allows authentication through a pre-shared key.

Similarly to WEP, it requires the same key to be entered on all devices on the network. With WPA, as the key is constantly changing, incursions into the wireless network are more difficult than with WEP.

PSK or Pre-Shared Key is based on the security of a shared password formed between 8 and 63 characters. It is easy to use and configure, so it is recommended in family or small business environments. Any computer that has the key will be able to connect to the network.

The main weakness of WPA-PSK is precisely the use of a shared key between stations, as when a system bases its security on a password, it is always susceptible to a brute force attack. However, if the length of the password is adequate and well-chosen, it should not pose a major problem.

### WiFi Protected Access 2 (WPA2)

WPA2 is a WiFi encryption protocol that was developed to solve the vulnerability problems detected in the first version (WPA).

WPA2 specifications are not public, so the amount of information available is really scarce. It is known that WPA2 includes the AES (Advanced Encryption Standard) encryption algorithm, developed by NIS.

As already mentioned, this is a WiFi block cipher algorithm with a 128-bit key.

Powerful hardware is required to perform WPA2 algorithms, which means that older devices without sufficient processing capabilities will not be able to incorporate WPA2.

Personal Mode or Pre-Shared Key (PSK) works in the same way as WPA security and is the easiest WiFi encryption protocol to install, as it requires a simple password to be created. Although WPA2 provides strong encryption and security, and is "potentially uncrackable" by attackers if a long and strong password is used.

### MAC Filtering

The purpose of MAC filtering is to restrict network access to a specific device or group of devices. For example, let's say we have a computer and we don't want it to connect to the home network. We would need to know its MAC address and create