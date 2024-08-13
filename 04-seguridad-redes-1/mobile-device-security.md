---
title: "Mobile Device Security"  
subtitle: "Protecting Mobility: Strategies and Threats in Mobile Device Security"  
tags: ["networks"]  
authors: ["blindma1den", "lorenagubaira"]

---

Mobile security refers to the strategies, infrastructure, and software used to protect any mobile device that travels with users, including smartphones, tablets, and notebooks. Mobile device security includes protecting data on the local device, on endpoints connected to the device, and on network equipment. As long as these devices continue to be preferred by users, rather than desktops, they will remain prime targets for hackers.

### Why is mobile security so important?

As more and more users travel and work from home, mobile devices have become increasingly integrated into their daily lives, including corporate employees. Web browsing activity used to be limited to desktop computers, and the only people with laptops were employees who had to travel for work. Now, cell phones, notebooks, and tablets are the most widely used for web browsing and traffic from these devices has become the primary form of browsing, ahead of PCs.

Mobile devices offer a much larger attack surface than desktops, making them a more serious threat to corporate security. A desktop computer doesn't move, so most of the threats it endures come from the outside, but these devices are vulnerable to physical and virtual attacks. Users carry them with them wherever they go, so administrators need to be more concerned about physical attacks (e.g., theft and loss) and virtual threats from external applications and Wi-Fi networks (e.g., man-in-the-middle attacks). Stationary desktops do not move from the corporate network, making it easier for administrators to control security both on the network and at the touchpoints. In the case of mobile devices, users can root them (gain privileged control of the root directory), add any application, or physically lose them.

> 💡 For these reasons and many others, corporations face much higher costs when creating IT security strategies for mobile devices. Even with the additional costs, it is a critical part of cybersecurity, as these devices pose significant threats to data integrity.

The future of computing and communication is in mobile devices, such as laptops, tablets, and smartphones with desktop capabilities. Their size, operating systems, applications, and processing power make them ideal for use from anywhere with an Internet connection. With the expansion of ruggedized devices, the Internet of Things (IoT), and operating systems, such as Chrome OS, Linux, and Windows, any piece of hardware that is enhanced with this software and these capabilities becomes a mobile computing device.

As mobile devices have become more accessible and portable, organizations and users have preferred to buy and use them instead of desktop computers. With ubiquitous wireless Internet access, all varieties of mobile devices are increasingly vulnerable to attacks and data breaches.

Authentication and authorization via mobile devices offer convenience, but increase risk by removing the constraints of a secure enterprise perimeter. For example, a smartphone's capabilities increase with multi-touch screens, gyroscopes, accelerometers, GPS, microphones, multi-megapixel cameras, and ports, allowing more devices to be attached. These new capabilities change the way users are authenticated and authorized locally to the device and applications and services on a network. As a result, the new capabilities are also increasing the number of endpoints that need protection from cybersecurity threats.

Today, cybercriminals can hack cars, security cameras, baby monitors, and implanted healthcare devices. By 2025, there could be more than 75 billion "things" connected to the Internet, such as cameras, thermostats, door locks, smart TVs, health monitors, lighting devices and many other devices.

## Threats and vulnerabilities to mobile device security

### Threats to applications

Administrators can block the installation of apps on a desktop computer, but a user can install anything on a mobile device. External applications introduce several security issues for these devices. Corporations should create security policies that help users understand the dangers of installing unapproved external applications.

Users should not be able to root or create a superuser on their phones, but some users do, effectively rendering system security controls useless. External applications running on rooted devices can reveal data to a hacker if the hacker uses certain attack methods. External applications may also contain malware and keyloggers in their source code. It is possible to install anti-malware programs, but devices that have been rooted leave even these applications susceptible to malware manipulation.

While it is certainly critical to establish and enforce an enterprise-wide security policy, a policy alone is not enough to counter the volume and variety of today's mobile threats. In 2019, [Verizon conducted a study (PDF, 77 KB, external link to ibm.com)](https://www.verizon.com/business/resources/reports/ves-msi-infographic.pdf) with leading mobile security companies, including IBM, Lookout, and Wandera, surveying 670 security professionals. The study revealed that 1 in 3 respondents reported an incident involving a mobile device. Forty-seven percent say remediation was "difficult and costly," and 64 percent say they suffered downtime.

