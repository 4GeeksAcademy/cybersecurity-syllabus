---
title: "Preparing the Virtualization Environment"
subtitle: "Learn how to prepare your virtualization environment in Linux: types, benefits, and step-by-step guide to installing and configuring virtual machines."
tags: ["linux", "virtualization"]
authors: ["blindma1den", "lorenagubaira"]
---

In IT, there is a technological proposition called virtualization, which allows the creation of services with resources that are typically limited to hardware. We can see this technology in this way: imagine having three physical servers, each with specific purposes—a mail server, a web server, and a server running internal legacy applications. Each server uses around 30% of its capacity, meaning only a part of its potential is utilized. However, as the legacy applications are still important for internal operations, they need to be preserved along with the third server hosting them.

Thanks to virtualization, we can divide the mail server into two other servers that can handle independent tasks, thus transferring the legacy applications. The same hardware is used more efficiently.

In virtualization, there is software called a hypervisor that separates physical resources from the virtual environments that need them. These hypervisors can control an operating system or install directly on the hardware. They take the physical resources of the hardware and divide them so that virtual environments can use them. These virtual environments are called virtual machines, and a virtual machine functions like a single data file. Therefore, just like any digital file, it can be moved from one computer to another, opened on any of them, and it will work the same way.

## Types of Virtualization

### Data Virtualization

All data distributed across various locations can be consolidated into a single source. Data virtualization enables companies to treat data as a dynamic supply, providing processing functions that allow data from various sources to be gathered and new data to be easily incorporated according to user needs.

### Server Virtualization

Server virtualization, which involves dividing a server so its elements can be used to perform multiple tasks, allows for executing more specific functions.

### Desktop Virtualization

In this type of virtualization, a central administrator or an automated management tool can deploy simulated desktop environments on hundreds of physical machines simultaneously. Unlike traditional desktop environments that are installed, configured, and updated physically on each machine, desktop virtualization allows administrators to perform multiple configurations, updates, and security checks across all virtual desktops.

By using virtualization, it is possible to interact with any hardware resource more flexibly. Physical servers consume electricity, take up storage space, and need maintenance. Access to these servers is often limited by physical proximity and network design. Virtualization resolves all these limitations by abstracting the functionality of physical hardware into software. It is possible to manage, maintain, and use hardware infrastructure like a web application. This provides several benefits to any organization, such as:

- Efficient use of hardware resources
- Automated IT management
- Faster disaster recovery

## Choosing the Operating System to Virtualize

To prepare a virtualization environment, we need software that allows virtualization and the operating system.

Some software that can enable virtualization includes:

- VMware
- VirtualBox
- Hyper-V (Available on Windows)

In Linux, operating systems can be found as distributions. These are operating systems designed from the Linux kernel that support user programs, repositories, and libraries. Various versions of these operating systems can be found, aimed at different user groups.

### Popular Linux Distributions

- **Ubuntu**

Ubuntu is a Linux distribution based on Debian. It is developed by Canonical and a community of developers. It has three official editions: Desktop, Server, and Core, which can run on both computers and virtual machines.

- **Debian**

The Debian project is a community of developers and users that maintain the GNU OS based on open-source software. Currently, Debian systems use the Linux or FreeBSD kernel. However, they are also working on offering Debian for other kernels.

- **Fedora**

Fedora is a Linux distribution developed by the Fedora Project. It is developed and maintained by the community and serves as the upstream source for the commercial RHEL distribution. Fedora often has more modern software versions, considered "unstable," which are later included in RHEL.

- **Arch Linux**

Arch Linux is a Linux distribution based on five principles: simplicity, modernity, pragmatism, user-centricity, and versatility. Updates follow a rolling release model.

**For users focused on cybersecurity and hacking:**

- **Kali Linux**

Perhaps the most renowned security distribution. Created by Offensive Security and based on Debian, it is a distro that integrates hundreds of tools to make security audits easier. It is used for penetration tests, forensic analysis, and security audits.

- **Parrot Security OS**

Another favorite for many, it serves as a good alternative to Kali. Parrot Security OS, or ParrotSec, is based on Debian and was created by the FrozenBox development team. They chose the MATE desktop environment and LightDM display manager to make it lighter. Like Kali, it includes hundreds of security tools (penetration, forensic, and general audits).

- **BlackArch**

BlackArch, as the name implies, is based on Arch Linux. It has an extensive repository with around 1500 packages corresponding to pentesting, forensic analysis, and general security audit tools. They can be installed individually or in groups by category according to needs.

## Downloading and Installing a Linux Distribution on a Virtual Machine

Once we choose the distribution we will use, we go to the distribution's website to download it. We have two options:

1. **VDI file**, which contains virtual disk images with associated metadata and is the native image format of VirtualBox.
2. **ISO image file**, which represents an identical storage image of optical media, meaning it contains the same data that would be transferred to a CD, DVD, or Blu-ray.

## Installing Virtual Machine Software

After the initial configuration, we start the virtual machine from the top menu by selecting the start option.

![Start Virtual Machine](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/iniciar-maquina-virtual.png)

- **Initial Operating System Configuration**

In the main installation window, we have several options. We select the graphical installation option.

![Operating System Configuration](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/configuracion-del-sistema-operativo.png)

1. Follow all the installation instructions:
   - Select the system language.
   - Select the location to set the time zone.
   - Select the keyboard layout.
   - Select the machine name.

![Kali](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/kali.png)

2. Add the machine domain name.

![Add Domain Name](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/nombre-dominio-kali.png)

3. Create the system username and password.

![User and Password](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/usuario-y-contraseña.png)

![Configure User and Password](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/configurar-usuario-y-contraseña.png)

4. In the disk partition option, since we are using a virtual disk, select the option to use the entire disk.

![Disk Partition](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/particion-de-discos.png)

5. Select the programs you want to install along with the operating system.

![Program Selection](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/seleccion-de-programas.png)

6. Let the program files load during installation.
7. You will be asked if you want to install the GRUB bootloader. Accept this option.

![Install GRUB Bootloader](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/cargador-de-arranque.png)

8. Once the installation is complete, proceed to restart the virtual machine.

![Restart Virtual Machine](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/reiniciar-la-maquina-virtual.png)

## 💡 Lab: Installing and Configuring an Operating System

**For this lab, we will install Kali Linux on a VirtualBox virtual machine.**

1. Open the VirtualBox interface and select the new option.

![VirtualBox](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/virtualbox.png)

2. Fill in the virtual machine information:
   - Name: The name of the virtual machine (generally, the name of the operating system you will use).
   - Folder: The folder where the virtual machine will be stored.
   - ISO Image: The ISO file to install the virtual machine.

![Virtual Machine](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/maquina-virtual.png)

3. Set the amount of memory and processors you want to assign to the virtual machine. In this case, assign two processors and 4 GB of RAM.

![Memory and Processors](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/memoria-y-procesadores.png)

4. Assign the amount of virtual memory you want to allocate to the virtual machine.

![Memory and Processors](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/memoria-y-procesadores.png)

5. Review the summary and ensure everything is set as needed.

![Installation Summary](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/resumen-instalacion.png)