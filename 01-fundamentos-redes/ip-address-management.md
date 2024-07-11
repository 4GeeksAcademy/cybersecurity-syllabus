---
title: "IP address management"
subtitle: "Mastering IP address management: vital skills for network and cybersecurity professionals. Discover how IP addresses drive network infrastructure and cybersecurity."
tags: ["direccion-ip"]
authors: ["blindma1den", "lorenagubaira"]

---

A network and cybersecurity professional needs to know how to manage IP addresses because IP addresses are essential elements in any network infrastructure, and play a critical role in cybersecurity.

## IP address

- An IP (Internet Protocol) address is a unique number assigned to each device connected to a network, whether on a local area network (LAN) or the Internet (WAN).
- It works similarly to a house address on a street, identifying the location of a device on the network.

Imagine you have a home network with several devices, such as your computer, your phone and your printer. Each of these devices has its unique IP address, like an address label so that data can reach the correct destination.

## Subnetting: How networks are made up

- Subnetting is the process of dividing a network into smaller subnets. This is done for several reasons, including improving network efficiency and security.
- In cybersecurity and pentesting, subnetting is used to segment a network into smaller parts, which can help isolate and control traffic. This is crucial to protect critical resources and limit the spread of threats in a network.

> 💭 Imagine you have a corporate network with different departments, such as sales and accounting. You can use subnetting to create separate subnets for each department, which helps keep your traffic separate and secure. If an attacker enters a subnet, their ability to move to other parts of the network will be limited thanks to segmentation.

- A cybersecurity professional must **understand** how IP addresses are assigned and managed on a network to detect and respond to threats. This includes identifying suspicious or unauthorized devices that may attempt to access the network.
- Knowledge of subnetting is essential for designing and configuring effective security measures, such as firewalls, that can limit unauthorized traffic between subnets.
- In pentesting, knowledge of subnetting is crucial for assessing the security of a network, identifying potential points of vulnerability and effectively simulating attacks within subnets.

IP addresses are assigned by organizations responsible for managing and allocating IP address resources around the world. The primary entity that oversees the allocation of IP addresses on the Internet is the **Internet Assigned Numbers Authority (IANA)**, which is an entity that operates under the supervision of the **Internet Corporation for Assigned Names and Numbers (ICANN)**.

The IANA is responsible for allocating IP address blocks to **Internet Regions**, which are five designated geographic regions around the world:

1. **North America**
2. **Europe**
3. **Asia Pacific**
4. **Latin America and the Caribbean**
5. **Africa**

Each of these regions has its own **Regional Internet Registry** (RIR), which is an organization that manages and distributes IP addresses in its corresponding geographic area. These RIRs are:

| ARIN (American Registry for Internet Numbers) | Responsible for North America. |
| --- | --- |
| RIPE NCC (Réseaux IP Européens Network Coordination Centre) | Responsible for Europe, Middle East and part of Central Asia |
| APNIC (Asia-Pacific Network Information Centre) | Responsible for the region of Pacífic Asia. |
| LACNIC (Latin America and Caribbean Network Information Centre) | In charge of Latin America and the Caribbean. |
| AfriNIC (African Network Information Centre) |  Responsible for Africa. |

These RIRs, in turn, allocate smaller blocks of IP addresses to Internet Service Providers (ISPs), enterprises and other organizations that need IP addresses for their networks.

Therefore, IP address allocation follows a hierarchy, from IANA to the RIRs and finally to end users. The RIRs work to ensure a fair and efficient allocation of IP addresses in their respective regions and also keep records of the allocations made. This ensures that IP addresses are used effectively and are not quickly exhausted at any given time.

## IP addresses

The IP address also known as the Internet protocol address, is the address of a device such as a computer web server or printer, on an internal or external network. One way to understand the concept is the address of a person so that mail can reach him, that mail has to carry the exact address of the person receiving it so that the mail staff knows where to send it. In the case of the Internet, that address would be a specific "door number" to be able to communicate with other devices and receive data packets from them. The IP address is based on the internet protocol, and each address can only be assigned once at a time.

There are two types of IP addresses with very different aspects, what they may have in common is that they are composed of a network identifier so that it can find its way in the IP routing, and a device identifier so that it can reach a specific device.

The two types of IP address are:

### IPV4

