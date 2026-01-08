# Linux Luminarium

## Module 7: Shell Variables

### Printing Variables

Solution: used echo with a $ before the variable name to print it out 

Terminal: 
```bash
hacker@variables~printing-variables:~$ echo $FLAG
pwn.college{0gLwfsscpGQbEUdZ7qrt3iKDGmt.QX3UTN0wiM1IzNxEzW}
```
Flag: 
pwn.college{0gLwfsscpGQbEUdZ7qrt3iKDGmt.QX3UTN0wiM1IzNxEzW}

### Setting Variables

Solution: simply set the variable equal to the value mentioned

Terminal: 
```bash
hacker@variables~setting-variables:~$ PWN="COLLEGE"
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{c1tIdTUsLfYxEUtTi4eCqFpsSbR.QX5UTN0wiM1IzNxEzW}
```
Flag: 
pwn.college{c1tIdTUsLfYxEUtTi4eCqFpsSbR.QX5UTN0wiM1IzNxEzW}

### Multi-word Variables

Solution: used quotes to pass multiple words as variable value

Terminal: 
```bash
hacker@variables~multi-word-variables:~$ PWN="COLLEGE YEAH"
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{8tZHWseL6Zt2LglGUqb2WcQUWoj.QXwYTN0wiM1IzNxEzW}
```
Flag: 
pwn.college{8tZHWseL6Zt2LglGUqb2WcQUWoj.QXwYTN0wiM1IzNxEzW}

### Exporting Variables

Solution: used export correctly to set one variable to a value and export, similarly for the second but without exporting. then used them as arguments to /challenge/run

Terminal: 
```bash
hacker@variables~exporting-variables:~$ export PWN="COLLEGE"
You've set the PWN variable to the proper value!
hacker@variables~exporting-variables:~$ COLLEGE="PWN"
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ /challenge/run PWN COLLEGE
CORRECT!
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great
job! Here is your flag:
pwn.college{st0P-j9z39ByN2uLE0uPsA0D9Yy.QXyYTN0wiM1IzNxEzW}
```
Flag: 
pwn.college{st0P-j9z39ByN2uLE0uPsA0D9Yy.QXyYTN0wiM1IzNxEzW}

### Printing Exported Variables

Solution: used env to list all exported vars

Terminal: 
```bash
hacker@variables~printing-exported-variables:~$ env
SHELL=/run/dojo/bin/bash
HOSTNAME=variables~printing-exported-variables
PWD=/home/hacker
MANPATH=/run/dojo/share/man:
DOJO_AUTH_TOKEN=d68ffd78fcae91ee876c642474646d5316e94412bf7b18a79bbba17aaa5b4a3f
HOME=/home/hacker
LANG=C.UTF-8
FLAG=pwn.college{gwbqwyMglppvLRnTevsOSHkuiF1.QX4UTN0wiM1IzNxEzW}
TERMINFO=/run/dojo/share/terminfo
TERM=xterm-256color
SHLVL=2
LC_CTYPE=C.UTF-8
SSL_CERT_FILE=/run/dojo/etc/ssl/certs/ca-bundle.crt
PATH=/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
DEBIAN_FRONTEND=noninteractive
_=/run/dojo/bin/env
```
Flag: 
pwn.college{gwbqwyMglppvLRnTevsOSHkuiF1.QX4UTN0wiM1IzNxEzW}

### Storing Command Output

Solution: used command substitution to store output of /challenge/run in a var

Terminal: 
```bash
hacker@variables~storing-command-output:~$ PWN=$(/challenge/run)
Congratulations! You have read the flag into the PWN variable. Now print it out
and submit it!
hacker@variables~storing-command-output:~$ echo $PWN
pwn.college{g_txsYiSCD1oBGcI3gPS2i_fu7J.QX1cDN1wiM1IzNxEzW}
```
Flag: 
pwn.college{g_txsYiSCD1oBGcI3gPS2i_fu7J.QX1cDN1wiM1IzNxEzW}

### Reading Input

Solution: used read to give user input

Terminal: 
```bash
hacker@variables~reading-input:~$ read PWN
COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{wkMDnQZdJ2PqbOkkgwgzv3ZQHif.QX4cTN0wiM1IzNxEzW}
```
Flag: 
pwn.college{wkMDnQZdJ2PqbOkkgwgzv3ZQHif.QX4cTN0wiM1IzNxEzW}

### Reading Files

Solution: used read to read a file into the stdin

Terminal: 
```bash
hacker@variables~reading-files:~$ read PWN < /challenge/read_me
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{4S2xIToPQLNWhDWllY41ePH6rO7.QXwIDO0wiM1IzNxEzW}
```
Flag: 
pwn.college{4S2xIToPQLNWhDWllY41ePH6rO7.QXwIDO0wiM1IzNxEzW}
