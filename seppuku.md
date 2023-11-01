```
> rustscan -b 1000 -u 5000 -r 0-65535 -a 192.168.241.90 -- -Pn
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
Open 192.168.241.90:21
Open 192.168.241.90:22
Open 192.168.241.90:80
Open 192.168.241.90:139
Open 192.168.241.90:445
Open 192.168.241.90:7080
Open 192.168.241.90:7601
Open 192.168.241.90:8088
[~] Starting Script(s)
[>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")

Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2023-11-01 00:45 EDT
Initiating Parallel DNS resolution of 1 host. at 00:45
Completed Parallel DNS resolution of 1 host. at 00:45, 0.01s elapsed
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating Connect Scan at 00:45
Scanning 192.168.241.90 [8 ports]
Discovered open port 22/tcp on 192.168.241.90
Discovered open port 21/tcp on 192.168.241.90
Discovered open port 139/tcp on 192.168.241.90
Discovered open port 80/tcp on 192.168.241.90
Discovered open port 445/tcp on 192.168.241.90
Discovered open port 7080/tcp on 192.168.241.90
Discovered open port 8088/tcp on 192.168.241.90
Discovered open port 7601/tcp on 192.168.241.90
Completed Connect Scan at 00:45, 0.75s elapsed (8 total ports)
Nmap scan report for 192.168.241.90
Host is up, received user-set (0.75s latency).
Scanned at 2023-11-01 00:45:24 EDT for 1s

PORT     STATE SERVICE      REASON
21/tcp   open  ftp          syn-ack
22/tcp   open  ssh          syn-ack
80/tcp   open  http         syn-ack
139/tcp  open  netbios-ssn  syn-ack
445/tcp  open  microsoft-ds syn-ack
7080/tcp open  empowerid    syn-ack
7601/tcp open  unknown      syn-ack
8088/tcp open  radan-http   syn-ack

Read data files from: /usr/bin/../share/nmap
Nmap done: 1 IP address (1 host up) scanned in 0.78 seconds
```

```
http://192.168.241.90
```
![image](https://github.com/karanshergill/OffSec-Play-Labs/assets/83878909/1af3f6b0-6dba-4a6a-b2a0-ca83790ab652)
