
# EXTRACTING NEW LINES WITH HEAD 

This challenge teaches you about head flag which by default gives first 10 lines of output.


# FLAG

My flag ~ pwn.college{AcRTsq6xNDTsjRJDLAE0drxvMJz.0lNxEzNxwCN0AzNzEzW}

# SOLUTION

Here challenge asked to to retrieve first 7 lines of /challenge/pwn which is done by /challenge/pwn |head -n 7 and it also asked to pipe it to /challenge/college which is done by further adding | /challenge/college

```
hacker@data~extracting-the-first-lines-with-head:~$ /challenge/pwn | head -n 7 | /challenge/college
Congratulations, you piped the right codes!
pwn.college{AcRTsq6xNDTsjRJDLAE0drxvMJz.0lNxEzNxwCN0AzNzEzW
```

# WHAT I LEARNT

Head command along with -n is used to retrieve first n lines of output of command

