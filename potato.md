```shell
> rustscan -b 1000 -u 5000 -r 0-65535 -a 192.168.224.101 -- -Pn
```
```shell
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
Open 192.168.224.101:22
Open 192.168.224.101:80
Open 192.168.224.101:2112
[~] Starting Script(s)
[>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")

Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2023-10-18 02:28 EDT
Initiating Parallel DNS resolution of 1 host. at 02:28
Completed Parallel DNS resolution of 1 host. at 02:28, 0.01s elapsed
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating Connect Scan at 02:28
Scanning 192.168.224.101 [3 ports]
Discovered open port 80/tcp on 192.168.224.101
Discovered open port 22/tcp on 192.168.224.101
Discovered open port 2112/tcp on 192.168.224.101
Completed Connect Scan at 02:28, 0.26s elapsed (3 total ports)
Nmap scan report for 192.168.224.101
Host is up, received user-set (0.26s latency).
Scanned at 2023-10-18 02:28:29 EDT for 0s

PORT     STATE SERVICE REASON
22/tcp   open  ssh     syn-ack
80/tcp   open  http    syn-ack
2112/tcp open  kip     syn-ack

Read data files from: /usr/bin/../share/nmap
Nmap done: 1 IP address (1 host up) scanned in 0.33 seconds
```
```shell
> rustscan -u 5000 -p 22,80,2112 -a 192.168.224.101 -- -Pn -sCV
```
```shell
.----. .-. .-. .----..---.  .----. .---.   .--.  .-. .-.
| {}  }| { } |{ {__ {_   _}{ {__  /  ___} / {} \ |  `| |
| .-. \| {_} |.-._} } | |  .-._} }\     }/  /\  \| |\  |
`-' `-'`-----'`----'  `-'  `----'  `---' `-'  `-'`-' `-'
The Modern Day Port Scanner.
________________________________________
: https://discord.gg/GFrQsGy           :
: https://github.com/RustScan/RustScan :
 --------------------------------------
Real hackers hack time ⌛

[~] The config file is expected to be at "/home/superuser/.rustscan.toml"
[~] Automatically increasing ulimit value to 5000.
Open 192.168.224.101:22
Open 192.168.224.101:80
Open 192.168.224.101:2112
[~] Starting Script(s)
[>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")

Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2023-10-18 02:30 EDT
NSE: Loaded 156 scripts for scanning.
NSE: Script Pre-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 02:30
Completed NSE at 02:30, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 02:30
Completed NSE at 02:30, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 02:30
Completed NSE at 02:30, 0.00s elapsed
Initiating Parallel DNS resolution of 1 host. at 02:30
Completed Parallel DNS resolution of 1 host. at 02:30, 0.01s elapsed
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating Connect Scan at 02:30
Scanning 192.168.224.101 [3 ports]
Discovered open port 22/tcp on 192.168.224.101
Discovered open port 80/tcp on 192.168.224.101
Discovered open port 2112/tcp on 192.168.224.101
Completed Connect Scan at 02:30, 0.16s elapsed (3 total ports)
Initiating Service scan at 02:30
Scanning 3 services on 192.168.224.101
Completed Service scan at 02:30, 11.52s elapsed (3 services on 1 host)
NSE: Script scanning 192.168.224.101.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 02:30
NSE: [ftp-bounce 192.168.224.101:2112] PORT response: 500 Illegal PORT command
Completed NSE at 02:30, 5.50s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 02:30
Completed NSE at 02:30, 1.14s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 02:30
Completed NSE at 02:30, 0.00s elapsed
Nmap scan report for 192.168.224.101
Host is up, received user-set (0.16s latency).
Scanned at 2023-10-18 02:30:07 EDT for 18s

PORT     STATE SERVICE REASON  VERSION
22/tcp   open  ssh     syn-ack OpenSSH 8.2p1 Ubuntu 4ubuntu0.1 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   3072 ef:24:0e:ab:d2:b3:16:b4:4b:2e:27:c0:5f:48:79:8b (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQDamdAqH2ZyWoYj0tstPK0vbVKI+9OCgtkGDoynffxqV2kE4ceZn77FBuMGFKLU50Uv5RMUTFTX4hm1ijh77KMGG1CmAk2YWvEDhxbCBPCohp+xXMBXHBYoMbEVl/loKL2UW6USnKorOgwxUdoMAwDxIrohGHQ5WNUADRaqt1eHuHxuJ8Bgi8yzqP/26ePQTLCfwAZMq+SYPJedZBmfJJ3Brhb/CGgzgRU8BpJGI8IfBL5791JTn2niEgoMAZ1vdfnSx0m49uk8npd0h5hPQ+ucyMh+Q35lJ1zDq94E24mkgawDhEgmLtb23JDNdY4rv/7mAAHYA5AsRSDDFgmbXEVcC7N1c3cyrwVH/w+zF5SKOqQ8hOF7LRCqv0YQZ05wyiBu2OzbeAvhhiKJteICMuitQAuF6zU/dwjX7oEAxbZ2GsQ66kU3/JnL4clTDATbT01REKJzH9nHpO5sZdebfLJdVfx38qDrlS+risx1QngpnRvWTmJ7XBXt8UrfXGenR3U=
|   256 f2:d8:35:3f:49:59:85:85:07:e6:a2:0e:65:7a:8c:4b (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBNoh1z4mRbfROqXjtv9CG7ZYGiwN29OQQCVXMLce4ejLzy+0Bvo7tYSb5PKVqgO5jd1JaB3LLGWreXo6ZY3Z8T8=
|   256 0b:23:89:c3:c0:26:d5:64:5e:93:b7:ba:f5:14:7f:3e (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIDXv++bn0YEgaoSEmMm3RzCzm6pyUJJSsSW9FMBqvZQ3
80/tcp   open  http    syn-ack Apache httpd 2.4.41 ((Ubuntu))
|_http-title: Potato company
|_http-server-header: Apache/2.4.41 (Ubuntu)
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
2112/tcp open  ftp     syn-ack ProFTPD
| ftp-anon: Anonymous FTP login allowed (FTP code 230)
| -rw-r--r--   1 ftp      ftp           901 Aug  2  2020 index.php.bak
|_-rw-r--r--   1 ftp      ftp            54 Aug  2  2020 welcome.msg
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

NSE: Script Post-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 02:30
Completed NSE at 02:30, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 02:30
Completed NSE at 02:30, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 02:30
Completed NSE at 02:30, 0.00s elapsed
Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 18.84 seconds
```

FTP:
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/bbdfde18-c893-4094-90d9-0be4ccc12184)

```shell
> ftp 192.168.224.101 -P 2112
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/8adaa352-db00-448f-9ce7-2cfd38202eac)

Backup File
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/3ca994c3-9657-4fa5-a1f8-d257bf2c6e39)

Message File
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/eaf3cf4e-8e15-4f6f-9b44-39b1cc875c34)

HTTP:
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/fc450dcc-f1c6-45bb-91ef-45622be28469)