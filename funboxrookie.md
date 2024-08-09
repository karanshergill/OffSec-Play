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

## FTP
```
> ftp 192.168.172.107
Connected to 192.168.172.107.
220 ProFTPD 1.3.5e Server (Debian) [::ffff:192.168.172.107]
Name (192.168.172.107:superuser): anonymous
331 Anonymous login ok, send your complete email address as your password
Password: 
230-Welcome, archive user anonymous@192.168.45.224 !
230-
230-The local time is: Fri Aug 09 06:01:26 2024
230-
230-This is an experimental FTP server.  If you have any unusual problems,
230-please report them via e-mail to <root@funbox2>.
230-
230 Anonymous access granted, restrictions apply
Remote system type is UNIX.
Using binary mode to transfer files.

ftp> ls
229 Entering Extended Passive Mode (|||65460|)
150 Opening ASCII mode data connection for file list
-rw-rw-r--   1 ftp      ftp          1477 Jul 25  2020 anna.zip
-rw-rw-r--   1 ftp      ftp          1477 Jul 25  2020 ariel.zip
-rw-rw-r--   1 ftp      ftp          1477 Jul 25  2020 bud.zip
-rw-rw-r--   1 ftp      ftp          1477 Jul 25  2020 cathrine.zip
-rw-rw-r--   1 ftp      ftp          1477 Jul 25  2020 homer.zip
-rw-rw-r--   1 ftp      ftp          1477 Jul 25  2020 jessica.zip
-rw-rw-r--   1 ftp      ftp          1477 Jul 25  2020 john.zip
-rw-rw-r--   1 ftp      ftp          1477 Jul 25  2020 marge.zip
-rw-rw-r--   1 ftp      ftp          1477 Jul 25  2020 miriam.zip
-r--r--r--   1 ftp      ftp          1477 Jul 25  2020 tom.zip
-rw-r--r--   1 ftp      ftp           170 Jan 10  2018 welcome.msg
-rw-rw-r--   1 ftp      ftp          1477 Jul 25  2020 zlatan.zip
226 Transfer complete
```

Download all zip files:
```shell
ftp> prompt
Interactive mode off.
ftp> mget *
```

```shell
ftp> prompt                                                                                                                                                    
Interactive mode off.                                                                                                                                          
ftp> mget *                                                                                                                                                    
local: jessica.zip remote: jessica.zip                                                                                                                         
229 Entering Extended Passive Mode (|||16029|)                                                                                                                 
150 Opening BINARY mode data connection for jessica.zip (1477 bytes)                                                                                           
100% |******************************************************************************************************************|  1477       32.01 MiB/s    00:00 ETA 
226 Transfer complete                                                                                                                                          
1477 bytes received in 00:00 (13.36 KiB/s)                                                                                                                     
local: bud.zip remote: bud.zip                                                                                                                                 
229 Entering Extended Passive Mode (|||27241|)                                                                                                                 
150 Opening BINARY mode data connection for bud.zip (1477 bytes)                                                                                               
100% |******************************************************************************************************************|  1477       23.87 MiB/s    00:00 ETA 
226 Transfer complete                                                                                                                                          
1477 bytes received in 00:00 (13.56 KiB/s)                                                                                                                     
local: marge.zip remote: marge.zip                                                                                                                             
229 Entering Extended Passive Mode (|||56148|)                                                                                                                 
150 Opening BINARY mode data connection for marge.zip (1477 bytes)                                                                                             
100% |******************************************************************************************************************|  1477       15.14 MiB/s    00:00 ETA
226 Transfer complete
1477 bytes received in 00:00 (13.85 KiB/s)
local: homer.zip remote: homer.zip
229 Entering Extended Passive Mode (|||24880|)
150 Opening BINARY mode data connection for homer.zip (1477 bytes)
100% |******************************************************************************************************************|  1477       32.01 MiB/s    00:00 ETA
226 Transfer complete
1477 bytes received in 00:00 (14.43 KiB/s)
local: john.zip remote: john.zip
229 Entering Extended Passive Mode (|||64341|)
150 Opening BINARY mode data connection for john.zip (1477 bytes)
100% |******************************************************************************************************************|  1477       27.61 MiB/s    00:00 ETA
226 Transfer complete
1477 bytes received in 00:00 (12.91 KiB/s)
local: cathrine.zip remote: cathrine.zip
229 Entering Extended Passive Mode (|||55034|)
150 Opening BINARY mode data connection for cathrine.zip (1477 bytes)
100% |******************************************************************************************************************|  1477      136.29 KiB/s    00:00 ETA
226 Transfer complete
1477 bytes received in 00:00 (13.02 KiB/s)
local: ariel.zip remote: ariel.zip
229 Entering Extended Passive Mode (|||25135|)
150 Opening BINARY mode data connection for ariel.zip (1477 bytes)
100% |******************************************************************************************************************|  1477       22.35 MiB/s    00:00 ETA
226 Transfer complete
1477 bytes received in 00:00 (13.90 KiB/s)
local: anna.zip remote: anna.zip
229 Entering Extended Passive Mode (|||25872|)
150 Opening BINARY mode data connection for anna.zip (1477 bytes)
100% |******************************************************************************************************************|  1477       30.62 MiB/s    00:00 ETA
226 Transfer complete
1477 bytes received in 00:00 (14.50 KiB/s)
local: welcome.msg remote: welcome.msg
229 Entering Extended Passive Mode (|||40133|)
150 Opening BINARY mode data connection for welcome.msg (170 bytes)
100% |******************************************************************************************************************|   170        1.19 MiB/s    00:00 ETA
226 Transfer complete
170 bytes received in 00:00 (1.63 KiB/s)
local: tom.zip remote: tom.zip
229 Entering Extended Passive Mode (|||10886|)
150 Opening BINARY mode data connection for tom.zip (1477 bytes)
100% |******************************************************************************************************************|  1477       36.11 MiB/s    00:00 ETA
226 Transfer complete
1477 bytes received in 00:00 (14.34 KiB/s)
local: zlatan.zip remote: zlatan.zip
229 Entering Extended Passive Mode (|||56847|)
150 Opening BINARY mode data connection for zlatan.zip (1477 bytes)
100% |******************************************************************************************************************|  1477       32.75 MiB/s    00:00 ETA
226 Transfer complete
1477 bytes received in 00:00 (13.80 KiB/s)
```

Crack downloaded .zip file:
```shell
for file in *zip; do
echo "Cracking $file..."
    fcrackzip -v -u -D -p /usr/share/wordlists/rockyou.txt "$file"
done
```
