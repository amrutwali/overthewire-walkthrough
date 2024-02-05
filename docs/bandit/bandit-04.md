---
title: 'Bandit Level 3 -> 4'
sidebar_position: 5
---

## Prerequisites:

- Intermediate command-line skills.
- Understanding of SSH (Secure Shell) protocol.

## Level Goal

The password for the next level is stored in a _hidden file_ in the `inhere` directory.

### Commands needed to solve challenge

`ls` , `cd` , `cat` , `file` , `du` , `find`

## Walkthrough

This level introduces the concept of hidden files and requires you to explore the inhere directory to find the password.

### 1. Navigating to the Directory

Use the following commands to navigate to the inhere directory:

```bash
cd ~/inhere
ls -a  # List all files, including hidden ones
```

### 2. Identifying the Hidden File

Hidden files start with a dot (.) in Unix-like systems. Look for files with names starting with a dot in the inhere directory. Use ls -a to list them.

```bash
ls -a
```

### 3. Reading the Content

Once you identify the hidden file, use cat to read its content:

```bash
cat .hidden
```

### 4. SSH to Level 4:

With the password obtained, use SSH to log into bandit4:

```bash
ssh bandit4@bandit.labs.overthewire.org -p 2220
```

Enter the password when prompted.

## Conclusion

This level emphasizes the importance of exploring directories for hidden files. Continue to refine your skills in navigating and interacting with files on the command line for the upcoming challenges.