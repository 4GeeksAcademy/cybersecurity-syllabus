---
title: "Introduction to Linux Server Administration"
subtitle: "Manage servers: Install Linux on a Virtual Machine. Discover concepts, advantages, and more. Start now!"
tags: ["servers"]
authors: ["blindma1den", "lorenagubaira"]

---

Servers generally store and process critical data for organizations. Therefore, understanding how to manage them securely is crucial to protect information and ensure system integrity. In the following module, we will learn everything necessary to know how to administer servers, from installing and configuring them to managing permissions and users and monitoring server activities and performance.

## What is a Server and its Importance in Network Environments

A server is a computing device that provides services, resources, and storage to other devices connected to the network. The server is a fundamental component in network environments as it acts as an intermediary between users and the resources they need to access.

A server's primary purpose is to manage and facilitate access to its resources and services. These resources can include files, applications, databases, email services, web pages, and more.

Among the different types of servers that exist, we can find:

- **File Servers**: Store and share files on a network, allowing users to access and share information in a centralized manner.
- **Web Servers**: Host and serve web pages to users who request them through a browser. These servers are essential for websites to be accessible on the Internet.
- **Email Servers**: Manage the sending, receiving, and storage of emails. They allow users to send and receive messages over a network.
- **Database Servers**: Store and manage large amounts of structured data. These servers allow efficient access and manipulation of the information stored in the databases.

Servers are an important part of the IT department and a company because they can centralize and efficiently manage network resources such as files, applications, databases, email, and more. By using a server, users can access these resources quickly and securely without having to store them locally on their own devices.

Another attribute or benefit we can have thanks to servers is the ability to share resources. For example: in an office network, multiple users can access and share files stored on a central server, facilitating collaboration and information exchange among team members.

Regarding security, when we centralize company resources on a server, we can implement more robust security measures such as firewalls, authentication systems, data encryption, and security software to protect sensitive information and prevent unauthorized access. Centralizing resources can also help simplify network management and maintenance, including tasks such as assigning access permissions and monitoring network performance.

During this module, we will explore all the advantages of working with a server and how to manage its resources to get the most out of its performance.

### **Advantages of Linux as a Server Operating System**

As server administrators, it is normal to wonder which is the best operating system to use. In previous modules, we have talked about GNU/Linux and mentioned that it is an open-source operating system based on Unix. The reality is that GNU/Linux has become a popular option for servers in business and development environments, especially for small and medium-sized companies that rely heavily on the stability of their websites. One of the advantages that Linux offers is greater stability and security, as well as the ability to handle a larger number of processes smoothly.

These are the advantages we can have when using Linux as an operating system on a server:

| Stability and Reliability | One of Linux's best-known characteristics is its stability and reliability. This is especially important in a server environment since availability and uptime are critical elements. |
| --- | --- |
| Security | Linux is known for being a robust operating system in terms of security. Being open-source, thousands of developers worldwide constantly work to identify and fix vulnerabilities. The permission structure and ability to customize security settings also make Linux a secure server option. |
| Flexibility and Customization | Linux offers great flexibility and customization capabilities. These characteristics allow server administrators to choose from various distributions and configure the system according to their specific needs, optimizing performance, and adapting the system to the requirements. |
| Cost | Being an open-source operating system, Linux does not require paying for licenses, which can result in significant savings compared to other commercial operating systems. Additionally, users can access the source code and modify and adapt it according to their needs. |
| Community and Support | Linux has many users and developers who offer support and assistance. We can find a wide range of online resources, forums, and documentation available to solve problems and get help when needed. |

### Basic Concepts for Server Administration

We can define server administration as a set of practices and knowledge necessary to efficiently manage and maintain servers in a network environment.

Some concepts that we need to be clear about when talking about server administration are:

1. **Operating System:** It is the fundamental software that enables the server to function. It is important to have a good understanding of the operating system used on the server, such as Linux, Windows Server, macOS Server, among others. This includes the installation, configuration, and updating of the operating system.
2. **Roles and Services:** Servers can perform different roles and offer various services. Common examples include web servers, email servers, database servers, file servers, among others. It is important to understand the roles and services needed in the network and how to configure them properly on the server.
3. **Security:** Security is a critical aspect of server administration, as it involves implementing security measures such as firewalls, intrusion detection systems, data encryption, and secure password policies. It is also important to keep the operating system and applications updated to protect against known vulnerabilities.
4. **Backups:** Performing regular backups is essential to protect the data stored on the server. This involves establishing an appropriate backup strategy, including the frequency of backups, the storage media used, and regular verification of the integrity of backup data.
5. **Process Monitoring:** It is important to monitor server performance to ensure its proper functioning. This involves monitoring resource usage such as CPU, memory, and storage, as well as network traffic. Monitoring allows identifying potential bottlenecks and taking measures to optimize server performance.
6. **Remote Administration:** Remote administration allows managing the server from any location. This is achieved through remote administration tools such as SSH (Secure Shell) or centralized administration tools. Remote administration facilitates configuration, monitoring, and troubleshooting without the need to be physically present where the server is located.
7. **Cloud Server:** It is a centralized and pooled server resource hosted and distributed over a network and accessible to multiple users as needed. Cloud servers can perform the same functions as a traditional physical server, providing processing power, storage, and applications. For its operation, a management software called hypervisor is installed on physical servers to connect and virtualize them. The combined resources are decoupled and pooled to create virtual servers.

