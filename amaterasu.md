# Amaterasu

```shell
> rustscan -b 1000 -u 5000 -r 0-65535 -a 192.168.241.249 -- -Pn
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
Real hackers hack time ⌛

[~] The config file is expected to be at "/home/superuser/.rustscan.toml"
[~] Automatically increasing ulimit value to 5000.
Open 192.168.241.249:21
Open 192.168.241.249:25022
Open 192.168.241.249:33414
Open 192.168.241.249:40080
[~] Starting Script(s)
[>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")

Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2023-10-12 08:26 EDT
Initiating Parallel DNS resolution of 1 host. at 08:26
Completed Parallel DNS resolution of 1 host. at 08:26, 0.01s elapsed
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating Connect Scan at 08:26
Scanning 192.168.241.249 [4 ports]
Discovered open port 21/tcp on 192.168.241.249
Discovered open port 25022/tcp on 192.168.241.249
Discovered open port 40080/tcp on 192.168.241.249
Discovered open port 33414/tcp on 192.168.241.249
Completed Connect Scan at 08:26, 0.15s elapsed (4 total ports)
Nmap scan report for 192.168.241.249
Host is up, received user-set (0.15s latency).
Scanned at 2023-10-12 08:26:41 EDT for 0s

PORT      STATE SERVICE REASON
21/tcp    open  ftp     syn-ack
25022/tcp open  unknown syn-ack
33414/tcp open  unknown syn-ack
40080/tcp open  unknown syn-ack

Read data files from: /usr/bin/../share/nmap
Nmap done: 1 IP address (1 host up) scanned in 0.20 seconds
```

