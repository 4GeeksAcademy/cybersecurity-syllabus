---
title: "Current Trends in Network Security"  
subtitle: "Network Security Trends 2024: Emerging Threats and Innovative Solutions for a Hybrid and Distributed World"  
tags: ["redes"]  
authors: ["blindma1den", "lorenagubaira"]

---

- **The risk associated with teleworking remains.** The return to the office in 2022 will be slower than initially anticipated. Moreover, much of the telework generated during the health crisis will remain, and hybrid work environments will be consolidated. This will mean that everything related to *remote location cybersecurity* will continue to play a role. Organizations are finalizing and defining their security strategies and policies for these new hybrid environments, so that the security posture is the same across all network environments in the organization, regardless of where they are located.
- **DNS over HTTPS (DoH) as a threat vector.** The increasing use of DoH services is on the rise by organizations, and cybercriminals will seek to exploit this system as an attack vector, as it provides an encrypted channel to the DoH server, and malware developers are aware that it is a means to circumvent security controls. Many service providers and enterprises are implementing DoH as a defensive strategy, to have their own DNS infrastructure and avoid relying on third-party DoH servers, but this can pose a risk.
- **Zero Trust Strategies.** The proliferation of hybrid and distributed work environments and IoT network environments will increase the adoption of *"Zero Trust"* security strategies by 2022. A "Zero Trust" strategy consists of the creation of "white lists" of devices that are granted access to network and IT resources, once they have been inventoried and secured by corporate security policies. This strategy will prevent IoT devices or teleworkers' devices from being used as attack vectors over DNS. Intelligent *DNS security solutions* that allow strict device filtering based on these whitelists will play a fundamental role in these strategies. Any DNS request will only be resolved if it is made against a recognized and authorized domain, all others will be denied.
- **Phishing and data exfiltration.** Phishing will continue to be, along with ransomware, one of the main threats driving up the cost of security breaches for enterprises. Data exfiltration occurs either through network intrusions, loss of corporate devices with sensitive information, or through malware tools.
   
    According to an IDC report, 26% of companies surveyed reported having suffered security breaches with data exfiltration as a result of DNS attacks. By 2024, enterprises will increasingly use *DNS as a first line of defense*, to monitor IP traffic and identify and prevent data theft.
   
- **Ransomware as a Service (RaaS).** Ransomware has grown over the past two years exponentially, and as early as 2023, there has been growth in so-called *Ransomware as a Service (RaaS)*. Both modalities will continue to be prominent in 2024 As in other areas, cybercriminals are also using the new IT service delivery models available in the market. Many criminal organizations lack the skills to create their ransomware and contract this service over the network. The use of highly targeted RaaS attacks is proving lucrative for cybercriminals. These are not mass attacks, but rather use social engineering to craft legitimate-looking attack vectors, such as well-crafted emails. In other cases, threat actors may target specific vulnerabilities of a targeted victim group.

## Challenges and opportunities for network security

Network security is the area of cybersecurity that focuses on protecting computer networks from cyber threats. It has three main objectives: preventing unauthorized access to network resources, detecting and neutralizing ongoing cyberattacks and security breaches, and ensuring that authorized users have secure access to the network resources they need when they need them.

The risk of cyberattack increases as the size and complexity of networks grows. For example, according to IBM's Cost of a 2022 Data Breach report, 83% of organizations surveyed have experienced more than one data breach, i.e., a security breach that resulted in unauthorized access to sensitive or confidential information. These attacks are extremely costly: the average cost of a data breach worldwide is $4.35 million, a figure that more than doubles in the United States ($9.44 million).

Network security protects the integrity of network infrastructure, resources, and traffic to thwart these attacks and minimize their financial and operational impact.

### Types of network security technologies

Network security systems operate at the perimeter and within the network.

At the perimeter, security controls attempt to prevent cyber threats from entering the network. But attackers sometimes manage to infiltrate, which is why network security teams also implement controls around resources within the network, such as laptops and data. Even if attackers do manage to infiltrate the network, they will not have a free hand. This strategy, which involves placing a series of control devices between hackers and potential vulnerabilities, is known as "defense in depth".

Every challenge presents an opportunity for improvement and there is much to work on as 2024 is expected, as every year, to see an increase in cybercriminal activity and greater sophistication in both techniques and tools. Let's point out the fundamental cases to be taken into account on what we should pay attention to most. The establishment of network security systems involves the combination of the following tools:

### Firewall

A firewall is a software or hardware that prevents suspicious traffic from entering or leaving a network while allowing legitimate traffic to pass through. Firewalls can be installed at the edge of a network or used internally to divide larger networks into smaller subnets. This way, if one part is compromised, hackers cannot access the rest of the network.

There are different types of firewalls with different characteristics. Basic firewalls use packet filtering to inspect traffic. More advanced, next-generation systems offer enhanced protection with intrusion prevention, AI and machine learning, application monitoring and control, plus threat intelligence feeds.

### Network Access Control (NAC)

Network access control (NAC) solutions act as gatekeepers, authenticating and authorizing users to determine who is authorized to access the network and what they can do on it. The "authentication" part consists of verifying that a user is who they say they are. The "authorization" part consists of granting authenticated users authorization to access network resources.

NAC solutions are often used to enforce role-based access control (RBAC) policies, which require that users' privileges reflect their roles. For example, junior developers can view and edit code, but not put it into production. Senior developers, on the other hand, are allowed to read, write, and put code into production. The RBAC system helps prevent data breaches by keeping unauthorized users away from resources they have no right to access.

In addition to authenticating users, some NAC solutions can assess risks on users' endpoints. The goal is to prevent unsecured or compromised devices from accessing the network. If a user attempts to access the network on a device equipped with outdated or misconfigured anti-malware software, the system will deny access. Some advanced NAC tools are even capable of automatically resolving endpoint non-compliance issues.

