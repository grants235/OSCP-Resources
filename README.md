# OSCP

## Enumeration Tools

- Nmap
``` 
nmap -sC -sV <ip>
```
- Gobster
``` 
gobuster dir -t 50 -x php,html -f -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt -u <ip>
```
- enum4linux 
```
enum4linux -a <ip>
```
