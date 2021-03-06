# Shebang4

![Category](http://img.shields.io/badge/Category-Shebang-orange?style=for-the-badge) ![Points](http://img.shields.io/badge/Points-200-brightgreen?style=for-the-badge)

We connect to the shell using this command `ssh -p 1337 shebang4@cyberyoddha.baycyber.net` and the flag from the Shebang3 challenge as the password.

running the `ls` command in our current directory shows us the file `flag.png`, but we cannot view the image from a shell!?

Instead we read the file into a base64 encoded string using `cat flag.png | base64`;

```
iVBORw0KGgoAAAANSUhEUgAAAqUAAABfCAYAAADRTr5kAAABQ2lDQ1BJQ0MgUHJvZmlsZQAAKJFj
YGASSSwoyGFhYGDIzSspCnJ3UoiIjFJgf8LAxcDMwMugySCVmFxc4BgQ4ANUwgCjUcG3awyMIPqy
Lsiss6I2hw5wJOdkt29Lsfrx9hamehTAlZJanAyk/wBxanJBUQkDA2MKkK1cXlIAYncA2SJFQEcB
2XNA7HQIewOInQRhHwGrCQlyBrJvANkCyRmJQDMYXwDZOklI4ulIbKi9IMDt467gFurjo+DhQsC1
ZICS1IoSEO2cX1BZlJmeUaLgCAylVAXPvGQ9HQUjAyMDBgZQmENUf74BDktGMQ6EWCHQj1aeDAxM
uQixhAAGhh0fQF5FiKnqMDDwHGdgOBBbkFiUCHcA4zeW4jRjIwibezsDA+u0//8/hzMwsGsyMPy9
/v//7+3///9dxsDADIyrA98A1ZdftU2VNlAAAABWZVhJZk1NACoAAAAIAAGHaQAEAAAAAQAAABoA
AAAAAAOShgAHAAAAEgAAAESgAgAEAAAAAQAAAqWgAwAEAAAAAQAAAF8AAAAAQVNDSUkAAABTY3Jl
ZW5zaG90MBidHgAAAdVpVFh0WE1MOmNvbS5hZG9iZS54bXAAAAAAADx4OnhtcG1ldGEgeG1sbnM6
eD0iYWRvYmU6bnM6bWV0YS8iIHg6eG1wdGs9IlhNUCBDb3JlIDUuNC4wIj4KICAgPHJkZjpSREYg
eG1sbnM6cmRmPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5LzAyLzIyLXJkZi1zeW50YXgtbnMjIj4K
ICAgICAgPHJkZjpEZXNjcmlwdGlvbiByZGY6YWJvdXQ9IiIKICAgICAgICAgICAgeG1sbnM6ZXhp
Zj0iaHR0cDovL25zLmFkb2JlLmNvbS9leGlmLzEuMC8iPgogICAgICAgICA8ZXhpZjpQaXhlbFhE
aW1lbnNpb24+Njc3PC9leGlmOlBpeGVsWERpbWVuc2lvbj4KICAgICAgICAgPGV4aWY6VXNlckNv
bW1lbnQ+U2NyZWVuc2hvdDwvZXhpZjpVc2VyQ29tbWVudD4KICAgICAgICAgPGV4aWY6UGl4ZWxZ
RGltZW5zaW9uPjk1PC9leGlmOlBpeGVsWURpbWVuc2lvbj4KICAgICAgPC9yZGY6RGVzY3JpcHRp
b24+CiAgIDwvcmRmOlJERj4KPC94OnhtcG1ldGE+Cn92PpgAACzHSURBVHgB7Z0FtARHsYYnuLtL
Etw9OCS4uwbX4ME9QLCgwYO7S/DgFtxdggWCu7vPq6/zqk9tz/TenZ21e/PXOffObE/r31ZdXdW9
S2vUiISAEBACQkAICAEhIASEwBoRONoa01bSQkAICAEhIASEgBAQAkIgISCmVA1BCAgBISAEhIAQ
EAJCYO0IiCldexUoA0JACAgBISAEhIAQEAJiStUGhIAQEAJCQAgIASEgBNaOgJjStVeBMiAEhIAQ
EAJCQAgIASEgplRtQAgIASEgBISAEBACQmDtCIgpXXsVKANCQAgIASEgBISAEBACYkrVBoSAEBAC
QkAICAEhIATWjoCY0rVXgTIgBISAEBACQkAICAEhIKZUbUAICAEhIASEgBAQAkJg7QiIKV17FSgD
QkAICAEhIASEgBAQAmJK1QaEgBAQAkJACAgBISAE1o6AmNK1V4EyIASEgBAQAkJACAgBISCmVG1A
CAgBISAEhIAQEAJCYO0IiCldexUoA0JACAgBISAEhIAQEAJiStUGhIAQEAJCQAgIASEgBNaOgJjS
tVeBMiAEhIAQEAJCQAgIASEgplRtQAgIASEgBISAEBACQmDtCIgpXXsVKANCQAgIASEgBISAEBAC
YkrVBoSAEBACQkAICAEhIATWjoCY0rVXgTIgBISAEBACQkAICAEhIKZUbUAICAEhIASEgBAQAkJg
7QiIKV17FSgDQkAICAEhIASEgBAQAmJK1QaEgBAQAkJACAgBISAE1o6AmNK1V4EyIASEgBAQAkJA
CAgBISCmVG1ACAgBISAEhIAQEAJCYO0IiCldexUoA0JACAgBISAEhIAQEAJiStUGhIAQEAJCQAgI
ASEgBNaOgJjStVeBMiAEhIAQEAJCQAgIASEgplRtQAgIASEgBISAEBACQmDtCIgpXXsVKANCQAgI
ASEgBISAEBACYkrVBoSAEBiMwEtf+tLmrW996+BwBBgTdq4EFUgICAEhIAS2BQK7tEbbIqfKpBAQ
AmtH4H//+1/zpS99qbnc5S7XnPGMZ2ze+c53Nmc605lmyteYsDMlIE9CQAgIASGwrRFYOVP6ne98
p3nJS17SfOpTn2p+9KMfNb/+9a+b05/+9M1ZznKW5tKXvnRzj3vcoznxiU+cQWUiu+Md79j8+9//
Tm5Xu9rVmlvc4hb5+7SX17zmNc273/3u5OXUpz51c+CBB/Z6/+c//5mkPm94wxua733veylfxzjG
MVKezna2szV3uMMdmr322qsT9s1vfnPzlre8peM+q8NBBx2UynrXu961+ctf/jJrsOSPPMEYlPSs
Zz2recELXtD89Kc/bf7xj380v/vd75onP/nJDbhDBxxwQLPrrruWwdJvsCbe//znP+n3Fa94xea2
t71tr18cSedjH/tY+v7ABz6wOd/5zpf9HnbYYQmbb33rWykfl7jEJZrLXOYyzUUucpEGbPvo7ne/
e/OnP/2pOc95ztM8+MEPzl5q7tnDAl8++MEPJrzI7yMf+cgFxrwZUdGPXve61zVf/OIXm+9///uJ
oaTfUTenPe1pq5n885//nCScz3zmM1MfiR7PcIYzNPvvv39z+9vfvjna0bqbL2PCxnTmeadfHetY
x0p/Hv6Tn/xk89znPjf9vP/9799c4AIX8E+jnz/+8Y+bl73sZQ3t/oc//GH6+8UvftGc/OQnT+Mc
jPzVr3715iY3uUlz0pOedOb0+soxc+A1e/zvf//bvP3tb2/e//73Z0zAhvGGsZ+/8573vM3Nb37z
5pKXvOSac7t5yf/2t79N7WcTclYbi2vum5DnnZSHRzziEc1Tn/rU5jSnOU1zqUtdKr2f4hSn2ElF
bBokpasg61jt9a9/faSyU/9OcpKTtDbxTWTpIQ95SA5zvOMdrzXGceJ73w/8HP/4x8/hjBHu89Ye
fPDBrVVq9lfL3+Uvf/nWmOiJOGK+auGmuf/kJz9J8Z3oRCfaMv0yHptUJ/LCjxe+8IWdeP7617+2
xtRnd5swO+HcwRYK2R/pGZPpn3qfNpFk/zYZJz82AbX77rtve/SjHz1/i3m3SaelLfTRyU52shRm
zz33nPhcc5/wtIAftkBqjWFPebDFzwJi3KwoqN9znOMcvfViC4X25S9/eW+Gjalsz33uc/eGi3VL
fyhpTNgyrqG/bVHaGqPdfvzjH58IauoDuSymgjDxbd4fxui2N77xjavtPuLEuzHKrTFhLW1uK6qV
Y6tw6/7+xz/+sX3KU57S7r777hnvEofy91nPetbWFk3rzvpGpG+ChfZmN7tZe+UrX3kj8kMmamNx
zX1jMr5DMmLCn4m+dOYzn7k1IdIOKd2RxVgJU/r1r3+93W233SbAPPvZz97e8IY3bO9yl7u017rW
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
QEzpigFXckJACAgBISAEhIAQEAJdBMSUdjGRixAQAkJACAgBISAEhMCKERBTumLAlZwQEAJCQAgI
ASEgBIRAFwExpV1M5CIEhIAQEAJCQAgIASGwYgTElK4YcCUnBISAEBACQkAICAEh0EVATGkXE7kI
ASEgBISAEBACQkAIrBgBMaUrBlzJCQEhIASEgBAQAkJACHQREFPaxUQuQkAICAEhIASEgBAQAitG
QEzpigFXckJACAgBISAEhIAQEAJdBMSUdjGRixAQAkJACAgBISAEhMCKERBTumLAlZwQEAJCQAgI
ASEgBIRAFwExpV1M5CIEhIAQEAJCQAgIASGwYgTElK4YcCUnBISAEBACQkAICAEh0EVATGkXE7kI
ASEgBISAEBACQkAIrBgBMaUrBlzJCQEhIASEgBAQAkJACHQREFPaxUQuQkAICAEhIASEgBAQAitG
QEzpigFXckJACAgBISAEhIAQEAJdBMSUdjGRixAQAkJACAgBISAEhMCKERBTumLAlZwQEAJCQAgI
ASEgBIRAFwExpV1M5CIEhIAQEAJCQAgIASGwYgTElK4YcCUnBISAEBACQkAICAEh0EVATGkXE7kI
ASEgBISAEBACQkAIrBgBMaUrBlzJCQEhIASEgBAQAkJACHQREFPaxUQuQkAICAEhIASEgBAQAitG
QEzpigFXckJACAgBISAEhIAQEAJdBMSUdjGRixAQAkJACAgBISAEhMCKEfg/VHQJ29J8npIAAAAA
SUVORK5CYII=
```

Back on my own PC I save the b64 output to a file called `flag.b64` and then use the following command to convert it back to a "**png**" file;

`cat flag.b64 | base64 -d > flag.png`

Viewing the resulting image we can seee the below flag;

![Flag](https://github.com/CTSecUK/CyberYoddha-CTF-2020/blob/main/images/shebang4_flag.png)