### Intrusion Detection and Prevention Systems (IDPS)

An intrusion detection and prevention system (IDPS), sometimes referred to simply as an intrusion prevention system (IPS), can be deployed directly behind a firewall to scan incoming traffic for security threats. These tools are derived from intrusion detection systems (IDSs), which merely flag suspicious activity for examination. IDPS systems are now able to react automatically to possible breaches, for example by blocking traffic or restoring the connection. They are particularly effective in detecting and blocking brute force, denial of service (DoS), and distributed denial of service (DDoS) attacks.

### Virtual private networks (VPNs)

A virtual private network (VPN) is used to protect a user's identity by encrypting their data and masking their IP address and location. When someone uses a VPN, they no longer connect directly to the Internet, but to a secure server that connects to the Internet on their behalf.

VPNs allow teleworkers to access corporate networks securely, even over unsecured public wifi connections, such as those found in coffee shops and airports. VPNs encrypt user traffic, protecting it from hackers who want to intercept their communications.

Instead of VPNs, some organizations use the Zero Trust Network Access (or ZTNA) model (instead of using a proxy server, ZTNA connects remote users securely using zero trust access control policies). When remote users connect to a network through ZTNA, they do not gain access to the entire network. They only have access to the resources they are authorized to use, and must be controlled each time they access a new resource.

### Application Security

Application security refers to measures taken to protect applications and application programming interfaces (APIs) from attackers. Today, many companies use applications to perform critical business functions or process sensitive data, so cybercriminals often attack applications. And because many enterprise applications are hosted in public clouds, hackers can exploit their vulnerabilities to break into companies' private networks.

Application security measures protect applications from malicious actors. The most common tools are web application firewalls (WAF), runtime application self-protection (RASP), and static and dynamic application security testing (SAST and DAST).

### Email security

IBM Security's X-Force Threat Intelligence Index shows that phishing is the most common initial cyberattack vector. Email security tools can help thwart phishing attacks and other attempts to compromise users' email. Most email services include security tools, such as anti-spam filters and message encryption. Some tools are equipped with sandboxes, isolated environments where security teams can inspect email attachments for malware without exposing the network.

### Associated security technologies

Although the following tools are not strictly network security tools, administrators often use them to protect network areas and assets.

Data loss prevention (DLP) refers to IT security strategies and tools that prevent the theft or accidental leakage of sensitive data. This approach brings together security policies and specialized technologies that track data flows, encrypt sensitive information, and trigger alerts if suspicious activity is detected.

Endpoint security solutions protect all devices that connect to a network (laptops, desktops, servers, mobile devices, IoT devices) from hackers attempting to use them to infiltrate the network. Antivirus software can detect and destroy Trojans, spyware, and other malware on a device before they spread to the rest of the network. Endpoint detection and response (EDR) solutions are more advanced tools that monitor endpoint behavior and automatically react to security threat events. Unified endpoint management (UEM) software enables organizations to monitor, manage, and secure all end-user devices from a single console.

Web security solutions, such as secure web gateways, block malicious Internet traffic and prevent users from connecting to suspicious sites and applications.

Network segmentation is a way of dividing large networks into smaller subnets, either physically or through software. This technique limits the spread of ransomware and other malware by isolating a compromised subnet from the rest of the network. It also has the advantage of keeping legitimate users away from resources they should not have access to.

Cloud security solutions protect data centers, applications, and other cloud assets against cyberattacks. In most cases, these are simply standard network security measures (firewalls, NACs, and VPNs) applied to cloud environments. Many cloud service providers incorporate security controls into their services or offer them as add-ons.

User and entity behavioral analysis (UEBA) uses behavioral analysis and machine learning to detect anomalous user and device activity. UEBA is used to detect insider threats and hackers who have taken over user accounts.

### A zero-trust approach to network security

In the past, corporate networks were centralized, with key endpoints, data, and applications located on company premises. Security systems of that era focused on preventing threats from getting through the network perimeter. Once a user was inside, they were considered trusted and had virtually unlimited access.

However, as organizations digitize and adopt hybrid cloud environments, networks become increasingly decentralized. Network resources can now be found in the cloud (data center), on-premises and remote devices, as well as on mobile and IoT devices.

Perimeter-level security controls are less effective for distributed networks, which is why many IT security teams are turning to zero trust. This type of security places controls around each resource rather than at the perimeter. The trust placed in users is never implicit. Every time someone tries to access a resource, they must be authenticated and authorized, even if they are already on the corporate network. Authenticated users are only granted the least privileged access, and their authorizations are revoked as soon as the task is completed.

Zero trust network security relies on precise access policies, continuous validation, and data collected from as many sources as possible (including most of the tools described above) to ensure that only the right users can access the right resources, for the right reasons, at the right time.

## Security solutions for enterprise networks

While a defense-in-depth approach can protect an enterprise network, it also requires the IT security team to manage several independent controls. Enterprise network security platforms can help streamline management by integrating disparate tools and allowing teams to monitor the entire network from a single console. The most common network security platforms are:

Security information and event management (SIEM) solutions collect information from internal security tools, collate it into a central log and report anomalies. Security orchestration, automation, and response (SOAR) solutions collect and analyze security data, enabling specialist teams to define and execute automated actions in the event of cyber threats. Network detection and response (NDR) tools use AI and machine learning to monitor network traffic and detect suspicious activity.

Extended detection and response (XDR) solutions are an open cybersecurity architecture that integrates security tools and operations for all layers: endpoints, email, applications, networks, cloud workloads, and data. With XDR, security solutions that are not necessarily designed to work together can interoperate seamlessly in threat prevention, detection, investigation, and response. XDR can also automate threat detection, incident classification, and threat search workflows.