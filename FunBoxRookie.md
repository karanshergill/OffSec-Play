# FunBoxRookie

```shell
> rustscan -b 1000 -u 5000 -r 0-65535 -a 192.168.172.107
.----. .-. .-. .----..---.  .----. .---.   .--.  .-. .-.
| {}  }| { } |{ {__ {_   _}{ {__  /  ___} / {} \ |  `| |
| .-. \| {_} |.-._} } | |  .-._} }\     }/  /\  \| |\  |
`-' `-'`-----'`----'  `-'  `----'  `---' `-'  `-'`-' `-'
The Modern Day Port Scanner.
________________________________________
: http://discord.skerritt.blog         :
: https://github.com/RustScan/RustScan :
 --------------------------------------
With RustScan, I scan ports so fast, even my firewall gets whiplash 💨

[~] The config file is expected to be at "/home/superuser/.rustscan.toml"
[~] Automatically increasing ulimit value to 5000.
Open 192.168.172.107:21
Open 192.168.172.107:22
Open 192.168.172.107:80
[~] Starting Script(s)
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2024-08-09 01:41 EDT
Initiating Ping Scan at 01:41
Scanning 192.168.172.107 [2 ports]
Completed Ping Scan at 01:41, 0.09s elapsed (1 total hosts)
Initiating Parallel DNS resolution of 1 host. at 01:41
Completed Parallel DNS resolution of 1 host. at 01:41, 0.00s elapsed
DNS resolution of 1 IPs took 0.00s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating Connect Scan at 01:41
Scanning 192.168.172.107 [3 ports]
Discovered open port 80/tcp on 192.168.172.107
Discovered open port 22/tcp on 192.168.172.107
Discovered open port 21/tcp on 192.168.172.107
Completed Connect Scan at 01:41, 0.10s elapsed (3 total ports)
Nmap scan report for 192.168.172.107
Host is up, received syn-ack (0.093s latency).
Scanned at 2024-08-09 01:41:35 EDT for 1s

PORT   STATE SERVICE REASON
21/tcp open  ftp     syn-ack
22/tcp open  ssh     syn-ack
80/tcp open  http    syn-ack

