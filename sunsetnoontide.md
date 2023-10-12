# SunsetNoontide

```shell
> rustscan -b 1000 -u 5000 -r 0-65535 -a 192.168.241.120 -- -Pn
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
😵 https://admin.tryhackme.com

[~] The config file is expected to be at "/home/superuser/.rustscan.toml"
[~] Automatically increasing ulimit value to 5000.
Open 192.168.241.120:6667
Open 192.168.241.120:6697
Open 192.168.241.120:8067
[~] Starting Script(s)
[>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")

Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2023-10-12 02:40 EDT
Initiating Parallel DNS resolution of 1 host. at 02:40
Completed Parallel DNS resolution of 1 host. at 02:40, 0.01s elapsed
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating Connect Scan at 02:40
Scanning 192.168.241.120 [3 ports]
Discovered open port 6697/tcp on 192.168.241.120
Discovered open port 8067/tcp on 192.168.241.120
Discovered open port 6667/tcp on 192.168.241.120
Completed Connect Scan at 02:40, 0.16s elapsed (3 total ports)
Nmap scan report for 192.168.241.120
Host is up, received user-set (0.16s latency).
Scanned at 2023-10-12 02:40:55 EDT for 0s

PORT     STATE SERVICE    REASON
6667/tcp open  irc        syn-ack
6697/tcp open  ircs-u     syn-ack
8067/tcp open  infi-async syn-ack

Read data files from: /usr/bin/../share/nmap
Nmap done: 1 IP address (1 host up) scanned in 0.21 seconds
```

```shell
> rustscan -u 5000 -p 6667,6697,8067 -a 192.168.241.120 -- -Pn -sCV
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
Nmap? More like slowmap.🐢

[~] The config file is expected to be at "/home/superuser/.rustscan.toml"
[~] Automatically increasing ulimit value to 5000.
Open 192.168.241.120:6667
Open 192.168.241.120:6697
Open 192.168.241.120:8067
[~] Starting Script(s)
[>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")

Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2023-10-12 02:42 EDT
NSE: Loaded 156 scripts for scanning.
NSE: Script Pre-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 02:42
Completed NSE at 02:42, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 02:42
Completed NSE at 02:42, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 02:42
Completed NSE at 02:42, 0.00s elapsed
Initiating Parallel DNS resolution of 1 host. at 02:42
Completed Parallel DNS resolution of 1 host. at 02:42, 0.01s elapsed
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating Connect Scan at 02:42
Scanning 192.168.241.120 [3 ports]
Discovered open port 6667/tcp on 192.168.241.120
Discovered open port 6697/tcp on 192.168.241.120
Discovered open port 8067/tcp on 192.168.241.120
Completed Connect Scan at 02:42, 0.16s elapsed (3 total ports)
Initiating Service scan at 02:42
Scanning 3 services on 192.168.241.120
Completed Service scan at 02:42, 0.32s elapsed (3 services on 1 host)
NSE: Script scanning 192.168.241.120.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 02:42
Completed NSE at 02:42, 0.33s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 02:42
Completed NSE at 02:42, 1.29s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 02:42
Completed NSE at 02:42, 0.00s elapsed
Nmap scan report for 192.168.241.120
Host is up, received user-set (0.16s latency).
Scanned at 2023-10-12 02:42:50 EDT for 2s

PORT     STATE SERVICE REASON  VERSION
6667/tcp open  irc     syn-ack UnrealIRCd
6697/tcp open  irc     syn-ack UnrealIRCd
8067/tcp open  irc     syn-ack UnrealIRCd

NSE: Script Post-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 02:42
Completed NSE at 02:42, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 02:42
Completed NSE at 02:42, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 02:42
Completed NSE at 02:42, 0.00s elapsed
Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 2.58 seconds
```

```shell
> searchsploit UnrealIRCd
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/cfa93d1c-13cc-42b3-a8f1-c4aab91b3b23)


