---
title: "Package and Software Management"
subtitle: "Master Package Management in Linux: Install, Update, and Remove Software with Ease. Learn to Configure Repositories and Keep Your System Secure."
tags: ["linux"]
authors: ["blindma1den", "lorenagubaira"]

---

Previously, we talked about using package managers and how they can help us install applications and update software. Remember that in the Linux server environment, package managers are fundamental tools for efficient software management. They simplify the installation, updating, and removal of software packages on a server, which is essential to keeping the system updated and secure.

## Package Manager apt-get

One of the most popular package managers on Linux servers is `apt-get`, used in Debian and Ubuntu-based distributions. With apt-get, system administrators can easily install software using simple commands. For example, to install a package named "package_name," you just need to run the command:

```bash
sudo apt-get install <package_name>
```

The package manager will handle downloading and installing the package and resolving necessary dependencies.

## Package Manager YUM

Another common package manager on Linux servers is yum, used in distributions like Red Hat and CentOS. Like apt-get, yum allows for easy installation, updating, and removal of software packages. To install a package with yum, you can run the command:

```bash
sudo yum install <package_name>
```

Yum will also handle dependencies and ensure successful installation.

## Other Package Managers for Linux

Besides apt-get and yum, there are other popular package managers for Linux servers, such as zypper (used in openSUSE) and dnf (used in Fedora).

Each package manager has its own syntax and specific commands, but they all share the goal of simplifying software management on a Linux server.

Below is a list of other package managers:

- **DPKG**: The base package manager for Debian-based distributions.
- **Apt-get**: An interface that makes the DPKG system more user-friendly and adds functions, found in Debian-based distributions.
- **Aptitude**: Aptitude is an interface for APT for Debian-based distributions. It displays a list of software packages and allows the user to interactively choose which to install or remove.
- **Synaptic**: Synaptic is installed by default in Debian desktop versions. It is a graphical package management tool based on GTK+ and APT.
- **RPM**: The base package manager found in Red Hat-based distributions, such as Red Hat Enterprise Linux, CentOS, and Fedora.
- **Yum**: A front-end for the RPM system, found in Red Hat-based distributions.
- **Pacman**: The package manager for Arch Linux-based distributions.


## Keeping Your Software Updated

Many computer vulnerabilities occur due to outdated software and packages. When a vulnerability in a package is detected, developers fix it and publish a new version of the package. It is important to stay up to date.

One of the key advantages of using package managers on Linux servers is the ability to keep software updated easily. With a simple command, such as `sudo apt-get update` in apt-get or `sudo yum update` in yum, you can check for available updates for the installed packages on the server. Then, you can run `sudo apt-get upgrade` or `sudo yum upgrade` to install the updates. This ensures that the software is up to date and protected against known vulnerabilities.

Additionally, package managers on Linux servers also allow efficient software removal. If you no longer need a package, you can use the corresponding command to uninstall it. For example, `sudo apt-get remove package_name` in apt-get or `sudo yum remove package_name` in yum. This ensures proper system cleanup and prevents the accumulation of unnecessary software.

On our Ubuntu server, we will try our software package manager by updating and installing software.

1. First, we will use the command `sudo apt update` to fetch all the applications available in the system.

![apt-update](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/linux-apt-update-69.jpg?raw=true) 

2. Once the packages are updated, we proceed to install the updates with the command `sudo apt upgrade`.

![apt upgrade](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/manejo-de-paquetes-70.jpg?raw=true)

To install software, we install Samba, which is software that implements the SMB protocol and allows file and printer sharing with any other device on the network.

![apt install samba](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/manejo-de-paquetes-71.jpg?raw=true)

![apt install samba terminal output](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/manejo-de-paquetes-72.jpg?raw=true)

> 🤓 As practice, we leave you to investigate how to configure the Samba service.

### Installing Multiple Packages at Once

We can also concatenate multiple packages to perform a single installation.

```bash
sudo apt install -y <package1> <package2>
```

## Searching and Removing Packages

Searching and removing packages in Linux is a common task for system administrators. Sometimes, finding a specific package or removing one that is no longer needed is necessary. Fortunately, Linux has powerful tools to facilitate these tasks.

To search for packages in Linux, you can use the package manager specific to your distribution. For example, in Debian and Ubuntu-based distributions, you can use the command `apt-cache search search_term` with the apt-get package manager. This will search the available repositories and display a list of packages that match the search term. You can refine the search using regular expressions or more specific keywords.

![apt-cache search mysql](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/manejo-de-paquetes-73.jpg?raw=true)

In distributions like Red Hat and CentOS, which use the yum package manager, you can use the command `yum search search_term` to search for packages. Like apt-get, this will display a list of packages that match the search term in the available repositories.

Besides package managers, you can also use additional tools to search for packages in Linux. For example, you can use the command `dpkg -l | grep search_term` in Debian-based distributions to search for locally installed packages. This will display a list of packages that match the search term.

![dpkg grep mysql](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/manejo-de-paquetes-75.jpg?raw=true)

Once you have found the package you want to remove, you can use the corresponding package manager to remove it. In Debian and Ubuntu-based distributions, you can use the command `sudo apt-get remove package_name` with apt-get. This will remove the package and all its associated files from the system.

In distributions like Red Hat and CentOS, you can use the command `sudo yum remove package_name` with yum to remove a package. Like apt-get, this will remove the package and its associated files.

If you want to completely remove a package, including configuration files, you can use the command `sudo apt-get purge package_name` in Debian and Ubuntu-based distributions, or `sudo yum remove package_name` in distributions like Red Hat and CentOS.

It's important to note that removing a package may also remove other packages that depend on it. The package manager will inform you of the changes before proceeding with the removal.

## Configuring Software Repositories

Knowing how to configure software repositories is another essential skill for system administrators. Remember that repositories are centralized locations where software packages are stored, and configuring them correctly allows easy and secure access to a wide variety of software.

In operating systems like Linux, software repositories are especially important. These repositories contain precompiled software packages ready to be installed on the system. By configuring the appropriate repositories, system administrators can access a wide range of software and keep it updated easily.

Repository configuration varies depending on the Linux distribution you are using. For example, in Debian and Ubuntu-based distributions, repository configuration is done through the `/etc/apt/sources.list` file. This file contains the URLs of the repositories and the components that should be enabled, such as "main," "universe," "restricted," and "multiverse." By editing this file and adding or modifying the repository URLs, you can configure the software repositories you want to use.

![source.list file for configuring packages](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/manejo-de-paquetes-76.jpg?raw=true)

In distributions like Red Hat and CentOS, repository configuration is done through files located in the `/etc/yum.repos.d/` directory. These files contain information about the repositories, such as the base URL, enabled components, and authentication keys. By creating or modifying these files, you can configure the software repositories you want to use on your system.

It's important to note that when configuring software repositories, using reliable and secure sources is essential. Official distribution repositories are generally the most reliable as they are maintained by the developers and undergo rigorous testing. However, there are also third-party repositories that can offer additional software. When using third-party repositories, it is important to research and ensure they are reliable and well-maintained.

Once you have configured the software repositories, you can use the corresponding package managers, such as apt-get or yum, to access the available packages in the repositories. These package managers will handle downloading and installing the software efficiently, automatically resolving necessary dependencies.