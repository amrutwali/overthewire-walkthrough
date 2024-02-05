---
title: 'Bandit Level 2 -> 3'
sidebar_position: 4
---

## Prerequisites:

- Intermediate command-line skills.
- Understanding of SSH (Secure Shell) protocol.

## Level Goal

The password for the next level is stored in a file called `spaces in this filename` located in the home directory

### Commands needed to solve challenge

`ls` , `cd` , `cat` , `file` , `du` , `find`


### Helpful Reading Material

- [Google Search for “spaces in filename”](https://www.google.com/search?q=spaces+in+filename)

## Walkthrough

To solve this challenge, you'll need to deal with a filename that contains spaces. This often requires special handling to ensure commands interpret the spaces correctly.

### 1. Navigating to the File

Use the following commands to navigate to the home directory and list the files:

```bash
cd ~  # Navigate to the home directory
ls   # List files in the home directory
```

Locate the file named _"spaces in this filename."_

### 2. Reading the Content

Now, use cat to read the contents of the file. Ensure to **escape** spaces using the backslash character

```bash
cat spaces\ in\ this\ filename
```

This will display the content of the file, revealing the password for the next level.

### 3. SSH to Level 3:

With the password obtained, use SSH to log into bandit3:

```bash
ssh bandit3@bandit.labs.overthewire.org -p 2220
```

Enter the password when prompted.

## Conclusion

This level challenges you to navigate and interact with a file containing spaces in its name. It emphasizes the importance of correctly handling special characters in filenames. Continue honing your command-line skills for the upcoming challenges.