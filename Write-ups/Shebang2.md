# Shebang2

![Category](http://img.shields.io/badge/Category-Shebang-orange?style=for-the-badge) ![Points](http://img.shields.io/badge/Points-150-brightgreen?style=for-the-badge)

We connect to the shell using this command `ssh -p 1337 shebang2@cyberyoddha.baycyber.net` and the flag from the Shebang1 challenge as the password.

Once connected we try to see what's in our working dircetory but there are a lot of files and folders!

Running the command `$ find . -type f | wc -l` confirm there are infact `10000` files!

Also, running the command `grep -r "flag"` also doesn't not work as the files all contains strinsg such as: `This is not a flag`.

Instead to find the flag we can again take advantage of the fact we know the flag format `CYCTF{....}`.

Searching for files with the string `CYCTF` gives a better result;

$ grep -r "CYCTF"    
86/13:CYCTF{W0w_th@t$_@_l0t_0f_f1l3s}

And there's the next flag;

## CYCTF{W0w_th@t$_@_l0t_0f_f1l3s}
