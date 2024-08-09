---
title: "Vulnerabilities and Threats to Data Security"
subtitle: "Protecting Information: Threats, Vulnerabilities, and Security Measures"
tags: ["data security", "cybersecurity"]
authors: ["blindma1den", "lorenagubaira"]

---

It's obvious that cybercriminals are becoming increasingly sophisticated in their quest for valuable personal data. But they also pose a significant threat to data security and organizational data.

Let's look at attacks that can jeopardize availability, integrity, and confidentiality.

There is an extensive list of **types of cyberattacks** because there are thousands of variants. Each presenting unique threats to data security.

## Ransomware

Among the types of cyberattacks, ransomware is an encrypted malware designed to deny access to resources, such as user files, to force the owner of the infected system to pay a ransom to regain access to the encrypted resources.

This type of cyberattack is one of the most common; in addition to data encryption, extortion techniques are also used, as hackers threaten to expose confidential information if the ransom is not paid.

## Malware is a threat to data security

As we saw earlier, ransomware is only a part of this large family of malicious code used in cyberattacks. It can be used for various purposes:

- Information theft
- Content alteration
- Permanent damage to a computer system

### Common types of malware include

- **Botnet malware:** Used for criminal activities and operate through a botnet where infected systems are installed.
- **Cryptominers:** Mining cryptocurrencies from the victim's computer.
- **Banking trojans:** Extract information and credentials from financial institutions or users to steal or transfer resources electronically.
- **Mobile malware:** Installing malicious code through mobile applications.
- **Rootkits:** Installed on devices to give attackers full control.
- **Adware:** Presenting ads to obtain information or install malicious software.

## Phishing

Phishing emails can be difficult to detect and are one of the most common threats to data security. For example, they often address you by name to seem legitimate, but cybercriminals can easily find this information online. Therefore, it's important to stay alert and think before clicking. Phishing is very common and often works. For instance, in August 2020, elite gaming brand Razer suffered a data breach that exposed the personal information of approximately 100,000 customers.

A security consultant discovered that a cloud cluster (a group of linked servers providing data storage, databases, networks, and software over the Internet) was misconfigured, exposing a segment of Razer's infrastructure to the public Internet, leading to a data leak. Razer took more than three weeks to secure the cloud instance from public access, during which cybercriminals had access to customer information that could have been used in social engineering and fraud attacks.

Organizations must adopt a proactive approach to cloud security to ensure sensitive data is protected.

## Denial of Service

![Denial of Service Attack](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/04-seguridad-redes/threats-vulnerabilities-data/threats-vulnerabilities-data-security-image-1.jpg?raw=true)

### Denial of Service (DoS) Attacks

are a type of network attack that is relatively easy to carry out, even by an unskilled attacker. A DoS attack results in some kind of disruption of network service to users, devices, or applications.

- **Overwhelming traffic volume:** This is when a large amount of data is sent to a network, host, or application at a speed they cannot handle. This causes a slowdown in transmission speed or response or a failure in a device or service.
- **Maliciously formatted packets:** A packet is a collection of data flowing between a source computer or application and a recipient over a network, like the Internet. When a maliciously formatted packet is sent, the recipient cannot handle it. For example, if an attacker forwards packets containing errors or incorrectly formatted packets that an application cannot identify, this will cause the receiving device to function very slowly or crash. DoS attacks are considered a significant risk because they can easily disrupt communication and cause substantial time and money losses.
- **Distributed DoS:** A Distributed DoS (DDoS) attack is similar to a DoS attack but comes from multiple coordinated sources. For example:
    - An attacker creates a network (botnet) of infected hosts called zombies, controlled by management systems.
    - The zombie computers continuously scan and infect more hosts, creating more zombies.
    - When ready, the hacker instructs the managing systems to have the zombie botnets carry out a DDoS attack.

## Social Engineering as a threat to data security

Social engineering is the manipulation of people to perform actions or divulge confidential information. Social engineers frequently rely on people's willingness to help, but they also exploit their vulnerabilities. For example, an attacker will call an authorized employee with an urgent problem requiring immediate network access and appeal to the employee's vanity or greed or invoke authority by using name-dropping techniques to gain access.

### How does social engineering work?

![Social Engineering](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/04-seguridad-redes/threats-vulnerabilities-data/threats-vulnerabilities-data-security2.us.png?raw=true)

### Types of Social Engineering

![Types of Social Engineering](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/04-seguridad-redes/threats-vulnerabilities-data/threats-vulnerabilities-data-security3.us.png?raw=true)

