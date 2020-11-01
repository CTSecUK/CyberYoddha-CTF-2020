# Data Store

![Category](http://img.shields.io/badge/Category-Web%20Exploitation-orange?style=for-the-badge) ![Points](http://img.shields.io/badge/Points-175-brightgreen?style=for-the-badge)

## Details

![Details](https://github.com/CTSecUK/CyberYoddha-CTF-2020/blob/main/images/datastore_details.png)
\
Firstly, I navigated to the URL provided and had a look around "https://cyberyoddha.baycyber.net:33002"
Looking at the webpage you are only presented with a login page.\
\
Viewing the source gave no indication, so i tried some default username and passwords:- admin:admin admin:password admin:123456
Which just gave me errors,(see below).\
\
![Image](https://github.com/CTSecUK/CyberYoddha-CTF-2020/blob/main/images/datastore_admin_login_failed.png)
\
Reading the challenge details again and looking at what the challenge is called "Data Store", i started to think that it must be a authentication bypass or SQL Injection.\
\
Web Expoloitation isn't my strong suit so i ended up using a google search "SQLI vulnerability testing" which then led me to googling "sql injection practical cheat sheet"\
\
Looking through some of the websites, i came across this one "https://perspectiverisk.com/mysql-sql-injection-practical-cheat-sheet/", i knew that i would be looking for something like 1=1\
\
or something along those lines so i scrolled through till i found a section with a similar example.\
\
![Image](https://github.com/CTSecUK/CyberYoddha-CTF-2020/blob/main/images/datastore_SQLI_test.png)
\
So i tried that in the admin login box, in this format " admin ' OR '1' = '1 "\
\
![Image](https://github.com/CTSecUK/CyberYoddha-CTF-2020/blob/main/images/datastore_admin_login_SQLI.png)
\
What do we have here!\
\
![Image](https://github.com/CTSecUK/CyberYoddha-CTF-2020/blob/main/images/datastore_flag.png)\
\
Looks like we have the flag:  ***cyctf{1_l0v3_$qli}***