```shell
> rustscan -u 5000 -p 21,25022,33414,40080 -a 192.168.241.249 -- -Pn -sCV
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
Please contribute more quotes to our GitHub https://github.com/rustscan/rustscan

[~] The config file is expected to be at "/home/superuser/.rustscan.toml"
[~] Automatically increasing ulimit value to 5000.
Open 192.168.241.249:40080
Open 192.168.241.249:33414
Open 192.168.241.249:25022
Open 192.168.241.249:21
[~] Starting Script(s)
[>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")

Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2023-10-12 08:31 EDT
NSE: Loaded 156 scripts for scanning.
NSE: Script Pre-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 08:31
Completed NSE at 08:31, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 08:31
Completed NSE at 08:31, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 08:31
Completed NSE at 08:31, 0.00s elapsed
Initiating Parallel DNS resolution of 1 host. at 08:31
Completed Parallel DNS resolution of 1 host. at 08:31, 0.01s elapsed
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating Connect Scan at 08:31
Scanning 192.168.241.249 [4 ports]
Discovered open port 21/tcp on 192.168.241.249
Discovered open port 40080/tcp on 192.168.241.249
Discovered open port 25022/tcp on 192.168.241.249
Discovered open port 33414/tcp on 192.168.241.249
Completed Connect Scan at 08:31, 0.15s elapsed (4 total ports)
Initiating Service scan at 08:31
Scanning 4 services on 192.168.241.249
Completed Service scan at 08:33, 93.38s elapsed (4 services on 1 host)
NSE: Script scanning 192.168.241.249.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 08:33
NSE: [ftp-bounce 192.168.241.249:21] PORT response: 500 Illegal PORT command.
NSE Timing: About 99.82% done; ETC: 08:33 (0:00:00 remaining)
Completed NSE at 08:33, 31.81s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 08:33
Completed NSE at 08:33, 1.21s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 08:33
Completed NSE at 08:33, 0.00s elapsed
Nmap scan report for 192.168.241.249
Host is up, received user-set (0.15s latency).
Scanned at 2023-10-12 08:31:40 EDT for 127s

PORT      STATE SERVICE REASON  VERSION
21/tcp    open  ftp     syn-ack vsftpd 3.0.3
| ftp-syst: 
|   STAT: 
| FTP server status:
|      Connected to 192.168.45.226
|      Logged in as ftp
|      TYPE: ASCII
|      No session bandwidth limit
|      Session timeout in seconds is 300
|      Control connection is plain text
|      Data connections will be plain text
|      At session startup, client count was 2
|      vsFTPd 3.0.3 - secure, fast, stable
|_End of status
| ftp-anon: Anonymous FTP login allowed (FTP code 230)
|_Can't get directory listing: TIMEOUT
25022/tcp open  ssh     syn-ack OpenSSH 8.6 (protocol 2.0)
| ssh-hostkey: 
|   256 68:c6:05:e8:dc:f2:9a:2a:78:9b:ee:a1:ae:f6:38:1a (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBD6xv/PZkusP5TZdYJWDT8TTNY2xojo5b2DU/zrXm1tP4kkjNCGmwq8UwFrjo5EbEbk3wMmgHBnE73XwgnqaPd4=
|   256 e9:89:cc:c2:17:14:f3:bc:62:21:06:4a:5e:71:80:ce (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIHRX3RvvSVPY3FJV9u7N2xIQbLJgQoEMkmRMey39/Jxz
33414/tcp open  unknown syn-ack
| fingerprint-strings: 
|   GetRequest, HTTPOptions: 
|     HTTP/1.1 404 NOT FOUND
|     Server: Werkzeug/2.2.3 Python/3.9.13
|     Date: Thu, 12 Oct 2023 12:31:48 GMT
|     Content-Type: text/html; charset=utf-8
|     Content-Length: 207
|     Connection: close
|     <!doctype html>
|     <html lang=en>
|     <title>404 Not Found</title>
|     <h1>Not Found</h1>
|     <p>The requested URL was not found on the server. If you entered the URL manually please check your spelling and try again.</p>
|   Help: 
|     <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
|     "http://www.w3.org/TR/html4/strict.dtd">
|     <html>
|     <head>
|     <meta http-equiv="Content-Type" content="text/html;charset=utf-8">
|     <title>Error response</title>
|     </head>
|     <body>
|     <h1>Error response</h1>
|     <p>Error code: 400</p>
|     <p>Message: Bad request syntax ('HELP').</p>
|     <p>Error code explanation: HTTPStatus.BAD_REQUEST - Bad request syntax or unsupported method.</p>
|     </body>
|     </html>
|   RTSPRequest: 
|     <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
|     "http://www.w3.org/TR/html4/strict.dtd">
|     <html>
|     <head>
|     <meta http-equiv="Content-Type" content="text/html;charset=utf-8">
|     <title>Error response</title>
|     </head>
|     <body>
|     <h1>Error response</h1>
|     <p>Error code: 400</p>
|     <p>Message: Bad request version ('RTSP/1.0').</p>
|     <p>Error code explanation: HTTPStatus.BAD_REQUEST - Bad request syntax or unsupported method.</p>
|     </body>
|_    </html>
40080/tcp open  http    syn-ack Apache httpd 2.4.53 ((Fedora))
|_http-server-header: Apache/2.4.53 (Fedora)
| http-methods: 
|   Supported Methods: GET POST OPTIONS HEAD TRACE
|_  Potentially risky methods: TRACE
|_http-title: My test page
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port33414-TCP:V=7.94%I=7%D=10/12%Time=6527E733%P=x86_64-pc-linux-gnu%r(
SF:GetRequest,184,"HTTP/1\.1\x20404\x20NOT\x20FOUND\r\nServer:\x20Werkzeug
SF:/2\.2\.3\x20Python/3\.9\.13\r\nDate:\x20Thu,\x2012\x20Oct\x202023\x2012
SF::31:48\x20GMT\r\nContent-Type:\x20text/html;\x20charset=utf-8\r\nConten
SF:t-Length:\x20207\r\nConnection:\x20close\r\n\r\n<!doctype\x20html>\n<ht
SF:ml\x20lang=en>\n<title>404\x20Not\x20Found</title>\n<h1>Not\x20Found</h
SF:1>\n<p>The\x20requested\x20URL\x20was\x20not\x20found\x20on\x20the\x20s
SF:erver\.\x20If\x20you\x20entered\x20the\x20URL\x20manually\x20please\x20
SF:check\x20your\x20spelling\x20and\x20try\x20again\.</p>\n")%r(HTTPOption
SF:s,184,"HTTP/1\.1\x20404\x20NOT\x20FOUND\r\nServer:\x20Werkzeug/2\.2\.3\
SF:x20Python/3\.9\.13\r\nDate:\x20Thu,\x2012\x20Oct\x202023\x2012:31:48\x2
SF:0GMT\r\nContent-Type:\x20text/html;\x20charset=utf-8\r\nContent-Length:
SF:\x20207\r\nConnection:\x20close\r\n\r\n<!doctype\x20html>\n<html\x20lan
SF:g=en>\n<title>404\x20Not\x20Found</title>\n<h1>Not\x20Found</h1>\n<p>Th
SF:e\x20requested\x20URL\x20was\x20not\x20found\x20on\x20the\x20server\.\x
SF:20If\x20you\x20entered\x20the\x20URL\x20manually\x20please\x20check\x20
SF:your\x20spelling\x20and\x20try\x20again\.</p>\n")%r(RTSPRequest,1F4,"<!
SF:DOCTYPE\x20HTML\x20PUBLIC\x20\"-//W3C//DTD\x20HTML\x204\.01//EN\"\n\x20
SF:\x20\x20\x20\x20\x20\x20\x20\"http://www\.w3\.org/TR/html4/strict\.dtd\
SF:">\n<html>\n\x20\x20\x20\x20<head>\n\x20\x20\x20\x20\x20\x20\x20\x20<me
SF:ta\x20http-equiv=\"Content-Type\"\x20content=\"text/html;charset=utf-8\
SF:">\n\x20\x20\x20\x20\x20\x20\x20\x20<title>Error\x20response</title>\n\
SF:x20\x20\x20\x20</head>\n\x20\x20\x20\x20<body>\n\x20\x20\x20\x20\x20\x2
SF:0\x20\x20<h1>Error\x20response</h1>\n\x20\x20\x20\x20\x20\x20\x20\x20<p
SF:>Error\x20code:\x20400</p>\n\x20\x20\x20\x20\x20\x20\x20\x20<p>Message:
SF:\x20Bad\x20request\x20version\x20\('RTSP/1\.0'\)\.</p>\n\x20\x20\x20\x2
SF:0\x20\x20\x20\x20<p>Error\x20code\x20explanation:\x20HTTPStatus\.BAD_RE
SF:QUEST\x20-\x20Bad\x20request\x20syntax\x20or\x20unsupported\x20method\.
SF:</p>\n\x20\x20\x20\x20</body>\n</html>\n")%r(Help,1EF,"<!DOCTYPE\x20HTM
SF:L\x20PUBLIC\x20\"-//W3C//DTD\x20HTML\x204\.01//EN\"\n\x20\x20\x20\x20\x
SF:20\x20\x20\x20\"http://www\.w3\.org/TR/html4/strict\.dtd\">\n<html>\n\x
SF:20\x20\x20\x20<head>\n\x20\x20\x20\x20\x20\x20\x20\x20<meta\x20http-equ
SF:iv=\"Content-Type\"\x20content=\"text/html;charset=utf-8\">\n\x20\x20\x
SF:20\x20\x20\x20\x20\x20<title>Error\x20response</title>\n\x20\x20\x20\x2
SF:0</head>\n\x20\x20\x20\x20<body>\n\x20\x20\x20\x20\x20\x20\x20\x20<h1>E
SF:rror\x20response</h1>\n\x20\x20\x20\x20\x20\x20\x20\x20<p>Error\x20code
SF::\x20400</p>\n\x20\x20\x20\x20\x20\x20\x20\x20<p>Message:\x20Bad\x20req
SF:uest\x20syntax\x20\('HELP'\)\.</p>\n\x20\x20\x20\x20\x20\x20\x20\x20<p>
SF:Error\x20code\x20explanation:\x20HTTPStatus\.BAD_REQUEST\x20-\x20Bad\x2
SF:0request\x20syntax\x20or\x20unsupported\x20method\.</p>\n\x20\x20\x20\x
SF:20</body>\n</html>\n");
Service Info: OS: Unix

NSE: Script Post-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 08:33
Completed NSE at 08:33, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 08:33
Completed NSE at 08:33, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 08:33
Completed NSE at 08:33, 0.00s elapsed
Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 126.89 seconds
```

```shell

```