Two-level attacks:

![Types of Social Engineering](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/04-seguridad-redes/threats-vulnerabilities-data/threats-vulnerabilities-data-security4.us.png?raw=true)

## How to protect ourselves?

- Raise awareness and educate about security
- Promote the adoption of preventive measures
- Never disclose sensitive information to strangers or in public places
- Implement security policies in the organization
- Conduct physical security controls to reduce the inherent danger to people
- Perform audits and conduct social engineering to detect security gaps of this nature

## Security Measures for Data Security

### Data Security Engineering

**Thinking about data security and building defenses from the start is crucial.** Security engineers aim to protect the network from threats from the beginning until they are reliable and secure. **Security engineers design systems that protect the right things in the right way. If a software engineer's goal is to ensure things happen, the security engineer's goal is to ensure that bad things don't happen** by designing, implementing, and testing complete and secure systems.

Security engineering covers a lot of ground and includes many measures, **from regular security testing and code reviews to creating security architectures and threat models** to keep a network locked down and secure from a holistic standpoint.

### Encryption

If data security engineering protects the network and other physical assets like servers, computers, and databases, **encryption protects the actual data and files stored on them or traveling between them over the Internet.** Encryption strategies are crucial for any company using the cloud and are an excellent way to protect hard drives, data, and files in transit through email, browsers, or on their way to the cloud.

In the event of data interception, encryption makes it difficult for hackers to do anything with them. This is because **encrypted data is unreadable to unauthorized users without the encryption key.** Encryption should not be left for the end and must be carefully integrated into the network and existing workflow to be more successful.

### Intrusion Detection and Breach Response

If suspicious actions occur on the network, like someone or something trying to break in, intrusion detection will be triggered. **Network Intrusion Detection Systems (NIDS) continuously and passively monitor network traffic for behavior that appears illicit or abnormal and flag it for review.** NIDS not only block that traffic but **also gather information about it and alert network administrators.**

Despite all this, threats to data security still result in breaches. That's why **it's important to have a breach response plan.** You must be prepared to act with an effective system. This system can be updated as often as needed, for example, if network components change or new threats arise that need to be addressed. **A solid breach response system will ensure you have the resources ready and that it's easy to follow a set of instructions to seal the breach and everything that comes with it,** whether you need legal assistance, insurance policies, data recovery plans, or notify any partner about the issue.

### Firewall

How to keep unwanted visitors and malicious software out of the network? When connected to the Internet, a good way to ensure that only the right people and files receive our data is through **firewalls: software or hardware designed with a set of rules to block unauthorized users from accessing the network.** They are excellent lines of defense to prevent data interception and block malware trying to enter the network and also prevent important information from leaving, like passwords or confidential data.

### Vulnerability Analysis

Hackers often actively or passively scan networks for holes and vulnerabilities. Data security analysts and **vulnerability assessment professionals are key in identifying possible holes and closing them.** **Security scanning software is used to exploit any vulnerability in a computer, network, or communication infrastructure, prioritizing and addressing each with data security plans that protect, detect, and react.**

### Penetration Testing

Vulnerability analysis (which

 identifies potential threats) can also deliberately investigate a network or system to detect flaws or conduct **penetration testing. It's an excellent way to identify vulnerabilities early and design a plan to fix them.** If there are flaws in operating systems, compliance issues, certain application code, or other similar problems, a network administrator skilled in penetration testing can help locate these issues and apply patches to reduce the likelihood of an attack.

> Penetration testing involves executing manual or automated processes that disrupt servers, applications, networks, and even end-user devices to see if intrusion is possible and where the breach occurred. From this, they can generate a report for auditors as proof of compliance.

A comprehensive penetration test **can save you time and money** by preventing costly attacks in weak areas you were unaware of. System downtime can be another annoying side effect of malicious attacks, so conducting penetration tests regularly is an excellent way to avoid problems before they arise.

### Security Information and Event Management (SIEM)

There is an even more holistic line of defense that can be employed to keep an eye on every touchpoint. It's known as **Security Information and Event Management (SIEM).** SIEM is a comprehensive approach that **monitors and gathers any details about IT security-related activity that may occur anywhere in the network, whether on servers, user devices, or security software like NIDS and firewalls.** SIEM systems then compile and centralize that information to be managed and analyzed in real-time, identifying standout patterns.

These systems can be quite complex to set up and maintain, so it's essential to hire an expert SIEM administrator.

### Cybersecurity: HTTPS, SSL, and TLS

