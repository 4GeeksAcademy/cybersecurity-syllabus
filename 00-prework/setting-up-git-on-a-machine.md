---
title: "Configuring Git on a Machine"
subtitle: "Step-by-step guide to setting up and using Git on your local or virtual machine. Learn how to verify the installation, configure your GitHub credentials, and work with repositories."
tags: ["cybersecurity"]
authors: ["rosinni"]

---

# Configuring Git on a Machine

During the various exercises we will be conducting, you will be asked to download some repositories to your host machine or to some of your virtual machines. This will allow us to carry out certain verifications to ensure your learning is successful. Below, we provide a step-by-step guide on how to perform this configuration for the first time on any of your machines.

## 1. Verify the Installation

The first thing we will do is verify that Git is correctly installed:

```bash
git --version
```

If it is not installed, you should download it from the official git page.

## 2. Configure Git
After verifying that Git is installed, you need to configure it with your GitHub user information. This information is used to identify the commits you make. Configure your name and email with the following commands:

```bash
git config --global user.name "usuario de github"
git config --global user.email "email de github"
```

## 3. View All Git Configurations:

```bash
git config --list
```

You have now configured Git!

## Cloning a Repository

When you need to clone a repository to your machine, you should navigate with the command line to the path where you want to save the project and specify the following command:

```bash
git clone https://github.com/git/git.git
```

This will create a copy of a remote repository on your local or virtual machine.

## How to Work with the Repository

To work on the cloned or created repository on your machine, you should use the following commands:

```bash
git add . # Adds all the files that have been created or modified
git commit -m "Add README file" # Confirms the changes
git push origin <branch_name> # Sends the changes to the remote repository on GitHub
```

> 💡 The branch name is usually main or master

These steps should help you set up and use Git on your virtual machine.