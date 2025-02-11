---
title: Basic User and Group Administration
tags:
  - servers
authors:
  - blindma1den
  - lorenagubaira
description: >-
  Master essential user and group administration on Linux servers! Learn secure
  practices for managing accounts, permissions, and groups effectively. Discover
  more!
---
## Creating and Managing User Accounts

Within the system, the system administrator has the privilege of being the root user, which means they are the only authorized user to create and manage user accounts and groups, and administer all these files. This practice is not recommended because in the event of an error, we can cause severe system failures. Therefore, in the following practices, we will be under a system user and grant superuser privileges with sudo.

As system administrators, knowing how to create and manage user accounts is essential, as users are the people or entities that will interact with the server and require access to specific resources and services. Creating a user account is not difficult in Linux; it also involves creating a password and assigning it to a group and permissions. Here is an example of how to create and manage a user account. We will open the virtual machine of our server and follow these steps:

- To create a user, we will use the `useradd` command followed by the username. Once the command is entered, you will be prompted to enter a password for the user.

![Creating and Managing User Accounts - Create User](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/users-groups-management/administracion-basica-de-usuarios-imagen-1.jpg)

- If we want to change the password, we do it with the `passwd` command followed by the username whose password we want to change.

![Creating and Managing User Accounts - Change Password Command](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/users-groups-management/administracion-basica-de-usuarios-imagen-2.jpg)

- One way to facilitate directory and file permission management is through groups. We can create groups with the **groupadd** command and assign the user to the group with the `usermod` command along with the `a` (to add to a group) and `G` flags for adding to a secondary group. If we want to see the groups to which the user belongs, we use the `groups` command.

![Creating and Managing User Accounts - Create Groups](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/users-groups-management/administracion-basica-de-usuarios-imagen-3.jpg)

![Creating and Managing User Accounts - Usermod Command](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/users-groups-management/administracion-basica-de-usuarios-imagen-4.jpg)

![Creating and Managing User Accounts - User in Group](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/users-groups-management/administracion-basica-de-usuarios-imagen-5.jpg)

- If we want to see the groups that exist in the system, we can find them in the /etc/group directory.

![Creating and Managing User Accounts - Existing Groups](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/users-groups-management/administracion-basica-de-usuarios-imagen-6.jpg)

- When we need to remove a user from the system, we do it with the `userdel` command followed by the username.

![Creating and Managing User Accounts - Userdel Command](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/users-groups-management/administracion-basica-de-usuarios-imagen-7.jpg)

**It is recommended to manage and create users using sudo user privileges and not from the root user since an error from the root user can be fatal for the system.**

> ⚠️ Remember that creating and managing user accounts on Linux servers should be done securely and follow best security practices. This includes using strong passwords, appropriate permission assignment, and implementing security policies.

## Assigning Permissions and Privileges

As system administrators, it is essential to know how to manage and assign permissions and privileges to each system user, as permissions determine what actions users can perform and privileges define the level of access and control over the system.

When managing a server, one of the best practices for protecting information is implementing the principle of least privilege, which involves assigning the minimum necessary access permissions for users to perform activities on the system. To do this, it is essential to understand permissions and how to manage them.

In Linux, permissions include read (r), write (w), and execute (x). These permissions are assigned to three groups of users: the file owner, the group to which the file belongs, and other users. We can see these permissions in directories or files with the `ls -l` command.

![Assigning Permissions and Privileges - ls Command](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/users-groups-management/administracion-basica-de-usuarios-privilegios-imagen-1.jpg "The ls -l command allows us to visualize permissions in directories or files")

In the following image, we can see a file called `text.txt` with its permissions grouped into three groups:

- The first three permissions are for the file owner ("user"). In this case, we have read (r) and write (w) permissions but not execute. rw-
- The second group of permissions is for users in the group ("ITdepartment"), which has the same read and write permissions but not execute. rw-
- The third group of permissions is for other system users, who can only read the file but not write or execute it.

> 💡 It is common to separate all system users into groups so that they can only access the files they need to read, write, or execute according to their level of privilege, thereby protecting confidential information from other organization departments. Once we create a user, it is necessary to give permissions according to the tasks they will perform in the organization.

With the `chmod` command, we can change and grant permissions to users on a file.

