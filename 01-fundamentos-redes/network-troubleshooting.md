---
title: "Network Troubleshooting"
subtitle: "Mastering Network Troubleshooting: Diagnostic Tools, Problem Identification, Resolution, and Event Monitoring for Optimal Performance."
tags: ["networks"]
authors: ["blindma1den", "lorenagubaira"]

---

Sometimes we may have performance problems in our network, and it is necessary to know the reason so we can take corrective actions. For this, we have tools that can perform a network diagnostic.

A network diagnosis is the procedure we perform to determine and inspect everything that is happening within our network.

For this purpose, different tools are applied that will allow us to detect possible failures or errors in the registers, as well as to eliminate them and correct the deviations.

Thanks to a network diagnosis we can increase the Internet connection speed, we can verify how many IP addresses are connected to our network, we can also control why a node cannot connect easily, and above all, with a network diagnosis, we can know what level of security the network has.

To perform a network analysis what we need is to know the structure, the design, and the degree of implementation of the network. To do this, we have to collect data and concepts that exist in the network. When it is a small network this step can be done quickly, but when we find ourselves with networks with a good number of nodes it is advisable to do it with great caution at this point.

The first thing we will do is to get to know the users and other people involved in the network. Then we will focus on the physical structure with its theoretical and real hardware diagram.

We will focus on layers 1, 2, and 3 of the 7-layer network model.

To achieve a good result at this stage we will make an inventory of all the cabling, connectors, and availability of nearby electricity, we will also determine the amount of optical fiber or ADSL, and we will analyze the routing of the other cables that work for the Internet connection.

Knowing the entry points and cables, we will go to the information traffic, studying the different protocols that exist in the network and thus be able to define the quality of service they are providing.

Once we have all this data, we will have to confirm and identify the security that the network has concerning Internet browsing through firewall and other security devices, both in hardware and software.

## Identification of and resolution of common problems

When we know that something is wrong with our network, the first thing to do is to focus directly on our device.

To do this, it is advisable to turn it off or reboot it and check if the problem still exists.

If this is not solved we will have to verify the hardware part of our network, we will analyze the cable connections between our router and the devices, and if we have a LAN network, we will verify the state of the connectors as well as the general state of all the external components.

In the case of Windows, it has its network diagnostic tool, which we can get in "network and internet" and look for the option "Network troubleshooter". We can also get tools such as Uptrends Uptime Monitor and Wifi Explorer.

Among the most common problems that we can get in our network, we can get:

- **Slow Network**.

There can be many reasons why a network that provided adequate performance in the past now frustrates users. A failed switch port or link can cause traffic to be routed around the failure and overload another link.

Another network speed issue could arise if employees decide to download high-definition videos while at work because downloading in the office is faster than if they use their Internet connection at home

> 💡 This we could solve with a network monitoring tool.

- **Physical connectivity problems**.

A network connection can be suddenly interrupted by physical connectivity problems, this problem is common when a network cable is damaged or comes loose. At the moment cables may be added or removed on a switch, and one of the other cables may accidentally disconnect.

- **Slow DNS lookup**

DNS matches the common name used to match server or service names to the Internet address that routes a network request. For the most commonly used names, the match is probably already stored in the system's DNS cache, and the lookup is fast. For lesser-used names, the match may be stored in a more distant cache, such as the root server of the top-level name, like .com, .org

Each DNS server along the path checks its cache before requesting the next server along the path. The next server then checks its cache, repeating the process. If the lookup is slow, there may be a slow link in the path or a slow or overloaded server. To solve this problem, the local network administrator can reconfigure the local routers to move requests to a faster server chain.

- **Duplicate and static IP addresses**.

In a network, no two systems can share the same Internet address. If there are duplicate Internet addresses, neither system can reliably access the network. Addresses for most network devices are assigned when the Dynamic Host Configuration Protocol (DHCP) boots the systems on the local network. DHCP maintains a pool of addresses assigned to the local network, assigning a different address from the pool to each system.

Workstations are not assigned permanent addresses but receive one for a limited time from DHCP. Systems reapply before the time runs out and usually receive the same address. If the system is shut down without re-requesting and the time times out, it loses this address and may receive a different one on boot up.

## Network Monitoring and Event Logging

We usually call the activities of users on the network events, and this generates information about individual events or tracks trends of events to quickly identify abnormal behavior, one of the functions of this monitoring is to ensure security and protect the company's data.

Among the data that we can monitor, we have:

- Logins.
- Session closures.
- Web page loads.
- Application Programming Interface (API) calls.

All these events can be stored in an event log file, and are available for viewing and downloading after 24 hours.

**Other uses we can give to the event monitoring:**

- Monitor data loss: In some cases such as a former employee leaving with a competitor, if we have not removed their user from the system they could access their account and obtain company information, so with event monitoring we could discover those activities.
- Optimize performance: Sometimes it is difficult to determine the cause of poor network performance, and event monitoring can determine if the cause is related to a network problem or some other reason.

>💪 **Challenge:**
>
>Perform a test on your event monitoring computer and review all the events that have occurred in your session. Then describe the events that seem most important to you at the corporate level.
