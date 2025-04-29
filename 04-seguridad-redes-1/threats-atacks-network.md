---

title: "Network Threats, Vulnerabilities, and Security Procedures"
subtitle: "Network Security: Threats, Vulnerabilities, and Defense Strategies. Learn to Combat DoS, DDoS, MITM Attacks, and More"
tags: ["networks", "cybersecurity"]
authors: ["blindma1den", "lorenagubaira"]

---

In the last ten to fifteen years, we have seen a paradigm shift where **crackers or cybercriminals** seek to exploit all possible vulnerabilities within any organization or national infrastructure. To counteract this, we must all change our perspective on how we view security in the computing and networking fields. We need to understand certain attacks and learn what we can from them to be as prepared as possible and sometimes even avoid them. In the world of security, we cannot say we are prepared to prevent every attack.

## DoS Attack or Denial of Service Attack

A **denial of service attack** aims to **disable the use of a system**, application, computer, or server to block the service for which it is intended. This attack can affect both the source that provides the information, such as an application or the transmission channel, and the computer network. In other words, the cybercriminal will try to prevent users from accessing information or services.

The most common type is when **an attacker "floods" a network** with a large amount of data, causing the entire network to become saturated. For example, in a DoS attack on a website, when we enter a URL and access it, we send a request to display the information. An attacker could make millions of requests to crash the entire system. Hence, this attack is called "denial of service" because it prevents access to the targeted site.

Some problems we will encounter if subjected to a DoS attack include significant network performance degradation and slowness (opening files or accessing websites). A particular website becomes completely inaccessible and unavailable. We will be unable to enter any websites we attempt to access. There will be a drastic increase in the amount of spam we receive.

## Types of DoS Attacks

Beyond knowing what it is, there are several types of DoS attacks.

### ICMP Flood Attack

This type of denial of service attack depletes the victim's bandwidth. It involves sending a large amount of information using ICMP Echo Request packets, i.e., the typical ping, but modified to be larger than usual. The victim might also respond with ICMP Echo Reply (ping response) packets, adding additional overload to the network and the victim. Usually, one or more powerful computers are used to attack a single victim, preventing the victim from properly handling the generated traffic.

### Ping of the Dead

This attack is similar to the previous one. It involves sending a packet larger than 65536 bytes, causing the operating system to crash as it attempts to reassemble the large packet. Today, this attack does not work because operating systems discard such packets directly. Knowing about this attack is essential to avoid it in the future, but current operating systems have many protections to prevent it.

### Tear Drop Attack

This attack involves sending a series of large packets, making it impossible for the destination (victim) to reassemble them, overwhelming the operating system and causing it to crash. Once the attack stops, a restart might be needed to return to normal operation. Modern operating system kernels incorporate protections against these attacks.

### Jolt Dos Attack

This attack fragments an ICMP packet so that the victim cannot reassemble it. This increases CPU usage in the victim, creating a significant bottleneck. As a result, the victim's computer becomes very slow because the CPU is busy trying to reassemble the packet.

### Land Attack

This attack sends a fake TCP SYN packet with the target's IP address used as both the source and destination. When the target receives the packet, it becomes confused and does not know where to send it, causing a crash. This type of attack is typically recognized by operating systems, firewalls, and even antivirus suites.

### Smurf Attack

This attack sends many ICMP Echo Request messages to the broadcast IP address with the victim's IP address as the source. This way, the victim receives all the ICMP Echo Reply responses from the network, causing it to become overwhelmed. Before executing this attack, IP Spoofing must be done to fake the ICMP Echo Request's source IP address. This massive attack makes the network stop functioning normally due to high broadcast traffic. Today, switches are designed to automatically prevent these attacks based on PPS (Packets Per Second).

### SYN Flood

This attack is one of the most widely used globally. It sends TCP packets with the SYN flag activated, sending hundreds or thousands of packets to a server to open multiple connections, aiming to overwhelm it completely. This attack typically uses a fake source IP address, so all responses go to a non-existent IP or a victim's IP, which also becomes overwhelmed by TCP responses from the server.

> 👉 SYN Flood attacks can be easily prevented with a firewall by limiting the number of TCP SYN packets that can be received and even placing an intermediate proxy to add additional verification before passing messages to the web server or any other service using the TCP protocol.

### Fraggle Dos Attack

