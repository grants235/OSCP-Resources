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

## Privilege Esclation

- Service Exploit
  ```
  service --status-all
  ```
- File permissions
  ```
  /etc/passwd
  /etc/shadow
  /etc/crontab
  /etc/cron.d/*
  ```
- Sudo 
  ```
  sudo -l 
  > then use https://gtfobins.github.io
  ```
- Cron
  ```
  cat /etc/crontab
  > Look for jobs and files that are being ran
  > Also look for the PATH variable to see if there is any realtive directory files and a path directory you can write to
  ```
- SUID 
  ```
  find / -type f -a \( -perm -u+s -o -perm -g+s \) -exec ls -l {} \; 2> /dev/null
  > Look for know exploits, Shared Object Injection, and /usr/bin/systemctl
  ```
- Command History 
  ```
  cat ~/.*history | less
  ```
- Config files
  ```
  ls -la /home/<user>/
  > Look for .ssh and other config-type filese that could contain password or hashes
  ```
- Kernel Exploits
  ```
  uname -a
  ```
