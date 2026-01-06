# Linux Luminarium

## Module 8: Data Manipulation

### Translating characters

Solution: used tr to swap case of all chars

Terminal: 
```bash
hacker@data~translating-characters:~$ /challenge/run | tr ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ
yOUR CASE-SWAPPED FLAG:
pwn.college{EcCKAA7bzCNrcqB3LQay4umu6G_.01MxEzNxwiM1IzNxEzW}
```
Flag: 
pwn.college{EcCKAA7bzCNrcqB3LQay4umu6G_.01MxEzNxwiM1IzNxEzW}

### Deleting characters

Solution: simply deleted the mentioned chars

Terminal: 
```bash
hacker@data~deleting-characters:~$ /challenge/run | tr -d ^%
Your character-stuffed flag:
pwn.college{wsb7E-zGAa9FmWPiEAQDHIyy_JZ.0FNxEzNxwiM1IzNxEzW}
```
Flag: 
pwn.college{wsb7E-zGAa9FmWPiEAQDHIyy_JZ.0FNxEzNxwiM1IzNxEzW}

### Deleting newlines

Solution: used "\n" as arg to delete all newlines

Terminal: 
```bash
hacker@data~deleting-newlines:~$ /challenge/run | tr -d "\n"
Your line-split flag: pwn.college{UrU0VLafF3FI2hyBMui7XG8_GEc.0VNxEzNxwiM1IzNxEzW}
```
Flag: 
pwn.college{UrU0VLafF3FI2hyBMui7XG8_GEc.0VNxEzNxwiM1IzNxEzW}

### Extracting the first lines with head

Solution: used piping twice and the head command

Terminal: 
```bash
hacker@data~extracting-the-first-lines-with-head:~$ /challenge/pwn | head -n 7 | /challenge/college
Congratulations, you piped the right codes!
pwn.college{oGspkOiEEvVbyz2vgWOW4ah38AR.0lNxEzNxwiM1IzNxEzW}
```
Flag: 
pwn.college{oGspkOiEEvVbyz2vgWOW4ah38AR.0lNxEzNxwiM1IzNxEzW}

### Extracting specific sections of text

Solution: used cut and tr both to obtain the flag

Terminal: 
```bash
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run | cut -d " " -f 2 | tr -d "\n"
pwn.college{koeTVv2jjE813faC9bwLJ5Z9Afl.01NxEzNxwiM1IzNxEzW}
```
Flag: 
pwn.college{koeTVv2jjE813faC9bwLJ5Z9Afl.01NxEzNxwiM1IzNxEzW}

### Sorting data

Solution: used sort and chose the last flag

