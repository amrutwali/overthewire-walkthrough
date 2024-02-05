---
title: 'Bandit Level 4 -> 5'
sidebar_position: 6
---

## Prerequisites:

- Intermediate command-line skills.
- Understanding of SSH (Secure Shell) protocol.

## Level Goal

The password for the next level is stored in the only _human-readable_ file in the `inhere` directory. 

:::tip

If your terminal is messed up, try the `reset` command.

:::

### Commands needed to solve challenge

`ls` , `cd` , `cat` , `file` , `du` , `find`

## Walkthrough

This level challenges you to identify the only human-readable file in the inhere directory.

### 1. Navigating to the Directory

Use the following commands to navigate to the inhere directory:

```bash
cd ~/inhere
ls  # List files in the directory
```

### 2. Identifying the Human-Readable File

You can now use the `file` command to check the file type of all the files in the directory. 

```bash
file ./-file00
```

:::tip[Escape the `-` character]

Here you can notice that there is a `-` character prefixed to each file. So it has to be escaped in the `file` command.

:::

Do this for all the files

#### \[ Optional \]: Write a looping script to do the same

You can write a simple `for-loop` to do the same for all files rather than typing all the commands manually.

```bash title="For loop to read file type"
for i in {0..9}; do
    echo $i | find "./file0${i}";
done
```

### 3. Reading the Content

You can see that all the files are data file and only `/-file07` is an `ASCII text` file. So you have to read it to reveal the password

```bash
cat ./-file07
```

### 4. SSH to Level 5:

With the password obtained, use SSH to log into bandit5:

```bash
ssh bandit5@bandit.labs.overthewire.org -p 2220
```

Enter the password when prompted.

## Conclusion

This level focuses on identifying human-readable files in a directory. Continue honing your skills in using commands like file to inspect file types and cat to read content. Prepare for more challenges ahead!
