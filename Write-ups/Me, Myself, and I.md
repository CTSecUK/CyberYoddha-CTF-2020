# Me, Myself, and I

![Category](http://img.shields.io/badge/Category-Password%20Cracking-orange?style=for-the-badge) ![Points](http://img.shields.io/badge/Points-225-brightgreen?style=for-the-badge)

This time we're given a longer hash;

`2412f72f0f0213c98c1f9f6065728da4529000e5c3a2e16c4e1379bd3e13ccf543201eec4eb7b400eb5a6c9b774bf0c0eeda44869e08f3a54a0b13109a7644aa`

Again i run this through hash-identifier;

![hash-dentifier](https://github.com/CTSecUK/CyberYoddha-CTF-2020/blob/main/images/me_myself_and_i_hash-identifier.png)

Well before we try cracking a SHA-512 let's look at the whirlpool option;

I head over to the site [https://md5hashing.net](https://md5hashing.net/hash/whirlpool/2412f72f0f0213c98c1f9f6065728da4529000e5c3a2e16c4e1379bd3e13ccf543201eec4eb7b400eb5a6c9b774bf0c0eeda44869e08f3a54a0b13109a7644aa) and try decrypting the hash as a **whirlpool** hash.

And the hash is decrpyted;

![screenshot](https://github.com/CTSecUK/CyberYoddha-CTF-2020/blob/main/images/me_myself_and_i_whirlpool%20decrypt.png)

## cyctf{whoami}
