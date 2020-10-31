# Crack the Zip

![Category](http://img.shields.io/badge/Category-Password%20Cracking-orange?style=for-the-badge) ![Points](http://img.shields.io/badge/Points-200-brightgreen?style=for-the-badge)

```
[jaxigt@MBA crack_the_zip]$ zip2john flag.zip 
ver 1.0 efh 5455 efh 7875 flag.zip/flag.txt PKZIP Encr: 2b chk, TS_chk, cmplen=42, decmplen=30, crc=6DB4BCF0
flag.zip/flag.txt:$pkzip2$1*2*2*0*2a*1e*6db4bcf0*0*42*0*2a*6db4*8500*a456e7cb9788f0047910f60de3cf4af8c9cca229c1528aebb42245dcc34ed6a5c088ef9155a717b2e2c2*$/pkzip2$:flag.txt:flag.zip::flag.zip
```

`zip2john flag.zip > flag.hash`

```
[jaxigt@MBA crack_the_zip]$ john --wordlist=/usr/share/wordlists/rockyou.txt flag.hash
Using default input encoding: UTF-8
Loaded 1 password hash (PKZIP [32/64])
Will run 4 OpenMP threads
Press 'q' or Ctrl-C to abort, almost any other key for status
not2secure       (flag.zip/flag.txt)
1g 0:00:00:00 DONE (2020-10-31 00:23) 2.380g/s 11936Kp/s 11936Kc/s 11936KC/s nothingnew74..norijoy
Use the "--show" option to display all of the cracked passwords reliably
Session completed
```

here we can see it cracked the password which is `not2secure`

Let's unzip the file now 

```
[jaxigt@MBA crack_the_zip]$ unzip flag.zip 
Archive:  flag.zip

[flag.zip] flag.txt password: 
 extracting: flag.txt                
```

And finally, get the flag;

```
[jaxigt@MBA crack_the_zip]$ cat flag.txt 
cyctf{y0u_cr@ck3d_th3_z!p...}
```

## cyctf{y0u_cr@ck3d_th3_z!p...}