This attack sends a lot of UDP traffic to a broadcast IP address with the victim's IP address as the source. IP Spoofing must be done to carry out this attack. The network will deliver the traffic to all hosts because we are sending UDP packets to the broadcast address, and the devices will respond. This causes the victim to receive a large amount of traffic that it cannot handle properly and will be unable to function normally.

## Distributed Denial of Service (DDoS) Attack

This network attack overwhelms a victim from multiple source computers, such as a botnet of a thousand computers attacking a target. These attacks are common and use techniques such as SYN Flood. Even if a powerful server can handle millions of SYN Flood requests, it cannot withstand a botnet attack from hundreds or thousands of computers and will eventually crash. This attack is "distributed" among different devices, including computers, other infected servers, hacked IoT devices, and more.

Tips for mitigating DDoS attacks include:

- Properly configure the router firewall.
- Block all network traffic except what is specifically allowed.
- Disable any unused services.
- Regularly check network settings and logs.
- Implement a robust logging policy for event correlation (SIEM).
- Have a good password policy with appropriate permissions.
- Limit network bandwidth per port to prevent attacks from within your network.

### HTTP Request Smuggling Attack

An **HTTP Request Smuggling attack** exploits discrepancies in analysis when one or more HTTP devices/entities are in the data flow between the user and the web server. This technique interferes with how a website processes HTTP request sequences received from one or more users. These vulnerabilities are often critical, allowing the cybercriminal to bypass security controls, gain unauthorized access to private data, and even directly compromise other users of the application. This illegal HTTP request traffic allows for various attacks such as cache poisoning, session hijacking, and bypassing web application firewall protection.

This attack can affect different devices and services: the web server, firewall, or proxy server. It originated in 2005, demonstrated by Watchfire researchers, including Klein, Ronen Heled, Chaim Linhart, and Steve Orrin. In recent years, enhancements have expanded the attack surface, allowing maximum privilege access to internal APIs and cache poisoning.

### How HTTP Request Smuggling Occurs

Web applications frequently use chains of **HTTP servers** between users and the final application logic. Users send requests to a front-end application server, which then forwards them to one or more back-end service servers. This architecture is increasingly common and sometimes unavoidable in cloud-based applications.

When a front-end application server forwards HTTP requests to a back-end service server, it usually sends multiple requests over the same back-end network connection. This is done for efficiency and higher performance. First, HTTP requests are sent one after the other. Then, the receiving server parses the headers of each HTTP request to determine where one request ends and the next begins.

The **front-end and back-end systems** must **agree on the request boundaries**. If not, a cybercriminal could send an ambiguous request to the front-end and back-end systems, which might interpret it differently.

Here, the attacker causes part of their front-end request to be interpreted by the back-end server as the start of the next request. This interferences with the application's processing of that request, leading to an HTTP Request Smuggling attack, which can have disastrous consequences for the server owner.

### Why HTTP Request Smuggling Attacks Occur

Many HTTP Request Smuggling vulnerabilities arise because the HTTP specification provides two ways to specify where a request ends. One header is simple, specifying the message body length in bytes. This can indicate that the message body uses chunked encoding, meaning the body contains one or more data chunks. Some security administrators are unaware that chunked encoding can be used in HTTP requests, which poses a problem.

If a single message uses both methods simultaneously, they conflict. The HTTP protocol attempts to solve this by stating that if both Content-Length and Transfer-Encoding headers are present, the Content-Length header should not be used. This approach may suffice to avoid ambiguity with a single server, but not with two or more chained servers.

If the front-end and back-end servers behave differently regarding a potentially obfuscated Transfer-Encoding header, they might disagree on the boundaries between successive requests. This could lead to vulnerabilities and an HTTP Request Smuggling attack.

### How to Prevent HTTP Request Smuggling

HTTP Request Smuggling attacks involve placing both the Content-Length and Transfer-Encoding headers in the same HTTP request and then manipulating them so that front-end and back-end servers process the request differently.

