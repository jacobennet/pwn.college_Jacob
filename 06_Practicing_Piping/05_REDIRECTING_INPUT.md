
# REDIRECTING INPUT

This module teaches you how you can redirect input as well

# FLAG

My flag ~ pwn.college{MwTGVSFDY7YgWAeVVw8cKkc2jyu.QXwcTN0wCN0AzNzEzW}

# SOLUTION

First redirect the contents of college  to PWN using echo and then redirect the input  using < to /challenge/run.

```
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{MwTGVSFDY7YgWAeVVw8cKkc2jyu.QXwcTN0wCN0AzNzEzW}
```

# WHAT  I LEARNT

 you can redirect input  to programs using < 