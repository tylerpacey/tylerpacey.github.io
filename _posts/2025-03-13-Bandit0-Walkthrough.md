---
title: Bandit Level 0 -> 1 - Getting Started
date: 2025-03-13 4:32:00  -0500
description: An introduction to Linux basics, covering SSH access, directory navigation, and file reading.
categories: [CTF Write-Ups]
tags: [CTF, OverTheWire, Bandit, Linux Basics]
---

# Challenge Overview

**Category:** Linux Basics, Command Line Navigation

**Difficulty:** Beginner

This is the first level of the bandit wargame on OverTheWire. The challenge is simple: after connecting to the server via SSH, we need to find a README file in our home directory and display its contents. This introduces Linux directory navigation and file reading commands, which are essential for working in terminal environments.

# Walkthrough: 

### Step 1: Connect to the Server

Before we can do anything, we need to connect to the remote system using `SSH`. The credentials for Level 0 are provided by OverTheWire.

    ssh bandit.labs.overthewire.org -p 2220 -l bandit0

When prompted, enter the password: bandit0

### Step 2: List the Files in the Directory

Once connected, we need to check that the files are available in our home directory. The `ls` command lists the contents of a directory:

    ls

This should return:

    readme

### Step 3: Read the Contents of `README`

To view the contents of the `readme` file, we use the `cat` command:

    cat readme

Output:

    Congratulations on your first steps into the bandit game!!
    Please make sure you have read the rules at https://overthewire.org/rules/
    If you are following a course, workshop, walkthrough or other educational activity,
    please inform the instructor about the rules as well and encourage them to
    contribute to the OverTheWire community so we can keep these games free!

    The password you are looking for is: ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If


Copy the password and use it to log into Level 1!

Key Takeaways:

`ls` - Lists files and directories

`cat [filename]` - Displays the contents of a file.

`ssh [domain or IP]` - Used to connect to remote servers

- `-p 2220` - Specifies the port number (default SSH is 22, but bandit uses 2220)

- `-l bandit0` - Specifies the user on the domain as bandit0

<!-- markdownlint-capture -->
<!-- markdownlint-disable -->
> I found this way to be more practical so I could filter through previous ssh commands and easily change the user by changing the number at the end of the command instead of having to change a value in the middle.
{: .prompt-tip }

<!-- markdownlint-restore -->

With this challenge complete we have a basic understanding of Linux navigation and file reading. Let's move on to the next level!
