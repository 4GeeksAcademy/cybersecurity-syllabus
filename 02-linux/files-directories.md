---
title: "File and Directory Management"
subtitle: "Navigating and Manipulating Files in Linux: Essential Commands and Best Practices for System Administrators."
tags: ["linux", "the-terminal"]
authors: ["blindma1den", "lorenagubaira"]
---

For a system administrator, having knowledge of navigating and manipulating files and directories is a fundamental part of the job. In Linux, all this can be achieved from the command line. Through certain commands and tools, we can navigate the file system, create, copy, move, and delete files and directories.

To begin, it's important to understand the directory structure. The file system is organized hierarchically, with a root directory represented by "/". From there, directories are organized in a tree structure, allowing for easy navigation and location of files.

Among the basic commands are:

| Command | Flags | Function |
| --- | --- | --- |
| pwd |  | Prints the current working directory |
| cd |  | Change the working directory |
| ls |  | List directory contents |
|  | -R | Lists all files within subdirectories |
|  | -a | Shows all hidden files |
|  | -al | Shows detailed information about files and directories |
| head |  | Displays the first 10 lines of a text file |
|  | -n or --lines | Prints a custom number of lines (up to 10) |
| tail |  | Displays the last 10 lines of a text file |
|  | -n or --lines | Displays a custom number of lines |
| cat |  | Concatenates and writes file contents to standard output, can also be used to view file contents |
| cp |  | Copies files or directories and their contents |
|  |   | Specify the file name to copy and the destination directory |
| cp filename.txt /home/username/Documents |  |  |
| mv |  | Moves one or more files or directories and their contents to another directory |
|  |   | Specify the file name to move and the destination directory |
| mv filename.txt /home/username/Documents |  |  |
| rm |  | Deletes a file or directory from the system |
|  | -i | Asks for confirmation before deleting a file |
|  | -f | Forces deletion without confirmation |
|  | -r | Recursively deletes files and directories |
| touch |  | Creates a blank file |
| mkdir |  | Creates a directory |
|   |   |   |

> ⚠️ It's important to be cautious when using file and directory manipulation commands, as actions are irreversible and can permanently affect data. Always ensure you have up-to-date backups and double-check before executing commands that may have unintended consequences.

## Configuring File Permissions and Attributes

Permissions are a set of rules and settings that determine what actions users and groups can perform on a file or directory within the system. These are necessary as they increase system security and provide better access control. Linux is a multi-user operating system, so it's common for multiple registered users to access the system simultaneously. Therefore, as system administrators, part of our duties is to periodically review existing permissions.

Imagine we have an FTP server with different users and groups. If all users had admin permissions, they could read, write, and execute any file within the folders. Thus, it's essential to properly manage permissions for all users and groups to ensure they can only access the files and directories we want them to, regardless of their ability to authenticate in the system.

Among the different accounts we can have within the Linux system are:

- Superuser: `Root`, generally assigned to the system administrator.
- Normal User: `ls`

Previously, we discussed permissions in Linux. Let's review them:

- **Read (r):** This is the first permission we encounter. It allows a user to view the content they want to access.
- **Write (w):** This permission gives the user the ability to modify a file. Similarly, it applies to directories.
- **Execute (x):** This permission allows users to execute various parameters within the system.
- **No Permissions (-):** Indicates that the user has no permissions over the shared resource or content. 

Additionally, we can touch on the permission levels again, which define some parameters regarding the abilities of one or more users over the files.

- **Owner Permissions:** This is the user who creates the file from their computer. Linux assigns this user access to the created information and the ability to make changes to it. This is identified by the parameter `u`.
- **Group Permissions:** When a user belongs to a group within the Linux directory, they are granted the same permissions as the other users in that group. The system identifies this with the parameter `g`.
- **Others' Permissions:** These are users who are not the creators of the file and do not belong to the previously mentioned group. The permissions and access of these users can be set by the owner. The system identifies them with the parameter `o`.

Some techniques we can use when assigning permissions to ensure greater system security include:

