---
title: Basic System Administration
tags:
  - linux
authors:
  - blindma1den
  - lorenagubaira
description: >-
  Master Linux user and group management, network configuration, and system
  resource monitoring. Discover essential commands for efficient system
  administration!
---
## User and Group Management

Linux can be described as a multi-user operating system. There are two types of users: the root or administrator user and other regular users.

The root user can perform all kinds of system administration tasks. Changes or modifications made with this user can cause security issues for the entire system, so it is recommended to use root only when absolutely necessary to perform an administrative task. Once finished, we should switch back to our normal user. Additionally, it is suggested that to access the administrator user, one should first log in through a normal user account; this measure prevents working with root by default.

Other types of users in Linux, normal or non-administrative users, can use system tools normally but cannot perform administrative tasks.

Administrative permissions are required to switch from `normal` to `root` users. This can be done either by providing the root user password and logging in or by setting up a list of users who can have access as administrators. From a security perspective, it is advisable to opt for the latter option, as sharing the root user's password with multiple people involves transferring sensitive information and puts the system in a vulnerable situation.

Groups in Linux are primarily used to grant permissions on files and directories, that is, for user management. The operating system already includes certain predefined groups with specific functions. Each group created in Linux is independent of the others. Moreover, groups in Linux can have passwords. These groups can be primary or secondary for user management in Linux:

- **Primary Group**: It determines which group will own the files created by the user. The primary group is associated with the account by default, to which the user's files and directories are assigned. The group name is usually the same as the username.
- **Secondary Groups**: These are additional groups to which the user belongs.

Some commands we can use for user and group management are:

| Command   | Description                   |
|-----------|-------------------------------|
| `useradd` | Adds a user                   |
| `userdel` | Deletes a user                |
| `passwd`  | Changes a user's password     |
| `groupadd`| Creates a group               |
| `groupdel`| Deletes a group               |
| `whoami`  | Displays the current user     |

## Network Configuration and Connection

One of the advantages of network configuration and connection in Linux is that it can be easily done through the terminal with several commands. Let's see which ones:

- If we want to check how the **TCP/IP network** is configured, we can use the command `ifconfig` or `ip add`

The command response will show the machine's IP (inet), network mask (netmask), and broadcast address.

- If we want to change the IP address, we use the same command `ifconfig`:

```bash
ifconfig eth0 192.168.1.100 netmask 255.255.255.0 broadcast 192.168.1.255
```

> 🛟 `eth0` is the network interface we will configure.

- The `ping` command is very useful for measuring latency and network connectivity. Through this command, data packets are sent to the address specified in the command, waiting for a response from that address. for example:

```bash
ping 127.0.0.1
```

Pinging the IP address with 32 bytes of data:

```bash
Reply from 127.0.0.1: bytes=32 time= <10 ms TTL=128
```

> 💡 TTL= is the packet's time-to-live value, and its optimal value is 128.

**Netstat** is another tool we can use through the command line. It allows us to monitor networks and troubleshoot certain issues that may arise.

When dealing with excessive traffic or malicious software, Netstat gives us a great advantage with incoming and outgoing connections of a computer or server. These connections are established at their corresponding network address, which among other things, indicates the port that has been opened for communication.

The different flags we can get with this command are:

| Command Flag     | Description                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| `Netstat –a`     | Allows us to know all the networks that are active or inactive at any given moment.          |
| `Netstat –e`     | Displays statistics on incoming and outgoing network packets on a network card.              |
| `Netstat –f`     | Shows the full domain name of remote addresses.                                              |
| `Netstat –n`     | Displays port numbers instead of names.                                                      |
| `Netstat –o`     | Shows the ID of each process in each connection.                                             |
| `Netstat –p X`   | Filters connections according to the protocol (TCP, UDP, tcpv6, or tcpv4).                   |
| `Netstat –q`     | Queries listening and non-listening ports.                                                   |
| `Netstat –s`     | Displays grouped statistics by protocol.                                                     |
| `Netstat –r`     | Shows the routing table of the current network.                                              |
| `Netstat –t`     | Provides information about connections in download state.                                    |
| `Netstat –x`     | Provides information about all NetworkDirect connections.                                    |

## System Resource Monitoring

Sometimes, our system may have performance issues, and we need to see which application is consuming the most system resources. GNU/Linux has several command-line tools available, all of which offer dynamic information on what is running in the system. They provide a summary of that information and a task list that can be sorted by CPU consumption, RAM consumption, etc.

Among the available tools, we have:

- **Top**

This program provides a dynamic, real-time view of the system's performance. It can show a summary of system information and a list of tasks currently managed by the Linux kernel.

![Top](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/top.png)

- **ps**

This command tracks memory and CPU usage. When the command is executed, the system responds with the name of each process, its process identification number (PID), the amount of CPU time consumed, and the associated terminal or user. The information provided by the system is very useful, offering an initial overview to quickly identify any problems. A great combination is to concatenate the `ps` command with `grep` to examine a specific process.
