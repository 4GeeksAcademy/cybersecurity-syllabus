---
title: "Complete Guide to Internet Connectivity: DSL, Cable, Fiber Optics, and Internet Service Providers (ISP)"
subtitle: "Understand the Main Internet Connection Technologies and Configure Your Network with Routers and DHCP"
tags: ["cybersecurity", "networks"]
authors: ["blindma1den", "lorenagubaira"]

---

## Internet connectivity

We know that the internet is a protocol that connects all the networks and so access to them, it is used by different types of users. Nowadays there are companies in charge of managing these connections. Using different types of technologies for this, among which we have:

- **DSL**

DSL stands for digital subscriber line and is used to provide a broadband internet connection and there are several types of DSL.

DSL technologies use two types of data transmission modes: symmetric and asymmetric.

- **Symmetrical DSL**

Symmetric digital subscriber line (SDSL), developed to overcome the limitations of traditional access technology. Compared to this older traditional transmission technology, DSL is easy to install and error-correct.

Multiplexing supports voice, video and data multiplexing services. HDSL, SDSL, IDSL technologies are some of the main forms of symmetrical DSL.

- **SDSL**

Single Line DSL (Single Line DSL) is a version of HDSL that uses a single cable and provides bidirectional bit-rate, high-speed variable data transfer also known as SHDSL. It uses the single twisted pair of wires to deliver a payload of 192 kbit/s to 2,312 kbit/s in 8 kbit/s increments and 384 kbit/s to 4,624 kbit/s in 16 kbit/s increments for two pairs of wires.

In SDSL the upstream (subscriber to network) and downstream (network to subscriber) bandwidth direction is identical to each other and can be considered as the counterpart of the asymmetrical digital subscriber line (ADSL), but with slight variations.

- **HDSL**

HDSL stands for High Bit Rate Data subscriber line. This DSL technology falls under the symmetrical data transmission mode; this transmission protocol was approved in 1994 and was the first DSL technology. It uses two pairs of twisted-pair copper wires to transmit data at various speeds of N × 64 kbps, up to E1 speed. Over 3.6 km, HDSL can transmit data normally without the need for amplifiers. HDSL2 and HDSL4, proprietary SDSL, and G.SHDSL are the enhanced versions.

- **Asymmetric DSL**

In asymmetric DSL technology, the upstream bandwidth is less than the downstream bandwidth. It provides bi-directional bandwidth for different requirements such as web browsing, multimedia on demand and information distribution. Asymmetric DSL technologies mainly include ADSL and VDSL.

- **ADSL**

ADSL (Asymmetric DSL / Asymmetric DSL) also uses a twisted pair of copper telephone lines with a downstream speed capacity of up to 8Mbps and upstream of 1Mbps. It can transmit up to 3 or 5 kilometers. Typically in the home, ADSL only needs to install ADSL equipment at both ends of the line to provide high-speed broadband services without the need for rewiring.

- **VDSL**

VDSL (Very High-Speed Digital Subscriber Line) is the transmission bandwidth, is one of the highest xDSL access technologies, it is regarded as the transfer of high-end residential broadband services on the copper end technology. VDSL technology has the following characteristics.

The transmission speed is high, providing symmetrical and asymmetrical transmission modes in both uplink and downlink. In asymmetric mode, the maximum downlink speed of VDSL can reach 52 Mbit/s (in the 300 m range), and the maximum speed in symmetric mode can reach 34 Mbit/s (in the 300 m range). VDSL overcomes the shortcomings of ADSL's insufficient bandwidth in the upstream direction.

## Coaxial cable connection

Coaxial cable is a type of specially constructed copper cable with metal shielding and other components designed to block signal interference.

Coaxial cables have concentric layers of electrical conductors and insulating material. This construction ensures that signals are enclosed within the cable and prevents electrical noise from interfering with the signal.

The center conductor layer is a thin conductive wire, either solid copper or stranded. A dielectric layer, consisting of an insulating material with well-defined electrical characteristics, surrounds the wire. Then, a shield layer surrounds the dielectric layer with a metal foil or braided copper mesh. The entire assembly is wrapped in an insulating sheath. The outer metal shield layer of the coaxial cable is usually grounded at the connectors at both ends to protect the signals and as a place for stray interference signals to dissipate.

Generally we can see this type of connection in the internet services provided by cable television companies.

### Fiber optic

Fiber optic Internet is a broadband connection that can reach speeds of up to 940 Megabits per second (Mbps) with little delay. The technology uses fiber optic cable, which surprisingly can send data at a speed of approximately 70% the speed of light. In addition, fiber optic cables are not as susceptible to harsh weather conditions as other types of traditional cables, minimizing service interruptions. They also resist electrical interference more effectively.

Fiber optic Internet is a complex technology that enables the transmission of information in the form of light, rather than electricity. There are many components that make up this advanced technology, but two of the main ones are the optical fiber and what is called the “last mile” of the fiber optic network.

Optical fibers are tiny, with a diameter of approximately 125 microns or just a little larger than a human hair. Many of these fibers are bundled together to form cables (not to be confused with coaxial cables, which are composed of copper). Optical fibers conduct pulses of laser or LED light down the line, which transmit information in “binary” form, similar to the 0's and 1's used in electronics.

