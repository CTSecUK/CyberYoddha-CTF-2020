# Shebang2


We connect to the shell using this command `ssh -p 1337 shebang1@cyberyoddha.baycyber.net` and the flag from the Shebang1 challenge as the password.

Once connected we try to see what's in our working dircetory but htere are a lot of files and folders!

Running the command `$ find . -type f | wc -l` confirm there are infact `10000` files!

running `grep -r "flag"` also does not work asthe files containg the string `This is not a flag`.

Instead to Find the flag we can again take advnateg of the flag format.

Searching for files with the string `CYCTF` gives a better result

$ grep -r "CYCTF"    
86/13:CYCTF{W0w_th@t$_@_l0t_0f_f1l3s}

And there's the next flag;

## CYCTF{W0w_th@t$_@_l0t_0f_f1l3s}