The Internet itself is considered an insecure network, which can be frightening when we realize it is the backbone of many information transactions between organizations. To protect ourselves from unknowingly sharing our private information across the Internet, various standards and protocols exist for how information is transmitted over this network. **Encrypted connections and secure pages with HTTPS protocols can hide and protect data sent and received in browsers. To create secure communication channels, Internet security professionals can implement TCP/IP protocols (with interwoven cryptographic measures) and encryption methods like Secure Sockets Layer (SSL) or Transport Layer Security (TLS).**

Anti-malware and anti-spyware software are also important. They are designed to monitor incoming Internet traffic or malware like spyware, adware, or Trojan viruses.

### Endpoint Threat Detection

Ransomware attacks can be prevented by following good security practices, such as having antivirus software, the latest operating system, and data backups in the cloud and on a local device. However, this is different for organizations with multiple personnel, systems, and facilities susceptible to attacks.

**Actual users, along with the devices they use to access the network (e.g., mobile phones, laptops, or mobile POS systems), are often the weakest link in the security chain. Several levels of protection, such as authorization technology that grants device access to the network, should be implemented.**

### Data Loss Prevention (DLP)

Within endpoint security, another important data security strategy is **Data Loss Prevention (DLP).** Essentially, this encompasses measures taken to ensure that sensitive data is not sent out of the network, either intentionally or accidentally. **DLP software can be implemented to monitor the network and ensure that authorized end users are not copying or sharing private information or data they shouldn't.**

> 💡 **LIMIT ACCESS TO INFORMATION**
> It's important to **protect information by limiting its availability.** Some of the most common actions include **encrypting the information** so that anyone attempting to access **private data** cannot do so without knowing the **decryption key.**
>
> For businesses, to ensure business continuity, access to sensitive company data should be **limited** to employees.

### Secure and Dynamic Passwords

Although it may seem obvious, there are still users, in the era of digital transformation, who use passwords based on basic sequences such as 1234 or ABCD. For a password to be considered secure, it must have **a minimum of 8 characters and contain at least one uppercase letter, numbers, and special characters.**

Another recommendation to consider is that passwords should be **random,** **avoiding personal information.** Additionally, they should be different for each device or account and **changed periodically.**

Although it may seem complicated, there are **tools that generate secure passwords.** One of the most common options for those who can never remember passwords is to create a **file with all the passwords.** This document should be protected by antivirus software.

These passwords should **also be applied to home networks** such as the ADSL router and Wi-Fi.

### Protecting Email

**Email,** along with social networks, has become a **source of sensitive information** that needs to be protected. One must be aware of all the data that can be concentrated in an email, as well as the multiple traps like **phishing** that can extract even **credit card information.**

One of the recommended security measures is to **use spam filters** and **message encryption systems.** These actions will **ensure the protection and privacy of the information stored** in the email. Email attacks are one of the **most recurring threats and frauds in information systems.**

### Performing Backups and Secure Deletions

**Regularly performing backups** is another action that needs to be taken if we want to protect our **database.**

To avoid losing data that interferes with any company's activity, as well as personal photos or content, it is essential to perform backups periodically. However, it is equally important to **restore that information and securely delete information that is no longer useful.**

### Accessing Secure Websites and Making Secure Purchases

Another common mistake among users is accessing websites that do not have the **https protocol in their URL.** If it has the **s at the end,** it means that the website or site **meets security standards.**

In addition to monitoring the URL, it is also important to **check the electronic payment methods offered by the website.** More and more e-commerce sites are including several verification processes within their payment gateway to make the transaction as secure as possible.

### Cloud, Network, and Local Storage

Possibly, this advice may be more linked to business use, although it is also an option for individuals. **The cloud** is a virtual storage space that allows storing all kinds of information. However, since it is on the network, it is vital to be well protected against any **targeted attack.** Another data storage system that can be used is **local storage** through **physical devices,** and **Network Storage**, which stores information on an **internal network** that can be accessed through permissions.

### Hiring Comprehensive Security Services and Keeping Up-to-Date

Although it may seem incredible, there are still users who do not have antivirus software installed on their computers. Whether you are a company or an individual, **you must have comprehensive security software installed** such as **antivirus,** **anti-spyware,** or a **firewall.** This action will protect the information from any possible attack.

Besides having comprehensive security services, it is important that all programs and operating systems installed on the PC are up-to-date. Always try to have the latest version.

### Monitoring Internet Connections and Browsing

Experts advise **activating private modes in browsers and controlling and deleting cookies** to leave no trace of our activity on visited websites.

