```
> rustscan -b 1000 -u 5000 -r 0-65535 -a 192.168.166.217 -- -Pn
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
Open 192.168.166.217:22
Open 192.168.166.217:80
[~] Starting Script(s)
[>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")

Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2023-11-04 07:17 EDT
Initiating Parallel DNS resolution of 1 host. at 07:17
Completed Parallel DNS resolution of 1 host. at 07:17, 0.01s elapsed
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating Connect Scan at 07:17
Scanning 192.168.166.217 [2 ports]
Discovered open port 22/tcp on 192.168.166.217
Discovered open port 80/tcp on 192.168.166.217
Completed Connect Scan at 07:17, 0.15s elapsed (2 total ports)
Nmap scan report for 192.168.166.217
Host is up, received user-set (0.15s latency).
Scanned at 2023-11-04 07:17:50 EDT for 0s

PORT   STATE SERVICE REASON
22/tcp open  ssh     syn-ack
80/tcp open  http    syn-ack

Read data files from: /usr/bin/../share/nmap
Nmap done: 1 IP address (1 host up) scanned in 0.21 seconds
```

```
> rustscan -u 5000 -p 22,80 -a 192.168.166.217 -- -Pn -sCV
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
Open 192.168.166.217:22
Open 192.168.166.217:80
[~] Starting Script(s)
[>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")

Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2023-11-04 07:19 EDT
NSE: Loaded 156 scripts for scanning.
NSE: Script Pre-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 07:19
Completed NSE at 07:19, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 07:19
Completed NSE at 07:19, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 07:19
Completed NSE at 07:19, 0.00s elapsed
Initiating Parallel DNS resolution of 1 host. at 07:19
Completed Parallel DNS resolution of 1 host. at 07:19, 0.01s elapsed
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating Connect Scan at 07:19
Scanning 192.168.166.217 [2 ports]
Discovered open port 80/tcp on 192.168.166.217
Discovered open port 22/tcp on 192.168.166.217
Completed Connect Scan at 07:19, 0.15s elapsed (2 total ports)
Initiating Service scan at 07:19
Scanning 2 services on 192.168.166.217
Completed Service scan at 07:19, 6.31s elapsed (2 services on 1 host)
NSE: Script scanning 192.168.166.217.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 07:19
Completed NSE at 07:19, 4.39s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 07:19
Completed NSE at 07:19, 0.60s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 07:19
Completed NSE at 07:19, 0.00s elapsed
Nmap scan report for 192.168.166.217
Host is up, received user-set (0.15s latency).
Scanned at 2023-11-04 07:19:04 EDT for 12s

PORT   STATE SERVICE REASON  VERSION
22/tcp open  ssh     syn-ack OpenSSH 7.2p2 Ubuntu 4ubuntu2.10 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   2048 95:1d:82:8f:5e:de:9a:00:a8:07:39:bd:ac:ad:d3:44 (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQCxOfkU+Q4dfPLCyiHlcl3+Rl8fCPL9YJ7GzzYAG8Vl75YbD21HXms6zE8KDBFuMu34+hvYCGxHIZVtZRMf9MFHdamqdx4YC++ZU7EFYy4eSQjPSukpIZOz4S4md5AmMFNucvvVOq9XVhWnxy86WSZzLO62y7ygqjG6w3sIXlrOjalqCUVgD60wnk53PW6Etkr6kpJwtrBXl60I6LOrb8hmTO63copeWbcYwi4OhlYAKV9EJjAFl9OohQX7uTR7uzoYPwaztG2HGQw/LQEQeV6KAfL+cb5QQMnP3ZW3r/nMKKZW3zw5h20sVaeoNcgVZ9ANv3EvldJqrRRG/R1wYJHV
|   256 d7:b4:52:a2:c8:fa:b7:0e:d1:a8:d0:70:cd:6b:36:90 (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBE6ost/PYmYfXkZxdW+XZSdvrXfTYifdCxxeASUc4llXCR9sRC0lxNP0AnjWlQq+xnAg95xDHNYSsNoPDaaqgHE=
|   256 df:f2:4f:77:33:44:d5:93:d7:79:17:45:5a:a1:36:8b (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAICNUmat0TujFtlTGYNCBEuh1P+MbsML6IJihp6I7mERS
80/tcp open  http    syn-ack Apache httpd 2.4.18 ((Ubuntu))
|_http-title: Blogger | Home
|_http-server-header: Apache/2.4.18 (Ubuntu)
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

NSE: Script Post-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 07:19
Completed NSE at 07:19, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 07:19
Completed NSE at 07:19, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 07:19
Completed NSE at 07:19, 0.00s elapsed
Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 11.70 seconds
```

