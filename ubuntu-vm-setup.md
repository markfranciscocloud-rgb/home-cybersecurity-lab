# Ubuntu VM Setup and User Password Change

## Purpose

This VM is used for Linux command-line practice, networking labs, cybersecurity tools, and documentation for my home cybersecurity lab.

## VM Specs

| Setting | Value |
|---|---|
| OS | Ubuntu |
| RAM | 8192 MB |
| CPU | 4 processors |
| Disk | 25 GB |
| Network | NAT |

## Installation Steps

1. Created a new Ubuntu 64-bit VM in VirtualBox.
2. Assigned memory and CPU resources.
3. Created a virtual hard disk.
4. Attached the Ubuntu ISO.
5. Login Password change through GRUP
7. Installed Ubuntu.
8. Updated the system.
9. Installed basic networking and security tools.

## Commands Used
```bash
Edit Boot Entry: Highlight the desired kernel and press 'e' to edit.
Modify Parameters: Locate the line starting with linux and add rw init=/bin/bash or single at the end of the line.
Boot: Press Ctrl+X or F10 to boot into a root shell.
Reset Password: At the command prompt, type passwd to change the root password, or use passwd username to change a specific user's password.
Reboot: Type exec /sbin/init or reboot the machine to apply changes. 
sudo apt update && sudo apt upgrade -y
sudo apt install -y git curl wget net-tools dnsutils traceroute nmap wireshark
uname -a
ip a
