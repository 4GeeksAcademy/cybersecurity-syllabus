---
title: "Installing Linux on a Virtual Machine"  
subtitle: "Linux Installation on a Virtual Machine: Complete Guide to Preparing, Configuring, and Installing on Servers. Learn Step by Step!"  
tags: ["servers"]  
authors: ["blindma1den", "lorenagubaira"]

---

## Preparation of the virtualization environment

Although we have already touched on the subject of virtualization before, we will briefly recall the concept. Virtualization is a technology that allows the creation of multiple virtual environments on a single physical server. These virtual environments, also known as virtual machines, are independent of each other and can run different operating systems and applications.

Preparing an environment for virtualization can consist of different steps, such as:

- **Suitable hardware**: Before you start, make sure you have hardware that is suitable for virtualization. This includes a powerful server with sufficient storage, RAM, and processing power to support the virtual machines you plan to create.
- **Selecting virtualization software**: There are different virtualization software options, such as VMware, VirtualBox, and Hyper-V. It is important to research and select the software that best suits your needs and requirements.
- **Installing the software**: Once you have selected the virtualization software, you will need to install it on the server. We can follow the documentation of the software developer or get documentation online.
- **Network configuration**: This step is essential to enable communication between the virtual machines and the rest of the network. Configure the network interfaces according to your needs, and make sure to assign unique IP addresses to each virtual machine.
- **Creating virtual machines**: Once the virtualization environment is configured, you will be able to create the virtual machines. Define the resources assigned to each virtual machine, such as the amount of RAM, disk space, and number of processor cores.
- **Installing operating systems and applications**: After creating the virtual machines, you will need to install the required operating systems and applications on each of them. This can be done using ISO images or installation disks.
- **Security configuration**: Don't forget to configure appropriate security measures to protect your virtualization environment. This includes configuring firewalls, security updates, and access policies.

Preparing a virtualization environment is a process that requires careful planning and execution. However, the benefits of virtualization can be significant, so it is worth investing the time and resources necessary to prepare a suitable environment.

## Downloading and installing a Linux distribution on servers

Recall that a Linux distribution is an operating system that can use the Linux kernel, and each version can vary in its package management system and libraries.

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

There are different ways to install a Linux distribution for a server. To do a direct installation we must have the ISO image that we downloaded in the previous step, and we convert it into an installation media with a CD or a USB memory to install it directly to the machine that we want to use in our server, the advantage of this method is that we will be taking advantage of 100% of all the resources dedicated to the service or services that we want to use.

Another method of installation that can be quite useful is virtualization, which we have previously mentioned allows you to create virtual versions of computing resources such as servers, networks, storage, and operating systems and so instead of relying on a single physical instance, virtualization allows the creation of multiple virtual instances that run independently in a shared environment, virtualization involves the creation of virtual servers running on an underlying physical server.

For this module, we will install the Ubuntu server in a virtual machine to familiarize ourselves with this environment.

Just like installing a Linux distribution, we can download the operating system through the distribution's support web page, for this module we are going to install the Ubuntu server by going to [https://ubuntu.com/download/server](https://ubuntu.com/download/server) and downloading the LTS (Long Term Support) version. If you want to try another server distribution, you can find out which is the download page for the distribution you want to use.

Once downloaded we open our virtualization software, for this module, we will continue with Virtual Box. If you have not downloaded it, you can do it through [https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads).

![Virtual Box Image](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/instalacion-de-sistema-linux/instalacion-de-sistema-linux-image-1.jpg)

To start the configuration of our server we select the new option and fill in the information about the features we want to put in our virtual machine:

![Virtual Machine installation - step 1](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/instalacion-de-sistema-linux/instalacion-de-sistema-linux-image-2.jpg)

1. We assign 2 GB of RAM and two processors.

![Virtual Machine installation - step 2](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/instalacion-de-sistema-linux/instalacion-de-sistema-linux-image-3.jpg)

2. Select the option to create a virtual hard disk and allocate the amount of memory.

![Virtual Machine installation - step 3](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/instalacion-de-sistema-linux/instalacion-de-sistema-linux-image-4.jpg)

3. We see the summary of how our virtual machine will be configured and we accept.

![Virtual Machine installation - step 4](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/instalacion-de-sistema-linux/instalacion-de-sistema-linux-image-5.jpg)

> 👉 Now we have our virtual machine configured and ready to work, in the next reading we will learn how to configure the Ubuntu server and for the first time see the environment of a server.

## Initial configuration of the operating system

