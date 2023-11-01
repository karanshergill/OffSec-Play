```
> rustscan -b 1000 -u 5000 -r 0-65535 -a 192.168.241.73 -- -Pn
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
Real hackers hack time ⌛

[~] The config file is expected to be at "/home/superuser/.rustscan.toml"
[~] Automatically increasing ulimit value to 5000.
Open 192.168.241.73:22
Open 192.168.241.73:80
[~] Starting Script(s)
[>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")

Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2023-10-31 22:40 EDT
Initiating Parallel DNS resolution of 1 host. at 22:40
Completed Parallel DNS resolution of 1 host. at 22:40, 0.01s elapsed
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating Connect Scan at 22:40
Scanning 192.168.241.73 [2 ports]
Discovered open port 80/tcp on 192.168.241.73
Discovered open port 22/tcp on 192.168.241.73
Completed Connect Scan at 22:40, 0.16s elapsed (2 total ports)
Nmap scan report for 192.168.241.73
Host is up, received user-set (0.16s latency).
Scanned at 2023-10-31 22:40:43 EDT for 0s

PORT   STATE SERVICE REASON
22/tcp open  ssh     syn-ack
80/tcp open  http    syn-ack

Read data files from: /usr/bin/../share/nmap
Nmap done: 1 IP address (1 host up) scanned in 0.21 seconds
```

```
> rustscan -u 5000 -p 22,80 -a 192.168.241.73 -- -Pn -sCV
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
Open 192.168.241.73:80
Open 192.168.241.73:22
[~] Starting Script(s)
[>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")

Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2023-10-31 22:42 EDT
NSE: Loaded 156 scripts for scanning.
NSE: Script Pre-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 22:42
Completed NSE at 22:42, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 22:42
Completed NSE at 22:42, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 22:42
Completed NSE at 22:42, 0.00s elapsed
Initiating Parallel DNS resolution of 1 host. at 22:42
Completed Parallel DNS resolution of 1 host. at 22:42, 0.12s elapsed
DNS resolution of 1 IPs took 0.12s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating Connect Scan at 22:42
Scanning 192.168.241.73 [2 ports]
Discovered open port 22/tcp on 192.168.241.73
Discovered open port 80/tcp on 192.168.241.73
Completed Connect Scan at 22:42, 0.16s elapsed (2 total ports)
Initiating Service scan at 22:42
Scanning 2 services on 192.168.241.73
Completed Service scan at 22:42, 6.36s elapsed (2 services on 1 host)
NSE: Script scanning 192.168.241.73.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 22:42
Completed NSE at 22:42, 4.78s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 22:42
Completed NSE at 22:42, 0.67s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 22:42
Completed NSE at 22:42, 0.00s elapsed
Nmap scan report for 192.168.241.73
Host is up, received user-set (0.16s latency).
Scanned at 2023-10-31 22:42:12 EDT for 12s

PORT   STATE SERVICE REASON  VERSION
22/tcp open  ssh     syn-ack OpenSSH 7.9p1 Debian 10+deb10u2 (protocol 2.0)
| ssh-hostkey: 
|   2048 1f:31:30:67:3f:08:30:2e:6d:ae:e3:20:9e:bd:6b:ba (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQC99CVoBmDEZGefSkVfvgPRyFNH5rKQF9KMAsqFTL+Xkbwg2S3t+8tIFpPon/m7SYAH+NTqfv3uYXPq2DkVAXD8i2iXKnRa0+QKHNe2bupBbaTX3xyWGHeL7aBh4Io7xxEiTaCLD9wrDA9aHxHhXdUC0QMvld21dIJygyOoV9P17FC3EwBqJEOjLnCNTxzi25W0f6Gqv1vZXHFeQJfT4CLRZCE8BtpBAaoiKMGFOMJEOy+gVe1YgFim/smodNO51fx7zZKxMjhcE46BBRgcywE1FflXPFx3NYDTkou3Wmo0ENEvXcmD36tZsFeMHLyAv/rD2NG1cCWJp6tfcD/SbSPj
|   256 7d:88:55:a8:6f:56:c8:05:a4:73:82:dc:d8:db:47:59 (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBJVCfO2orE34rbwG0NoOp8DNLMEusESLX7L7c45ZjSk7DgSn8edbEuGlswfCdyyROevxZ/aHgMQO8avPFE/ZAME=
|   256 cc:de:de:4e:84:a8:91:f5:1a:d6:d2:a6:2e:9e:1c:e0 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIAc1RjhxOyboK+O9fxD5/tbd04IwXVwrQQDT16A111tu
80/tcp open  http    syn-ack Apache httpd 2.4.38 ((Debian))
|_http-server-header: Apache/2.4.38 (Debian)
| http-methods: 
|_  Supported Methods: OPTIONS HEAD GET POST
|_http-title: Site doesn't have a title (text/html).
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

NSE: Script Post-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 22:42
Completed NSE at 22:42, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 22:42
Completed NSE at 22:42, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 22:42
Completed NSE at 22:42, 0.00s elapsed
Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 12.53 seconds
```

```
http://192.168.241.73/
```
![image](https://github.com/karanshergill/OffSec-Play-Labs/assets/83878909/e7f461fe-8a58-48ee-beec-62d080d77139)

Content Discovery
```

```

```
http://192.168.241.73/admin/
```
![image](https://github.com/karanshergill/OffSec-Play-Labs/assets/83878909/103b8fe0-6439-4729-bca1-5fc478d8635a)

```
http://192.168.241.73/admin/admin.php
```
![image](https://github.com/karanshergill/OffSec-Play-Labs/assets/83878909/10274197-73a0-4d11-8c1b-5620faa371f1)

```
http://192.168.241.73/manual/en/index.html
```
![image](https://github.com/karanshergill/OffSec-Play-Labs/assets/83878909/1d5f494a-5d7d-42b4-b993-500339ea1d39)
