# What’s the Password?

![Category](http://img.shields.io/badge/Category-Forensics-orange?style=for-the-badge) ![Points](http://img.shields.io/badge/Points-175-brightgreen?style=for-the-badge)

We download and look at the image listed in the challenge description which can be seen below;

![image](https://github.com/CTSecUK/CyberYoddha-CTF-2020/blob/main/images/whats_the_password_sudo.jpg)

This along with the title of the challenge seems like a pretty good clue as to what we might need to do!

We try extracting data from the image file using `steghide` with a password of `sudo`;

```
[jaxigt@MBA whats_the_password]$ steghide --extract -sf sudo.jpg 
Enter passphrase: 
wrote extracted data to "steganopayload457819.txt".
```

If we look at the contents of the extracted file `steganopayload457819.txt` using the **cat** comand we see the flag: `CYCTF{U$3_sud0_t0_achi3v3_y0ur_dr3@m$!}`

## CYCTF{U$3_sud0_t0_achi3v3_y0ur_dr3@m$!}
