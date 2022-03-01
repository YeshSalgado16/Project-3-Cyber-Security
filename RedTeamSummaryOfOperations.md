# Red Team: Summary of Operations

## Table of Contents
- Exposed Services
- Critical Vulnerabilities
- Exploitation

### Exposed Services
_TODO: Fill out the information below._

Nmap scan results for each machine reveal the below services and OS details:
```bash
$ nmap -sV 192.168.1.110  
```
![](Images/Project3NmapScan.png)  
This scan identifies the services below as potential points of entry:
- Target 1
  - List of Exposed Ports
    22/tcp
    80/tcp
    111/tcp
    139/tcp
    445/tcp
  - Exposed Services      VERSION
    open ssh              OpenSSH 6.7p1 Debian 5+deb8u4
    open http             Apache httpd 2.4.10 ((Debian))
    open rpcbind          2-4 (RPC #100000)
    open netbios-ssn      Samba smbd 3.X - 4.X (workgroup: WORKGROUP) 
    open netbios-ssn      Samba smbd 3.X - 4.X (workgroup: WORKGROUP)
_TODO: Fill out the list below. Include severity, and CVE numbers, if possible._

The following vulnerabilities were identified on each target:
- Target 1
  - List of
    open port 22 ssh
  - Critical
    high
  - Vulnerabilities
    weak passwords were exploited; such as Michael's password being michael and Steven's password being easily cracked by John The Ripper. 
    Identified the users Michael and Steven
    Michael contained the same password as username
    MySQL Server login contained the login credentials in wp-config.php file in plain text. 
    The user Steven was able to execute python code to escalate his priveleges to root.
_TODO: Include vulnerability scan results to prove the identified vulnerabilities.

### Exploitation
_TODO: Fill out the details below. Include screenshots where possible._

The Red Team was able to penetrate `Target 1` and retrieve the following confidential data:
- Target 1
  - `flag1.txt`: _TODO: Insert `flag1.txt` hash value_
![](Images/Flag1ScreenShot.png)
    - **Exploit Used**
      - _TODO: Identify the exploit used_
      - _TODO: Include the command run_ 
  - `flag2.txt`: _TODO: Insert `flag2.txt` hash value_
![](Images/Flag2ScreenShot.png)
    - **Exploit Used**
      - _TODO: Identify the exploit used_
      - _TODO: Include the command run_
