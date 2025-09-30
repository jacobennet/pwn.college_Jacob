
# REDIRECTING ERRORS

This module teaches how you can redirect errors as well to a file

# FLAG 

My flag ~ pwn.college{QXwlX_7gp8-NQyg72kKKjHCMsNG.QX3YTN0wCN0AzNzEzW}

# SOLUTION

Use 2> to redirect errors to file instructions and > to redirect output or the flag to myflag file.

```
hacker@piping~redirecting-errors:~$ /challenge/run > myflag 2> instructions
hacker@piping~redirecting-errors:~$ cat instructions
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will check that error output is redirected to a specific file path : instructions
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!

[TEST] You should have redirected my stderr to instructions. Checking...

[PASS] The file at the other end of my stderr looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-errors:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{QXwlX_7gp8-NQyg72kKKjHCMsNG.QX3YTN0wCN0AzNzEzW}
```

# WHAT I LEARNT

A File Descriptor (FD) is a number that _describes_ a communication channel in Linux.
- FD 0: Standard Input
- FD 1: Standard Output
- FD 2: Standard Error 
When you redirect process communication, you do it by FD number

