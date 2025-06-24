---
title: Introduction to Linux
tags:
  - linux
  - operating systems
authors:
  - blindma1den
  - lorenagubaira
description: >-
  Discover the fundamentals of Linux, from security to user management. Learn
  how to protect your system and unlock the power of open-source software!
---
## What is Linux and its Importance in Computing

Contrary to what you might generally hear about Linux, it is actually a kernel, or **kernel**, that can control hardware. A simpler way to explain it is that Linux is a set of drivers necessary to use a device like a computer or laptop. It was created as a kernel similar to a UNIX operating system.

This kernel was developed by Linus Torvalds when, in 1991, he began working with ideas for a free operating system kernel similar to UNIX. Therefore, he used the Minix system as a basis, a UNIX clone, and created a monolithic kernel. With the help of collaborators, he released the first version of Linux, version 0.01.

Today, Linux is a hybrid monolithic kernel with device drivers and kernel extensions that usually run in a privileged space known as ring 0, with unrestricted access to hardware, although some run in user space.

In 1992, the Linux kernel developers began working with the GNU project, developed by Richard Stallman in 1983, thus creating GNU/Linux, a family of Unix-like operating systems composed of free and open-source software, seeking a freely distributable operating system solution frustrated by the licensing used by MINIX.

Among the components we find within the GNU/Linux system are:

- A bootloader, which loads the Linux kernel into the main memory of the computer when it is turned on and after the firmware initialization. We can find it as GNU Grub, LILO, or SYSLINUX.
- An init program, which is the first process launched by the Linux kernel and where all the processes initiated through init are found, such as system services and login requests.
- Software libraries that contain code that can be used by running processes, including a standard C library, which is necessary to run all C programs on a computer system.
- A package management system, with a specific package format. Alternatively, packages can be compiled from binary or source *tar files*.
- User interface programs such as command shells or window managers.

## Differences Between Linux and Other Operating Systems

Linux, unlike Windows, offers true multitasking and is multi-user, featuring a security scheme based on users and permissions for reading, writing, and executing files and directories. This means that each user owns their files, and another user cannot access these files. This ownership prevents the spread of viruses among files of different users.

| Feature | Windows | Linux |
| --- | --- | --- |
| Type of operating system | Commercial (bought and sold) | Open source, freely downloadable and modifiable |
| Stability | Less stable | More stable |
| Graphical interface | High tech but unstable | Variety of interfaces, more complex handling |
| Suitable for beginners | Yes, thanks to intuitive graphical interfaces | More complex, requires familiarity with the command line |
| Security | Frequent security failures and vulnerabilities | Rarely threatened by security failures |
| Updates | Simple and automated | Sometimes can be complex |

### Advantages and Benefits of Using Linux

The fact that it is *free software* means that, along with the system, you can obtain the source code of any part of it and modify it to your liking. This provides several advantages, for example:

- The security of knowing *what* a program does just by looking at the source code, or at least having the assurance that with the code being available,
- The freedom provided by the GPL license allows any programmer to modify and improve any part of the system, resulting in very high-quality software included in GNU/Linux.
- The fact that the system is maintained by a large community of programmers and users around the world provides a rapid response rate to errors in programs as they are discovered, unmatched by any commercial software company.

In addition to the advantages listed above, GNU/Linux is ideal for use in a work environment for two reasons:

- Being free software, there is no cost for licenses, and a copy of the GNU/Linux system can be installed on as many computers as needed.
- There are office work utilities that are compatible with MS-Office suite tools.
