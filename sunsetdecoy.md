```shell
> rustscan -b 1000 -u 5000 -r 0-65535 -a 192.168.224.85 -- -Pn
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
Open 192.168.224.85:22
Open 192.168.224.85:80
[~] Starting Script(s)
[>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")

Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2023-10-20 04:07 EDT
Initiating Parallel DNS resolution of 1 host. at 04:07
Completed Parallel DNS resolution of 1 host. at 04:07, 0.01s elapsed
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating Connect Scan at 04:07
Scanning 192.168.224.85 [2 ports]
Discovered open port 22/tcp on 192.168.224.85
Discovered open port 80/tcp on 192.168.224.85
Completed Connect Scan at 04:07, 0.17s elapsed (2 total ports)
Nmap scan report for 192.168.224.85
Host is up, received user-set (0.17s latency).
Scanned at 2023-10-20 04:07:49 EDT for 0s

PORT   STATE SERVICE REASON
22/tcp open  ssh     syn-ack
80/tcp open  http    syn-ack

Read data files from: /usr/bin/../share/nmap
Nmap done: 1 IP address (1 host up) scanned in 0.21 seconds
```

```shell
> rustscan -u 5000 -p 22,80 -a 192.168.224.85 -- -Pn -sCV
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
Open 192.168.224.85:80
Open 192.168.224.85:22
[~] Starting Script(s)
[>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")

Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2023-10-20 04:09 EDT
NSE: Loaded 156 scripts for scanning.
NSE: Script Pre-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 04:09
Completed NSE at 04:09, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 04:09
Completed NSE at 04:09, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 04:09
Completed NSE at 04:09, 0.00s elapsed
Initiating Parallel DNS resolution of 1 host. at 04:09
Completed Parallel DNS resolution of 1 host. at 04:09, 0.01s elapsed
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating Connect Scan at 04:09
Scanning 192.168.224.85 [2 ports]
Discovered open port 80/tcp on 192.168.224.85
Discovered open port 22/tcp on 192.168.224.85
Completed Connect Scan at 04:09, 0.17s elapsed (2 total ports)
Initiating Service scan at 04:09
Scanning 2 services on 192.168.224.85
Completed Service scan at 04:09, 6.35s elapsed (2 services on 1 host)
NSE: Script scanning 192.168.224.85.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 04:09
Completed NSE at 04:09, 5.08s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 04:09
Completed NSE at 04:09, 0.68s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 04:09
Completed NSE at 04:09, 0.00s elapsed
Nmap scan report for 192.168.224.85
Host is up, received user-set (0.17s latency).
Scanned at 2023-10-20 04:09:20 EDT for 12s

PORT   STATE SERVICE REASON  VERSION
22/tcp open  ssh     syn-ack OpenSSH 7.9p1 Debian 10+deb10u2 (protocol 2.0)
| ssh-hostkey: 
|   2048 a9:b5:3e:3b:e3:74:e4:ff:b6:d5:9f:f1:81:e7:a4:4f (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQCxxReThUimjbPP7ZO1dPbvqSobxafY5J8i9Un5zUH7z9uIZEOHNXzEsq8Vko44IBRv2a7xvuuqtk7yN3XwKdyh8mrt1bV/C7Yx6CZ1q7CiQyYd0QoUqyrp6dGdT6T4fYZ7OwUwyubgqEYdkmiS8qNvlKI2qWdj9hntzzWF9X0F+jbxhLOi6Ovo5DGaSiKxsU/ISjnDsR3geodqeVHbMR+jRq7ucIjRSIOHvp8u9LvrugorZDhdv14yJQj7zfySL1T8WcI8kKUECmZgZTk6iUKYLWZ95oo07kKIs6EeTEGNswUeTjEVebhUFHMep6W1ehU7cE6OREkeZ0Rvuh4EpUTx
|   256 ce:f3:b3:e7:0e:90:e2:64:ac:8d:87:0f:15:88:aa:5f (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBGKuMuZL3YT/QadMNsFaoWvNYLjKK/DlWoz1/15wGhrauU2OMlHQWEc7ChAX+QdIWc1aEN6IAabgvzIzHPnRYV0=
|   256 66:a9:80:91:f3:d8:4b:0a:69:b0:00:22:9f:3c:4c:5a (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAILNCj4KmJHpZhhE3ZdD/NkVmz1ePM2XW6l0uK3yCT0Og
80/tcp open  http    syn-ack Apache httpd 2.4.38
| http-ls: Volume /
| SIZE  TIME              FILENAME
| 3.0K  2020-07-07 16:36  save.zip
|_
|_http-title: Index of /
|_http-server-header: Apache/2.4.38 (Debian)
| http-methods: 
|_  Supported Methods: GET POST OPTIONS HEAD
Service Info: Host: 127.0.0.1; OS: Linux; CPE: cpe:/o:linux:linux_kernel

NSE: Script Post-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 04:09
Completed NSE at 04:09, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 04:09
Completed NSE at 04:09, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 04:09
Completed NSE at 04:09, 0.00s elapsed
Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 12.74 seconds
```
