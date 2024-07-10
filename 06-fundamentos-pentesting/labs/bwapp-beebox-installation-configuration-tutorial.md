# Installing bWapp using a Virtual Machine (BeeBox) 

At 4Geeks Academy, we are committed to providing the best learning experience for our students, especially regarding understanding web security. One essential tool in our curriculum is bWAPP (Buggy Web Application), a free and open-source web application that is deliberately vulnerable, designed to help students learn about web security vulnerabilities and how to mitigate them. 

There are two primary ways to install bWAPP:
1. **Manual Installation:** Installing the files directly on your own LAMP (Linux, Apache, MySQL, PHP) or WAMP (Windows, Apache, MySQL, PHP) server.
2. **Virtual Machine Installation:** Running bWAPP using a pre-configured virtual machine (VM) like BeeBox.

At 4Geeks Academy, we have chosen to use the virtual machine approach for several compelling reasons that would can read at the end of this article.

## How to Install bWAPP Using a Virtual Machine

Here are the steps to get bWAPP up and running using BeeBox:

1. **Extract the Compressed File:**
   Download and extract the BeeBox VM file from the [official website](http://www.itsecgames.com/).

2. **Double Click on the VM Configuration File:**
   Locate the `bee-box.vmx` file and double-click it, or import the VM into your VMware software.

3. **Start the VM:**
   Launch the VM. It will log in automatically.

4. **Check the IP Address of the VM:**
   Within the VM, check the IP address assigned to it and make sure the network adapter is properly configured.

   ![network adapter virtualbox](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/network-adapter-beebox.png)

6. **Go to the bWAPP Login Page:**
   Open a web browser on your host machine and navigate to the bWAPP login page using the VM's IP address. For example:
   ```
   http://[IP]/bWAPP/
   http://[IP]/bWAPP/login.php
   ```

7. **Login with Default bWAPP Credentials:**
   Use the default credentials to log in, or create a new user.
   ```
   Default credentials: bee/bug
   ```

8. **You Are Ready to Explore and Exploit bWAPP:**
   Begin exploring and exploiting the vulnerabilities within bWAPP in a safe and controlled environment.

> 🔥 IMPORTANT: Avoid upgrading the Linux operating system, as it will diminish the fun by resolving many of the vulnerabilities!

## Important Installation Notes

* **Linux Credentials:**
  ```
  bee/bug
  root/bug
  ```

* **MySQL Credentials:**
  ```
  root/bug
  ```

* **Modify the Postfix Settings:**
  Adjust the `relayhost` and other settings to match your environment.
  ```
  Configuration file: /etc/postfix/main.cf
  ```

* **Defacing and Hacking:**
  BeeBox offers several ways to deface the bWAPP website. It's even possible to hack BeeBox to gain root access. Have fun!

* **Snapshot Before Hacking:**
  Take a snapshot of the VM before starting your hacking activities. There is also a backup of the bWAPP website available at `/var/www/bWAPP_BAK`.

* **Reinstalling the bWAPP Database:**
  If needed, you can delete the database using phpMyAdmin (http://[IP]/phpmyadmin/). Then, reinstall the bWAPP database by browsing to:
  ```
  http://[IP]/bWAPP/install.php
  ```

## The Benefits of Using a Virtual Machine to Install bWAPP

1. **Ease of Use:**
   Setting up bWAPP manually involves several steps: installing a web server, configuring PHP, setting up a MySQL database, and troubleshooting potential issues. This can be time-consuming and complex, especially for beginners. In contrast, using a VM like BeeBox is straightforward. You simply download the VM, import it into your virtualization software (such as VirtualBox or VMware), and start it up. The environment is pre-configured and ready to use, saving valuable time and effort.

2. **Consistent Environment:**
   With a VM, you get a consistent and stable environment. This eliminates the variability that can occur when setting up bWAPP on different systems with different configurations. Students and instructors can be confident that they are all working in the same environment, which makes it easier to follow along with lessons and troubleshoot any issues that arise.

3. **Isolation and Security:**
   Running bWAPP on your own server can expose your computer to security vulnerabilities. Since bWAPP is intentionally vulnerable, any misconfiguration or oversight can lead to security risks. By using a VM, you isolate bWAPP from your main operating system. This isolation minimizes the risk of compromising your personal files or other applications on your computer. The VM acts as a sandbox, containing any potential security threats within the virtual environment.

4. **Resource Management:**
   Virtual machines are designed to efficiently manage system resources. You can allocate specific amounts of CPU, memory, and storage to the VM, ensuring that your main operating system remains responsive and functional even while running resource-intensive applications like bWAPP.

5. **Portability:**
   VMs are highly portable. You can easily move a VM from one computer to another, share it with classmates or colleagues, or back it up for future use. This portability makes it easy to maintain a consistent development environment across different machines and locations.

#### Conclusion

At 4Geeks Academy, we believe in leveraging the best tools and practices to enhance our educational programs. By using a virtual machine to run bWAPP, we simplify the setup process, ensure a consistent and secure learning environment, and protect our systems from potential vulnerabilities. This approach not only benefits our students but also aligns with our commitment to delivering high-quality education in the field of web security.

Whether you're a student, educator, or professional, we highly recommend using the virtual machine approach for bWAPP installation. It's a decision that brings convenience, security, and peace of mind.
