# Shebang0 

![Category](http://img.shields.io/badge/Category-Shebang-orange?style=for-the-badge) ![Points](http://img.shields.io/badge/Points-125-brightgreen?style=for-the-badge)

We connect to the shell given in the challenge description.

`ssh -p 1337 shebang0@cyberyoddha.baycyber.net`

```
$ ls -al
total 12
dr-x------ 1 shebang0 root 4096 Oct 30 20:47 .
drwxr-xr-x 1 root     root 4096 Oct 30 20:47 ..
-rw-r--r-- 1 root     root   33 Oct  6 00:26 .flag.txt
```

Notice the file is hidden by preceedign with a `.`

To read the file we can use;

```
$ cat ./.flag.txt
CYCTF{w3ll_1_gu3$$_b@sh_1s_e@zy}
```

So that's the flag for this challenge;

## CYCTF{w3ll_1_gu3$$_b@sh_1s_e@zy}
