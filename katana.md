```
> rustscan -b 1000 -u 5000 -r 0-65535 -a 192.168.172.83 -- -Pn
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

```shell
> rustscan -u 5000 -p 21,22,80,7080,8088,8715 -a 192.168.172.83 -- -Pn -sCV
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
Open 192.168.172.83:80
Open 192.168.172.83:7080
Open 192.168.172.83:22
Open 192.168.172.83:8088
Open 192.168.172.83:8715
[~] Starting Script(s)
[>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")

Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2023-10-19 14:50 EDT
NSE: Loaded 156 scripts for scanning.
NSE: Script Pre-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 14:50
Completed NSE at 14:50, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 14:50
Completed NSE at 14:50, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 14:50
Completed NSE at 14:50, 0.00s elapsed
Initiating Parallel DNS resolution of 1 host. at 14:50
Completed Parallel DNS resolution of 1 host. at 14:50, 0.01s elapsed
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating Connect Scan at 14:50
Scanning 192.168.172.83 [6 ports]
Discovered open port 22/tcp on 192.168.172.83
Discovered open port 80/tcp on 192.168.172.83
Discovered open port 21/tcp on 192.168.172.83
Discovered open port 8715/tcp on 192.168.172.83
Discovered open port 8088/tcp on 192.168.172.83
Discovered open port 7080/tcp on 192.168.172.83
Completed Connect Scan at 14:50, 0.18s elapsed (6 total ports)
Initiating Service scan at 14:50
Scanning 6 services on 192.168.172.83
Completed Service scan at 14:51, 27.94s elapsed (6 services on 1 host)
NSE: Script scanning 192.168.172.83.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 14:51
Completed NSE at 14:51, 9.07s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 14:51
Completed NSE at 14:51, 2.29s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 14:51
Completed NSE at 14:51, 0.00s elapsed
Nmap scan report for 192.168.172.83
Host is up, received user-set (0.18s latency).
Scanned at 2023-10-19 14:50:41 EDT for 39s

PORT     STATE SERVICE        REASON  VERSION
21/tcp   open  ftp            syn-ack vsftpd 3.0.3
22/tcp   open  ssh            syn-ack OpenSSH 7.9p1 Debian 10+deb10u2 (protocol 2.0)
| ssh-hostkey: 
|   2048 89:4f:3a:54:01:f8:dc:b6:6e:e0:78:fc:60:a6:de:35 (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDp0J8d7K55SuQO/Uuh8GyKm2xlwCUG3/Jb6+7RlfgbwrCIOzuKXICcMHq4i8z52l/0x0JnN0GUIeNu6Ek/ZGEMK4y+zvAs0R6oPNlScpx0IaLDXTGrjPOcutmx+fy6WDW3/jJGLxwu+55d6pAjzzQR37P1eqH8k9F6fbv6YUFbU+i68x9p5bXCC1m17PDO98Che+q32N6yM26CrQMOl5t1OzO3t1pbvMd3VOQA8Qd+fhz5tpxtRBTSM9ylQj2B+z6XjJnbMPhnO3C1oaYHjjL6KiTfD5YabDqsBf+ZHIdZpM+7fOqKkgHa4bbIWPUXB/OuOJnORvEeRCALOzjcSrxr
|   256 dd:ac:cc:4e:43:81:6b:e3:2d:f3:12:a1:3e:4b:a3:22 (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBDBsZi0z31ChZ3SWO/gDe+8WyFVPrFX7KgZNp8u/1vlhOSrmdZ32WAZZhTT8bblwgv83FeXPvH7btjDMzTuoYA8=
|   256 cc:e6:25:c0:c6:11:9f:88:f6:c4:26:1e:de:fa:e9:8b (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAICo+dAzFw2csa366udGUkSre2W0qWWGoyWXwKiHk3YQc
80/tcp   open  http           syn-ack Apache httpd 2.4.38 ((Debian))
| http-methods: 
|_  Supported Methods: HEAD GET POST OPTIONS
|_http-server-header: Apache/2.4.38 (Debian)
|_http-title: Katana X
7080/tcp open  ssl/empoweri syn-ack LiteSpeed
|_http-server-header: LiteSpeed
| ssl-cert: Subject: commonName=katana/organizationName=webadmin/countryName=US/X509v3 Subject Alternative Name=DNS.1=1.55.254.232
| Issuer: commonName=katana/organizationName=webadmin/countryName=US/X509v3 Subject Alternative Name=DNS.1=1.55.254.232
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2020-05-11T13:57:36
| Not valid after:  2022-05-11T13:57:36
| MD5:   0443:4a65:9ba1:0b75:ea8d:d1b8:c855:e495
| SHA-1: f89e:f85e:e6b3:6b10:4ebc:5354:80a0:0ae3:7e10:50cc
| -----BEGIN CERTIFICATE-----
| MIIDfTCCAmWgAwIBAgIUAXyRP1qy58OWLRWfP6CNoErg93wwDQYJKoZIhvcNAQEL
| BQAwTjEPMA0GA1UEAwwGa2F0YW5hMREwDwYDVQQKDAh3ZWJhZG1pbjELMAkGA1UE
| BhMCVVMxGzAZBgNVHREMEkROUy4xPTEuNTUuMjU0LjIzMjAeFw0yMDA1MTExMzU3
| MzZaFw0yMjA1MTExMzU3MzZaME4xDzANBgNVBAMMBmthdGFuYTERMA8GA1UECgwI
| d2ViYWRtaW4xCzAJBgNVBAYTAlVTMRswGQYDVR0RDBJETlMuMT0xLjU1LjI1NC4y
| MzIwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQDUrg/knoyr6L8pJhlZ
| bEp2vj/1S/2lEiYzl3CbBtCDcNnSQLB2b7hC5vkzIFT5XOHcboXGSWWZ7g1Mlo/U
| irtoeuFYH0KyqYqKH6cJIUCUuIvsKFvEuSpcLB5oHMH1bNYHl8gk2uxnXDRHfxL1
| mhhV+tDewjGu7TzjWcGapvZmJKCQYJto6X4JagN/Xx7bWZQYKb22E/K/17PPg1Wg
| szg2C8a/sj/GWBiw5HADUx5FnQY0FfljwBBSQr10nGiex+w/NAYK8obUTsvUz1P7
| h2aG1V/9FtXHa6HK7YrApieVVTyBZTf4adj5OvmIT5w43vEBZXgCTUMLcf6JmiGy
| OMmdAgMBAAGjUzBRMB0GA1UdDgQWBBRpfqzDB3dS6IMabVgYjX+nQE8xZzAfBgNV
| HSMEGDAWgBRpfqzDB3dS6IMabVgYjX+nQE8xZzAPBgNVHRMBAf8EBTADAQH/MA0G
| CSqGSIb3DQEBCwUAA4IBAQCGCOYvcHj7XrE0fnuDbc4rdQzSVOCOK31F4aV4pWEh
| a6h/WQX9wQBHcs5XPl9D4JVDFQvtxBPWsmnzqqXm8CbeZ7cfAjzPGd994jFBeom6
| 3gnAXmCFSlRsPuqvKkGhBaSDDtzrWE4eZC0H2g9BJp0f6w4sRJSjCH1wZ30Jvgm+
| 9Hkcw9cG0WxkHEBk3SPB7d9iG6rFLJvZE4dcVbA6jtkhQZDrCAqaH69exWtKSQpV
| oBu7+tHFy/8uv7yRuC4fQY7Nmc0JD5otoax1yOpGN/eSz8zRFh+jl5VzdONtXQCO
| H8o8x5fxVi65kRQYil6UcG3lX56V51h/33dxWIDw+lAE
|_-----END CERTIFICATE-----
|_http-title: Did not follow redirect to https://192.168.172.83:7080/
| tls-alpn: 
|   h2
|   spdy/3
|   spdy/2
|_  http/1.1
| http-methods: 
|_  Supported Methods: GET HEAD POST
|_ssl-date: TLS randomness does not represent time
8088/tcp open  http           syn-ack LiteSpeed httpd
|_http-title: Katana X
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
|_http-server-header: LiteSpeed
8715/tcp open  http           syn-ack nginx 1.14.2
|_http-title: 401 Authorization Required
| http-auth: 
| HTTP/1.1 401 Unauthorized\x0D
|_  Basic realm=Restricted Content
|_http-server-header: nginx/1.14.2
Service Info: OSs: Unix, Linux; CPE: cpe:/o:linux:linux_kernel

NSE: Script Post-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 14:51
Completed NSE at 14:51, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 14:51
Completed NSE at 14:51, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 14:51
Completed NSE at 14:51, 0.00s elapsed
Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 39.75 seconds

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
 ___  ___  __   __     __      __         __   ___
|__  |__  |__) |__) | /  `    /  \ \_/ | |  \ |__
|    |___ |  \ |  \ | \__,    \__/ / \ | |__/ |___
by Ben "epi" Risher 🤓                 ver: 2.10.0
───────────────────────────┬──────────────────────
 🎯  Target Url            │ http://192.168.172.83
 🚀  Threads               │ 50
 📖  Wordlist              │ /usr/share/wordlists/seclists/Discovery/Web-Content/directory-list-2.3-small.txt
 👌  Status Codes          │ All Status Codes!
 💥  Timeout (secs)        │ 7
 🦡  User-Agent            │ Random
 💉  Config File           │ /etc/feroxbuster/ferox-config.toml
 🏁  HTTP methods          │ [GET]
 🚫  Do Not Recurse        │ true
───────────────────────────┴──────────────────────
 🏁  Press [ENTER] to use the Scan Management Menu™
──────────────────────────────────────────────────
404      GET        9l       31w      276c Auto-filtering found 404-like response and created new filter; toggle off with --dont-filter
403      GET        9l       28w      279c Auto-filtering found 404-like response and created new filter; toggle off with --dont-filter
200      GET       23l       73w      655c http://192.168.172.83/
301      GET        9l       28w      316c http://192.168.172.83/ebook => http://192.168.172.83/ebook/
[####################] - 5m     87650/87650   0s      found:2       errors:0      
[####################] - 5m     87650/87650   275/s   http://192.168.172.83/   
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

```shell
> searchsploit cse bookstore
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/1e77690b-9c36-45fa-9f6f-0a7da4cf270d)


TCP-8088/HTTP
```http

```
