---
title: 'Bandit Level 0 -> 1'
sidebar_position: 2
---

## Prerequisites:

- Intermediate command-line skills.
- Understanding of SSH (Secure Shell) protocol.

## Level Goal

The password for the next level is stored in a file called `readme` located in the home directory. Use this _password_ to log into `bandit1` using SSH. Whenever you find a password for a level, use _SSH_ (on port 2220) to log into that level and continue the game.

### Commands needed to solve challenge

`ls` , `cd` , `cat` , `file` , `du` , `find`

## Walkthrough

### 1. Navigate to Home Directory:

Use the cd command to navigate to the home directory:

```bash title="change current directory to /home"
cd ~
```

### 2. Locate Password File:

Use the `ls` command to list the files in the home directory:

```bash
ls
```

This will display a file named `readme`.

### 3. Read contents of the readme file

Use the `cat` command to read the contents of the readme file

``` bash
cat readme
```

This will disply the password for the next level.

### 4. SSH to Level 1:

Now that you have the password, use SSH to log into bandit1:

```bash title="ssh into bandit1"
ssh bandit1@bandit.labs.overthewire.org -p 2220
```

Enter the password when prompted.

## Conclusion

This level just teaches you the basics of how to navigate the storage using the terminal, find files, and read them by demonstrating the use of `cd`, `ls`, `cat` commands.
