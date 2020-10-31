# Shebang1

![Category](http://img.shields.io/badge/Category-Shebang-orange?style=for-the-badge) ![Points](http://img.shields.io/badge/Points-125-brightgreen?style=for-the-badge)

We connect to the shell again using this command `ssh -p 1337 shebang1@cyberyoddha.baycyber.net` and the flag from the Shebang0 challenge as the password.

Once connected we run and ls to see what's in our working dircetory;

```
$ ls -al
total 300
dr-x------ 1 shebang1 root   4096 Oct 30 20:47 .
drwxr-xr-x 1 root     root   4096 Oct 30 20:47 ..
-rw-r--r-- 1 root     root 298902 Oct  6 22:43 flag.txt
```

As you can see the flag is right there, and although the file is owend by root we have read access to it.

But you may also notice the file size... it's pretty large for a flag string!?!

If you just try to cat the file to the screen it will spit out endless lines of text to the console.

Instead we need to grep the output to get the flag.

We know the flags start with CYCTF so we can try the following;

```
$ cat flag.txt | grep CYCTF
CYCTF{w3ll_1_gu3$$_y0u_kn0w_h0w_t0_gr3p}
```

And there's our flag;

## CYCTF{w3ll_1_gu3$$_y0u_kn0w_h0w_t0_gr3p}
