```
> rustscan -b 1000 -u 5000 -r 0-65535 -a 192.168.207.14 -- -Pn
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
😵 https://admin.tryhackme.com

[~] The config file is expected to be at "/home/superuser/.rustscan.toml"
[~] Automatically increasing ulimit value to 5000.
Open 192.168.207.14:21
Open 192.168.207.14:22
Open 192.168.207.14:80
[~] Starting Script(s)
[>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")

Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2023-11-06 08:34 EST
Initiating Parallel DNS resolution of 1 host. at 08:34
Completed Parallel DNS resolution of 1 host. at 08:34, 0.01s elapsed
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating Connect Scan at 08:34
Scanning 192.168.207.14 [3 ports]
Discovered open port 22/tcp on 192.168.207.14
Discovered open port 21/tcp on 192.168.207.14
Discovered open port 80/tcp on 192.168.207.14
Completed Connect Scan at 08:34, 0.15s elapsed (3 total ports)
Nmap scan report for 192.168.207.14
Host is up, received user-set (0.15s latency).
Scanned at 2023-11-06 08:34:26 EST for 0s

PORT   STATE SERVICE REASON
21/tcp open  ftp     syn-ack
22/tcp open  ssh     syn-ack
80/tcp open  http    syn-ack

Read data files from: /usr/bin/../share/nmap
Nmap done: 1 IP address (1 host up) scanned in 0.21 seconds
```

```
> rustscan -u 5000 -p 21,22,80 -a 192.168.207.14 -- -Pn -sCV
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
Open 192.168.207.14:21
Open 192.168.207.14:22
Open 192.168.207.14:80
[~] Starting Script(s)
[>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")

Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2023-11-06 08:36 EST
NSE: Loaded 156 scripts for scanning.
NSE: Script Pre-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 08:36
Completed NSE at 08:36, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 08:36
Completed NSE at 08:36, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 08:36
Completed NSE at 08:36, 0.00s elapsed
Initiating Parallel DNS resolution of 1 host. at 08:36
Completed Parallel DNS resolution of 1 host. at 08:36, 0.01s elapsed
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating Connect Scan at 08:36
Scanning 192.168.207.14 [3 ports]
Discovered open port 21/tcp on 192.168.207.14
Discovered open port 80/tcp on 192.168.207.14
Discovered open port 22/tcp on 192.168.207.14
Completed Connect Scan at 08:36, 0.15s elapsed (3 total ports)
Initiating Service scan at 08:36
Scanning 3 services on 192.168.207.14
Completed Service scan at 08:36, 6.32s elapsed (3 services on 1 host)
NSE: Script scanning 192.168.207.14.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 08:36
NSE: [ftp-bounce 192.168.207.14:21] PORT response: 500 Illegal PORT command.
Completed NSE at 08:36, 5.28s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 08:36
Completed NSE at 08:36, 1.08s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 08:36
Completed NSE at 08:36, 0.00s elapsed
Nmap scan report for 192.168.207.14
Host is up, received user-set (0.15s latency).
Scanned at 2023-11-06 08:36:08 EST for 13s

PORT   STATE SERVICE REASON  VERSION
21/tcp open  ftp     syn-ack vsftpd 3.0.3
| ftp-anon: Anonymous FTP login allowed (FTP code 230)
|_drwxrwxrwx    2 0        0            4096 Feb 08  2020 pub [NSE: writeable]
| ftp-syst: 
|   STAT: 
| FTP server status:
|      Connected to ::ffff:192.168.45.233
|      Logged in as ftp
|      TYPE: ASCII
|      No session bandwidth limit
|      Session timeout in seconds is 300
|      Control connection is plain text
|      Data connections will be plain text
|      At session startup, client count was 2
|      vsFTPd 3.0.3 - secure, fast, stable
|_End of status
22/tcp open  ssh     syn-ack OpenSSH 7.9p1 Debian 10+deb10u1 (protocol 2.0)
| ssh-hostkey: 
|   2048 06:1b:a3:92:83:a5:7a:15:bd:40:6e:0c:8d:98:27:7b (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQC8Yl88LxuiPiXQGaZ6fB6K88oCmL/yXhY4Y3j/9PjnFHPRCqM18y4Ol7Q9LMr5CN042Zs/WMt05YE99R5j98fPGD0hIqxKpRpW8ZeDsfZdG479t3dSkM0OAL+hY4V4Wwbk768DxnLUw0ujGuh38UDl3gyYVBFpFZgRb7zBuYRzjIdWijpXm23sbXti4TO6KTC4KVm1BTzT4CVFxBakuuvk1Ieraeusc9agTfCVx7dkN2OX79jAc1uzZNE+BtokFGIYMvMAA7ejZT504cp1Bccbn+OUwlcRLFJbOO2jrXPj8j4MKEz6klMO7mIMvaHFRQ1Z5kBtH7QIGG97D5qhkD8X
|   256 cb:38:83:26:1a:9f:d3:5d:d3:fe:9b:a1:d3:bc:ab:2c (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBGNCidfAh8l1B4elJK42/1YqrUEBlGWDjg7ZWacpptAfCGBbSC+agR4LWiEtsnQYX4aWXRGydjc7UggCgpHbDr0=
|   256 65:54:fc:2d:12:ac:e1:84:78:3e:00:23:fb:e4:c9:ee (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIJEkCe1XYRTFeHyzWuvZ3JkIkWwD4pGHBcTGEGYYcJhv
80/tcp open  http    syn-ack Apache httpd 2.4.38 ((Debian))
|_http-title: Apache2 Debian Default Page: It works
|_http-server-header: Apache/2.4.38 (Debian)
| http-methods: 
|_  Supported Methods: POST OPTIONS HEAD GET
Service Info: OSs: Unix, Linux; CPE: cpe:/o:linux:linux_kernel

NSE: Script Post-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 08:36
Completed NSE at 08:36, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 08:36
Completed NSE at 08:36, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 08:36
Completed NSE at 08:36, 0.00s elapsed
Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 13.19 seconds
```

