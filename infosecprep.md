```
> rustscan -b 1000 -u 5000 -r 0-65535 -a 192.168.222.89 -- -Pn
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
Open 192.168.222.89:22
Open 192.168.222.89:80
Open 192.168.222.89:33060
[~] Starting Script(s)
[>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")

Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2023-10-31 06:55 EDT
Initiating Parallel DNS resolution of 1 host. at 06:55
Completed Parallel DNS resolution of 1 host. at 06:55, 0.01s elapsed
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating Connect Scan at 06:55
Scanning 192.168.222.89 [3 ports]
Discovered open port 80/tcp on 192.168.222.89
Discovered open port 22/tcp on 192.168.222.89
Discovered open port 33060/tcp on 192.168.222.89
Completed Connect Scan at 06:55, 0.16s elapsed (3 total ports)
Nmap scan report for 192.168.222.89
Host is up, received user-set (0.16s latency).
Scanned at 2023-10-31 06:55:06 EDT for 1s

PORT      STATE SERVICE REASON
22/tcp    open  ssh     syn-ack
80/tcp    open  http    syn-ack
33060/tcp open  mysqlx  syn-ack

Read data files from: /usr/bin/../share/nmap
Nmap done: 1 IP address (1 host up) scanned in 0.21 seconds
```

```
> rustscan -u 5000 -p 22,80,33060 -a 192.168.222.89 -- -Pn -sCV
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
🌍HACK THE PLANET🌍

[~] The config file is expected to be at "/home/superuser/.rustscan.toml"
[~] Automatically increasing ulimit value to 5000.
Open 192.168.222.89:80
Open 192.168.222.89:22
Open 192.168.222.89:33060
[~] Starting Script(s)
[>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")

Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2023-10-31 06:56 EDT
NSE: Loaded 156 scripts for scanning.
NSE: Script Pre-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 06:56
Completed NSE at 06:56, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 06:56
Completed NSE at 06:56, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 06:56
Completed NSE at 06:56, 0.00s elapsed
Initiating Parallel DNS resolution of 1 host. at 06:56
Completed Parallel DNS resolution of 1 host. at 06:56, 0.01s elapsed
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating Connect Scan at 06:56
Scanning 192.168.222.89 [3 ports]
Discovered open port 80/tcp on 192.168.222.89
Discovered open port 22/tcp on 192.168.222.89
Discovered open port 33060/tcp on 192.168.222.89
Completed Connect Scan at 06:56, 0.16s elapsed (3 total ports)
Initiating Service scan at 06:56
Scanning 3 services on 192.168.222.89
Completed Service scan at 06:56, 29.63s elapsed (3 services on 1 host)
NSE: Script scanning 192.168.222.89.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 06:56
Completed NSE at 06:56, 5.05s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 06:56
Completed NSE at 06:56, 0.66s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 06:56
Completed NSE at 06:56, 0.00s elapsed
Nmap scan report for 192.168.222.89
Host is up, received user-set (0.15s latency).
Scanned at 2023-10-31 06:56:05 EDT for 36s

PORT      STATE SERVICE REASON  VERSION
22/tcp    open  ssh     syn-ack OpenSSH 8.2p1 Ubuntu 4ubuntu0.1 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   3072 91:ba:0d:d4:39:05:e3:13:55:57:8f:1b:46:90:db:e4 (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQDTlNTlvI4qQLNU17b70iKB5xuJlNnZ3zMZeHzfG3H5TcsVNmgImTe4FjEez0e4lKqJvTMsxrPVFHTq6gqfYHwN0KN34x0dv0ngrc+wrrWNoHQrQQqeFuTZy0Tt6BY97082YpFvZfDAvAwJoutkyCxeBb1+C9Y7g6kQYXlNFOuHoq/2m6vki9yVW7Bu3IVeLryw/7pnwzb/tr3K86GEsGc8+87ZIyFrgE1Rca/Y1hD03Uk0s/Kpmi3hCybJwPIoB1WmO2Xz2US8xqzuefsX6UzRazFTQKlTCq5gTTkpNE5fJzS/WmvK7w79aoFJPmVBCXOSXkoe9uoi9a64OnsY0jF8ao7uOUJp84QIUyPRLuPXqlxXwZenqt5RKH6dXyw9tsV2Q3BvZwJwvStFjiQFIi2zIp5jmVcYxwqV4CTt7Ev0ybATE00YAfCoS5i2LJR+fquN9XkS4ay3p9qoZZW7Q4uujWfUUaSO/gYLiOTpbTOl4Smgzc+NvqFrUk1OxPttDSc=
|   256 0f:35:d1:a1:31:f2:f6:aa:75:e8:17:01:e7:1e:d1:d5 (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBOX6nl2HC2/Prh0l8uVsnAzinDT2+rhj1VasPM8Df3ntzgb8XzQat7zC/nHm0v7yLWo/CjpI6pD+mrBh3P/wuqk=
|   256 af:f1:53:ea:7b:4d:d7:fa:d8:de:0d:f2:28:fc:86:d7 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIBefJyPm1sjN+QedhTj6S1CPbXQZEFXb58RICJh970R8
80/tcp    open  http    syn-ack Apache httpd 2.4.41 ((Ubuntu))
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
|_http-server-header: Apache/2.4.41 (Ubuntu)
| http-robots.txt: 1 disallowed entry 
|_/secret.txt
|_http-generator: WordPress 5.4.2
|_http-title: OSCP Voucher &#8211; Just another WordPress site
33060/tcp open  mysqlx? syn-ack
| fingerprint-strings: 
|   DNSStatusRequestTCP, LDAPSearchReq, NotesRPC, SSLSessionReq, TLSSessionReq, X11Probe, afp: 
|     Invalid message"
|_    HY000
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port33060-TCP:V=7.94%I=7%D=10/31%Time=6540DD4C%P=x86_64-pc-linux-gnu%r(
SF:NULL,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(GenericLines,9,"\x05\0\0\0\x0b
SF:\x08\x05\x1a\0")%r(GetRequest,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(HTTPO
SF:ptions,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(RTSPRequest,9,"\x05\0\0\0\x0
SF:b\x08\x05\x1a\0")%r(RPCCheck,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(DNSVer
SF:sionBindReqTCP,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(DNSStatusRequestTCP,
SF:2B,"\x05\0\0\0\x0b\x08\x05\x1a\0\x1e\0\0\0\x01\x08\x01\x10\x88'\x1a\x0f
SF:Invalid\x20message\"\x05HY000")%r(Help,9,"\x05\0\0\0\x0b\x08\x05\x1a\0"
SF:)%r(SSLSessionReq,2B,"\x05\0\0\0\x0b\x08\x05\x1a\0\x1e\0\0\0\x01\x08\x0
SF:1\x10\x88'\x1a\x0fInvalid\x20message\"\x05HY000")%r(TerminalServerCooki
SF:e,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(TLSSessionReq,2B,"\x05\0\0\0\x0b\
SF:x08\x05\x1a\0\x1e\0\0\0\x01\x08\x01\x10\x88'\x1a\x0fInvalid\x20message\
SF:"\x05HY000")%r(Kerberos,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(SMBProgNeg,
SF:9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(X11Probe,2B,"\x05\0\0\0\x0b\x08\x05
SF:\x1a\0\x1e\0\0\0\x01\x08\x01\x10\x88'\x1a\x0fInvalid\x20message\"\x05HY
SF:000")%r(FourOhFourRequest,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(LPDString
SF:,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(LDAPSearchReq,2B,"\x05\0\0\0\x0b\x
SF:08\x05\x1a\0\x1e\0\0\0\x01\x08\x01\x10\x88'\x1a\x0fInvalid\x20message\"
SF:\x05HY000")%r(LDAPBindReq,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(SIPOption
SF:s,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(LANDesk-RC,9,"\x05\0\0\0\x0b\x08\
SF:x05\x1a\0")%r(TerminalServer,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(NCP,9,
SF:"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(NotesRPC,2B,"\x05\0\0\0\x0b\x08\x05\x
SF:1a\0\x1e\0\0\0\x01\x08\x01\x10\x88'\x1a\x0fInvalid\x20message\"\x05HY00
SF:0")%r(JavaRMI,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(WMSRequest,9,"\x05\0\
SF:0\0\x0b\x08\x05\x1a\0")%r(oracle-tns,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%
SF:r(ms-sql-s,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(afp,2B,"\x05\0\0\0\x0b\x
SF:08\x05\x1a\0\x1e\0\0\0\x01\x08\x01\x10\x88'\x1a\x0fInvalid\x20message\"
SF:\x05HY000")%r(giop,9,"\x05\0\0\0\x0b\x08\x05\x1a\0");
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

NSE: Script Post-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 06:56
Completed NSE at 06:56, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 06:56
Completed NSE at 06:56, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 06:56
Completed NSE at 06:56, 0.00s elapsed
Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 35.96 seconds
```
