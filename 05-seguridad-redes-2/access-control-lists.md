---
title: "Access Control Lists"  
subtitle: "Explore the world of Access Control Lists (ACLs) in networking: types, implementation, and application for efficient security."  
tags: ["cybersecurity", "networks"]  
authors: ["blindma1den", "lorenagubaira"]  

---

Access Control Lists (ACLs) are tools for filtering network packets, fundamental in network security, used to control traffic and protect network resources.

Access Control Lists (ACLs) are a feature that is generally included in most network devices, such as routers and switches, especially in equipment from manufacturers like Cisco, Juniper, HP, and others.

## Definition and Purpose

ACLs are sets of rules that allow or deny traffic on a network. They are used to implement security policies and control access to specific resources.

> ⚠️ In the following reading, we focus on Cisco devices and syntax as they are the most popular in the market.

## Types of ACLs

There are two main types of ACLs: **standard** and **extended**.

**Standard ACLs** filter traffic based solely on source IP addresses. They are less flexible than extended ACLs and are generally applied near the traffic destination.  
**Extended ACLs** allow more detailed control by filtering traffic based on multiple criteria, including source and destination IP addresses, protocols, and port numbers.

## How Do ACLs Work?

- **Basic Operation:** ACLs examine packet headers and apply rules to permit or deny traffic according to specified criteria.
- **Packet Filtering:** This is when ACLs analyze data packets and make decisions based on defined rules.

## Access Control Application for Standard ACLs

To apply an ACL to a specific interface, in the case of Cisco routers, you must enter "interface configuration mode" and use the `ip access-group` command. The syntax is:

```bash
$ router(config)# interface interface-name
$ router(config-if)# ip access-group N {in|out}
```

`interface-name` is the Cisco-specific syntax. For example: "ethernet-0",  
`N` is the number identifying the ACL to be associated with the interface.  
`IN` indicates incoming traffic and `OUT` indicates outgoing traffic.

In the figure, we want to allow all traffic from external networks (beyond the ethernet-1 interface) except for traffic from the 144.21.0.0 network. The ACL would be:

![Access control table](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/05-seguridad-en-redes-2/access-control-list/listas-de-control-de-acceso-image-1.jpg)

```bash
$ router(config)# access-list 1 deny 144.21.0.0 0.0.255.255
$ router(config)# access-list 1 permit any The second line is mandatory.
```

If it is not considered, the "default" rule already mentioned will apply, which, even if not visible, is:

```bash
$ router(config)# access-list 1 deny any
```

To apply the ACL to the ethernet-1 interface, the commands would be:

```bash
$ router(config)# interface ethernet-1
$ router(config-if)# ip access-group 1 in
```

Filtering only the incoming traffic in this way.

## Access Control Application for Extended ACLs

**Extended ACLs** share all other characteristics of **standard ACLs**, but they have a more complicated syntax because they allow filtering using many other criteria:

```bash
$ router(config)# access-list N {permit|deny} protocol source-IP [source-mask] [op source-port] destination-IP [destination-mask] [op destination-port]
```

In this case, N is a number between 100 and 199, to indicate that it is an extended list, protocol refers to the IP header protocol number field, and op can be:

- `lt`, meaning "less than."
- `le`, meaning "less than or equal to."
- `gt`, meaning "greater than."
- `ge`, meaning "greater than or equal to."
- `eq`, meaning "equal to."
- `ne`, meaning "not equal to."
- `range`, allowing a range of numbers to be specified.

If you want the following policy to be fulfilled in the same topology as the previous figure:

- Do not allow external Telnet traffic except from the address `155.15.1.1`.
- Allow any type of traffic from the address `133.11.1.3`.
- Do not allow general traffic except from the `144.21.0.0` network.

The access list would be:

```bash
$ router(config)# access-list 101 permit ip host 133.11.1.3 any
$ router(config)# access-list 101 permit tcp 155.15.11.1 any eq 23
$ router(config)# access-list 101 permit ip 144.21.0.0 0.0.255.255 any
```

As before, the default implicit condition does not allow more traffic to enter.
