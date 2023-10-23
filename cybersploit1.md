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
```
username:itsskv
```

Feroxbuster
```
> feroxbuster -u http://192.168.187.92 -w /usr/share/wordlists/seclists/Discovery/Web-Content/directory-list-2.3-small.txt --no-recursion --dont-extract-links --random-agent --filter-status 404

 ___  ___  __   __     __      __         __   ___
|__  |__  |__) |__) | /  `    /  \ \_/ | |  \ |__
|    |___ |  \ |  \ | \__,    \__/ / \ | |__/ |___
by Ben "epi" Risher 🤓                 ver: 2.10.0
───────────────────────────┬──────────────────────
 🎯  Target Url            │ http://192.168.187.92
 🚀  Threads               │ 50
 📖  Wordlist              │ /usr/share/wordlists/seclists/Discovery/Web-Content/directory-list-2.3-small.txt
 💢  Status Code Filters   │ [404]
 💥  Timeout (secs)        │ 7
 🦡  User-Agent            │ Random
 💉  Config File           │ /etc/feroxbuster/ferox-config.toml
 🏁  HTTP methods          │ [GET]
 🚫  Do Not Recurse        │ true
───────────────────────────┴──────────────────────
 🏁  Press [ENTER] to use the Scan Management Menu™
──────────────────────────────────────────────────
403      GET       10l       30w        -c Auto-filtering found 404-like response and created new filter; toggle off with --dont-filter
404      GET        9l       32w        -c Auto-filtering found 404-like response and created new filter; toggle off with --dont-filter
200      GET       50l      133w     2333c http://192.168.187.92/
200      GET       50l      133w     2333c http://192.168.187.92/index
200      GET        1l        1w       53c http://192.168.187.92/robots
200      GET        0l        0w  3757743c http://192.168.187.92/hacker
[####################] - 5m     87650/87650   0s      found:4       errors:0      
[####################] - 5m     87650/87650   290/s   http://192.168.187.92/  
```

```
http://192.168.187.92/robots
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/9b2f982e-ac4d-4d7e-9b4d-c2728b57dc52)
