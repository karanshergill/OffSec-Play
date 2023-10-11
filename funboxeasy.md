# FunboxEasy

```shell
> rustscan -b 1000 -u 5000 -r 0-65535 -a 192.168.196.111 -- -Pn
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
Open 192.168.196.111:22
Open 192.168.196.111:80
Open 192.168.196.111:33060
[~] Starting Script(s)
[>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")

Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2023-10-11 06:43 EDT
Initiating Parallel DNS resolution of 1 host. at 06:43
Completed Parallel DNS resolution of 1 host. at 06:43, 0.01s elapsed
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating Connect Scan at 06:43
Scanning 192.168.196.111 [3 ports]
Discovered open port 80/tcp on 192.168.196.111
Discovered open port 33060/tcp on 192.168.196.111
Discovered open port 22/tcp on 192.168.196.111
Completed Connect Scan at 06:43, 1.94s elapsed (3 total ports)
Nmap scan report for 192.168.196.111
Host is up, received user-set (0.16s latency).
Scanned at 2023-10-11 06:43:13 EDT for 2s

PORT      STATE SERVICE REASON
22/tcp    open  ssh     syn-ack
80/tcp    open  http    syn-ack
33060/tcp open  mysqlx  syn-ack

Read data files from: /usr/bin/../share/nmap
Nmap done: 1 IP address (1 host up) scanned in 2.00 seconds
```

