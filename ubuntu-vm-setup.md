<img width="1230" height="681" alt="Screenshot 2026-04-28 151014" src="https://github.com/user-attachments/assets/25557717-f854-44c6-88ab-1c2820c0349d" />
<img width="1920" height="1020" alt="Screenshot 2026-04-28 150838" src="https://github.com/user-attachments/assets/a9ae91d7-eb34-43dc-bae2-4022d50282ef" />
<img width="1230" height="681" alt="Screenshot 2026-04-28 150800" src="https://github.com/user-attachments/assets/df22c5f1-8138-4211-87f9-e836a5793173" />
<img width="1230" height="681" alt="Screenshot 2026-04-28 150658" src="https://github.com/user-attachments/assets/61ecbff7-c7bf-43bb-ae68-e5ff52c17865" />
<img width="1230" height="681" alt="Screenshot 2026-04-28 150559" src="https://github.com/user-attachments/assets/4b6e797d-82d5-4e78-979e-133296364f3b" />
<img width="1230" height="681" alt="Screenshot 2026-04-28 150227" src="https://github.com/user-attachments/assets/470ac69b-dea2-48c9-a62b-b3ec76240e1c" />
<img width="2560" height="1392" alt="Screenshot 2026-04-28 145823" src="https://github.com/user-attachments/assets/20a56d4f-3eec-46e9-bbca-c91be76f343c" />
<img width="2560" height="1392" alt="Screenshot 2026-04-28 145729" src="https://github.com/user-attachments/assets/ffb7fa8d-8891-4438-8fd0-9d7f19843a53" />
<img width="2560" height="1392" alt="Screenshot 2026-04-28 145657" src="https://github.com/user-attachments/assets/726a8fa7-85c0-49f6-a83a-f90a4464208e" />
<img width="2560" height="1392" alt="Screenshot 2026-04-28 145504" src="https://github.com/user-attachments/assets/ecfcfa16-b823-471f-814b-1a4f6de9638a" />
<img width="2560" height="1392" alt="Screenshot 2026-04-28 145104" src="https://github.com/user-attachments/assets/870157b6-0717-49e1-a8d2-93b256cdf822" />
<img width="2560" height="1392" alt="Screenshot 2026-04-28 145048" src="https://github.com/user-attachments/assets/64e71f67-e119-43c4-b14e-10d7cc9b58ef" />
<img width="995" height="1020" alt="Screenshot 2026-04-28 140355" src="https://github.com/user-attachments/assets/2fdd5ba5-453c-4877-974a-589632e0f6d6" />
<img width="577" height="261" alt="Screenshot 2026-04-28 124801" src="https://github.com/user-attachments/assets/3d768dc4-b4d7-4628-b040-ab11c06f8058" />
<img width="618" height="489" alt="Screenshot 2026-04-28 124550" src="https://github.com/user-attachments/assets/7483d1ea-1fb8-4fd0-9253-2e2d8e5e6571" />
<img width="618" height="489" alt="Screenshot 2026-04-28 124544" src="https://github.com/user-attachments/assets/1e615cd6-6496-4e77-a6ee-3dae9e4f2500" />
<img width="2551" height="1280" alt="Screenshot 2026-04-28 124531" src="https://github.com/user-attachments/assets/f78c8f0e-8687-49d9-adae-f7b3463798ce" />
<img width="618" height="489" alt="Screenshot 2026-04-28 124509" src="https://github.com/user-attachments/assets/530e0a14-cd2d-4690-87ad-0fa2d5da2390" />
<img width="618" height="489" alt="Screenshot 2026-04-28 124444" src="https://github.com/user-attachments/assets/95ee2ca7-acb0-4586-96ae-aac71954b7c8" />
<img width="618" height="489" alt="Screenshot 2026-04-28 124433" src="https://github.com/user-attachments/assets/88b64d78-56b0-4af7-8a87-fbf59b721a2b" />
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
