```
> rustscan -b 1000 -u 5000 -r 0-65535 -a 192.168.223.35 -- -Pn
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
Nmap? More like slowmap.🐢

[~] The config file is expected to be at "/home/superuser/.rustscan.toml"
[~] Automatically increasing ulimit value to 5000.
Open 192.168.223.35:22
Open 192.168.223.35:80
[~] Starting Script(s)
[>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")

Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2023-10-26 00:39 EDT
Initiating Parallel DNS resolution of 1 host. at 00:39
Completed Parallel DNS resolution of 1 host. at 00:39, 0.01s elapsed
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating Connect Scan at 00:39
Scanning 192.168.223.35 [2 ports]
Discovered open port 80/tcp on 192.168.223.35
Discovered open port 22/tcp on 192.168.223.35
Completed Connect Scan at 00:39, 0.18s elapsed (2 total ports)
Nmap scan report for 192.168.223.35
Host is up, received user-set (0.18s latency).
Scanned at 2023-10-26 00:39:56 EDT for 0s

PORT   STATE SERVICE REASON
22/tcp open  ssh     syn-ack
80/tcp open  http    syn-ack

Read data files from: /usr/bin/../share/nmap
Nmap done: 1 IP address (1 host up) scanned in 0.23 seconds
```

```
> rustscan -u 5000 -p 22,80 -a 192.168.223.35 -- -Pn -sCV
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
Please contribute more quotes to our GitHub https://github.com/rustscan/rustscan

[~] The config file is expected to be at "/home/superuser/.rustscan.toml"
[~] Automatically increasing ulimit value to 5000.
Open 192.168.223.35:22
Open 192.168.223.35:80
[~] Starting Script(s)
[>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")

Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2023-10-26 00:41 EDT
NSE: Loaded 156 scripts for scanning.
NSE: Script Pre-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 00:41
Completed NSE at 00:41, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 00:41
Completed NSE at 00:41, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 00:41
Completed NSE at 00:41, 0.00s elapsed
Initiating Parallel DNS resolution of 1 host. at 00:41
Completed Parallel DNS resolution of 1 host. at 00:41, 0.01s elapsed
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating Connect Scan at 00:41
Scanning 192.168.223.35 [2 ports]
Discovered open port 80/tcp on 192.168.223.35
Discovered open port 22/tcp on 192.168.223.35
Completed Connect Scan at 00:41, 0.18s elapsed (2 total ports)
Initiating Service scan at 00:41
Scanning 2 services on 192.168.223.35
Completed Service scan at 00:41, 6.37s elapsed (2 services on 1 host)
NSE: Script scanning 192.168.223.35.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 00:41
Completed NSE at 00:41, 5.23s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 00:41
Completed NSE at 00:41, 0.72s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 00:41
Completed NSE at 00:41, 0.00s elapsed
Nmap scan report for 192.168.223.35
Host is up, received user-set (0.18s latency).
Scanned at 2023-10-26 00:41:07 EDT for 13s

PORT   STATE SERVICE REASON  VERSION
22/tcp open  ssh     syn-ack OpenSSH 7.6p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   2048 33:40:be:13:cf:51:7d:d6:a5:9c:64:c8:13:e5:f2:9f (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDHy/WJJHLFdbwbJpTyRYhEyj2jZV024UPWIdXfNHxq45uh08jkihv3znZ98caLP/pz352c0ZYD31We0bTSbHyjQce2bSAJHubDYp13hU/P4tbV5GIJ72W2rWkLTslH/SJoHUSqlManB7ZzgVyU2KQ4fnNx/V1XGJYsshquRqTrXKeeal+yQvTC4gnsr8ENIGMq0yJnYxMAasx6kmSc+S+065Mie65xkyisFXo2MQyxzsFdCu2w1bYmb3pegYDm6Y0c/EJP0sxDizXVwkUOS0XSVdGuk3RUYjt5GQ2fL24ZsML6CwN+HD2ZTnD0FK90PQTLuvlp6BoI/ZWvIenNvu63
|   256 8a:4e:ab:0b:de:e3:69:40:50:98:98:58:32:8f:71:9e (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBFgxutbLnN4K2tj6ZHzrlzTKS+RRuly+RkA0J63JsQFiwyvz4PqA64w/h0Se3gymZV6zJ9XBpS41b6IoEymeiSA=
|   256 e6:2f:55:1c:db:d0:bb:46:92:80:dd:5f:8e:a3:0a:41 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIM+5254x35Vwa2S7X73YLY87Q58qQOD9oQeSKMpmmT0o
80/tcp open  http    syn-ack Apache httpd 2.4.29 ((Ubuntu))
|_http-title: Apache2 Ubuntu Default Page: It works
|_http-server-header: Apache/2.4.29 (Ubuntu)
| http-methods: 
|_  Supported Methods: GET POST OPTIONS HEAD
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

NSE: Script Post-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 00:41
Completed NSE at 00:41, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 00:41
Completed NSE at 00:41, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 00:41
Completed NSE at 00:41, 0.00s elapsed
Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 12.95 seconds
```
