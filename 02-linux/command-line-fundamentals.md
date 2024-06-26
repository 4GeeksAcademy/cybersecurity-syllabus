---
title: "Command Line Basics"
subtitle: "Discover the basics of the command line: how to navigate, manipulate files and manage permissions in Linux. Learn from scratch in this complete tutorial!"
tags: ["linux", "command-line"]
authors: ["blindma1den", "lorenagubaira"]

---

In IT, using a terminal or command interpreter to communicate with our computer or laptop is common. These commands help us communicate directly with our computer, as we are giving an order that can be interpreted and processed by a computer language, thus having a significant level of interaction with the PC. In other words, commands as a form of interaction can rescue us when the system is overloaded.

A terminal is a computing device that allows a user to interact with a computer system, usually to perform tasks such as running programs, logging in and out of the system, or conducting web searches.

For years, the computing terminal has been a key tool for programmers and IT experts. This powerful tool allows us to interact with our computing systems, enabling users to perform various functions such as executing commands, updating system software, or creating and modifying files.

A command interpreter or Shell is a computer program capable of translating orders entered by users through a set of instructions provided by it directly to the core and the set of tools that make up the operating system. Orders are entered following the syntax incorporated by the interpreter within the environment provided by the terminal, using a prompt that waits for commands or instructions to be entered:

```bash
PROMPT>commandname argument/s /path/to/the/file/or/files
```

When entering the order with the 'Enter' key, the interpreter analyzes the sequence of characters entered and, if the syntax of the order is correct, it executes it, using the functions offered by the operating system or the program it represents, whether it be a bank data manager, an FTP session, ssh, etc. The response to the user is displayed on the monitor or in the background. Interaction is interactive, that is, the user and the machine communicate successively.

The command-line interface (CLI) is a type of computer user interface that allows users to give instructions to some computer program or the operating system through a simple line of text.

CLIs can be used interactively, typing instructions into some kind of text input, or they can be used in a much more automated way, reading orders from a script file.

Some frequently encountered CLI shells are:

- Bash
- Bourne Shell
- Command Prompt (Windows)
- Zsh

## Basic Commands for Navigation and File and Directory Manipulation

These are several basic commands that will help you navigate in the terminal.

Flags are a way to pass options to commands to get a more specific result.

| Command | Flags | Function |
| --- | --- | --- |
| pwd |  | Prints the current working directory |
| cd |  | Change the working directory |
| ls |  | List directory content |
|  | -R | Will list all files within the subdirectories |
|  | -a | Will show all hidden files |
|  | -al | Will show detailed information of files and directories |
| find |  | Will search for files within a specific directory |
|  | -iname | Will search for files by name or extension in the directory |
|  | -type | Will search for files by type -f (file) -d (directory) |
|  | -size | Filters files by their size |
|  | -user, -group | Filters files by file or directory owner |
| head |  | Allows viewing up to the first 10 lines of text from a file |
|  | -n or -lines | Prints a customized number of lines (up to 10) |
| tail |  | Allows viewing the last 10 lines of text from a file |
|  | -n or -lines | Allows viewing a customized number of lines (up to 10) |
| cat |  | Concatenates and writes file content to standard output, can also be used for file content |
| cp |  | Copies files or directories and their content.
Place the name of the file to copy and the destination directory 
cp filename.txt /home/username/Documents |
| mv |  | Moves one or more files or directories and their content to another directory
Place the name of the file to move and the destination directory 
mv filename.txt /home/username/Documents |
| rm |  | Used to delete a file or directory from the system |
|  | -i | System asks for confirmation before deleting a file |
|  | -f | Allows the system to delete without confirmation |
|  | -r | Deletes files and directories recursively |
| touch |  | Creates a blank file |
| grep |  | Allows finding a word within a specific file |
| mkdir |  | Creates a directory |
| chmod |  | Modifies read, write, and execute permissions of a file or directory |
| chown |  | Changes the ownership of a file, directory, or symbolic link to a specific username |
| kill |  | Manually terminate a non-responsive process |
| sudo |  | Execute a command as superuser
A password will be requested to confirm |

## File and Directory Permissions Management

In a Linux distribution, files and directories can be executed depending on their user permissions. We can see the permissions that a directory might have with the command **ls -l**

| drwxr-xr-x 1 user user 1046 Sep 14 16:24 Downloads |
| --- |
| drwxr-xr-x 1 user user 610 Sep 16 19:03 Desktop |
| drwxr-xr-x 1 user user 94 Sep 15 08:59 Documents |
| drwxr-xr-x 1 user user 42 Aug 27 11:38 Images |
| drwxr-xr-x 1 user user 0 Aug 18 19:20 Music |

Let's talk a bit more about this...

The first letter will indicate whether it is a directory or a file, in the case of a directory it will have the letter d, otherwise, it would have a (-).

Permissions can be:

- r - read
- w - write
- x - execute

**Permissions are divided into 3 parts:**

1. The file owner's permissions being the first 3 letters
2. The group member's user permissions being the second 3 letters
3. The other group members' user permissions being the last 3 letters

```bash
rw-r--r-- 1 user group 0 Sep 17 10:53 file
```

This description indicates that it is a file as it has a (-) at the beginning.

For the owner user, there will only be read and write permission, and for the rest of the group and system users, there will only be read permission; they will not be able to write or execute the file.

```bash
drwxr-xr-x 1 user user 24 Sep 15 09:04 network
```

The file is a directory, where the owner user will have write, read, and execute permissions, the group users will have read and execute permissions just like the system users.

Another way to manage user permissions in Linux is by their octets

Each permission has a value:

- r-4
- w-2
- x-1

Adding the permissions gives 7. To make the assignment, we must add the numbers of the permissions we want to grant:

- 7 = rwx
- 6 = rw-
- 5 = r-x
- 4 = r–
- 3 = -wx
- 2 = -w-
- 1 = –x

We can change all the permissions with the command chmod followed by the octets and permissions we want to grant:

**chmod 437 file**

This is summarized as granting read permission to the owner user, reading and executing permissions to the rest of the group users, and read and write permission to the rest of the system users.

```bash
r---wxrwx 1 user group 0 Sep 17 10:53 file
```

## 💡Laboratorio: Comando básico de navegación y manipulación de archivos y directorios

Abrimos nuestro intérprete de comandos y comienza a explorar por los distintos comandos básicos que les dejamos. 

Sientete libre tambien de experimentar con la asignacion de permisos a usuario y archivos 
