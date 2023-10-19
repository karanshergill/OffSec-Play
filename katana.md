```
> rustscan -b 1000 -u 5000 -r 0-65535 -a 192.168.172.83 -- -Pn
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
Open 192.168.172.83:21
Open 192.168.172.83:22
Open 192.168.172.83:80
Open 192.168.172.83:7080
Open 192.168.172.83:8088
Open 192.168.172.83:8715
[~] Starting Script(s)
[>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")

Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2023-10-19 14:34 EDT
Initiating Parallel DNS resolution of 1 host. at 14:34
Completed Parallel DNS resolution of 1 host. at 14:34, 0.01s elapsed
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating Connect Scan at 14:34
Scanning 192.168.172.83 [6 ports]
Discovered open port 21/tcp on 192.168.172.83
Discovered open port 80/tcp on 192.168.172.83
Discovered open port 22/tcp on 192.168.172.83
Discovered open port 7080/tcp on 192.168.172.83
Discovered open port 8088/tcp on 192.168.172.83
Discovered open port 8715/tcp on 192.168.172.83
Completed Connect Scan at 14:34, 0.18s elapsed (6 total ports)
Nmap scan report for 192.168.172.83
Host is up, received user-set (0.18s latency).
Scanned at 2023-10-19 14:34:18 EDT for 0s

PORT     STATE SERVICE    REASON
21/tcp   open  ftp        syn-ack
22/tcp   open  ssh        syn-ack
80/tcp   open  http       syn-ack
7080/tcp open  empowerid  syn-ack
8088/tcp open  radan-http syn-ack
8715/tcp open  unknown    syn-ack

Read data files from: /usr/bin/../share/nmap
Nmap done: 1 IP address (1 host up) scanned in 0.21 seconds
```

TCP-80/HTTP
```
http://192.168.172.83/
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/8b5529be-2f8b-4ba0-9853-a10eb3b95eac)


Directory Brute-Force
```
> feroxbuster -u http://192.168.172.83 -w /usr/share/wordlists/seclists/Discovery/Web-Content/directory-list-2.3-small.txt --no-recursion --dont-extract-links --status-codes 200 --random-agent
```
```

```

```http
http://192.168.172.83/ebook/
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/d98fcde9-8c95-4c6e-b87e-b275615b4cbc)

![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/5066a5ea-9fc9-4a25-9236-62521d63388f)

![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/41e72082-c6a1-47cf-ae67-b4f6d7eecfcd)

Default Crdentials:
```css
admin:admin
```

```http
http://192.168.172.83/ebook/admin_book.php
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/20af2dbc-4835-4938-b9ae-eaa8c8e00f41)

