---
title: 'Bandit Level 1 -> 2'
sidebar_position: 3
---

## Prerequisites:

- Intermediate command-line skills.
- Understanding of SSH (Secure Shell) protocol.

## Level Goal

The password for the next level is stored in a file called `-` located in the home directory

### Commands needed to solve challenge

`ls` , `cd` , `cat` , `file` , `du` , `find`


### Helpful Reading Material

- [Google Search for “dashed filename”](https://www.google.com/search?q=dashed+filename)
- [Advanced Bash-scripting Guide - Chapter 3 - Special Characters](http://tldp.org/LDP/abs/html/special-chars.html)

## Walkthrough

The first instinct you would've got is to just do `ls`, to check the files in the current directory, and then trying to use `cat` command to read the contents of the file only to find the cursor just blinking continuosly. This is because the filename is a special character, in this case, a dash (`-`).

### 1. Escaping the Special Character

In order to work with a filename that starts with a dash, you need to use the `./` to specify that it's a file and not an option for the command. Use the following commands:

```bash
cd ~  # Navigate to the home directory
cat ./-
```

This will display the content of the file, which contains the password for the next level.

:::tip

You can also wrap the filename with a double quote `"` to escape any other characters in the filename  
_Example:_ ```./"-"```

:::

### 2. SSH to Level 2

Now that you have the password, use SSH to log into bandit2:

```bash
ssh bandit2@bandit.labs.overthewire.org -p 2220
```

Enter the password when prompted.

## Conclusion

This level teaches you the importance of handling special characters in filenames and demonstrates the use of `./` to specify a file when dealing with special characters. Continue to apply your command-line skills in the upcoming challenges.
