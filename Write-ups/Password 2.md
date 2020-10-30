# Password 2

![Category](http://img.shields.io/badge/Category-Reverse%20Engineering-orange?style=for-the-badge) ![Points](http://img.shields.io/badge/Points-175-brightgreen?style=for-the-badge)

## Details

![Details](https://github.com/CTSecUK/CyberYoddha-CTF-2020/blob/main/images/password_2_details.png)

If we download and exmaine the python script we can see the following;

```python
import random

def checkPassword(password):
    if(len(password) != 47):
      return False
    newPass = list(password)
    for i in range(0,9):
      newPass[i] = password[i]
    for i in range(9,24):
      newPass[i] = password[32-i]
    for i in range(24,47,2):
      newPass[i] = password[70-i]
    for i in range(45,25,-2):
      newPass[i] = password[i]
    password = "".join(newPass);
    return password == "CYCTF{ju$@rcs_3l771l_@_t}bd3cfdr0y_u0t__03_0l3m"

password = input("Enter password: ")
if(checkPassword(password)):
  print("PASSWORD ACCEPTED\n")
else:
  print("PASSWORD DENIED\n")
```

Again (like in the previous challenge), we can see the flag is locate in the `checkPassword()` funtion, but is all jumbled up.

This time to decrypt we'll add a few lines of code to the script;

```python
decryptedPass = ""
for chr in newPass:
  decryptedPass = decryptedPass + chr
print(decryptedPass)
```

We'll also pass the jumbled password string through the funtion to save us having to copy and paste it in, and comment out the input request, like so; 

```python
#password = input("Enter password: ")
if(checkPassword("CYCTF{ju$@rcs_3l771l_@_t}bd3cfdr0y_u0t__03_0l3m")):
```

The updated script now looks like this;

```python
import random

def checkPassword(password):
    if(len(password) != 47):
      return False
    newPass = list(password)
    for i in range(0,9):
      newPass[i] = password[i]
    for i in range(9,24):
      newPass[i] = password[32-i]
    for i in range(24,47,2):
      newPass[i] = password[70-i]
    for i in range(45,25,-2):
      newPass[i] = password[i]
    
    decryptedPass = ""
    for chr in newPass:
      decryptedPass = decryptedPass + chr
    print(decryptedPass)

    password = "".join(newPass);
    return password == "CYCTF{ju$@rcs_3l771l_@_t}bd3cfdr0y_u0t__03_0l3m"
    

password = input("Enter password: ")
if(checkPassword("CYCTF{ju$@rcs_3l771l_@_t}bd3cfdr0y_u0t__03_0l3m")):
  print("PASSWORD ACCEPTED\n")
else:
  print("PASSWORD DENIED\n")
```

If we run this script 
```
[jaxigt@MBA password_2]$ python password2.py 
CYCTF{ju$t_@_l177l3_scr@mbl3_f0r_y0u_t0_d3c0d3}
PASSWORD DENIED
```

And there's our Flag;

## CYCTF{ju$t_@_l177l3_scr@mbl3_f0r_y0u_t0_d3c0d3}
