
# REDIRECTING MORE OUTPUT

This challlenge demonstrates how you can redirect the output of any command.

# FLAG

My flag ~ pwn.college{0PZN2URo_rLZ9aQfYwzr05v6lRh.QX1YTN0wCN0AzNzEzW}

# SOLUTION

Type in /challenge/run > myflag to redirect output to file myflag and read the file using cat.


```
hacker@piping~redirecting-more-output:~$ /challenge/run > myflag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-more-output:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{0PZN2URo_rLZ9aQfYwzr05v6lRh.QX1YTN0wCN0AzNzEzW}


```

# WHAT  I LEARNT

you can redirect the output of any command to a file using >.