# Shebang3

We connect to the shell using this command `ssh -p 1337 shebang1@cyberyoddha.baycyber.net` and the flag from the Shebang2 challenge as the password.

Once connected we run and ls to see what's in our working dircetory;

```
$ ls -al
total 273304
dr-x------ 1 shebang3 root      4096 Oct 30 20:47 .
drwxr-xr-x 1 root     root      4096 Oct 30 20:47 ..
-rw-r--r-- 1 root     root 139921497 Oct 14 18:58 file.txt
-rw-r--r-- 1 root     root 139922225 Oct 14 19:11 file2.txt
```

Again, like in previous chalenges,  notice the file size... it's too large to just be a flag string and to large to output straight to the screen.

We can try again to recursively grep for the flag using `$ grep -r "CYCTF"` but this yields no results.

The description for this challenge however suggests that both files are the same.?

We can see from the file size above atht this is not the case however!

If we run `diff file.txt file2.txt` we still get a fairly long list of differences but it is readable. If get just the first 50 lines using the head command `diff file.txt file2.txt | head -n 50` you can see the below

```
$ diff file.txt file2.txt | head -n 50
106526a106527
> C
107719a107721
> Y
108477a108480
> C
109644a109648
> T
109873a109878
> F
110293a110299
> {
111434a111441
> S
111715a111723
> P
111969a111978
> O
112285a112295
> T
112548a112559
> _
113046a113058
> T
113525a113538
> H
114286a114300
> 3
114773a114788
> _
115594a115610
> D
116750a116767
> 1
117691a117709
> F
118643a118662
> F
121288a121308
> }
602043c602063
< peque�a
---
> peque�a
675999c676019
< contrase�a
---
> contrase�a
746302c746322
< �repod

```
We could manually copy out the characters or we can use linux to do it for us;

```
$ diff file.txt file2.txt | head -n 40 | awk 'NR % 2 ==0 {print; }' | grep -Po '.(?=.{0}$)' | awk '{print}' ORS=''
CYCTF{SPOT_TH3_D1FF}
```

Next flag is;

## CYCTF{SPOT_TH3_D1FF}
