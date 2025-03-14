---
title: Bandit Level 1 -> 2 - Non-Standard File Names
date: 2025-03-13 -0500
description: Using basic command-line navigation to work with non-standard file names
categories: [CTF Write-Ups]
tags: [CTF, OverTheWire, Bandit, Linux Basics]
---

# Challenge Overview

**Category:** Linux Basics, Command Line Navigation

**Difficulty:** Beginner

In Level 1 of OverTheWire Bandit, the task is to explore your home directory using basic Linux commands and discover a file with a non-standard name: a single hyphen (-). This level tests your ability to navigate the filesystem and use command-line tricks to access files that might otherwise be misinterpreted by the shell.

# Walkthrough: 

### Step 1: Listing the Directory

Use the ls command to view current files and directories:

```bash
ls
```

Output:

```bash
-
```

### Step 2: Use command line tricks to execute `cat`

Use the `cat` command with a `./` to ensure the the `-` is not interpreted as a command.

```bash
cat ./-
```

Output: 

```bash
263JGJPfgU6LtdEvgfWU1XP5yac29mFx
```

Key Takeaways:

