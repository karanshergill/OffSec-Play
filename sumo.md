```
> rustscan -b 1000 -u 5000 -r 0-65535 -a 192.168.245.87 -- -Pn
```
```
.----. .-. .-. .----..---.  .----. .---.   .--.  .-. .-.
| {}  }| { } |{ {__ {_   _}{ {__  /  ___} / {} \ |  `| |
| .-. \| {_} |.-._} } | |  .-._} }\     }/  /\  \| |\  |
`-' `-'`-----'`----'  `-'  `----'  `---' `-'  `-'`-' `-'
The Modern Day Port Scanner.
________________________________________
: https://discord.gg/GFrQsGy           :
: https://github.com/RustScan/RustScan :
 --------------------------------------
🌍HACK THE PLANET🌍

[~] The config file is expected to be at "/home/superuser/.rustscan.toml"
[~] Automatically increasing ulimit value to 5000.
Open 192.168.245.87:22
Open 192.168.245.87:80
[~] Starting Script(s)
[>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")

Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2023-10-25 14:00 EDT
Initiating Parallel DNS resolution of 1 host. at 14:00
Completed Parallel DNS resolution of 1 host. at 14:00, 0.01s elapsed
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating Connect Scan at 14:00
Scanning 192.168.245.87 [2 ports]
Discovered open port 22/tcp on 192.168.245.87
Discovered open port 80/tcp on 192.168.245.87
Completed Connect Scan at 14:00, 0.16s elapsed (2 total ports)
Nmap scan report for 192.168.245.87
Host is up, received user-set (0.16s latency).
Scanned at 2023-10-25 14:00:08 EDT for 0s

PORT   STATE SERVICE REASON
22/tcp open  ssh     syn-ack
80/tcp open  http    syn-ack

Read data files from: /usr/bin/../share/nmap
Nmap done: 1 IP address (1 host up) scanned in 0.20 seconds
```

```
> rustscan -u 5000 -p 22,80 -a 192.168.245.87 -- -Pn -sCV
```
```
.----. .-. .-. .----..---.  .----. .---.   .--.  .-. .-.
| {}  }| { } |{ {__ {_   _}{ {__  /  ___} / {} \ |  `| |
| .-. \| {_} |.-._} } | |  .-._} }\     }/  /\  \| |\  |
`-' `-'`-----'`----'  `-'  `----'  `---' `-'  `-'`-' `-'
The Modern Day Port Scanner.
________________________________________
: https://discord.gg/GFrQsGy           :
: https://github.com/RustScan/RustScan :
 --------------------------------------
🌍HACK THE PLANET🌍

[~] The config file is expected to be at "/home/superuser/.rustscan.toml"
[~] Automatically increasing ulimit value to 5000.
Open 192.168.245.87:80
Open 192.168.245.87:22
[~] Starting Script(s)
[>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")

Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2023-10-25 14:00 EDT
NSE: Loaded 156 scripts for scanning.
NSE: Script Pre-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 14:00
Completed NSE at 14:00, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 14:00
Completed NSE at 14:00, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 14:00
Completed NSE at 14:00, 0.00s elapsed
Initiating Parallel DNS resolution of 1 host. at 14:00
Completed Parallel DNS resolution of 1 host. at 14:00, 0.01s elapsed
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating Connect Scan at 14:00
Scanning 192.168.245.87 [2 ports]
Discovered open port 22/tcp on 192.168.245.87
Discovered open port 80/tcp on 192.168.245.87
Completed Connect Scan at 14:00, 0.16s elapsed (2 total ports)
Initiating Service scan at 14:00
Scanning 2 services on 192.168.245.87
Completed Service scan at 14:00, 6.36s elapsed (2 services on 1 host)
NSE: Script scanning 192.168.245.87.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 14:00
Completed NSE at 14:01, 4.81s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 14:01
Completed NSE at 14:01, 0.66s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 14:01
Completed NSE at 14:01, 0.00s elapsed
Nmap scan report for 192.168.245.87
Host is up, received user-set (0.16s latency).
Scanned at 2023-10-25 14:00:51 EDT for 12s

PORT   STATE SERVICE REASON  VERSION
22/tcp open  ssh     syn-ack OpenSSH 5.9p1 Debian 5ubuntu1.10 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   1024 06:cb:9e:a3:af:f0:10:48:c4:17:93:4a:2c:45:d9:48 (DSA)
| ssh-dss AAAAB3NzaC1kc3MAAACBAO7z5YzRXLGqibzkX44TJn616aaDE3rvYcPwMiyWE3/J+WrJNkyMIRfqggIho1dxtYOA5xXP+UCk3osMe5XlMlocy3McGlmqhSrMFbQOOFrvm/PMAF649Xq/rDm2M/m+sXgxvQmJyLV36DqwbxxCL1wrICNk4cxfDG1K2yTGVw/rAAAAFQDa/l4YfWS1CNCRhv0XZbwXkGdxfwAAAIEAnMQzPH7CGQKfsHXgyFl3lsOMpj0ddXHG/rWZvFn+8NdAh48do0cN88Bti8C4Asibcp0zbEEga9KgxeR+dQi2lg3nHRzHFTPTnjybfUZqST4fU1VE9oJFCL3Q1cWHPfcvQzXNqbVDwMLSqpRYAbexXET64DgwX4fw8FSV6efKaQQAAACAVGZB5+2BdywfhdFT0HqANuHvcLfjGPQ8XkNTcO+XFSWxNFwTnLOzZE8FVNsTIBdMjXKjbWOwLMkzb4EHhkeyJglqDWvBoVTiDpXbRxctFiGt0Z83EvTJJSEAGYDCMHkux/dcVYe0WNjJYX9GBjXB2yhL/2kZuH0lzoNx9fITQ/U=
|   2048 b7:c5:42:7b:ba:ae:9b:9b:71:90:e7:47:b4:a4:de:5a (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQCwlghTOhfNbdMRHJF0N2ho6RlE8HR+wVE5aoFt/PPu6dveDLV7xt7GLS8Q849r1tAScErRUVryrD6gwQ0DB45hGrw8POQlnUHggTjyNp3+sshrWqRs5Dp93LL3NvhpBXl6YD9bJEC3e2qXY3Vwm+Wc/GE/9SxlB+aHL/ekjgNVWgpMT1y/fCKAWlF4TLKUl7Xc21GGWnQptGyYweSbefo4TPa7neg+YdpZkqMWaoK/eEbG+Ze5ocSEWrmB3jQMDHhgeZDO/gB3iuxSDrOToSZmsNcW6TtgqyVyo1q26VIjVRWZPlm9wyR1YB4M85uXZG2DSYu4TFKDwKhXBCqgnSHx
|   256 fa:81:cd:00:2d:52:66:0b:70:fc:b8:40:fa:db:18:30 (ECDSA)
|_ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBAf1vV7lVrnTZwOIFZj7gvuahGAK2YAv8dBxFD5jV7Ho5nXHPCulaGcA9aYW9z2ih2JL/0+3zfdPfk3JBYVyrM8=
80/tcp open  http    syn-ack Apache httpd 2.2.22 ((Ubuntu))
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
|_http-server-header: Apache/2.2.22 (Ubuntu)
|_http-title: Site doesn't have a title (text/html).
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

NSE: Script Post-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 14:01
Completed NSE at 14:01, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 14:01
Completed NSE at 14:01, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 14:01
Completed NSE at 14:01, 0.00s elapsed
Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 12.32 seconds
```

```
http://192.168.245.87/
```
![image](https://github.com/karanshergill/OffSec-Play-Labs/assets/83878909/c884b60d-0d05-4cac-8313-46732c859054)
