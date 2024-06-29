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