## Linux Distributions

Among the most popular Linux distributions for servers, we have:

- **Ubuntu Server:**

Ubuntu server is one of the most known and used distributions for servers currently on the market, it is a variation of Debian-based operating systems, which means that they can have a similar architecture and the same package management system, although, in a professional environment, Ubuntu Server can have a much easier management and a higher hardware compatibility.

It is relatively easy to install and configure the operating system and has a wealth of documentation and online resources to help you in the process. In addition, it supports a wide range of hardware architectures, giving you flexibility in choosing the right server for your needs.

The main disadvantage that the Ubuntu server can have is that it is an operating system that takes up a lot of space on the machine, and that system customizations are possible only within a limited frame

> 👉 Ubuntu Server is a great option when looking to manage a server within a more manageable framework, especially if you are switching from windows.

- **Red Hat Enterprise Linux (RHEL)**

This operating system is another of the most widely used platforms in server and enterprise environments and is certified on hundreds of clouds, RHEL stands out for its focus on stability, security, and performance.

One of the key features of RHEL for servers is its ability to handle critical, high-performance workloads. It is designed to deliver optimal performance and high availability, making it a reliable choice for enterprise applications and online services, and also offers a wide range of tools and services to facilitate server management and deployment.

The company behind RHEL, Red Hat, offers technical support and professional services, giving businesses the peace of mind of having expert assistance in the event of problems or specific needs. There is also a large community of RHEL users and developers who provide additional online resources and support.

Among the disadvantages of RHEL is that it is not a free system, as it is subscription-based, and it is not solely a command-line-based system, which makes it not ideal for beginners.

Although we mentioned as a disadvantage that RHEL is not a free system, we can also take this as an advantage because, in security, it offers several solutions such as Security-Enhanced Linux (SELinux) and mandatory access controls (MAC), which allow you to prevent intrusions and comply with current regulations. The platform is also certified according to Federal Information Processing Standards (FIPS) 140-2 and is the first Linux container framework support to obtain Common Criteria certification (v7.1).

This operating system is ideal when we want to work in a broad ecosystem of software, hardware, and cloud (AWS, Microsoft Azure, Oracle Cloud Infrastructure).

- **CentOS**

CentOS has been based on Red Hat Enterprise Linux (RHEL) since 2009 but is open source and free. The operating system is compatible with RHEL and stands out for its ease of use. Especially in the field of Linux server distributions, CentOS has always been convincing and was considered an entry-level solution that was valid for many users. However, Red Hat has announced that support for CentOS will end in 2024. The successor CentOS Stream is viewed with suspicion by many developers, as it is very experimental and not fully compatible with RHEL. The new solution functions more as a test environment for the system.

CentOS is and was considered a free entry-level solution that could offer the features of RHEL. The operating system runs very stable and is very secure thanks to strong monitoring and regular patches from the community.

However, CentOS is not a solution for the future, as operating system support will be discontinued shortly. Although many RHEL applications also run on CentOS, this is not always guaranteed because many necessary certifications are missing.

CentOS is only suitable for beginners who want to get to know RHEL without paying for it. For long-term projects, we recommend other Linux distributions.

- **Debian**

Debian is one of the classic and long-lived web server distributions. The system has been around since 1993 and has a huge community around the world. This community not only uses Debian but also maintains the system. Debian is the basis for many other Linux distributions, but it is also constantly being optimized by more than 1000 official developers. The operating system is equally recommended for servers, desktops, and laptops.

In addition to its free availability, Debian's stability and versatility speak for themselves. The operating system is not only reliable, but it is also compatible with numerous hardware architectures and allows users to make numerous individual adjustments.

Beginners may have difficulties with Debian, as installation and configuration can be complex. Upgrades do not occur at fixed intervals and are therefore difficult to plan. Personal package archives are not supported. In addition, the interface is clear, but not very modern.

Debian is a reliable solution for experienced developers who are mainly involved in the software and hardware sector.