---
title: "Communication & Networking"
subtitle: "Explore the fundamentals of computer networks, from different types to key protocols and essential devices. Learn more about IP addresses, routers, and switches!"
tags: ["networking", "cybersecurity"]
authors: ["blindma1den", "lorenagubaira"]

---

We can define the network as the technology that allows computers to connect, share, and send data between them. Nowadays, not only computers can be connected, but also any intelligent device from phones to TVs'.

There are various types of networks, such as:

| Local Area Network (LAN) | A LAN or "Local Area Network" is a communication network built by interconnecting nodes using cables or wireless media. The connection scope is limited by physical means, whether it's a building, a floor, or our room. In LANs, the main feature is that there are shared resources accessible only to the users belonging to it, with no possibility of external access. |
| --- | --- |
| Metropolitan Area Network (MAN) | A MAN, like LAN, is a communication network built by interconnecting nodes using cables or wireless media. The connection scope is limited by physical means, such as a building, floor, or room. The main feature is the existence of shared resources accessible only to users belonging to it, with no possibility of external access. |
| Wide Area Network (WAN) | It doesn't have a predefined limit but is the network that allows connecting different points worldwide composed of LAN or MAN areas through high-capacity trunk links. For example, the Internet is a WAN. |
| Wireless Local Area Network (WLAN) | In this network, we can connect without the need to be physically connected to it, thanks to a device called a router that emits the network signal through waves received by devices through a network card that captures this signal and establishes the connection. |

Thanks to these networks, we can send information from one place to another, using network protocols that dictate the rules on how devices will exchange information.

**The most used network protocols are:**

- **TCP/IP (Transmission Control protocol/ internet protocol)**

This protocol is a set of standardized rules that allow computers to communicate on a network like the Internet and how informational packets are sent and received. This explanation is known as the *TCP/IP* model.

The TCP/IP model is used for communications in networks and, like any protocol, it describes a set of general operation guidelines to enable a computer to communicate on a network. TCP/IP provides end-to-end connectivity by specifying how data should be formatted, addressed, transmitted, routed, and received by the recipient.

To achieve a reliable exchange of data between two computers, many separate procedures must be carried out. The result is that communication software is complex. With a layered or levels model, it is easier to group related functions and implement modular communication software.

The layers are hierarchical, meaning each layer is built upon its predecessor. The number of layers, their services, and functions vary with each type of network. However, in any network, the mission of each layer is to provide services to the upper layers, making the way these services are carried out transparent to them. In this way, each layer must deal exclusively with its immediately lower level, from which it requests services, and the immediately higher level, to which it returns results.

**The TCP/IP model consists of 4 layers:**

1. **Access Layer:** The access layer, also known as the data link layer, manages the physical infrastructure that allows computers to communicate with each other over the Internet. This includes, among other elements, Ethernet cables, wireless networks, network interface cards, and device drivers on the computer.
The access layer also includes technical infrastructure, such as the code that converts digital data into transmissible signals, making a connection possible.
2. **Internet Layer:** The Internet layer, also called the network layer, controls the flow and routing of traffic to ensure that data is sent quickly and correctly. This layer is also responsible for reassembling the data packet at the destination. If there is a lot of traffic on the Internet, this layer may take a little longer to send a file, but it is less likely that the file will be damaged.
3. **Transport Layer:** The transport layer is the one that provides a reliable data connection between two communication devices. It's like sending a secured package: the transport layer divides the data into packets, confirms the packets it has received from the sender, and ensures that the recipient confirms the packets received on their end.
4. **Application Layer:** The application layer is the group of applications that allows the user to access the network. For most of us, this means email, messaging apps, and cloud storage programs. This is what the end user sees and interacts with when receiving and sending data.

> 🏋️ **Exercise:** There is a network model called OSI that explains the entire process of sending information over the network in much more detail. It is a study model that consists of 7 layers. - Research this model and each of its layers to have a better understanding.

- **DNS (Domain Name System)**

This protocol is responsible for resolving the names of websites with respect to their numeric IP addresses, meaning translating easy-to-understand names for people into IP identifiers for devices connected to the network. This is done to be able to locate and address these devices worldwide.

The DNS server uses a distributed and hierarchical database that stores information associated with domain names on networks like the Internet. Although, as a database, DNS is capable of associating different types of information with each name, the most common uses are the assignment of domain names to IP addresses and the location of the email servers for each domain.