Klein, previously mentioned, advocates for normalizing outgoing HTTP requests from proxy servers and highlights the need for a robust, open-source web application firewall solution capable of handling such attacks. Klein has published a C++-based project

 to ensure all incoming HTTP requests are fully valid, compatible, and unambiguous. This work is available on GitHub [here](https://github.com/SafeBreach-Labs/RSFW).

Other measures to prevent an HTTP Request Smuggling attack include:

- Disabling back-end connection reuse so that each back-end request is sent over a separate network connection.
- Using HTTP/2 for back-end connections, as this protocol avoids ambiguity in request boundaries.
- Using the exact same web server software for front-end and back-end servers to ensure agreement on request boundaries.

As you have seen, HTTP Request Smuggling is a significant attack due to its severity. Although dangerous, we have different ways to prevent and mitigate this attack correctly.

## Man-In-The-Middle Attack

Man-in-the-Middle attacks are a type of attack that subsequently enables others. MITM attacks involve positioning oneself between the communication of two or more devices to read, modify, and even block traffic from the source to the destination. These attacks can intercept all online navigation and any communication while potentially redirecting all information to another existing device.

An example of a MITM attack is when a cybercriminal intercepts communication between two people or between us and a web server. The cybercriminal can intercept and capture all sensitive information we send to the site.

### How to Prevent Man-In-The-Middle Attacks

MITM attacks are not impossible to prevent. With Public Key Infrastructure (PKI) technology, we can protect devices from attacks. This allows us to authenticate securely with other users, verify the recipient's identity with public cryptography, digitally sign information, ensure non-repudiation, and send fully encrypted information to maintain confidentiality.

In a PKI cryptographic operation, at least the following parties are conceptually involved:

- An initiator of the operation.
- Server systems that validate the operation and ensure certificate validity, including the Certification Authority (CA), Registration Authority, and Time Stamping System.
- A recipient of the encrypted and signed data, guaranteed by the operation initiator.

Public key cryptographic operations use asymmetric encryption algorithms known and accessible to all, such as RSA or elliptic curve-based algorithms. Thus, PKI technology's security is strongly linked to the privacy of the private key.

## Social Engineering Attacks

Although social engineering attacks are not direct attacks on data networks, they are very popular and used by cybercriminals. These attacks involve manipulating a person into providing user credentials, private information, and more. Cybercriminals always look for ways to obtain user credentials, credit card numbers, bank accounts, etc., by tricking victims into thinking they are someone else.

These attacks are highly successful because they target the weakest link in cybersecurity: humans. It's easier to obtain a person's credentials through social engineering than to hack a service like Google to extract passwords. It's crucial to know whom to trust, when to trust, and when not to trust. No matter how secure our network is, if we trust the wrong person, all that security is worthless.

### How to Prevent Social Engineering Attacks

The first recommendation is not to rush to respond to cyber attackers. Many of these attacks always convey a sense of urgency, such as urgently needing to transfer money to an unfamiliar recipient. It is necessary to be suspicious of any strange or unsolicited message. If the email appears to be from a website or company we regularly use, we should conduct a small investigation, including contacting the company to verify the information.

- Be cautious with requests for banking information.
- Never provide access passwords, not even to banks.
- Reject any help from third parties; they may be cybercriminals trying to steal information or money.
- Avoid clicking on links in emails that could be phishing and avoid downloading suspicious documents.
- Set up spam filters, configure your computer with antivirus and firewalls, review email filters, and keep everything updated.

## OS Finger Printing

OS Finger Printing refers to any method used to determine the operating system used by the victim to exploit it. Typically, this type of attack is conducted during the pentesting phase. OS recognition is done by analyzing protocol indicators, response time to specific requests, and other values. Nmap is one of the most widely used programs for OS Finger Printing. Why would an attacker need to know the victim's operating system? To launch more targeted attacks, understand vulnerabilities, exploit them, and much more.

There are two types of OS Finger Printing:

- **Active**: Sending specially crafted packets to the target device and analyzing the response in detail to gather information. Nmap conducts this type of attack to obtain as much information as possible.
- **Passive**: Analyzing received information without sending specifically designed packets to the target device.

## Port Scanning

In any pentesting, port scanning is the first step to try to exploit a target. It is one of the most commonly used reconnaissance techniques by cybercriminals to discover exposed services with open ports, whether a firewall is in use, and even the victim's operating system. All devices connected to the local network or the Internet use many services that listen on specific TCP and UDP ports. Port scans identify which ports are open and which service is behind them, aiming to exploit a vulnerability in that service.

Port scans involve sending messages to each port one by one. Depending on the type of response received, the port will be open, filtered, or closed. Nmap is one of the most commonly used programs for port scanning, the Swiss Army knife of port scanning, because it also includes Nmap NSE, which allows the use of scripts to exploit known vulnerabilities or attack Samba, FTP, SSH servers, etc.

Knowing which ports are open is crucial because a port identifies a service running on the system. For example, the FTP protocol uses port 21; if it's open, it could mean an FTP server is listening, making it a target for attack. Port scanning is the first phase of pentesting.

### How to Prevent Port Scanning

We cannot prevent port scanning because we cannot stop a cybercriminal from trying to see which ports are open. However, we can protect all ports with a well-configured, restrictive firewall. Performing a port scan is illegal, as declared in several courts, because it is the first step of intrusion or exploiting a vulnerability.

To limit the information provided to an attacker during a port scan, we should:

- Close all firewall ports except those necessary for system operation.
- Use a restrictive firewall policy, only opening what will be used.
- Disable unnecessary operating system services.
- Configure web, SSH, and FTP services to limit information like version numbers to prevent exploitation.
- Use TCP Wrappers for greater flexibility in allowing or denying access to specific services.
- Use programs like fail2ban to block IP addresses conducting attacks.
- Use IDS/IPS like Snort or Suricata to block attackers' IPs.

## Other Attacks

Additionally, there are many other attacks you should be aware of.

### ARP Spoofing

This attack on data networks is one of the most popular, allowing attackers to target devices on the same local network, whether wired or wireless. When conducting an ARP Spoofing attack, the attacker can impersonate the router or gateway, causing all network traffic or traffic from a specific PC (victim) to pass through them, allowing them to read, modify, or block network traffic.

This attack only works on IPv4 networks, but a similar attack exists on IPv6 networks because the ARP protocol is only available on IPv4 networks. This attack is the easiest way to conduct a Man-in-the-Middle attack and capture all the victim's information. Reverse ARP could be used to detect these attacks, a protocol to query IPs associated with a MAC address. If we have more than one IP, it means we are under attack. Some security suites already detect these attacks, and even managed switches allow IP-MAC Binding to prevent them.

### MAC Flood Attack

This is one of the most typical attacks on data networks. It involves flooding a network with many MAC addresses from a switch, each with different source MAC addresses, aiming to overflow the switch's CAM table, causing the switch to function as a hub. Today, all switches have protections against this attack, allowing them to remove MAC addresses quickly, preventing overflow, but the switch's CPU will be 100%, causing network slowness.

In managed switches with VLANs, overflow only affects the specific VLAN, not the rest of the network's VLANs. To prevent these attacks, it's advisable to configure Port Security on switches and limit the number of MAC addresses per port. This way, the port can automatically shut down or restrict new MAC addresses until further notice.

### DNS Cache Poisoning

This attack involves providing false DNS data to a victim, causing them to visit fake or controlled websites. A device making DNS requests could receive spoofed IP addresses based on its DNS request, redirecting the victim to any site under the attacker's control.

### IP Spoofing

This attack involves impersonating the source IP address of a specific device, allowing TCP, UDP, or IP packets to be sent with a fake source IP, impersonating the real IP address. This has several objectives: hiding the true source identity or impersonating another device so that all responses go directly to it.

### ACK Flood

This attack involves sending TCP ACK packets to a specific target, usually with a fake IP, so IP spoofing is necessary. It is similar to TCP SYN attacks, but if the firewall blocks TCP SYN packets, this is an alternative to block the victim.

### TCP Session Hijacking

This attack involves taking over an existing TCP session used by the victim. For this attack to succeed, it must be done at an exact moment during the initial TCP connections when authentication occurs, which is when the cybercriminal executes the attack.

### ICMP Tunneling

This attack is mainly used to evade firewalls because firewalls usually do not block ICMP packets. It can also be used to establish an encrypted, hard-to-trace communication channel. An ICMP tunnel establishes a covert connection between two devices

, which can also be used with UDP using DNS.

To prevent ICMP tunnels, inspect ICMP traffic in detail and see what types of messages are exchanged. If data encryption is used, it becomes more complex, but it will be detected as "abnormal" ICMP traffic, triggering IDS/IPS alerts if configured correctly.

### LOKI Attack

This is not a network attack; it is a client/server program that allows information exfiltration through protocols that typically do not carry a payload. For example, SSH traffic can be tunneled within the ICMP protocol using ping or UDP for DNS. This can be used as a backdoor on Linux systems to extract information and send it remotely without raising suspicion. This is something that should also be controlled through firewalls.

One of its versions, LOKI II, is one of the first examples of a covert channel. These are communication methods using unconventional means to transfer information between different processes, systems, and even networks, bypassing common security policies. They are often used for data extraction from compromised systems or receiving commands from an attacker.

Despite this innovative system, modern intrusion detection techniques and security solutions have advanced significantly. Thus, these covert channels are now well-known and generally detected by modern security solutions. However, the concept of LOKI and other covert channels remains relevant. Attackers seek and use methods to evade detection and transfer data stealthily.

### TCP Sequence Attack

This attack attempts to predict the sequence number of TCP traffic to identify packets in a TCP connection and hijack the session. A typical scenario is when an attacker monitors the data flow between two devices. The attacker could disrupt the real device's communication and establish themselves as the real device by predicting the sequence number of the next TCP packet. The attacker "removes" the real device using a DoS attack or similar.

By predicting the sequence number, the attacker's packet can reach its destination before any legitimate host information because the latter is under a DoS attack, preventing communication with the victim host. The attacker's packet could gain system access, forcibly terminate a connection, or send malicious payloads.

> 💡 **How to Prevent TCP Sequence Attack:** In 2012, the IETF released a new standard to establish an improved algorithm to prevent attackers from guessing the initial sequence number in TCP communications. This standard is designed to enhance the robustness of TCP communications against predictive analysis and monitoring by attackers. Currently, all operating systems use this new standard to prevent this attack, so an attacker cannot predict sequence numbers, although in certain circumstances, they may still guess them, though it is much more difficult than before.

### ICMP Redirect Attack

This network attack, called ICMP Redirect, allows redirecting an originating host to use another gateway closer to the destination. Naturally, an attacker will position themselves as the gateway, so all traffic passes through them for capture, modification, or blocking. These messages are sent to different hosts, but Linux systems are not affected today because it is internally disabled. However, other operating systems might still be affected.

Some known attacks using ICMP Redirect are:

- Man-in-the-Middle Attacks
- Denial of Service
- Traffic Redirection to Malicious Sites

Ways to protect against these include:

- Disabling ICMP Redirect
- Filtering ICMP messages
- Intrusion detection
- Using private VPN networks.

### DNS Zone Transfer Attack

This attack targets DNS servers, involving the DNS server returning a list of hostnames and IP addresses in the domain. These zone transfers typically occur between authoritative DNS servers, but this attack could allow cybercriminals to query DNS servers for a host list to attack. However, these attacks have risks associated with zone transfer attacks, including:

- Detailed reconnaissance of the network structure, facilitating other attacks.
- DNS poisoning with the obtained information, making it easier for the attacker.
- Targeted attacks on specific locations, knowing specific servers and services.

Common ways to mitigate and prevent these issues include access restrictions and control lists. It is also important to monitor and alert the network and use security updates and features like DNSSEC.

## The Danger of a Web Shell

A web shell is a malicious script inserted into attacked systems. In most cases, web servers are the target. Once these systems have a web shell, the cybercriminal can remotely control it. Consequently, they have persistent access to the system and can manage it as they wish. This means web shells can create backdoors in compromised systems for partial or total control.

Moreover, web shells have a broader reach. They can also compromise network device management interfaces, making good secure network management practices crucial, especially in networks with hundreds or thousands of connected devices daily.

The rise of remote work brings known security risks that deserve special attention because working in a "secure" company network is not the same as working from home. However, you might wonder if using VPN services is enough to securely connect to organizational resources; that is only part of what a network administrator should do.

### Common Uses

One advantage of web shell attacks is their versatility and difficulty in detection. They are dangerous and can be used for:

- Data theft
- Infecting website visitors
- Launching DDoS attacks
- Modifying files with malicious intent
- Acting as a bot in a botnet.

### How It Works

These attacks are divided into several stages. First, the attacker creates a persistent mechanism on the server for remote access. Then, they try to gain necessary privileges to use backdoors or other methods to attack or use available resources for illicit activities. Once they have root privileges, they can make many changes at will, such as changing permissions, installing software, deleting content or users, stealing passwords, etc.

The attacks first target vulnerable servers using scanning programs. Once they find a vulnerability, they launch the attack immediately before the identified flaw is patched.

The script provides the attacker with the necessary backdoor for remote server access. Often, the hacker patches the vulnerability to prevent others from inserting another web shell through it and avoid detection. They may even set authentication factors like passwords so only a specific attacker can access it.

### Detecting a Web Shell

Detecting these attacks is complex because all actions must be performed within the server where the web shell is located. Here are some detection methods, but the most effective is prohibiting affected functions and auditing the server and website.

These audits can detect the **existence of a web shell** and prevent attackers from exploiting vulnerabilities to upload another shell.

The main challenge in detecting **this type of malware** is that attackers can use encryption methods to cover their malicious activity. This is a direct consequence of how easily scripts can be introduced. As we know, the possibilities for cyberattacks are endless, and network protection must be increasingly reinforced. Effective detection methods include:

- Comparing a different version of the web application to the one in production, which refers to the application available to users. This comparison analyzes differences for any unusual activity.
- Looking for anomalies in web application traffic using monitoring tools.
- Applying signature-based detection, verifying all modified web shells, even with minimal changes.
- Identifying unusual network traffic patterns.

> 👉 What tools and procedures should be applied to detect these malicious scripts? Below are fundamental recommendations for effective protection.

## How to Protect Your Systems and Networks

These web shells are also directly introduced to **systems and networks** that fall victim, mainly because web applications (mostly) and their vulnerable infrastructure have permissions to directly modify a web-accessible directory or pieces of web code. However, such permissions should not be granted.

Consequently, systems themselves open the door for cybercriminals to carry out attacks. Blocking modification permissions is recommended. If this is not possible, an alternative is available.

**Web shell attacks** can allow threat actors to execute commands remotely on a server, causing severe damage to organizations. One thing to remember is that script-based malware eventually channels through points like *cmd.exe*, *powershell.exe*, and *cscript.exe*.

**Prevention is crucial** and Microsoft recommends following a series of guidelines:

- Identify and correct vulnerabilities or misconfigurations in web applications and web servers.
- Implement proper perimeter network segmentation to ensure a compromised web server does not jeopardize the rest.
- Enable antivirus protection on web servers and activate cloud-based protection to obtain the latest defenses against new threats.
- Users should only be able to upload files to directories that can be scanned by antivirus. Additionally, these directories should be configured to prevent the execution of server-side scripts.
- Regularly audit and review web server logs to know which systems are directly exposed to the Internet.
- Use the Windows Defender Firewall, intrusion prevention devices, and network firewalls to prevent command and control server communication between endpoints whenever feasible.
- Verify the perimeter firewall and proxy to restrict unnecessary access to services.
- Implement a good account and credential policy, limiting the use of local or domain administrator accounts to the necessary minimum.

### IDS/IPS Systems and Web Application Firewalls

This alternative involves implementing a **file integrity monitoring** scheme for files hosted on application infrastructure. This way, administrators can see any changes in web directories and code pieces.

On the other hand, a **special firewall for web applications** is oriented to HTTP-based applications. It applies rules during **HTTP conversations**. An additional benefit is that these firewalls can also protect against other lethal attacks like Cross-Site Scripting and SQL injections. According to **[OWASP](https://owasp.org/)**, this firewall is oriented toward server protection, similar to how proxies protect hosts (users). Web Application Firewalls are considered a type of **reverse proxy**.

### NSA Resources

This renowned US agency has made a comprehensive repository available on **[Github](https://github.com/nsacyber/Mitigating-Web-Shells#endpoint-detection-and-response-edr-capabilities)**. This repository includes a wide range of methods and tools to help protect your system from web shell malware without significant investments in security solutions.

Microsoft's **PowerShell** is an example. In the shared repository, you will find support for detecting web shells using a "Known Good"

 comparison scheme and detecting suspicious requests in web server logs.

It is essential to be aware of the main vulnerabilities not only of web application servers but also of traditional applications and even data networks. The possibilities for cyberattacks are endless, and the protection shield must be as robust as possible. Fortunately, online resources and highly accessible tools can help administrators prevent many tragedies.

Certainly, it is an excellent way to **block such threats**, including:

- Scripts for comparing known good files with WinDiff, PowerShell, and Linux Diff.
- Detecting anomalous requests in web server logs with Splunk queries for web server logs, PowerShell script for Microsoft IIS logs, and Python script for Apache httpd logs.
- YARA rules to detect common web shells.
- HIPS rules to allow McAfee's host-based security system to block web directories.