This IP type consists of a 32-bit address separated into 4 octets (group of 8 bits), limited to 4,294,967,296 unique addresses, many of which LAN. From a technical point of view, it is a 32-digit binary code between 0 and 1. It is usually represented as a combination of decimal numbers with values between 0 and 255 separated by dots. An example of an IPv4 address would be 192.168.178.31.

Currently, this IP address allocation goes through a class architecture consisting of three classes of IP addresses that an organization can receive from the Internet Corporation for Assigned Names and Numbers (ICANN).

- **Class A Network**

The first octet is assigned to identify the network, reserving the last three octets (24 bits) to be assigned to hosts, which would make 16,777,214 hosts available.

- **Class B network**

The first two octets are assigned to identify the network, reserving the last two octets (16 bits) to be assigned to the hosts, so you would have 65,534 hosts.

- **Class C network**

The first 3 octets are assigned to identify the network, reserving the last octet to be assigned to the hosts, so the maximum number of hosts would be 254 hosts.

These calculations can be done by raising 2 by the number of bits reserved to identify the network minus 2 addresses that are reserved for the broadcast and the assigned address of the network.

In the following table we can see how each of the network classes are differentiated:

| Class | Bits | N networks | N addresses p/network | N hosts p/network | Mask | Network mask |
| --- | --- | --- | --- | --- | --- | --- |
| A | 0 | 0.0.0.0 - 127.255.255.255 | 224 = 16,777,216 | 224 - 2 = 16,777,214 | 255.0.0.0 |
| B | 10 | 128.0.0.0 - 191.255.255.255 | 216 = 65,536 | 216 - 2 = 65,534 | 255.255.0.0 |
| C | 110 | 192.0.0.0 - 233.255.255.255 | 28 = 256 | 28 - 2 = 254 | 255.255.255.0 |
| D (Multicast) | 1110 | 224.0.0.0 - 239.255.255.255 | - | - | - |
| E (Experimental) | 1111 | 240.0.0.0 - 255.255.255.254 | - | - | - |

### IPv6 addresses

They have the same function as the IPv4 address, which consists of 128 bits and is expressed in 32-digit hexadecimal notation, this was created to solve the problem of IPv4 address exhaustion, as this had 4,294,967,296 (232) which is a number less than the world population and total devices. At the beginning of 2010, there were less than 10% of unassigned addresses, so IPv6 was developed to support 2128 or 340 sextillion addresses.

The biggest change from IPv4 to IPv6 is the length of network addresses, for ipV6 was assigned 128 bits, which corresponds to 32 hexadecimal digits, in many occasions IPv6 addresses are composed of two logical parts: a 64-bit prefix and another 64-bit part that corresponds to the interface identifier, which is almost always automatically generated from the MAC address of the interface to which the address is assigned. This is written as 8 groups of four hexadecimal digits e.g.:

```bash
2001:0db8:85a4:0000:15e2::a8e2:1380:7545
```

A group of four digits can be compressed if it has the value of 0000.

```bash
2001:0db8:85a4::15e2::a8e2:1380:7545
```

Following this rule, if more than two consecutive groups are null, they can also be compressed as "::". If the address has more than one set of consecutive null groups compression is only allowed on one of them. Thus, the following are possible representations of the same address:

```bash
2001:0DB8:0000:0000:0000:0000:1428:57ab
2001:0DB8:0::0:1428:57ab
2001:0DB8::1428:57ab
```

### Network Division: Subnetting

A large broadcast domain is a network that connects many hosts. One problem we can have with these hosts is that they can generate excessive broadcasts and negatively affect the network. This results in slow network operations due to the significant amount of traffic it can cause and slow device operations because a device must accept and process each broadcast packet.

The solution is to reduce the size of the network to create smaller broadcast domains in a process called subnetting. These smaller network spaces are called subnets.

This division into subnets reduces overall network traffic and improves network performance. It also allows an administrator to implement security policies such as which subnets are allowed or not allowed to communicate with each other.

The function of subnetting is to divide a large network into several smaller subnets, this must be done with great care and planning so as not to waste IPv4 addresses.

The networks can be subdivided more easily in the octet limit /8, /16, /24. This can be calculated knowing the subnet mask of the IP that we are going to configure.