Here is a small guide on how to initially configure the Ubuntu server inside our virtual machine:

- Before starting the installation we have to make a previous configuration of the network so we will enter the configuration section of the menu.

![Virtual Box - Operating System Configuration](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/instalacion-de-sistema-linux/instalacion-de-sistema-linux-image-6.jpg)

- Select the network option and in the *Connected to:* option select the *Bridge adapter* option. This allows our virtual machine to connect to the network card that we have in the host machine, and we select accept.

![Virtual Box - Network Options ](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/instalacion-de-sistema-linux/instalacion-de-sistema-linux-image-7.jpg)

- Once the network has been configured, click on start and a new window will open with the virtual machine.

### Laboratory 1 Scenario:

You have just been hired by the start-up D'sistemas cta to be their system administrator, this company needs to set up some servers to be able to operate and facilitate access to their information, although you do not have much knowledge of how to install an operating system on a server, your boss decides to accompany you and explain at all times the step by step for the installation of our ubuntu server.

1. Once the installation is started we select the first option “Try or install Ubuntu Server”.

![Install Ubuntu server](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/instalacion-de-sistema-linux/instalacion-de-sistema-linux-image-8.jpg)

2. The first thing that we will configure will be the language, so we will select the language in which we want to manage our server.
3. The next window will indicate the keyboard language configuration, so we will also select the language we want to use on our keyboard.
4. In the next window it will give us to select the type of installation that we want to make
   
    ![Install Ubuntu server - language selection](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/instalacion-de-sistema-linux/instalacion-de-sistema-linux-image-9.jpg)
   
5. Ubuntu Server will install a series of packages that will help us in the management of our operating system.
6. Ubuntu server (Minimized) is a more adaptable version for test environments where some kind of user login is expected.
   
    ![Install Ubuntu server - Connect to internet](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/instalacion-de-sistema-linux/instalacion-de-sistema-linux-image-10.jpg)
   
7. Select the first option.
8. The next step is to configure a network adapter. Thanks to the bridge adapter network configuration we did previously, we can select our host machine's network card.
9. Then we must configure a Proxy server in case we have one available, if we don't have one we can skip this step
   
    ![Install Ubuntu server - Configure proxy](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/instalacion-de-sistema-linux/instalacion-de-sistema-linux-image-11.jpg)
   
10. After the configuration of a proxy, we will have to configure the Mirror file, this is the file to which we are going to connect to obtain the repositories of the file package manager, they are going to give us a default option which we are going to accept
   
    ![Install Ubuntu server - Mirror Address](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/instalacion-de-sistema-linux/instalacion-de-sistema-linux-image-12.jpg)
   
11. The next step will be to configure a disk in which we are going to store our operating system, in this case of virtualization, we will have the option of a virtual disk, and then we will have the summary of the partitions of the disk in which we will have two partitions, partition 1 that we will have the grub and partition 2 where we will have our operating system.
   
    ![Install Ubuntu server - Disk configuration](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/instalacion-de-sistema-linux/instalacion-de-sistema-linux-image-13.jpg)
   
12. In the next window, it will ask us to put the names of the machine and the server together with its password.
   
    ![Install Ubuntu server - Connect to the Internet](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/instalacion-de-sistema-linux/instalacion-de-sistema-linux-image-14.jpg)
   
    ![Install Ubuntu server - Server configuration](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/instalacion-de-sistema-linux/instalacion-de-sistema-linux-image-15.jpg)
   
13. The next step will ask us if we want to install the OpenSSH service, remember that SSH is a protocol that will allow us to access our server remotely, so it is advisable to accept.
   
    ![Install Ubuntu server - Install Open SSH Server](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/instalacion-de-sistema-linux/instalacion-de-sistema-linux-image-16.jpg)
   
14. We will select some packages that we want to have in our operating system, these selections are optional so we will not accept any for this practice.
   
    ![Install Ubuntu server - Server Snaps](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/instalacion-de-sistema-linux/instalacion-de-sistema-linux-image-17.jpg)
   
15. After the last step begins the installation of the operating system we will wait a few minutes to finish once the installation is finished, we select the reboot now option.
   
    ![Install Ubuntu server - Installation completed](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/instalacion-de-sistema-linux/instalacion-de-sistema-linux-image-18.jpg)
   
#### Reflect

💭 Once the installation is finished your boss sits down with you and asks you some questions to find out how much you learned in this process.

- Why was the type of installation chosen?
- If you have a proxy for the server, can it be added at the time of installation?
- What is the benefit of installing OpenSSH?
