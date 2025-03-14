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

In Level 1 of OverTheWire Bandit, we encounter a file with an unusual name: a single hyphen (-). The challenge is to read its contents despite the filename conflicting with common command-line syntax. This level introduces key techniques for handling files with non-standard names in Linux.

# Walkthrough: 

### Step 1: Listing the Directory

First, we use the `ls` command to check for files in our home directory:

```bash
ls
```

This returns:

```bash
-
```

We can see there’s a file named `-`, but trying to read it with `cat -` won’t work as expected, because `-` is often interpreted as an argument rather than a filename.

### Step 2: Use command line tricks to execute `cat`

To tell the shell that `-` is a filename rather than an option, we use `./`, which explicitly specifies the current directory:

```bash
cat ./-
```

This successfully displays the contents of the file, revealing the password for the next level: 

```bash
263JGJPfgU6LtdEvgfWU1XP5yac29mFx
```

Key Takeaways:

- Handling Unusual Filenames: Prefixing filenames with ./ ensures they are interpreted correctly.
- Understanding Command Behavior: The hyphen (-) is commonly used as a placeholder for standard input in Unix-like systems, which is why cat - alone doesn’t work.
- Command-Line Flexibility: Learning how to manipulate file paths is crucial for working efficiently in Linux.

With this challenge complete, we should now have a solid understanding of how to handle tricky filenames in the shell. On to the next level!