| Prefix length | Subnet mask | Netmask in binary | # hosts |
| --- | --- | --- | --- |
| /8 | 255.0.0.0 | 11111111.00000000.00000000.0000000 | 16.777.214 |
| /16 | 255.255.0.0 | 11111111.11111111.00000000.00000000 | 65534 |
| /24 | 255.255.255.0 | 11111111.11111111.11111111.00000000 | 254 |

To see it more clearly, if we have a private network 10.0.0.0/8 as an internal network, with the octet limit we know that we can connect 16,777,214 hosts to the broadcast network. This would be ideal so we can subdivide the address at the /16 limits into two networks (10.0.0.0/16 and 10.255.0.0/16) with each subnet capable of connecting 65,534 hosts.

When we want to calculate all the subnets that we can get by segmenting the network the first thing we must do is locate the IP address class

```bash
192.168.0.0
```

This is a class C address and according to the data in the IP table it will have a netmask **255.255.255.0**.

We convert the number to binary:

```bash
11111111.11111111.11111111.00000000
```

And in the last octet, we change by 1 for the number of subnets we want to have exponentially.

If we want to have 4 subnets we will have to add 2 1 since 2 raised to the 1 is 2 and two raised to the 2 is 4, that will cover the subnets that we need.

```bash
11111111.11111111.11111111.11000000
```

> 💡 255.255.255.192 This would be the submask we are going to work with.

We know that we need 4 subnets and that they will go from the address 192.168.0.0.0 to 192.168.0.255 which will have 256 hosts available, so if we divide them between the 4 subnets we would have 64 hosts per subnet.

Of the 64 hosts, we will have 62 to assign since we need the network host and the broadcast host.

The network address will be the first address of the subnet and the broadcast address will be the last address.

| Subnet                    | Network Address  | Broadcast        |
|---------------------------|------------------|------------------|
| 192.168.0.1 - 192.168.0.62| 192.168.0.0      | 192.168.0.63     |
| 192.168.0.65 - 192.168.0.126| 192.168.0.64   | 192.168.0.127    |
| 192.168.0.129 - 192.168.0.190| 192.168.0.128 | 192.168.0.191    |
| 192.168.0.193 - 192.168.0.254| 192.168.0.192 | 192.168.0.255    |

## Manual and automatic IP address configuration

The IP address is the way to identify a device within a network. The IP address of a device can be configured dynamically/automatically through the DHCP protocol and manually.

The Dynamic Host Configuration Protocol (DHCP) is a client-server protocol which automatically provides a host with its IP address and other related configuration information such as the subnet mask and default gateway.

This protocol generates certain advantages since this process is automated and centrally managed. The DHCP server maintains a pool of IP addresses and delivers an address to any DHCP-enabled client when it logs on to the network. Since IP addresses are dynamic, rather than static (permanently assigned), addresses that are no longer in use are automatically returned to the pool for reassignment.

### How to activate the DHCP protocol

#### Activate the DHCP protocol in Windows

1. Click Start > Settings > Network and Internet.
2. Click Ethernet or Wi-Fi. Select Manage and click Edit next to IP Assignment.
3. Under edit network IP settings, select Automatic (DHCP.)
4. Click `Save` to activate the new settings.

#### Activate the DHCP protocol in Linux

1. Look for the option to edit connections.
2. Go to the IPv4 Settings option.
3. In the method select the DHCP option.

> 💡 The manual method consists of us assigning the IP address we are interested in. This will bring us advantages since we will know what address a particular device has, so we will avoid many problems when connecting to it. It also allows us to establish a sort of classification so that whenever we find a device on our network, we know what type of device it is.

### How to configure the IP manually

#### Configure IP manually in Windows

1. Click Start > Settings > Network and Internet.
2. Click Ethernet or Wi-Fi. Select Manage and click `Edit` next to IP Assignment.
3. Under `Edit` network IP settings, select `Manual`.
4. Enter the IP address you want to use and the rest of the information.
5. Click Save to activate the new settings.

#### Configure IP manually in Linux

1. Look for the option to edit the connections.
2. Go to the IPv4 Settings option.
3. In the method, select the `Manual` option.
4. Enter the IP you want to use and the rest of the data.
5. Select `Save`.

>💡**Discussion topics**  
>
>What is the main reason why the ICAAN decided to release the ipV6 protocol?
>
>What advantage can we have when dividing networks in an organization?
>
>What is the importance of knowing the network mask in a network partitioning process?
>
