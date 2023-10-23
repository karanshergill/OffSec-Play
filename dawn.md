```
> rustscan -b 1000 -u 5000 -r 0-65535 -a 192.168.187.11 -- -Pn
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
Open 192.168.187.11:80
Open 192.168.187.11:139
Open 192.168.187.11:445
Open 192.168.187.11:3306
[~] Starting Script(s)
[>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")

Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2023-10-23 01:04 EDT
Initiating Parallel DNS resolution of 1 host. at 01:04
Completed Parallel DNS resolution of 1 host. at 01:04, 0.01s elapsed
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating Connect Scan at 01:04
Scanning 192.168.187.11 [4 ports]
Discovered open port 445/tcp on 192.168.187.11
Discovered open port 80/tcp on 192.168.187.11
Discovered open port 3306/tcp on 192.168.187.11
Discovered open port 139/tcp on 192.168.187.11
Completed Connect Scan at 01:04, 0.17s elapsed (4 total ports)
Nmap scan report for 192.168.187.11
Host is up, received user-set (0.17s latency).
Scanned at 2023-10-23 01:04:37 EDT for 0s

PORT     STATE SERVICE      REASON
80/tcp   open  http         syn-ack
139/tcp  open  netbios-ssn  syn-ack
445/tcp  open  microsoft-ds syn-ack
3306/tcp open  mysql        syn-ack

Read data files from: /usr/bin/../share/nmap
Nmap done: 1 IP address (1 host up) scanned in 0.22 seconds
```

```
> rustscan -u 5000 -p 80,139,445,3306 -a 192.168.187.11 -- -Pn -sCV
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
Open 192.168.187.11:80
Open 192.168.187.11:139
Open 192.168.187.11:445
Open 192.168.187.11:3306
[~] Starting Script(s)
[>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")

Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2023-10-23 01:06 EDT
NSE: Loaded 156 scripts for scanning.
NSE: Script Pre-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 01:06
Completed NSE at 01:06, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 01:06
Completed NSE at 01:06, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 01:06
Completed NSE at 01:06, 0.00s elapsed
Initiating Parallel DNS resolution of 1 host. at 01:06
Completed Parallel DNS resolution of 1 host. at 01:06, 0.01s elapsed
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating Connect Scan at 01:06
Scanning 192.168.187.11 [4 ports]
Discovered open port 139/tcp on 192.168.187.11
Discovered open port 3306/tcp on 192.168.187.11
Discovered open port 445/tcp on 192.168.187.11
Discovered open port 80/tcp on 192.168.187.11
Completed Connect Scan at 01:06, 0.17s elapsed (4 total ports)
Initiating Service scan at 01:06
Scanning 4 services on 192.168.187.11
Completed Service scan at 01:06, 11.60s elapsed (4 services on 1 host)
NSE: Script scanning 192.168.187.11.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 01:06
Completed NSE at 01:06, 10.36s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 01:06
Completed NSE at 01:06, 21.53s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 01:06
Completed NSE at 01:06, 0.00s elapsed
Nmap scan report for 192.168.187.11
Host is up, received user-set (0.17s latency).
Scanned at 2023-10-23 01:06:06 EDT for 44s

PORT     STATE SERVICE     REASON  VERSION
80/tcp   open  http        syn-ack Apache httpd 2.4.38 ((Debian))
|_http-title: Site doesn't have a title (text/html).
|_http-server-header: Apache/2.4.38 (Debian)
| http-methods: 
|_  Supported Methods: POST OPTIONS HEAD GET
139/tcp  open  netbios-ssn syn-ack Samba smbd 3.X - 4.X (workgroup: WORKGROUP)
445/tcp  open  �           syn-ack Samba smbd 4.9.5-Debian (workgroup: WORKGROUP)
3306/tcp open  mysql       syn-ack MySQL 5.5.5-10.3.15-MariaDB-1
| mysql-info: 
|   Protocol: 10
|   Version: 5.5.5-10.3.15-MariaDB-1
|   Thread ID: 18
|   Capabilities flags: 63486
|   Some Capabilities: Support41Auth, ConnectWithDatabase, ODBCClient, SupportsLoadDataLocal, Speaks41ProtocolOld, IgnoreSpaceBeforeParenthesis, SupportsTransactions, IgnoreSigpipes, DontAllowDatabaseTableColumn, FoundRows, LongColumnFlag, InteractiveClient, Speaks41ProtocolNew, SupportsCompression, SupportsMultipleResults, SupportsAuthPlugins, SupportsMultipleStatments
|   Status: Autocommit
|   Salt: )E_/hCSV8RuunFQGN3Q~
|_  Auth Plugin Name: mysql_native_password
Service Info: Host: DAWN

Host script results:
|_clock-skew: mean: 1h19m59s, deviation: 2h18m34s, median: 0s
| p2p-conficker: 
|   Checking for Conficker.C or higher...
|   Check 1 (port 40076/tcp): CLEAN (Couldn't connect)
|   Check 2 (port 28742/tcp): CLEAN (Couldn't connect)
|   Check 3 (port 53536/udp): CLEAN (Timeout)
|   Check 4 (port 24415/udp): CLEAN (Failed to receive data)
|_  0/4 checks are positive: Host is CLEAN or ports are blocked
| smb2-security-mode: 
|   3:1:1: 
|_    Message signing enabled but not required
| smb-os-discovery: 
|   OS: Windows 6.1 (Samba 4.9.5-Debian)
|   Computer name: dawn
|   NetBIOS computer name: DAWN\x00
|   Domain name: dawn
|   FQDN: dawn.dawn
|_  System time: 2023-10-23T01:06:19-04:00
| smb-security-mode: 
|   account_used: guest
|   authentication_level: user
|   challenge_response: supported
|_  message_signing: disabled (dangerous, but default)
| smb2-time: 
|   date: 2023-10-23T05:06:20
|_  start_date: N/A

NSE: Script Post-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 01:06
Completed NSE at 01:06, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 01:06
Completed NSE at 01:06, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 01:06
Completed NSE at 01:06, 0.00s elapsed
Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 44.00 seconds
```

SMB Enumeration
```
> smbclient -L \\192.168.187.11
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/ce755efd-048b-4a53-8318-55fa41395142)



TCP 80/HTTP
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/d40fe019-90cb-49aa-942a-219d8b1cd8c4)

```
> feroxbuster -u http://192.168.187.11 -w /usr/share/wordlists/seclists/Discovery/Web-Content/directory-list-2.3-small.txt --no-recursion --dont-extract-links --random-agent --filter-status 404


```

```
http://192.168.187.11/logs/
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/1a884529-734e-4bb5-8c0a-9ab1e01e7097)

```
http://192.168.187.11/cctv/
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/dc9f1ac9-86e9-460d-85bb-6ec5097fadbf)