- **Implement the Principle of Least Privilege:** This principle is based on granting only the necessary permissions for users or groups to perform their specific tasks. Avoiding unnecessary permissions helps reduce the risk of unauthorized access or unwanted changes to resources.
- **Use ACL (Access Control Lists):** ACLs provide a higher level of control over permissions in Linux by allowing more detailed permissions for specific users and groups. With ACLs, it's possible to grant or deny access permissions individually, increasing complexity.
- **Use User Groups:** Creating user groups and assigning permissions to those groups can simplify permission management and increase complexity. Users can belong to different groups and, depending on the assigned group permissions, have varying access levels to resources.
- **Limit Access to Sensitive Resources:** It's advisable to restrict access to sensitive resources, such as configuration files or critical system directories, to authorized users or groups only. This can be achieved by properly assigning permissions and using tools like SELinux (Security-Enhanced Linux) to enforce additional security policies.
- **Monitor and Audit Changes:** Establish monitoring and auditing mechanisms to track changes in resource permissions. This helps identify potential security breaches or unauthorized changes, allowing for timely corrective actions.

> 💡 To see the permissions a user has on a file, use the `ls -l` command. This will show the various permission types for the directory or file.

![user permissions on a file](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/linux-image36.jpg?raw=true)

In the following image, we see five directories where the group owners are separated by different groups. The user owner has full privileges, the group owner has read and write permissions, and other users only have read permissions.

To change permissions on a file or directory, use the `chmod` command followed by the permissions to be assigned and the file or directory to which the permissions will be applied.

There are two ways to assign permissions:

### Using Letters for System User Roles:

- `u`: user
- `g`: group
- `o`: others
- `a`: all (for applying the same permission to user, group, and others, use "a" to save time).

Then, add or remove permissions:

- `+`: add permissions
- `-`: remove permissions
- `=`: set specific permissions.

Finally, specify the permissions to be assigned:

1. `r`: read: Allows users to read a specific file or directory.
2. `w`: write: Gives the user the ability to modify the file for which permissions have been granted.
3. `x`: execute: Grants the ability to execute a file.

![assigning permissions](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/linux-image37.jpg?raw=true)

According to this image, we have a directory named IT with a file called `script.sh` inside. The group owner has read permissions but no write or execute permissions. We can change this using the `chmod` command and assigning permissions using the octal format of Linux permissions.

![how to view permissions in Linux](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/linux-image38.jpg?raw=true)

- Read (r), Write (w), Execute (x) rwx = 7
- Read (r), Write (w) rw- = 6
- Read (r), Execute (x) r-x = 5
- Read (r) r– = 4
- Write (w), Execute -wx = 3
- Write (w) -w- = 2
- Execute (x) –x = 1

We can perform the same exercise as before, this time changing permissions using the octal method.

![octal permissions](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/linux-image39.jpg?raw=true)

- Another command we'll learn is `mkdir`, which allows us to create a directory.
- `chown` changes the file or directory owner.
- `chgrp` changes the file or directory group owner.

## Searching and Filtering Files

A common task in system administration is searching and filtering files. As the number of files on a server increases, it becomes essential to quickly find the files we need. Several terminal commands can help us perform efficient searches and filters.

### `find` Command

This command is one of the most commonly used to search for files and directories based on various criteria such as file name, size, last modification date, and more.

For example, to find all .txt files within a path, use the following command:

![find command in Linux](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/linux-commando-find-image40.png?raw

=true)

> Other ways to search with the `find` command include:

- By type, whether it's a file (f) or directory (d).
- By file size.
- By user or group owner.

### `grep` Command

A useful tool for filtering files in Linux is the `grep` command. Unlike `find`, `grep` is used to search for content within files rather than searching for files themselves. You can search for specific words or patterns in one or more files using the following command:

![grep command](https://github.com/4GeeksAcademy/cybersecurity-syllabus/blob/main/assets/commando-grep-image41.jpg?raw=true)

In this example, we search for the word "test" within the file `script.sh`, and the result is displayed.

### `locate` Command

This command uses a database to perform quick searches for files throughout the system. It's especially useful when you need to search for files frequently and in large volumes.
