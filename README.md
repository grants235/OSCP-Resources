# OSCP

## Enumeration Tools

1. Nmap
``` nmap -sC -sV <ip> ```
1. Gobster
``` gobuster dir -t 50 -x php,html -f -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt -u <ip>
1. enum4linux 
``` enum4linux -a <ip>