Another action to take to preserve internet access security is **not connecting to public Wi-Fi networks.** Although it may seem like a very useful service, it is a double-edged sword. All open or shared Wi-Fi lines **can lead to personal identification.** As long as there is no encryption mechanism or virtual private networks (VPNs), avoid using them.

### Protecting Mobile Phones

Over the years, mobile phones have become an extension of ourselves. Their evolution is such that nowadays, you can have your bank account linked, sessions started to shop on e-commerce sites, etc.

Just like with the PC, we must **protect all possible accesses on the mobile phone with patterns or passwords.** Besides bank data, there are also email, personal images and videos, private conversations in instant messaging apps...

In addition to protecting the mobile phone with patterns, **regularly performing backups** to minimize the risk of data loss is also necessary.

### Logging Out and Turning Off the Internet

Finally, other security measures you should take during your online activity are **logging out and turning off the internet if you will not use it anymore.** By disconnecting, you reduce the possibility of suffering a **cyberattack.** You can also use **airplane mode** if you prefer.

In public spaces, be very mindful of the **remember password checkbox** during registration. **Never accept it,** as this option saves the password, and anyone could enter, even without knowing it.

These have been some of the most widespread cybersecurity tips to date, both for companies and individuals. If you find it interesting how to combat **threats and fraud in information systems, the [Master's in Information Security and Technological Risk Management](https://www.euncet.es/es/master-online-ciberseguridad)** is for you. Discover how to become an **expert in computer science** and security!

### Developing an Information Security Policy

Giving importance to company security is crucial. Therefore, it is necessary to designate who will be responsible for managing cybersecurity in small and medium-sized businesses and **develop a Security Policy that determines the risks** that will be accepted. Moreover, it is crucial that all employees or collaborators understand the importance of security. The policy should include:

- Ensuring the integrity of the information, the equipment containing it, and the processes it undergoes.
- Protecting the confidentiality of the information.
- Regulating the availability of the information so that it is always available to the authorized person for use, at any time and under any circumstance.

![Information Security Policies](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/04-seguridad-redes/threats-vulnerabilities-data/threats-vulnerabilities-data-security-image-5.jpg?raw=true)

This involves countless tasks, many of them technical. But others relate to the general administration of the organization, ranging from having the appropriate budget for implementation to overcoming any mental model objections regarding its use.

They must ensure that the information security policy established is the most convenient for the organization within the available resources and not merely a "cosmetic" solution.

In general, the criteria of **ISO 27002** are adopted, which establishes the general principles for the initiation, implementation, maintenance, and continuous improvement of information security management in an organization.

### Monitoring Networks and Services

![Monitoring Networks and Services](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/04-seguridad-redes/threats-vulnerabilities-data/threats-vulnerabilities-data-security-image-6.jpg?raw=true)

It is necessary for the SME's network to be protected from both external and internal attacks. It is advisable to check if the internet provider **includes a firewall that controls network connections** for internet access and that all of them are monitored.

Detecting hardware failures or abnormal activity is easier with **tools that are even free.** It is advisable to use them, and if we are talking about a medium-sized business, it is best to choose other options that include traffic analysis, IP usage, etc. **Detective mechanisms** are developed to detect changes in the system to alert about any intrusion attempt. Tools are used to monitor and notify of changes made, ensuring the integrity of the information stored in the systems.

These systems continuously monitor network components and individuals or intruders trying to enter illegally, describing activities or processes performed by unauthorized individuals or systems on network elements. They operate when the attack has already occurred, generating a log and an alert.

In practice, we find these systems when a company has networked computers and exchanges valuable information. The most widely used today are **IDS security software** that monitors the network and/or connected devices to detect unauthorized access attempts and generate an alert to notify the system administrator, who will determine the type of response or action to take based on the received information.

A **passive IDS** that detects malicious activity will generate alerts or log entries but will not take action. **An active IDS,** (IDPS) can also be configured to take action, such as blocking IP addresses or closing access to restricted resources.

### Controlling Users and Removable Devices

It is important to **control who the users are and where they enter a company's network.** The administrator must control the users and only grant access to the spaces that employees need within the platform. Personal data or information should be separated and monitored.

Removable devices like USB drives, SD cards, etc., can sometimes be a source of malware. Therefore, **it is recommended that they are controlled and provided by the system administrator** and their content is scanned before use.

### Hiring a Professional or Company in IT Security

It is crucial to **invest in hiring to be protected** both from own attacks and from damage that could be done to third parties.