```shell
> rustscan -u 5000 -p 22,80,33060 -a 192.168.196.111 -- -Pn -sCV
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
Open 192.168.196.111:33060
Open 192.168.196.111:80
Open 192.168.196.111:22
[~] Starting Script(s)
[>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")

Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2023-10-11 06:48 EDT
NSE: Loaded 156 scripts for scanning.
NSE: Script Pre-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 06:48
Completed NSE at 06:48, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 06:48
Completed NSE at 06:48, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 06:48
Completed NSE at 06:48, 0.00s elapsed
Initiating Parallel DNS resolution of 1 host. at 06:48
Completed Parallel DNS resolution of 1 host. at 06:48, 0.01s elapsed
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating Connect Scan at 06:48
Scanning 192.168.196.111 [3 ports]
Discovered open port 80/tcp on 192.168.196.111
Discovered open port 22/tcp on 192.168.196.111
Discovered open port 33060/tcp on 192.168.196.111
Completed Connect Scan at 06:48, 0.16s elapsed (3 total ports)
Initiating Service scan at 06:48
Scanning 3 services on 192.168.196.111
Completed Service scan at 06:49, 72.91s elapsed (3 services on 1 host)
NSE: Script scanning 192.168.196.111.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 06:49
Completed NSE at 06:49, 17.01s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 06:49
Completed NSE at 06:49, 1.44s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 06:49
Completed NSE at 06:49, 0.00s elapsed
Nmap scan report for 192.168.196.111
Host is up, received user-set (0.16s latency).
Scanned at 2023-10-11 06:48:08 EDT for 91s

PORT      STATE SERVICE REASON  VERSION
22/tcp    open  ssh     syn-ack OpenSSH 8.2p1 Ubuntu 4ubuntu0.1 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   3072 b2:d8:51:6e:c5:84:05:19:08:eb:c8:58:27:13:13:2f (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQDBFf9aHhJU3GLUWqDvIV38olRMjbK+4e5i8pnIvPF9Qwn+ENXGyYDnDkzX0ZtH4B47hLgn9YNyI42G93vImly3EkYAfcOqoVLod8LkoofwfE++CXozZqV/itluReYeTJUqdS3kVartO4BP0E95qkTcX9DgdSxA8FsYlZqo7Y9sBW/ZuM6sQKwjQj24UvoCTa6XypoGb7CYm0+cmcUb0Z8sD934oLyhfBJUrTZW9/pJ/Cv7+l4BVBASwNHgdJd36aa7ktGRh6eq4cxgVU4lWNAONKzzSyusK1R4xZYDzACCMBM8RRLbTB9Q2lz/LzZOrMi/sFFvUrDVMIblUUZyoCr6eSPhq1spSrSEkG6im2yPRMT/VyNgnslr99m3peVLPG6hQxqaKfuImfNTF8OE8iPB7kbGnGxfX6eH39Jyhy0+bTqa4vMuhwvFZXiXRIeHVdtfmNK3tQ+Rl7V+3NELpVw0AJ3ZTSuqN8N1FagoEHrLmtScwHsrjGjv1gNoOr5VNMU=
|   256 b0:de:97:03:a7:2f:f4:e2:ab:4a:9c:d9:43:9b:8a:48 (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBBj3AVqceVrNYPKcj93yFU/eGll7QOs4iCDa6gan7lG6NzelFXpcJU7yWo4Jw/CGTKWryHjUnt//0/uu7c3Qs8g=
|   256 9d:0f:9a:26:38:4f:01:80:a7:a6:80:9d:d1:d4:cf:ec (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAICvJsP8vRVvuxGvwmEbZzieFB8s+azVy6fwOOQToDJ8I
80/tcp    open  http    syn-ack Apache httpd 2.4.41
| http-robots.txt: 1 disallowed entry 
|_gym
|_http-server-header: Apache/2.4.41 (Ubuntu)
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
33060/tcp open  mysqlx? syn-ack
| fingerprint-strings: 
|   DNSStatusRequestTCP, LDAPSearchReq, NotesRPC, SSLSessionReq, TLSSessionReq, X11Probe: 
|     Invalid message"
|_    HY000
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port33060-TCP:V=7.94%I=7%D=10/11%Time=65267D6E%P=x86_64-pc-linux-gnu%r(
SF:NULL,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(GenericLines,9,"\x05\0\0\0\x0b
SF:\x08\x05\x1a\0")%r(HTTPOptions,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(RTSP
SF:Request,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(RPCCheck,9,"\x05\0\0\0\x0b\
SF:x08\x05\x1a\0")%r(DNSVersionBindReqTCP,9,"\x05\0\0\0\x0b\x08\x05\x1a\0"
SF:)%r(DNSStatusRequestTCP,2B,"\x05\0\0\0\x0b\x08\x05\x1a\0\x1e\0\0\0\x01\
SF:x08\x01\x10\x88'\x1a\x0fInvalid\x20message\"\x05HY000")%r(Help,9,"\x05\
SF:0\0\0\x0b\x08\x05\x1a\0")%r(SSLSessionReq,2B,"\x05\0\0\0\x0b\x08\x05\x1
SF:a\0\x1e\0\0\0\x01\x08\x01\x10\x88'\x1a\x0fInvalid\x20message\"\x05HY000
SF:")%r(TerminalServerCookie,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(TLSSessio
SF:nReq,2B,"\x05\0\0\0\x0b\x08\x05\x1a\0\x1e\0\0\0\x01\x08\x01\x10\x88'\x1
SF:a\x0fInvalid\x20message\"\x05HY000")%r(Kerberos,9,"\x05\0\0\0\x0b\x08\x
SF:05\x1a\0")%r(SMBProgNeg,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(X11Probe,2B
SF:,"\x05\0\0\0\x0b\x08\x05\x1a\0\x1e\0\0\0\x01\x08\x01\x10\x88'\x1a\x0fIn
SF:valid\x20message\"\x05HY000")%r(FourOhFourRequest,9,"\x05\0\0\0\x0b\x08
SF:\x05\x1a\0")%r(LPDString,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(LDAPSearch
SF:Req,2B,"\x05\0\0\0\x0b\x08\x05\x1a\0\x1e\0\0\0\x01\x08\x01\x10\x88'\x1a
SF:\x0fInvalid\x20message\"\x05HY000")%r(LDAPBindReq,9,"\x05\0\0\0\x0b\x08
SF:\x05\x1a\0")%r(SIPOptions,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(LANDesk-R
SF:C,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(TerminalServer,9,"\x05\0\0\0\x0b\
SF:x08\x05\x1a\0")%r(NCP,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(NotesRPC,2B,"
SF:\x05\0\0\0\x0b\x08\x05\x1a\0\x1e\0\0\0\x01\x08\x01\x10\x88'\x1a\x0fInva
SF:lid\x20message\"\x05HY000");
Service Info: Host: 127.0.1.1; OS: Linux; CPE: cpe:/o:linux:linux_kernel

NSE: Script Post-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 06:49
Completed NSE at 06:49, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 06:49
Completed NSE at 06:49, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 06:49
Completed NSE at 06:49, 0.00s elapsed
Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 91.76 seconds
```

TCP 80 - HTTP
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/56b386c2-5a59-4626-ab8e-3c16af480094)

