# Lorem Ipsum

We are given the following string of text, which we save as `file1.txt`;

```
Lorem ipsum dolorc sit amet, consectetury adipiscing celit, sed dot eiusmod tempor incifdidunt ut labore et dolore magna aliqual. Ut enim ad minima veniam, quist nostrud exercitation ullamcoi laboris nisin ut aliquip ex eai commodos consequat. Duis caute irure dolor in reprehenderit in voluptate velit oesse cillum dolore eu fugiat nulla pariatur. Excepteur osint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim lid est laborum.
```

Next we go to [https://loremipsum.io/](https://loremipsum.io/) and copy a near identical strong of text from it's generator, which we save to `file2.txt`;

```
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum. 
```

running a `diff` command on these to files show that there are diffreneces between them;

`diff file1.txt file2.txt`

Let use a python script to find those differnce and output the string in a nice, easy to read format;

```python
import difflib

a='Lorem ipsum dolorc sit amet, consectetury adipiscing celit, sed dot eiusmod tempor incifdidunt ut labore et dolore magna aliqual. Ut enim ad minima veniam, quist nostrud exercitation ullamcoi laboris nisin ut aliquip ex eai commodos consequat. Duis caute irure dolor in reprehenderit in voluptate velit oesse cillum dolore eu fugiat nulla pariatur. Excepteur osint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim lid est laborum.'
b='Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.'

diff = difflib.ndiff(a,b)

changes = [l for l in diff if l.startswith('+ ') or l.startswith('- ')]

flag = ""

for c in changes:
       flag = flag + c[len(c) -1]

print(flag)
```

rather than opening the files and reading in the input i simply coppied the lorem Ipsum text into the python script and save them as 2 different string variables.

Running our script, we get the below output

```
[jaxigt@MBA lorem_ipsum]$ python diff.py 
cyctflatiniscool
```

The flag is;

## cyctf{latiniscool}