```
http://192.168.207.14/
```
![image](https://github.com/karanshergill/OffSec-Play-Labs/assets/83878909/df646f31-8d18-4b9f-9f4e-5d8f9856b40c)

Content Discovery
```
> feroxbuster -u http://192.168.207.14 -w /usr/share/seclists/Discovery/Web-Content/common.txt --no-recursion --dont-extract-links --random-agent --filter-status 404 --redirects
```
```
 ___  ___  __   __     __      __         __   ___
|__  |__  |__) |__) | /  `    /  \ \_/ | |  \ |__
|    |___ |  \ |  \ | \__,    \__/ / \ | |__/ |___
by Ben "epi" Risher 🤓                 ver: 2.10.0
───────────────────────────┬──────────────────────
 🎯  Target Url            │ http://192.168.207.14
 🚀  Threads               │ 50
 📖  Wordlist              │ /usr/share/seclists/Discovery/Web-Content/common.txt
 💢  Status Code Filters   │ [404]
 💥  Timeout (secs)        │ 7
 🦡  User-Agent            │ Random
 💉  Config File           │ /etc/feroxbuster/ferox-config.toml
 🏁  HTTP methods          │ [GET]
 📍  Follow Redirects      │ true
 🚫  Do Not Recurse        │ true
───────────────────────────┴──────────────────────
 🏁  Press [ENTER] to use the Scan Management Menu™
──────────────────────────────────────────────────
404      GET        9l       31w      276c Auto-filtering found 404-like response and created new filter; toggle off with --dont-filter
403      GET        9l       28w      279c Auto-filtering found 404-like response and created new filter; toggle off with --dont-filter
200      GET      368l      933w    10701c http://192.168.207.14/
200      GET      368l      933w    10701c http://192.168.207.14/index.html
200      GET       13l       26w      626c http://192.168.207.14/manual/
200      GET        1l       11w       59c http://192.168.207.14/robots.txt
[####################] - 25s     4724/4724    0s      found:4       errors:37     
[####################] - 25s     4724/4724    191/s   http://192.168.207.14/    
```

```
http://192.168.207.14/robots.txt
```
![image](https://github.com/karanshergill/OffSec-Play-Labs/assets/83878909/5899f104-82a3-48d7-af14-7ec949593eb1)

User Agent for GoogleBot
```
Googlebot/2.1 (+http://www.google.com/bot.html)
```

Request sent with GoogleBot user agent
```
> curl http://192.168.207.14/robots.txt --user-agent "Googlebot/2.1 (+http://www.google.com/bot.html)"
```
![image](https://github.com/karanshergill/OffSec-Play-Labs/assets/83878909/6dc8e138-60cc-4a0b-8dc4-3c404ad80c41)

```
http://192.168.207.14/secret_information/
```
![image](https://github.com/karanshergill/OffSec-Play-Labs/assets/83878909/6adc693b-b21d-4d04-964e-c44a5b5629e5)