The assignment of names to IP addresses is certainly the most well-known function of DNS protocols. For example, if the IP address of the Google site is 216.58.210.163, most people reach this device by specifying [www.google.com](http://www.google.com/) and not the IP address. In addition to being easier to remember, the name is more reliable. The numerical address could change for many reasons without having to change the website name. Also, in the case that a website uses a Content Delivery Network (CDN), through DNS, the user will receive the IP address of the nearest server based on their geographic location (each CDN, in turn, has its own DNS servers).

- **DHCP (Dynamic Host Configuration Protocol)**

It is a network protocol through which a **DHCP** server dynamically assigns an IP address and other network configuration parameters to each device on a network so that it can communicate with other IP networks. This server has a list of dynamic IP addresses and assigns them to clients as they become available, knowing at all times who has had that IP, how long they have had it, and to whom it has been assigned afterward. This way, the clients on an IP network can obtain their configuration parameters automatically.

Each IP address must be manually configured on each device, and if the device moves to another subnet, a different IP address must be configured. DHCP allows the administrator to centrally monitor and distribute the necessary IP addresses, and automatically assign and send a new IP if the device is connected in a different location on the network.

- **IP Address**

An IP address has two main functions: identification of the network interface and addressing for its location.

The IP address can change frequently due to changes in the network or because the device responsible for assigning IP addresses within the network decides to assign another IP (for example, with the DHCP protocol). This form of IP address assignment is also called a dynamic IP address (usually abbreviated as dynamic IP). Internet sites that, due to their nature, need to be permanently connected generally require a fixed IP address (commonly known as a static IP). This address does not change over time. Public mail servers, DNS, FTP servers, and web servers must necessarily have a fixed or static IP address, as this allows their location on the network.

Devices connect through their respective IP addresses. However, for people, it is easier to remember a domain name than the numbers of the IP address. Domain Name System (DNS) servers "translate" the domain name into an IP address. If the dynamic IP address changes, it is sufficient to update the information on the DNS server. Everyone else will continue to access the device by the domain name.

IPv4 addresses are expressed as a binary number of 32 bits, allowing for an address space of up to 4,294,967,296 (2^32) possible addresses.

IP addresses can be expressed as decimal notation numbers: the 32 bits of the address are divided into four octets. The decimal value of each octet is in the range of 0 to 255 [the highest 8-bit binary number is 11111111, and these bits, from right to left, have decimal values of 1, 2, 4, 8, 16, 32, 64, and 128, which sum to 255].

### Network Devices

A **router** is a device that connects two or more packet-switched networks or subnetworks. It serves two main functions: managing traffic between these networks by forwarding data packets to their intended IP addresses and allowing multiple devices to use the same Internet connection.

There are various types of routers, but most of them pass data between **LANs** (Local Area Networks) and **WANs** (Wide Area Networks). A LAN is a group of connected devices restricted to a specific geographical area. Typically, a LAN needs only one router.

Data moves across any network in the form of data packets. Each data packet has a header containing information about the intended destination of the packet. As a packet travels to its destination, multiple routers may direct it several times. Routers perform this process millions of times per second with millions of packets.

When a data packet arrives, the router first looks up its address in a routing table. Then, the router forwards or moves the packet toward the next point in the network.

There are two different types of routing, based on how the router creates its routing tables:

- **Static Routing**

In static routing, a network administrator uses static tables to manually configure and select network routes. Static routing is useful in situations where the network design or parameters are expected to remain constant.

The static nature of this routing technique comes with expected drawbacks, such as network congestion. While administrators can configure backup routes in case a link fails, static routing generally decreases the adaptability and flexibility of networks, resulting in limited network performance.

- **Dynamic Routing**

In dynamic routing, routers create and update routing tables at runtime based on the actual network conditions. They attempt to find the fastest route from source to destination through a dynamic routing protocol, which is a set of rules that create, maintain, and update the dynamic routing table.

The major advantage of dynamic routing is its adaptability to changing network conditions, including traffic volume, bandwidth, and network failures.

Another device capable of performing routing is the **switch**. Switches are key building blocks for any network. They connect multiple devices, such as computers, wireless access points, printers, and servers, within the same network in a building or campus. A switch enables connected devices to share information and communicate with each other.

**There are various types of switches:**

**a)** **Unmanaged Switches**: An unmanaged network switch is designed to simply plug and play, requiring no configuration. Unmanaged switches are typically for basic connectivity and are often used in home networks or where a few additional ports are needed, such as on a desk, in a lab, or a conference room.

**b)** **Managed Switches**: Managed switches provide greater security, additional features, and flexibility because you can configure them to suit your network. With this increased control, you can better secure your network and enhance the quality of service for those accessing the network.



