
# DUPLICATING PIPED DATA WITH TREE

This challenge teaches you about tee command

# FLAG

My flag ~ pwn.college{8dxbRDLYsu1l9rzCxxdGbuSfhQ8.QXxITO0wCN0AzNzEzW}

# SOLUTION


```
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | tee pwn | /challenge/college
Processing...
WARNING: you are overwriting file pwn with tee's output...
The input to 'college' does not contain the correct secret code! This code
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ cat pwn
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "8dxbRDLY"
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret 8dxbRDLY | /challenge/college
Processing...
Correct! Passing secret value to /challenge/college...
Great job! Here is your flag:
pwn.college{8dxbRDLYsu1l9rzCxxdGbuSfhQ8.QXxITO0wCN0AzNzEzW}

```

# WHAT I LEARNT
The `tee` command, named after a "T-splitter" from _plumbing_ pipes, duplicates data flowing through your pipes to any number of files provided on the command line