Read data files from: /usr/bin/../share/nmap
Nmap done: 1 IP address (1 host up) scanned in 0.31 seconds
```

```shell
> rustscan -b 1000 -u 5000 -r 0-65535 -a 192.168.172.107 -- -sC -sV                                                                                            
.----. .-. .-. .----..---.  .----. .---.   .--.  .-. .-.                                                                                                       
| {}  }| { } |{ {__ {_   _}{ {__  /  ___} / {} \ |  `| |                                                                                                       
| .-. \| {_} |.-._} } | |  .-._} }\     }/  /\  \| |\  |                                                                                                       
`-' `-'`-----'`----'  `-'  `----'  `---' `-'  `-'`-' `-'                                                                                                       
The Modern Day Port Scanner.                                                                                                                                   
________________________________________                                                                                                                       
: http://discord.skerritt.blog         :                                                                                                                       
: https://github.com/RustScan/RustScan :                                                                                                                       
 --------------------------------------                                                                                                                        
Open ports, closed hearts.                                                                                                                                     
                                                                                                                                                               
[~] The config file is expected to be at "/home/superuser/.rustscan.toml"                                                                                      
[~] Automatically increasing ulimit value to 5000.
Open 192.168.172.107:21                                                                                                                                        
Open 192.168.172.107:22                                                                                                                                        
Open 192.168.172.107:80                                                                                                                                        
[~] Starting Script(s)                                                                                                                                         
[>] Running script "nmap -vvv -p {{port}} {{ip}} -sC -sV" on ip 192.168.172.107                                                                                
Depending on the complexity of the script, results may take some time to appear.                                                                               
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2024-08-09 01:43 EDT                                                                                            
NSE: Loaded 156 scripts for scanning.                                                                                                                          
NSE: Script Pre-scanning.                                                                                                                                      
NSE: Starting runlevel 1 (of 3) scan.                                                                                                                          
Initiating NSE at 01:43                                                                                                                                        
Completed NSE at 01:43, 0.00s elapsed                                                                                                                          
NSE: Starting runlevel 2 (of 3) scan.                                                                                                                          
Initiating NSE at 01:43                                                                                                                                        
Completed NSE at 01:43, 0.00s elapsed                                                                                                                          
NSE: Starting runlevel 3 (of 3) scan.                                                                                                                          
Initiating NSE at 01:43                                                                                                                                        
Completed NSE at 01:43, 0.00s elapsed                                                                                                                          
Initiating Ping Scan at 01:43                                                                                                                                  
Scanning 192.168.172.107 [2 ports]                                                                                                                             
Completed Ping Scan at 01:43, 0.10s elapsed (1 total hosts)                                                                                                    
Initiating Parallel DNS resolution of 1 host. at 01:43                                                                                                         
Completed Parallel DNS resolution of 1 host. at 01:43, 0.01s elapsed                                                                                           
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]                                                               
Initiating Connect Scan at 01:43
Scanning 192.168.172.107 [3 ports]                                                                                                                             
Discovered open port 22/tcp on 192.168.172.107                                                                                                                 
Discovered open port 80/tcp on 192.168.172.107
Discovered open port 21/tcp on 192.168.172.107
Completed Connect Scan at 01:43, 0.10s elapsed (3 total ports)
Initiating Service scan at 01:43
Scanning 3 services on 192.168.172.107
Completed Service scan at 01:43, 6.20s elapsed (3 services on 1 host)
NSE: Script scanning 192.168.172.107.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 01:43
NSE: [ftp-bounce 192.168.172.107:21] PORT response: 500 Illegal PORT command
Completed NSE at 01:43, 3.13s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 01:43
Completed NSE at 01:43, 0.78s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 01:43
Completed NSE at 01:43, 0.00s elapsed
Nmap scan report for 192.168.172.107
Host is up, received syn-ack (0.097s latency).
Scanned at 2024-08-09 01:43:28 EDT for 11s

PORT   STATE SERVICE REASON  VERSION
21/tcp open  ftp     syn-ack ProFTPD 1.3.5e
| ftp-anon: Anonymous FTP login allowed (FTP code 230)
| -rw-rw-r--   1 ftp      ftp          1477 Jul 25  2020 anna.zip
| -rw-rw-r--   1 ftp      ftp          1477 Jul 25  2020 ariel.zip
| -rw-rw-r--   1 ftp      ftp          1477 Jul 25  2020 bud.zip
| -rw-rw-r--   1 ftp      ftp          1477 Jul 25  2020 cathrine.zip
| -rw-rw-r--   1 ftp      ftp          1477 Jul 25  2020 homer.zip
| -rw-rw-r--   1 ftp      ftp          1477 Jul 25  2020 jessica.zip
| -rw-rw-r--   1 ftp      ftp          1477 Jul 25  2020 john.zip
| -rw-rw-r--   1 ftp      ftp          1477 Jul 25  2020 marge.zip
| -rw-rw-r--   1 ftp      ftp          1477 Jul 25  2020 miriam.zip
| -r--r--r--   1 ftp      ftp          1477 Jul 25  2020 tom.zip
| -rw-r--r--   1 ftp      ftp           170 Jan 10  2018 welcome.msg
|_-rw-rw-r--   1 ftp      ftp          1477 Jul 25  2020 zlatan.zip
22/tcp open  ssh     syn-ack OpenSSH 7.6p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)
22/tcp open  ssh     syn-ack OpenSSH 7.6p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   2048 f9:46:7d:fe:0c:4d:a9:7e:2d:77:74:0f:a2:51:72:51 (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDMD7EHN/CpFOxv4hW16hSiL9/hrqfgN7N5gfqvnRwCeDJ8jj4kzV9XNVm/NN3u+fE7zrclQWDtGRu4oryuQv+25XjPJG7z+OdJ6ncD8k/VyHm3ncPIt1skZ
NTe8WGR9BGHf2dSvyEgW6Iu2TqICR+Vak48KdMIbmjCo8jbiAx4pNvUjkv7z+vzmr3wJakRhiIa2aA7TFeAVe5o9/Se6IOc/I4ByXcarmeU6hOytDb8qmUSYxSV1nea1jYKinXgCZ7MpAoFB8qPtiy4wryzBgss
jAiqAFPEmPjaU96hDAsGMeQ0yFLeCoDTxeY8xnc+oWjU/mm1ISbiJ/IqX2N81xtP
|   256 15:00:46:67:80:9b:40:12:3a:0c:66:07:db:1d:18:47 (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBHG2MCQtlbU+bwb4Cuz2xWoPH4/WBRJtUP5pDp8LQM175mj/IP9ORztHIBB+dyfrCshyxnFcIFc35MXp2qhgJ
FM=
|   256 75:ba:66:95:bb:0f:16:de:7e:7e:a1:7b:27:3b:b0:58 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIFhzTG7CoqPllLoboDB4lTrHUfFJLHbEWIRUP1lMA4rT
80/tcp open  http    syn-ack Apache httpd 2.4.29 ((Ubuntu))
|_http-title: Apache2 Ubuntu Default Page: It works
| http-methods: 
|_  Supported Methods: OPTIONS HEAD GET POST
|_http-server-header: Apache/2.4.29 (Ubuntu)
| http-robots.txt: 1 disallowed entry 
|_/logs/
Service Info: OSs: Unix, Linux; CPE: cpe:/o:linux:linux_kernel

NSE: Script Post-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 01:43
Completed NSE at 01:43, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 01:43
Completed NSE at 01:43, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 01:43
Completed NSE at 01:43, 0.00s elapsed
Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 10.90 seconds
```