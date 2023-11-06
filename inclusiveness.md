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