Terminal: 
```bash
hacker@data~sorting-data:~$ cat /challenge/flags.txt | sort
ovm.bollefe{c3d0eUz_OklabCvx_KltbgH2-oW.0FL0MCOwviM1IzMxEyW}
ovm.cokkdge{c3d0eVy_NkmacCwy_KlsbgI2-oV.0FL0LDOwwhM1IzMwEzW}
ovm.college{c2d0eVy_OkmacCvy_KlsbfI2-oW.0FM0LDNxviL1IzNxEyV}
ovn.bnkkegd{c2d0eUz_OklacCwy_KksbgI2-nW.0FM0MCOxviL1IyMwDyW}
ovn.bnlkdge{b2c0eVz_OkmacCwy_KltbgI1-oV.0FM0MDOwviM1HzMwDyW}
ovn.cnlkegd{c2d0eVz_NkmabCwy_KlsagH2-nV.0FL0MCOxwiM0IyNxDzV}
ovn.collegd{c3d0eUz_OkmacBwy_KltbgH1-nV.0FM0MCOwwiM0IyNxEzW}
owm.bokldfe{c3c0eVz_NkmacBvy_KltbgI1-nW.0FM0MDNxviM1IzNxEyV}
owm.cnllege{b3c0eVz_OjlacCwx_KltbfI2-oV.0EM0LDNxviM0HzNwDzW}
owm.college{c2d0eUz_OkmabCwx_JltagI1-oW.0FL0MDOwviL1IyNxEzW}
own.bnllefe{c2c0dVz_OjmacCwy_KltagH1-oW.0EM0MDOxwiM1IzNwDyW}
own.bollege{c3c0dVz_OkmacCwy_KlsbgI2-oW.0FM0MDOxwiL0IyMxEzW}
own.cnklefe{c2d0eVz_NjmacCwy_KksbfI1-oV.0EM0MCNwwiM1IyNwEzW}
own.colkdgd{c3d0dVz_NkmacCwy_JltbgI2-oW.0EM0MDNxwiM1IzNwEzW}
own.colkegd{c3d0eUz_OklacCvy_KltafH2-oW.0EL0MDOxwiM1IyMxEzW}
own.colldgd{c3c0eUz_OkmacCwy_KltagH1-nW.0FM0MDNxviL0IzMwEzW}
own.colldgd{c3d0eVz_OkmacCwy_JltbgI2-oW.0FL0MCOxwiM1IzNxEzW}
own.collefe{c3d0eVy_NjmacCwy_KlsbgI2-oW.0FM0MCOxwiM0HyNxDzV}
own.college{b3d0eVz_OkmacCwy_KltbgI1-oW.0FM0MDOxwhM1IzNxEyW}
pvm.bokkdfe{c3c0dVz_OkmacCwy_KktafH2-oV.0FM0MDOxwiM0IzMxEyV}
pvm.bokkege{c3d0eVz_OkmacBwx_JktbfI2-oW.0FL0MDOxwiM1HzMxEzW}
pvm.bollege{c2d0dVy_OkmabCvy_KlsbgH2-nW.0FM0MDOxwiL1HzNxEzW}
pvm.cokkefe{c3c0eVz_OkmacCwy_KltbfH1-nV.0FM0LCNxviM0IzNxEzW}
pvm.coklefe{c2d0eUz_OkmacBvy_JksbgI2-nV.0FL0LCNxwiM0IyNxDyW}
pvm.colldgd{c3d0eVz_NkmacCwy_JltbfI1-nV.0FL0LCOwvhL0IzNxEzW}
pvn.bolkdge{c2d0dVz_NkmacCwy_KltagI1-oW.0FM0LCOwwiL1IzNxEzV}
pvn.bolkdge{c3d0eVy_OkmabCwy_JltafI2-oV.0EM0MCNwviM1IzNxEzV}
pvn.bolldge{b3c0dVz_OkmabCwy_KksbfI1-nW.0FM0LDOxwiL1IzMxDzW}
pvn.bollege{c2c0dUz_OklacCvx_KltagH2-oV.0FM0MCOxwiM1HzNwDzW}
pvn.cnkkege{c2c0dUz_OkmacBvy_JltbgI2-oV.0EM0MCNxwiM0IzNxEyW}
pvn.cnklege{c2d0eVz_OklacBwy_JltbgI2-oW.0FM0LDOxwhM1IzNxDzW}
pvn.cnllege{c3d0eVz_NjlacCwy_KltbgI2-nV.0FM0MCOwvhM1IzNxEzW}
pvn.cnllege{c3d0eVz_OkmacCvy_KltbgH2-oW.0EM0MDOxviM0HzNxEyW}
pvn.cnllege{c3d0eVz_OkmacCwy_KltbgI2-oW.0FM0MDOxwiM1IzNxEzW}
pvn.cokldgd{c3c0eVz_OkmabCwx_KlsbgI1-oW.0FM0MDOxwiM1IzNwEzW}
pvn.coklefe{c3d0eVz_OklacCvy_KltbgI2-oV.0FM0MCNxwiM1IyNwEzW}
pvn.collegd{b3d0eVz_OkmacBvx_KlsbgH2-oW.0FM0MDOxviL1IzNxDzW}
pvn.college{b3c0eVz_OkmacCwx_KktbfI2-oW.0FM0MCNwwiM1IzNwEzW}
pvn.college{c3d0eUz_OkmacCwy_KltbgI2-oW.0FM0MDOwwiM1IzNxEzW}
pwm.bolldgd{b3d0eVz_OklacCwy_KltbgI2-nW.0FM0MDOxwiM1IzNwEzV}
pwm.cnkkege{c3d0eUz_OklacCvy_KlsbgI2-oW.0EM0MDOxwiM1IzMxEzW}
pwm.cnllege{c2d0eVz_OkmacCwy_KltbgI2-oW.0FM0MDOxwiM1HzNxEzV}
pwm.colkefe{c3d0eUz_OkmacBwy_KltbgI2-nW.0FL0MDOwviM1IzNxEzW}
pwm.college{c3c0eVz_NkmacCwy_JltbgI1-oW.0EM0LDOxwhM0IyNwEzV}
pwm.college{c3d0eUz_OkmabCwx_KltbgI2-oW.0EM0MDOxwiM1IzMxEzW}
pwm.college{c3d0eUz_OkmabCwy_KktbgI2-oW.0EM0MDNxwiM1IyNxEyW}
pwn.bnllege{c3d0dVz_OklabBwy_KktagI2-nW.0FM0MDNxwiL0IyMxEzW}
pwn.bokkegd{c3d0eVy_OkmacCvy_KksbfI1-oV.0FM0MCNxwhM1HzNxEzW}
pwn.boklege{c3d0eVz_OkmacCwy_KltbgI2-oW.0EM0MDOwwiM1IzNxEzW}
pwn.bolldge{c3c0dVz_OkmacCwy_KltbgI2-oW.0FM0MDOxwiM1IzNxEzV}
pwn.bollegd{c3d0eUy_OkmabCwy_KltbgH1-oW.0EM0MCOxwiM1HzNxEzW}
pwn.bollege{c3d0eVz_OkmabCwy_JltbgI1-oW.0FM0MDOxwiM1IzNxEzW}
pwn.bollege{c3d0eVz_OkmacCwy_KlsbgI2-oW.0FL0MDOxwiM1IzNxEzW}
pwn.cnkkege{b3d0eVz_OkmacCwy_JksbgI2-oW.0FL0MDNxviM1IyNxEzW}
pwn.cnlldfe{c3d0eVy_NjmacBwx_JltagI1-oW.0FL0MCOxwhM1IzNwEzW}
pwn.cnllegd{c3d0eVz_OjmacCvy_KltagI2-oW.0FM0MCOxwiM1IzNxEyV}
pwn.cnllege{c3c0eVz_OkmacBwy_KltbgH1-oW.0EM0MCOxwiL1IzNwEzV}
pwn.cnllege{c3c0eVz_OkmacCwy_KktbgI2-oW.0FM0MCOwwiM0HyNxEzW}
pwn.cnllege{c3d0dUz_OjmabBwy_KltagI2-nV.0FM0MDNxwiL1IyMxEyW}
pwn.cnllege{c3d0eVy_OkmacCwy_JltbgI2-oW.0FM0LCNxwiM1IzNwEzW}
pwn.cnllege{c3d0eVz_OkmacCwy_KltbgI2-nW.0FM0MDOxwiM1IzNxEzW}
pwn.cokkege{b3c0eVz_OkmabCwx_JktagH2-oW.0EM0MCNxviM0HzNxEzW}
pwn.cokkege{c3c0dVy_OkmacCwy_JktbgI2-oW.0EL0LDNxwiM1IzNxEzV}
pwn.cokkege{c3d0eVz_OkmacCwy_KksbfI1-oW.0EL0MCOxwiM0IzNwDzW}
pwn.cokldgd{c2d0eVz_OjmacBwx_KktbfH2-nW.0FL0LDOxwiL1IzNxEyV}
pwn.cokldge{b3d0eVz_OklacCvx_KltbfI2-oW.0EL0LCOxviL1IzNxEzW}
pwn.coklegd{c3d0eVz_OkmacCwy_KltbgI2-oW.0FM0MDOxwiM1IzNxEzW}
pwn.coklege{c3d0dVz_OjmacCwy_KlsagI2-nV.0FM0MCOxwiM1IzNxEzV}
pwn.coklege{c3d0eVz_OkmabCwy_KltbgI2-nW.0EM0MDOxvhM1HzNxEzW}
pwn.coklege{c3d0eVz_OkmacCwy_KltbgI2-oW.0FM0MDOxwiM1IzNxEzW}
pwn.colkefe{c3d0eVz_OkmacCwy_KltbgI2-oW.0FM0MDOxwiM1IzNxEzW}
pwn.colkege{c3c0eVz_OkmacCvy_KktbgI2-oW.0EM0MDOxwiM1IzNxEyW}
pwn.colldfd{c3c0dUz_OjmacCvy_KltagH1-oV.0FM0MCNxwiM1IyMwEzW}
pwn.colldge{b3d0eUz_OkmacCwy_KltafH2-nW.0EM0LDOwviM0IzMwEzV}
pwn.colldge{c3c0dVy_OkmabBwy_KltbgI1-nV.0FM0LCNxwiM1HzMwDyV}
pwn.colldge{c3d0eUz_OkmacCwy_KlsbgI2-oW.0FM0LDOxwhM0IzNxEzV}
pwn.collefe{c3d0eVz_OkmacCwy_KltbgH2-nW.0FM0MDOxwhM1IzNxDyW}
pwn.collegd{c3c0dUz_NjmacCvx_JktbgI2-oV.0FL0LCOwwiM1HyNwDzW}
pwn.collegd{c3d0eUz_OkmacCwy_KltbgI2-oW.0FM0MDOxwiM1IzNxEyW}
pwn.college{b2d0dVy_OkmacCwy_KlsbgH2-oW.0FM0LDNxviM1IzNxEzV}
pwn.college{b3d0eUz_OkmacCwy_JktbgI2-oW.0FM0MCOxwiM1HzNwEzV}
pwn.college{c2c0eVz_OklacBwx_KktbgH1-oV.0FM0MCOxwhM0IzNxEzW}
pwn.college{c2d0dUz_OjmacBwy_KltagI1-oW.0FM0LDNxwhM0IzNxDzW}
pwn.college{c2d0eVy_OkmacCwy_JltbgI2-oW.0FM0MDOwwiM1HzNxEyW}
pwn.college{c2d0eVz_OkmacCwy_KltbgI2-nW.0FM0MDOxwiL1IzNwEzV}
pwn.college{c3d0eUz_OkmabCwy_JktbgI1-oW.0FM0MDOxwiL0IyNxEyW}
pwn.college{c3d0eVy_OkmacCwy_KlsagI2-oW.0EM0MDOxwiM1IzNxEzW}
pwn.college{c3d0eVy_OkmacCwy_KltbfI2-oW.0FM0MDOxviM1IzNxEzW}
pwn.college{c3d0eVz_OjmacCwy_KltbgI2-oW.0FM0MDOxwhM1IzNwEzW}
pwn.college{c3d0eVz_OjmacCwy_KltbgI2-oW.0FM0MDOxwiM1IzNxEzW}
pwn.college{c3d0eVz_OklacCvx_KltbgI2-nW.0EM0MDOxwiM1IyMxEzW}
pwn.college{c3d0eVz_OkmacBwy_KltbfI2-oW.0FL0MDOwviM1IzNxEzW}
pwn.college{c3d0eVz_OkmacCwy_KktbgI2-oW.0FM0MDOxwiM1IzNxEzW}
pwn.college{c3d0eVz_OkmacCwy_KltbgI2-oW.0FL0LDOxwiM1IzNxEzW}
pwn.college{c3d0eVz_OkmacCwy_KltbgI2-oW.0FL0MDOxwiM1IzNxEzW}
pwn.college{c3d0eVz_OkmacCwy_KltbgI2-oW.0FM0MDOxwiM1IzMxEzW}
pwn.college{c3d0eVz_OkmacCwy_KltbgI2-oW.0FM0MDOxwiM1IzNxEyW}
pwn.college{c3d0eVz_OkmacCwy_KltbgI2-oW.0FM0MDOxwiM1IzNxEzV}
pwn.college{c3d0eVz_OkmacCwy_KltbgI2-oW.0FM0MDOxwiM1IzNxEzW}
pwn.college{c3d0eVz_OkmacCwy_KltbgI2-oW.0FM0MDOxwiM1IzNxEzW}
pwn.college{c3d0eVz_OkmacCwy_KltbgI2-oW.0FM0MDOxwiM1IzNxEzW}
```
Flag: 
pwn.college{c3d0eVz_OkmacCwy_KltbgI2-oW.0FM0MDOxwiM1IzNxEzW}
