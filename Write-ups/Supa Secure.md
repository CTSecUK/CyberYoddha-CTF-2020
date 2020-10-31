# Supa Secure

![Category](http://img.shields.io/badge/Category-Password%20Cracking-orange?style=for-the-badge) ![Points](http://img.shields.io/badge/Points-225-brightgreen?style=for-the-badge)

In the challenge details we are We're given a string `19d14c463333a41a1538dbf9eb76aadf`.

I run it through `hash-identifier` and it detects it as a possible MD5

![hash-identifier](https://github.com/CTSecUK/CyberYoddha-CTF-2020/blob/main/images/supa_secure_hash-identifier.png)

Next i hop over to [https://www.md5online.org/](https://www.md5online.org/md5-decrypt.html) to see if it recognises the hash;

![md5Decrypt](https://github.com/CTSecUK/CyberYoddha-CTF-2020/blob/main/images/supa_secure_md5_decrypt.png)

And it does!

## cyctf{ilovesalt}
