---
title: "Virtual Machines to practice cybersecurity"
description: "Explore top virtual machines for cybersecurity training, including Metasploitable, DVWA, and OWASP WebGoat. Master skills like SQL injection, XSS, and network security through hands-on labs. Ideal for beginners to advanced learners. Enhance your cybersecurity expertise effectively."
tags: ["cybersecurity", "virtual-machines"]

---

# Virtual Machines and projects to practice cybersecurity

At 4Geeks, we like our students to learn in real-life environments similar to those they will find once they get a job in the field. That is why we like using virtual machines instead of cloud services like HackABox, TryHackMe, etc. We recommend using cloud services once you get familiar with installing and using real-life setups.

On the other hand, using a virtual machine is strongly recommended because you will be hacking a lot. You don't want your personal computer to become vulnerable or hacked; using virtual machines (VMs) is a great way to learn cybersecurity in a controlled and isolated environment. 

We use a mix of [internally developed](https://4geeks.com/docs/start/cybersecurity-virtual-machines) and/or publicly available VMs designed specifically for security training, ranging from beginner to advanced levels. These include pre-configured vulnerable applications and systems, which are ideal for practicing penetration testing, vulnerability analysis, and exploitation.

## 1. Metasploitable 2 and 3

- **Difficulty Level**: Beginner to Intermediate
- **Operating System**: Linux
- **Ideal Practices**: Network security, service exploitation, vulnerability assessment
- **Some example exercises you can do**:
  - Exploit known vulnerabilities in services like FTP, SSH, and HTTP.
  - Practice securing misconfigured services and permissions.
  - Use tools like Nmap and Metasploit to conduct penetration testing.
  - Service Enumeration: Use tools like Nmap to identify open ports and services running on the VM.
  - FTP Exploitation: Exploit vulnerable FTP services to gain unauthorized access or read/write files.
  - Apache Misconfigurations: Identify and exploit common misconfigurations in the Apache server.
  - Samba Shares Exploitation: Gain unauthorized access through misconfigured Samba shares.
  - Database Vulnerability Exploitation: Use SQL injection on vulnerable MySQL services to access or manipulate database contents.

## 2. DVWA (Damn Vulnerable Web Application)

- **Difficulty Level**: Beginner
- **Operating System**: Any LAMP stack (Linux, Apache, MySQL, PHP)
- **Ideal Practices**: Web application security, from SQL injection to XSS and CSRF
- **Some example exercises you can do**:
  - Perform SQL injections to reveal database contents.
  - Implement and test Cross-Site Scripting (XSS) attacks.
  - Secure applications against CSRF vulnerabilities.
  - SQL Injection Practice: Perform SQL injections to retrieve hidden data from the database.
  - Cross-Site Scripting (XSS): Craft and execute XSS payloads to understand client-side scripting vulnerabilities.
  - Command Injection: Exploit command injection vulnerabilities to execute unauthorized commands on the server.
  - File Upload Vulnerabilities: Test and exploit file upload functionalities to understand the risks associated with improper file handling.
  - Brute Force Attacks: Conduct brute force attacks on login forms to understand the importance of rate limiting and strong password policies.

## 3. OWASP WebGoat

- **Difficulty Level**: Beginner to Intermediate
- **Operating System**: Cross-platform (Java-based)
- **Ideal Practices**: Web application vulnerabilities and secure coding practices
- **Some example exercises you can do**:
  - Work through lessons that explain vulnerabilities with hands-on tasks.
  - Mitigate vulnerabilities in simulated scenarios.
  - Develop secure code patches for identified issues.
  - Authentication Flaws: Learn about flaws in authentication mechanisms and how to exploit them.
  - Access Control Flaws: Understand broken access controls and practice bypassing access controls.
  - Secure Code Review: Perform code reviews to identify security flaws in source code.
  - Injection Flaws: Practice exploiting various injection flaws, including SQL, XML, and LDAP injection.
  - Concurrency Flaws: Exploit concurrency to perform tasks like money transfer without proper synchronization.

## 4. OWASP Juice Shop

- **Difficulty Level**: Intermediate
- **Operating System**: Cross-platform (Node.js)
- **Ideal Practices**: Modern web application vulnerabilities, API security, and best security practices
- **Vulnerability Report**: [click to access](https://github.com/APTRS/APTRS/blob/main/Doc/Report/Web%20Application%20Penetration%20Testing%20Report%20of%20Juice%20Shop.pdf).
- **Some example exercises you can do**:
  - Conduct an XSS attack and then implement content security policies to mitigate it.
  - Perform Broken Access Control exercises.
  - Explore insecure deserialization and environmental misconfiguration.
  - Broken Authentication: Identify and exploit authentication issues to gain unauthorized access.
  - Sensitive Data Exposure: Explore various ways sensitive data might be improperly exposed and how to protect it.
  - XSS and CSRF: Experiment with Cross-Site Scripting and Cross-Site Request Forgery to understand these common web vulnerabilities.
  - Insecure Deserialization: Learn about and exploit insecure deserialization vulnerabilities.
  - API Security: Test and secure APIs from common vulnerabilities like improper asset management and lack of resource and rate limiting.

## 5. VulnHub VMs

- **Difficulty Level**: Beginner to Advanced (varies by VM)
- **Operating System**: Various
- **Ideal Practices**: Broad range of security practices, from beginner-friendly scenarios to complex setups
- **Some example exercises you can do**:
  - Each VM typically comes with a specific set of challenges, designed to practice a particular set of skills.
  - Tasks often involve discovering and exploiting vulnerabilities to gain higher access levels.
  - Vulnerability Scanning: Use tools like Nessus or OpenVAS to scan and identify vulnerabilities.
  - Penetration Testing: Perform structured penetration tests to exploit discovered vulnerabilities.
  - Reverse Engineering: Analyze binaries for hidden functionalities or vulnerabilities.
  - Exploit Development: Develop exploits for identified vulnerabilities.
  - Post-Exploitation: Understand the steps after gaining access, including maintaining access and clearing tracks.

## 6. Hack The Box

- **Difficulty Level**: Intermediate to Advanced
- **Operating System**: Various
- **Ideal Practices**: Real-world penetration testing, reverse engineering, and cryptoanalysis
- **Some example exercises you can do**:
  - Complete different boxes starting from enumeration to gaining root access.
  - Use various penetration testing tools in a controlled environment.
  - Reverse engineer applications to understand security flaws.

## Other computers provided through online platforms

The following free and paid services are specialized on providing several computers and VM's to practice:

### 7. Offensive Security’s Proving Grounds

- **Difficulty Level**: Intermediate to Advanced
- **Operating System**: Various
- **Ideal Practices**: Penetration testing in a safe, legal, and controlled environment
- **Some example exercises you can do**:
  - Follow structured paths for learning penetration testing.
  - Practice exploits on a variety of operating systems and software configurations.

### 8. PentesterLab

- **Difficulty Level**: Beginner to Intermediate
- **Operating System**: Various
- **Ideal Practices**: Specific web vulnerabilities and exploits, secure coding
- **Some example exercises you can do**:
  - Complete exercises that teach session hijacking, web attacks, and the use of security headers.
  - Analyze source code to find vulnerabilities.

### 9. TryHackMe

- **Difficulty Level**: Beginner to Intermediate
- **Operating System**: Various
- **Ideal Practices**: Network security, scripting for security, system exploitation
- **Some example exercises you can do**:
  - Engage in Capture The Flag (CTF) events.
  - Follow guided paths to learn about different aspects of cybersecurity.

### 10. SANS SIFT

- **Difficulty Level**: Intermediate to Advanced
- **Operating System**: Ubuntu Linux
- **Ideal Practices**: Digital forensics, incident response, and cybersecurity investigation
- **Some example exercises you can do**:
  - Perform forensic analysis of network captures.
  - Analyze disk images for evidence of intrusions.

This categorization should help in selecting the right environment for students' learning stages, from foundational practices in cybersecurity to more complex and specialized areas.
