---
title: 'Bandit Level 0'
sidebar_position: 1
---

:::caution[Warning]

This walkthrough is intended for educational purposes only. Ensure that you have the right to access and interact with the provided system. Unauthorized access to computer systems is illegal.

:::

## Prerequisites:

- Basic knowledge of using the command line.
- Understanding of SSH (Secure Shell) protocol.

## Level Goal

The goal of this level is for you to log into the game using SSH. The _host_ to which you need to connect is `bandit.labs.overthewire.org`, on port `2220`.
The _username_ is `bandit0` and the _password_ is `bandit0`. Once logged in, go to the Level 1 page to find out how to beat Level 1.

### Commands needed to solve challenge

`ssh`

### Helpful reading material

- [Secure Shell (SSH) on Wikipedia](https://en.wikipedia.org/wiki/Secure_Shell)
- [How to use SSH on wikiHow](https://www.wikihow.com/Use-SSH)

## Walkthrough

### 1. SSH into the remote machine

Connect to the specified machine by using the ssh command and passing the required arguments.

```bash title="ssh connection"
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

### 2. Enter Password:

When prompted, enter the password for `bandit0`, which is also `bandit0`

:::caution

Note that while typing the password, no characters or asterisks will be displayed on the screen for security reasons.

:::

## Conclusion

This level just teaches you the basics of how to ssh into a remote machine, using the login credentials and port number
