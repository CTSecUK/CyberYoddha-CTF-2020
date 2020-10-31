# What’s the Password?

We download the image and take a look at it;

![image](https://github.com/CTSecUK/CyberYoddha-CTF-2020/blob/main/images/whats_the_password_sudo.jpg)

this along with the  title of the challenge seems like a pretty good clue

Let's try extracting data from the image file using `steghide` with a password of `sudo`

```
[jaxigt@MBA whats_the_password]$ steghide --extract -sf sudo.jpg 
Enter passphrase: 
wrote extracted data to "steganopayload457819.txt".
```

If we look at the contets of the file `steganopayload457819.txt` using the **cat** comand we see the flag: `CYCTF{U$3_sud0_t0_achi3v3_y0ur_dr3@m$!}

## CYCTF{U$3_sud0_t0_achi3v3_y0ur_dr3@m$!