```
http://192.168.166.217
```
![image](https://github.com/karanshergill/OffSec-Play-Labs/assets/83878909/f594e337-5d4f-4246-a85e-6380a16f9c5f)

Content Discovery
```
> feroxbuster -u http://192.168.166.217 -w /usr/share/seclists/Discovery/Web-Content/directory-list-2.3-small.txt --no-recursion --dont-extract-links --random-agent --filter-status 404 --redirects
```
```
 ___  ___  __   __     __      __         __   ___
|__  |__  |__) |__) | /  `    /  \ \_/ | |  \ |__
|    |___ |  \ |  \ | \__,    \__/ / \ | |__/ |___
by Ben "epi" Risher 🤓                 ver: 2.10.0
───────────────────────────┬──────────────────────
 🎯  Target Url            │ http://192.168.166.217
 🚀  Threads               │ 50
 📖  Wordlist              │ /usr/share/seclists/Discovery/Web-Content/directory-list-2.3-small.txt
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
403      GET        9l       28w      280c Auto-filtering found 404-like response and created new filter; toggle off with --dont-filter
404      GET        9l       31w      277c Auto-filtering found 404-like response and created new filter; toggle off with --dont-filter
200      GET      986l     2382w    46199c http://192.168.166.217/
200      GET       19l       93w     1504c http://192.168.166.217/assets/
200      GET       23l      125w     2366c http://192.168.166.217/css/
200      GET       35l      241w     4668c http://192.168.166.217/images/
200      GET       24l      141w     2627c http://192.168.166.217/js/
[####################] - 5m     87650/87650   0s      found:5       errors:5      
[####################] - 5m     87650/87650   323/s   http://192.168.166.217/
```
![image](https://github.com/karanshergill/OffSec-Play-Labs/assets/83878909/8cd69a32-e255-48ec-aecb-19ff561dbaa0)
![image](https://github.com/karanshergill/OffSec-Play-Labs/assets/83878909/e6dd38d7-1204-4ad2-ba2f-b51378f7026c)
![image](https://github.com/karanshergill/OffSec-Play-Labs/assets/83878909/e50d60df-42f4-4628-b6ca-cd30f02818eb)

WP Scan
```
> wpscan --url http://192.168.166.217/assets/fonts/blog --plugins-detection aggressive --random-user-agent
```
```
_______________________________________________________________
         __          _______   _____
         \ \        / /  __ \ / ____|
          \ \  /\  / /| |__) | (___   ___  __ _ _ __ ®
           \ \/  \/ / |  ___/ \___ \ / __|/ _` | '_ \
            \  /\  /  | |     ____) | (__| (_| | | | |
             \/  \/   |_|    |_____/ \___|\__,_|_| |_|

         WordPress Security Scanner by the WPScan Team
                         Version 3.8.25
       Sponsored by Automattic - https://automattic.com/
       @_WPScan_, @ethicalhack3r, @erwan_lr, @firefart
_______________________________________________________________

[+] URL: http://192.168.166.217/assets/fonts/blog/ [192.168.166.217]
[+] Started: Sat Nov  4 07:32:53 2023

Interesting Finding(s):

[+] Headers
 | Interesting Entry: Server: Apache/2.4.18 (Ubuntu)
 | Found By: Headers (Passive Detection)
 | Confidence: 100%

[+] XML-RPC seems to be enabled: http://192.168.166.217/assets/fonts/blog/xmlrpc.php
 | Found By: Direct Access (Aggressive Detection)
 | Confidence: 100%
 | References:
 |  - http://codex.wordpress.org/XML-RPC_Pingback_API
 |  - https://www.rapid7.com/db/modules/auxiliary/scanner/http/wordpress_ghost_scanner/
 |  - https://www.rapid7.com/db/modules/auxiliary/dos/http/wordpress_xmlrpc_dos/
 |  - https://www.rapid7.com/db/modules/auxiliary/scanner/http/wordpress_xmlrpc_login/
 |  - https://www.rapid7.com/db/modules/auxiliary/scanner/http/wordpress_pingback_access/

[+] WordPress readme found: http://192.168.166.217/assets/fonts/blog/readme.html
 | Found By: Direct Access (Aggressive Detection)
 | Confidence: 100%

[+] Upload directory has listing enabled: http://192.168.166.217/assets/fonts/blog/wp-content/uploads/
 | Found By: Direct Access (Aggressive Detection)
 | Confidence: 100%

[+] The external WP-Cron seems to be enabled: http://192.168.166.217/assets/fonts/blog/wp-cron.php
 | Found By: Direct Access (Aggressive Detection)
 | Confidence: 60%
 | References:
 |  - https://www.iplocation.net/defend-wordpress-from-ddos
 |  - https://github.com/wpscanteam/wpscan/issues/1299

[+] WordPress version 4.9.8 identified (Insecure, released on 2018-08-02).
 | Found By: Emoji Settings (Passive Detection)
 |  - http://192.168.166.217/assets/fonts/blog/, Match: 'wp-includes\/js\/wp-emoji-release.min.js?ver=4.9.8'
 | Confirmed By: Meta Generator (Passive Detection)
 |  - http://192.168.166.217/assets/fonts/blog/, Match: 'WordPress 4.9.8'

[i] The main theme could not be detected.

[+] Enumerating All Plugins (via Aggressive Methods)
 Checking Known Locations - Time: 00:55:22 <=========================================================> (103860 / 103860) 100.00% Time: 00:55:22
[+] Checking Plugin Versions (via Passive and Aggressive Methods)

[i] Plugin(s) Identified:

[+] akismet
 | Location: http://192.168.166.217/assets/fonts/blog/wp-content/plugins/akismet/
 | Last Updated: 2023-09-13T20:24:00.000Z
 | Readme: http://192.168.166.217/assets/fonts/blog/wp-content/plugins/akismet/readme.txt
 | [!] The version is out of date, the latest version is 5.3
 |
 | Found By: Known Locations (Aggressive Detection)
 |  - http://192.168.166.217/assets/fonts/blog/wp-content/plugins/akismet/, status: 200
 |
 | Version: 4.0.8 (100% confidence)
 | Found By: Readme - Stable Tag (Aggressive Detection)
 |  - http://192.168.166.217/assets/fonts/blog/wp-content/plugins/akismet/readme.txt
 | Confirmed By: Readme - ChangeLog Section (Aggressive Detection)
 |  - http://192.168.166.217/assets/fonts/blog/wp-content/plugins/akismet/readme.txt

[+] wpdiscuz
 | Location: http://192.168.166.217/assets/fonts/blog/wp-content/plugins/wpdiscuz/
 | Last Updated: 2023-10-31T16:29:00.000Z
 | Readme: http://192.168.166.217/assets/fonts/blog/wp-content/plugins/wpdiscuz/readme.txt
 | [!] The version is out of date, the latest version is 7.6.12
 |
 | Found By: Known Locations (Aggressive Detection)
 |  - http://192.168.166.217/assets/fonts/blog/wp-content/plugins/wpdiscuz/, status: 200
 |
 | Version: 7.0.4 (80% confidence)
 | Found By: Readme - Stable Tag (Aggressive Detection)
 |  - http://192.168.166.217/assets/fonts/blog/wp-content/plugins/wpdiscuz/readme.txt

[+] Enumerating Config Backups (via Passive and Aggressive Methods)
 Checking Config Backups - Time: 00:00:04 <================================================================> (137 / 137) 100.00% Time: 00:00:04

[i] No Config Backups Found.

[!] No WPScan API Token given, as a result vulnerability data has not been output.
[!] You can get a free API token with 25 daily requests by registering at https://wpscan.com/register

[+] Finished: Sat Nov  4 08:28:37 2023
[+] Requests Done: 104033
[+] Cached Requests: 7
[+] Data Sent: 35.863 MB
[+] Data Received: 14.059 MB
[+] Memory used: 389.453 MB
[+] Elapsed time: 00:55:43
```