- If we want to give permission to a user (u), a group (g), or other system users (o), we use the flag followed by a + and the permission to be assigned.
- In this case, we manage read, write, and execute permissions only for the file owner (u).

![Assigning Permissions and Privileges - Granting Permissions to a User](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/users-groups-management/administracion-basica-de-usuarios-privilegios-imagen-2.jpg "Granting Permissions to a User")

> 💡 We can generate essential permissions with the setuid (suid) execution bit, the setgid (sgid) execution bit, and the sticky bit. The suid bit allows a file to be executed with the privileges of the owner, while the sgid bit allows a file to be executed with the privileges of the group. The sticky bit is primarily used in directories to prevent users from deleting files of other users.

![Assigning Permissions and Privileges - Setuid Execution Bit (suid)](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/users-groups-management/administracion-basica-de-usuarios-privilegios-imagen-3.jpg "Setuid Execution Bit (suid)")

In this case, we generate suid user and group privilege permissions for the `text.txt` file.

Another way to manage permissions is to assign them with the number of permission bits. Considering that each permission has a number of bits, we can calculate them as follows:

```txt
Read r (4)
Write w (2)
Execute x (1)
```

1. If we want to manage permissions by bits, this calculation may be useful:

```txt
Read (r), Write (w), Execute (x) rwx = 7
Read (r), Write (w) rw- = 6
Read (r), Execute (x) r-x = 5
Read (r) r-- = 4
Write (w), Execute -wx = 3
Write (w) -w- = 2
Execute (x) --x = 1
```

2. We will place the number of bits for the permissions we want to grant according to the position of user, group, and others.

![Assigning Permissions and Privileges - Number of Permission Bits for User, Group, and Others](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/users-groups-management/administracion-basica-de-usuarios-privilegios-imagen-4.jpg "Number of Permission Bits for User, Group, and Others")

> 💡 Assigning permissions and privileges in Linux is essential to ensure security and proper control over system resources.

## Configuring Groups and Assigning Users to Groups

Knowing how to configure and assign a user to a specific group is ideal when we want to save time and have a system with many users. A quick way to do this is by assigning users to a group with minimum user permissions according to their role. For example, we can have an IT department group that can execute system task automation scripts, while marketing department users cannot access these scripts.

To do this, we have commands such as `groupadd` to create a group.

For this exercise, we have created a group called marketingdepartment. Once created, we can add the user to the group with the `adduser` command followed by the username and the group to which we want them to belong.

![Configuring Groups and Assigning Users - Groupadd Command to Add Groups](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-s

yllabus/main/assets/users-groups-management/administracion-basica-de-usuarios-grupos-imagen-1.jpg "Groupadd Command to Add Groups")

![Configuring Groups and Assigning Users - Adding User to Marketingdepartment Group](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/users-groups-management/administracion-basica-de-usuarios-grupos-imagen-2.jpg "User1 will become part of the marketingdepartment group")

In this command, we made user1 part of the marketingdepartment group.

If we want to remove a user from the group, we can do it with the `deluser` command followed by the username and the group from which we want to remove them.

![Configuring Groups and Assigning Users - Removing User from Marketingdepartment Group](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/users-groups-management/administracion-basica-de-usuarios-grupos-imagen-3.jpg "Remove user1 from the marketingdepartment group")

One way to see the groups in the system is by accessing the /etc/group directory using the cat command. There, we can see all the groups followed by a group identifier (gid). Generally, when creating groups, the system assigns a gid of 1000 onwards. Gids less than 100 are reserved for system use and its special groups.

![Configuring Groups and Assigning Users - Cat Command to View Groups in the System](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/users-groups-management/administracion-basica-de-usuarios-grupos-imagen-4.jpg "Cat Command to View Groups in the System")

If we want to modify the gid or the group name, we can do it through the `groupmod` command followed by the new gid or name and the previous gid or name.

![Configuring Groups and Assigning Users - Modify gid or Group Name with Groupmod Command](https://raw.githubusercontent.com/4GeeksAcademy/cybersecurity-syllabus/main/assets/users-groups-management/administracion-basica-de-usuarios-grupos-imagen-5.jpg "Modify gid or Group Name with Groupmod Command 'new name or gid' + 'previous gid or name' ")
