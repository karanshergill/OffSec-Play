```
> rustscan -b 1000 -u 5000 -r 0-65535 -a 192.168.187.92 -- -Pn
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
Open 192.168.187.92:22
Open 192.168.187.92:80
[~] Starting Script(s)
[>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")

Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2023-10-23 03:25 EDT
Initiating Parallel DNS resolution of 1 host. at 03:25
Completed Parallel DNS resolution of 1 host. at 03:25, 0.01s elapsed
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating Connect Scan at 03:25
Scanning 192.168.187.92 [2 ports]
Discovered open port 80/tcp on 192.168.187.92
Discovered open port 22/tcp on 192.168.187.92
Completed Connect Scan at 03:25, 0.17s elapsed (2 total ports)
Nmap scan report for 192.168.187.92
Host is up, received user-set (0.17s latency).
Scanned at 2023-10-23 03:25:19 EDT for 0s

PORT   STATE SERVICE REASON
22/tcp open  ssh     syn-ack
80/tcp open  http    syn-ack

Read data files from: /usr/bin/../share/nmap
Nmap done: 1 IP address (1 host up) scanned in 0.20 seconds
```

```
http://192.168.187.92/
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/2b132ff5-f7b3-431e-b8d8-aa32c3efb864)
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/c944b990-66f2-4a8b-b39b-9d3b0cb48df3)