Once these superfast pulses of light reach their destination, they are converted into electrical power that devices can understand and use. This is accomplished by special equipment called an optical network terminal, which then sends the signal over an Ethernet connection to the user.

## Internet Service Providers (ISP)

An Internet Service Provider (ISP) is a company or entity that provides Internet access to users. ISPs play a key role in global connectivity, as they are responsible for providing access to the worldwide network of networks.

ISPs offer a variety of services, ranging from basic Internet connectivity to more advanced services such as IP telephony and Internet TV. To provide these services, ISPs use a network infrastructure that includes fiber optic cables, telephone lines, satellites and wireless technologies.

There are different types of ISPs, which are classified according to their scope and the way in which they provide the service. Tier 1 ISPs are the top-tier Internet providers, which have a global network infrastructure and connect directly to the Internet's traffic exchange points. These ISPs are usually large-scale telecommunications companies.

On the other hand, Tier 2 ISPs are regional or national providers that connect to Tier 1 ISPs for Internet access. These ISPs may offer services locally or in a specific region, and are typically smaller companies or telecommunications service providers.

In addition to Tier 1 and 2 ISPs, there are also Tier 3 ISPs, which are smaller service providers that connect to Tier 2 ISPs for Internet access. These ISPs typically offer services locally or in smaller geographic areas.
ISPs play a crucial role in Internet connectivity, as they are responsible for maintaining and managing the network infrastructure necessary to transmit data over the Internet. In addition to providing Internet access, ISPs may also offer additional services, such as website hosting, domain registration and online security.

> 💡 Importantly, ISPs may also enforce acceptable use policies and manage bandwidth to ensure fair and efficient use of network resources. They can also implement security measures, such as firewalls and intrusion detection systems, to protect users from online threats.

**Lab: Basic router configuration for Internet connection**. 

> 🔥 This lab uses cisco packet tracer.

1. We do the environment configuration.
2. We add a router and connect it to two switches, each switch will connect to two PCs.

![Switch](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/switch.png?raw=true)

3. Configure the router interfaces. There are two ways to do this
4. Through the graphical interface.
5. Click on the router and go to the **config** tab.
6. Click on the **FastEthernet0/0** tab and configure the ip.

- IPv4 Address:** `192.168.5.1`.
- Subnet Mask:** `255.255.255.0`.

7. Turn on the port by clicking on the **Port Status** box.

![Port Status](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/port-status.png?raw=true)

8. Repeat the process with port **FastEthernet0/1**.

- IPv4 Address:** `192.168.10.1` **Subnet Mask:** `255.255.255.0` **Subnet Mask:** `255.255.255.0` **Subnet Mask:** `255.255.255.0
- Subnet Mask:** `255.255.255.0` **Subnet Mask:** `255.255.255.0` **Terminal

**Through the terminal**

9. We click on the router and go to the CLI tab and add the following commands:

```
Router>enable
Router#configure terminal
Enter configuration commands, one per line. End with CNTL/Z.
Router(config)#interface FastEthernet0/0
Router(config-if)#ip address 192.168.5.1 255.255.255.255.0
Router(config-if)#no shutdown
Router(config-if)#
%LINK-5-CHANGED: Interface FastEthernet0/0, changed state to up
%LINEPROTO-5-UPDOWN: Line protocol on Interface FastEthernet0/0, changed state to up
exit
```

10. Repeat the process for interface **FastEthernet0/1**.

```
Router(config)#interface FastEthernet0/1
Router(config-if)#ip address 192.168.10.1 255.255.255.255.0
Router(config-if)#no shutdown
Router(config-if)#
%LINK-5-CHANGED: Interface FastEthernet0/1, changed state to up
%LINEPROTO-5-UPDOWN: Line protocol on Interface FastEthernet0/1, changed state to up
exit
```

![Router](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/router.png?raw=true)

**DHCP pool configuration**

A DHCP pool is the addresses within a given range. All IP addresses within that range will be allocated by the DHCP server as clients request them.

This pool is useful when we are configuring a large network and we want to assign ips through the DHCP protocol.

To configure the pool we enter again in the router in the **CLI** tab and add the following commands:

```
Router(config)#ip dhcp pool ip5
Router(dhcp-config)#network 192.168.5.0 255.255.255.255.0
Router(dhcp-config)#default-router 192.168.5.1
Router(dhcp-config)#exit
```

![Dialog](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/dialog.png?raw=true)

11. The ip dhcp pool **NAME** command creates a set of ip's with the chosen name and causes the router to enter DHCP configuration mode.
12. We repeat the process now with **ip10**.

```
Router(config)#ip dhcp pool ip10
Router(dhcp-config)#network 192.168.10.0 255.255.255.255.0
Router(dhcp-config)#default-router 192.168.10.1
Router(dhcp-config)#exit
```

13. Configuration of pc ip.
14. Now we are going to click on the computers and select the IP configuration option.
15. In the ip Configuration selection we select DHCP and wait for the IP assignment.

![DHCP](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/dhcp.png?raw=true)

It must be within the same network assigned on the network interface.

16. We can check that the connection between the computers on the network is established by pinging each other.
17.  The ipconfig command will give us the IP information of the device.

![ipconfig](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/ipconfig.png?raw=true)

In this way we can configure a network in order to have a better administration of the network, and also assign the IP range which we want to work in the different subnets that we can have.