Companies that adopt bring-your-own-device (BYOD) policies also open themselves up to greater security risks. They allow potentially insecure devices to access corporate servers and sensitive databases, exposing them to attack. Cybercriminals and fraudsters can exploit these vulnerabilities and cause damage or harm to the user and the organization. They look for trade secrets, privileged information, and unauthorized access to a secure network to find anything that can be profitable.

### Phishing

Phishing, the top mobile security threat, is a scam attempt to steal users' credentials or sensitive data, such as credit card numbers. Scammers send users emails or SMS (short text messages), commonly known as text messages, designed to appear to come from a legitimate source, using fake hyperlinks.

### Malware and ransomware

Mobile [malware](https://www.ibm.com/mx-es/topics/malware) is undetected software, such as a malicious application or spyware, created to damage, disrupt, or gain illegitimate access to a client, computer, server, or computer network. Ransomware, a form of malware, threatens to destroy or retain a victim's data or files unless a ransom is paid to decrypt the files and restore access.

### Cryptojacking

Cryptojacking, a form of malware, uses an organization's or an individual's computing power without their knowledge to mine cryptocurrencies, decreasing the processing power and efficiency of a device.

### Unsecured Wi-Fi network

Unsecured Wi-Fi hotspots without a virtual private network (VPN) make mobile devices more vulnerable to cyberattacks. Cybercriminals can intercept traffic and steal private information using methods such as man-in-the-middle attacks. Cybercriminals can also trick users into connecting to fraudulent access points, making it easier to extract corporate or personal data.

Mobile work teams, and especially bring-your-own-device (BYOD) teams, can create a threat to the internal network. It is not uncommon for malware to scan the network to open up storage locations or vulnerable resources to insert malicious executables and exploit them. This can happen stealthily on a mobile device that is not adequately protected.

Administrators can force anyone with a BYOD to install anti-malware programs, but this does not guarantee that the software is up to date. If the corporation offers public Wi-Fi networks for customers and employees, this can also be a point of concern. When employees connect to public Wi-Fi networks and transfer their data to locations where other users can read it, this leaves the network vulnerable to man-in-the-middle (MitM) attacks and possible account takeover if the attacker steals credentials.

### Outdated operating systems

Older operating systems often contain vulnerabilities that have been exploited by cybercriminals, and devices with outdated OSs remain vulnerable to attack. Manufacturer updates often include critical security patches to address vulnerabilities that can be actively exploited.

### Excessive app permissions

Mobile apps have the power to compromise data privacy through excessive app permissions. App permissions determine an app's functionality and its access to the user's device and its functions, such as the microphone and camera. Some apps are more dangerous than others. Some can be compromised, and sensitive data can be funneled through untrusted third parties.

### Web-based and endpoint threats

Mobile applications connect to data and internal applications via endpoints or endpoints of contact. These endpoints receive and process data and then return a response to the mobile device. Both endpoints and any web-based application add new threats to organizations. The endpoints used by the application must be properly encrypted with proper authentication controls to stop attackers. Improperly protected endpoints could be targets for a hacker willing to use them to compromise the application and steal data.

As cell phones and notebooks become increasingly popular, some web-based attacks target these users. Attackers use pages that look like official ones to trick users into uploading sensitive data or downloading malicious applications. It is not uncommon for an attacker to tell a user that they must download a specific application to view a video or other media. Users download the application without realizing that it is a malicious app that is used to scan devices for vulnerabilities and to disclose data.

## Security measures for the security of mobile devices

Securing mobile devices requires a unified, multi-layered approach. There are essential components to mobile device security, but each approach can be a little different. To optimize security, you must find the approach that best suits your network.

The basic security requirements remain the same for mobile devices as for non-mobile computers. In general, the requirements are to maintain and protect confidentiality, integrity, identity, and non-repudiation.

However, current trends in mobile security create new challenges and opportunities, requiring a redefinition of security for personal computing devices. For example, capabilities and expectations vary based on the form factor of the device (its shape and size), advances in security technologies, rapidly evolving threat tactics, and device interaction such as touch, audio, and video.

IT organizations and security teams must rethink how to achieve security requirements in light of device capabilities, the mobile threat landscape, and changing user expectations. In other words, these professionals need to secure multiple vulnerabilities within the dynamic and massively growing environment of mobile devices. A secure mobile environment will offer protection in at least six main areas: enterprise mobility management, email security, endpoint protection, VPN, secure gateways, and cloud access broker.

Organizations using mobile digital devices have a variety of options for protecting them against attackers. The components of mobile computing security can be used to define cybersecurity strategies. In addition to the infrastructure added to the corporate strategy, it is also important to create policies for these devices and BYOD that tell users what can and cannot be installed on the device.

The following components help any organization protect against attacks targeting mobile work teams:

- **Penetration scanners:** It is possible to use automated scanning services to find vulnerabilities in endpoints. While this is not the only cybersecurity measure that can be employed on endpoints, it is the first step in identifying authentication and authorization issues that could be used to compromise data.
- **VPN:** A virtual private network, or VPN, is an encrypted connection to the Internet from a device to a network. The encrypted connection helps ensure the secure transmission of sensitive data. It prevents unauthorized persons from eavesdropping on traffic and allows the remote user to work securely. Users connecting to a network from a remote location should always use a VPN. VPN services and always-on VPN alternatives installed on a mobile device encrypt data from the mobile device to the endpoint or from the mobile device to the internal network. Several external services are specifically configured to protect corporate traffic from a mobile device to the internal network.
- **Device monitoring and control:** While administrators cannot remotely control a cell phone or tablet, they can force users to install remote wipe and locate programs. GPS can be used to locate stolen devices, and remote wipe software deletes all critical data if it is stolen.
- **Email security**: Phishing is a major threat to any organization. Email services are often added to a mobile device so that users can access their emails. Any message containing phishing can attack mobile devices with malicious links or attachments. Email filters should block messages containing malicious links and attachments.
- **Endpoint security**: As organizations incorporate mobile and flexible workforces, they must implement networks that allow remote access. Endpoint security solutions protect corporations by monitoring the files and processes of every mobile device accessing the network. By constantly detecting malicious behavior, endpoint security can identify threats early. When they detect malicious behavior, endpoint solutions quickly alert security teams so that threats are eliminated before they can cause any damage. With technologies such as mobile, IoT, and cloud, organizations are connecting new and different endpoints to their response environment. Endpoint security includes anti-virus protection, data loss prevention, endpoint encryption, and endpoint security management.
- **Secure Web Gateway:** Secure Web Gateways provide powerful, end-to-end cloud security. Since 70 percent of attacks are organization-specific, enterprises need cloud security to identify attacks already in use before launch. Cloud security can work at the DNS and IP layers to protect you from phishing, malware, and ransomware early. By integrating cloud security, you can identify an attack at one location and immediately prevent it at other branch offices.
- **Email security**: Email is the most important business communication tool and the primary attack vector for security breaches. Proper email security includes advanced threat protection capabilities that detect, block, and resolve threats faster; prevent data loss; and protect important information in transit with end-to-end encryption. To protect data from email-based cyber threats such as malware, identity theft, and phishing scams, organizations must proactively monitor email traffic. Proper email protection includes anti-virus, anti-spam, image control, and content control services.
- **Cloud Access Security Broker:** A CASB is a policy enforcement point between users and cloud service providers (CSPs). It oversees cloud-related activity and enforces security, compliance, and governance rules around the use of cloud-based resources. Your network must protect where and how employees work, including the cloud. You'll need a cloud access security broker (CASB), a tool that functions as a gateway between on-premises infrastructure and cloud applications (Salesforce, Dropbox, etc.). A CASB identifies malicious cloud applications and protects against security breaches with a cloud data loss prevention (DLP) engine.
- **Enterprise Mobility Management:** Enterprise Mobility Management (EMM) is a collective set of tools and technologies that maintain and manage how mobile and portable devices are used within an organization for routine business operations.