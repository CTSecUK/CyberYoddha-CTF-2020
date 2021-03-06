# Beware the Ides of March

![Category](http://img.shields.io/badge/Category-Cryptography-orange?style=for-the-badge) ![Points](http://img.shields.io/badge/Points-50-brightgreen?style=for-the-badge)

## Details

![Details](https://github.com/CTSecUK/CyberYoddha-CTF-2020/blob/main/images/beware_the_ides_of_march_details.png)

Looking at the cipher string `JFJAM{j@3$@y_j!wo3y}` we can see that the format is familiar, the flags generally start with CYCTF so this looks like a simple Ceser Cipher.

We can eneter the string into CyberChef  and use a ROT13 recipe, varying the shift value until we find the correct flag string;

[https://gchq.github.io/CyberChef/#recipe=ROT13(true,true,19)&input=SkZKQU17akAzJEB5X2ohd28zeX0](https://gchq.github.io/CyberChef/#recipe=ROT13(true,true,19)&input=SkZKQU17akAzJEB5X2ohd28zeX0)

![Cyberchef](https://github.com/CTSecUK/CyberYoddha-CTF-2020/blob/main/images/beware_the_ides_of_march_cyberchef.png)

And there we have our flag;

## CYCTF{c@3$@r_c!ph3r}
